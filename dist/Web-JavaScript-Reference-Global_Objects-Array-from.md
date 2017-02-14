`**Array.from()**` 方法从类似数组或可迭代对象创建一个新的数组实例。

<div class="note">

在 ES6 中， `Class` 语法允许我们为内置类型（比如 `Array`）和自定义类新建子类（比如叫 `SubArray`）。这些子类也会继承父类的静态方法，比如 `SubArray.from()`，调用该方法后会返回子类 `SubArray` 的一个实例，而不是 `Array` 的实例。

</div>

## 语法

    Array.from(arrayLike[, mapFn[, thisArg]])

### 参数

<dl>

<dt>arrayLike</dt>

<dd>想要转换成真实数组的类数组对象或可遍历对象。</dd>

<dt>mapFn</dt>

<dd>可选参数，如果指定了该参数，则最后生成的数组会经过该函数的加工处理后再返回。</dd>

<dt>thisArg</dt>

<dd>可选参数，执行 `mapFn` 函数时 `this` 的值。</dd>

</dl>

### 返回值

一个新的[`Array`](/zh-CN/docs/Web/JavaScript/Reference/Array "此页面仍未被本地化, 期待您的翻译!")实例

## 描述

`Array.from()` 允许你创建数组从：

*   类数组对象（拥有一个 `length` 属性和若干索引属性的任意对象）
*   [可遍历对象](/zh-CN/docs/Web/JavaScript/Guide/iterable)（你可以从它身上迭代出若干个元素的对象，比如有 [`Map`](/zh-CN/docs/Web/JavaScript/Reference/Map "此页面仍未被本地化, 期待您的翻译!") 和 [`Set`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Set "集合（Set）对象允许你存储任意类型的唯一值（不能重复），无论它是原始值或者是对象引用。") 等）

`Array.from()` 方法有一个可选参数 `mapFn`，让你可以在最后生成的数组上再执行一次 [`map`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/map "map() 方法返回一个由原数组中的每个元素调用一个指定方法后的返回值组成的新数组。") 方法后再返回。也就是说`Array.from(obj, mapFn, thisArg)` 就相当于` Array.from(obj).map(mapFn, thisArg),` 除非创建的不是可用的中间数组。 这对一些数组的子类`,`如  [typed arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays)<font face="Consolas, Liberation Mono, Courier, monospace"> 来说很重要,</font> 因为中间数组的值在调用 map() 时需要是适当的类型。

`from()` 的 `length` 属性为 1 。

## 示例

<pre class="brush: js">// 将类数组对象（arguments）转换成数组
(function () {
    var args = Array.from(arguments);
    return args;
})(1, 2, 3);                            // [1, 2, 3]

// 将可迭代对象（Set 对象）转换成数组
Array.from(new Set(["foo", window]));       // ["foo", window]

// Map 对象也可以
var m = new Map([[1, 2], [2, 4], [4, 8]]);
Array.from(m);                          // [[1, 2], [2, 4], [4, 8]]  

// 字符串对象既是类数组又是可迭代对象
Array.from("foo");                      // ["f", "o", "o"]

// 使用 map 函数转换数组元素
Array.from([1, 2, 3], x => x + x);      // [2, 4, 6]

// 生成一个数字序列
Array.from({length:5}, (v, k) => k);    // [0, 1, 2, 3, 4]

</pre>

## Polyfill

ECMA-262 第六版标准添加了 `Array.from` 。有些实现中可能尚未包括在其中。你可以通过在脚本前添加如下内容作为替代方法，以使用未原生支持的 `Array.from` 方法。该算法按照  ECMA-262 第六版中的规范实现，并假定 `Object` 和 `TypeError` 有其本身的值，  `callback.call` 对应 [`Function.prototype.call`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/call "call() 方法在使用一个指定的this值和若干个指定的参数值的前提下调用某个函数或方法.") 。此外，鉴于无法使用 Polyfill 实现真正的的迭代器，该实现不支持规范中定义的泛型可迭代元素。

<pre class="brush: js">// Production steps of ECMA-262, Edition 6, 22.1.2.1
// Reference: https://people.mozilla.org/~jorendorff/es6-draft.html#sec-array.from
if (!Array.from) {
  Array.from = (function () {
    var toStr = Object.prototype.toString;
    var isCallable = function (fn) {
      return typeof fn === 'function' || toStr.call(fn) === '[object Function]';
    };
    var toInteger = function (value) {
      var number = Number(value);
      if (isNaN(number)) { return 0; }
      if (number === 0 || !isFinite(number)) { return number; }
      return (number > 0 ? 1 : -1) * Math.floor(Math.abs(number));
    };
    var maxSafeInteger = Math.pow(2, 53) - 1;
    var toLength = function (value) {
      var len = toInteger(value);
      return Math.min(Math.max(len, 0), maxSafeInteger);
    };

    // The length property of the from method is 1.
    return function from(arrayLike/*, mapFn, thisArg */) {
      // 1\. Let C be the this value.
      var C = this;

      // 2\. Let items be ToObject(arrayLike).
      var items = Object(arrayLike);

      // 3\. ReturnIfAbrupt(items).
      if (arrayLike == null) {
        throw new TypeError("Array.from requires an array-like object - not null or undefined");
      }

      // 4\. If mapfn is undefined, then let mapping be false.
      var mapFn = arguments.length > 1 ? arguments[1] : void undefined;
      var T;
      if (typeof mapFn !== 'undefined') {
        // 5\. else      
        // 5\. a If IsCallable(mapfn) is false, throw a TypeError exception.
        if (!isCallable(mapFn)) {
          throw new TypeError('Array.from: when provided, the second argument must be a function');
        }

        // 5\. b. If thisArg was supplied, let T be thisArg; else let T be undefined.
        if (arguments.length > 2) {
          T = arguments[2];
        }
      }

      // 10\. Let lenValue be Get(items, "length").
      // 11\. Let len be ToLength(lenValue).
      var len = toLength(items.length);

      // 13\. If IsConstructor(C) is true, then
      // 13\. a. Let A be the result of calling the [[Construct]] internal method of C with an argument list containing the single item len.
      // 14\. a. Else, Let A be ArrayCreate(len).
      var A = isCallable(C) ? Object(new C(len)) : new Array(len);

      // 16\. Let k be 0.
      var k = 0;
      // 17\. Repeat, while k < len… (also steps a - h)
      var kValue;
      while (k < len) {
        kValue = items[k];
        if (mapFn) {
          A[k] = typeof T === 'undefined' ? mapFn(kValue, k) : mapFn.call(T, kValue, k);
        } else {
          A[k] = kValue;
        }
        k += 1;
      }
      // 18\. Let putStatus be Put(A, "length", len, true).
      A.length = len;
      // 20\. Return A.
      return A;
    };
  }());
}
</pre>

## 规范

<table>

<tbody>

<tr>

<th scope="col">Specification</th>

<th scope="col">Status</th>

<th scope="col">Comment</th>

</tr>

<tr>

<td>[ECMAScript 2015 (6th Edition, ECMA-262)  
<small lang="zh-CN">Array.from</small>](http://www.ecma-international.org/ecma-262/6.0/#sec-array.from)</td>

<td><span class="spec-Standard">Standard</span></td>

<td>Initial definition.</td>

</tr>

<tr>

<td>[ECMAScript 2017 Draft (ECMA-262)  
<small lang="zh-CN">Array.from</small>](https://tc39.github.io/ecma262/#sec-array.from)</td>

<td><span class="spec-Draft">Draft</span></td>

<td> </td>

</tr>

</tbody>

</table>

## 浏览器兼容性

<div class="htab"><a name="AutoCompatibilityTable" id="AutoCompatibilityTable"></a>

*   <a>Desktop</a>
*   <a>Mobile</a>

</div>

<table>

<tbody>

<tr>

<th>Feature</th>

<th>Chrome</th>

<th>Firefox (Gecko)</th>

<th>Edge</th>

<th>Internet Explorer</th>

<th>Opera</th>

<th>Safari</th>

</tr>

<tr>

<td>Basic support</td>

<td>45</td>

<td>[32](/en-US/Firefox/Releases/32 "Released on 2014-09-02.") (32)</td>

<td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>

<td><span style="color: #f00;">未实现</span></td>

<td><span style="color: #f00;">未实现</span></td>

<td>9.0</td>

</tr>

</tbody>

</table>

<table>

<tbody>

<tr>

<th>Feature</th>

<th>Android</th>

<th>Chrome for Android</th>

<th>Firefox Mobile (Gecko)</th>

<th>IE Mobile</th>

<th>Opera Mobile</th>

<th>Safari Mobile</th>

</tr>

<tr>

<td>Basic support</td>

<td><span style="color: #f00;">未实现</span></td>

<td><span style="color: #f00;">未实现</span></td>

<td>32.0 (32)</td>

<td><span style="color: #f00;">未实现</span></td>

<td><span style="color: #f00;">未实现</span></td>

<td><span style="color: #f00;">未实现</span></td>

</tr>

</tbody>

</table>

## 相关链接

*   [`Array`](/zh-CN/docs/Web/JavaScript/Reference/Array "此页面仍未被本地化, 期待您的翻译!")
*   [`Array.prototype.map()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/map "map() 方法返回一个由原数组中的每个元素调用一个指定方法后的返回值组成的新数组。")
*   [`TypedArray.from()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from "此页面仍未被本地化, 期待您的翻译!")