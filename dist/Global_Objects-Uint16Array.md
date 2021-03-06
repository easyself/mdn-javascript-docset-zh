
                
                  <div><section class="Quick_links" id="Quick_Links"><!-- --></section></div>

<p>The <strong><code>Uint16Array</code></strong> typed array represents an array of 16-bit unsigned integers in the platform byte order. If control over byte order is needed, use <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/DataView" title="The DataView view provides a low-level interface for reading and writing multiple number types&#xA0;in an ArrayBuffer irrespective of the platform&apos;s endianness."><code>DataView</code></a> instead. The contents are initialized to <code>0</code>. Once established, you can reference elements in the array using the object&apos;s methods, or using standard array index syntax (that is, using bracket notation).</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox">new Uint16Array(length);
new Uint16Array(typedArray);
new Uint16Array(object);
new Uint16Array(buffer [, byteOffset [, length]]);</pre>

<p>For more information about the constructor syntax and the parameters, see <em><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#Syntax">TypedArray</a></em>.</p>

<h2 id="Properties">Properties</h2>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/BYTES_PER_ELEMENT" title="The TypedArray.BYTES_PER_ELEMENT property represents the size in bytes of each element in an typed array."><code>Uint16Array.BYTES_PER_ELEMENT</code></a></dt>
 <dd>Returns a number value of the element size. <code>2</code> in the case of an <code>Uint16Array</code>.</dd>
 <dt>Uint16Array.length</dt>
 <dd>Static length property whose value is 3. For the actual length (number of elements), see <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/length" title="The length accessor property represents the length (in elements) of a typed array."><code>Uint16Array.prototype.length</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/name" title="The TypedArray.name property represents a string value of the typed array constructor name."><code>Uint16Array.name</code></a></dt>
 <dd>Returns the string value of the constructor name. In the case of the <code>Uint16Array</code> type: &quot;Uint16Array&quot;.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/prototype" title="The TypedArray.prototype property represents the prototype for TypedArray constructors."><code>Uint16Array.prototype</code></a></dt>
 <dd>Prototype for the <em>TypedArray</em> objects.</dd>
</dl>

<h2 id="Methods">Methods</h2>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/from" title="The TypedArray.from() method creates a new typed array from an array-like or iterable object. This method is nearly the same as Array.from()."><code>Uint16Array.from()</code></a></dt>
 <dd>Creates a new <code>Uint16Array</code> from an array-like or iterable object. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from" title="The Array.from() method creates a new Array instance from an array-like or iterable object."><code>Array.from()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/of" title="The TypedArray.of() method creates a new typed array with a variable number of arguments. This method is nearly the same as Array.of()."><code>Uint16Array.of()</code></a></dt>
 <dd>Creates a new <code>Uint16Array</code> with a variable number of arguments. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/of" title="The Array.of() method creates a new Array instance with a variable number of arguments, regardless of number or type of the arguments."><code>Array.of()</code></a>.</dd>
</dl>

<h2 id="Uint16Array_prototype"><code>Uint16Array</code> prototype</h2>

<p>All <code>Uint16Array</code> objects inherit from <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/prototype" title="The TypedArray.prototype property represents the prototype for TypedArray constructors."><code>%TypedArray%.prototype</code></a>.</p>

<h3 id="Properties_2">Properties</h3>

<dl>
 <dt><code>Uint16Array.prototype.constructor</code></dt>
 <dd>Returns the function that created an instance&apos;s prototype. This is the <code>Uint16Array</code> constructor by default.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/buffer" title="The buffer accessor property represents the ArrayBuffer referenced by a TypedArray at construction time."><code>Uint16Array.prototype.buffer</code></a> <span class="inlineIndicator readOnly readOnlyInline" title="This value may not be changed.">Read only </span></dt>
 <dd>Returns the <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer" title="The ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You cannot directly manipulate the contents of an ArrayBuffer; instead, you create one of the typed array objects or a DataView object which represents the buffer in a specific format, and use that to read and write the contents of the buffer."><code>ArrayBuffer</code></a> referenced by the <code>Uint16Array</code> Fixed at construction time and thus <strong>read only</strong>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/byteLength" title="The byteLength accessor property represents the length (in bytes) of a typed array."><code>Uint16Array.prototype.byteLength</code></a> <span class="inlineIndicator readOnly readOnlyInline" title="This value may not be changed.">Read only </span></dt>
 <dd>Returns the length (in bytes) of the <code>Uint16Array</code> from the start of its <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer" title="The ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You cannot directly manipulate the contents of an ArrayBuffer; instead, you create one of the typed array objects or a DataView object which represents the buffer in a specific format, and use that to read and write the contents of the buffer."><code>ArrayBuffer</code></a>. Fixed at construction time and thus <strong>read only.</strong></dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/byteOffset" title="The byteOffset accessor property represents the offset (in bytes) of a typed array from the start of its ArrayBuffer."><code>Uint16Array.prototype.byteOffset</code></a> <span class="inlineIndicator readOnly readOnlyInline" title="This value may not be changed.">Read only </span></dt>
 <dd>Returns the offset (in bytes) of the <code>Uint16Array</code> from the start of its <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer" title="The ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You cannot directly manipulate the contents of an ArrayBuffer; instead, you create one of the typed array objects or a DataView object which represents the buffer in a specific format, and use that to read and write the contents of the buffer."><code>ArrayBuffer</code></a>. Fixed at construction time and thus <strong>read only.</strong></dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/length" title="The length accessor property represents the length (in elements) of a typed array."><code>Uint16Array.prototype.length</code></a> <span class="inlineIndicator readOnly readOnlyInline" title="This value may not be changed.">Read only </span></dt>
 <dd>Returns the number of elements hold in the <code>Uint16Array</code>. Fixed at construction time and thus <strong>read only.</strong></dd>
</dl>

<h3 id="Methods_2">Methods</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/copyWithin" title="The copyWithin() method copies the sequence of array elements within the array to the position starting at target. The copy is taken from the index positions of the second and third arguments start and end. The end argument is optional and defaults to the length of the array. This method has the same algorithm as Array.prototype.copyWithin. TypedArray is one of the typed array types here."><code>Uint16Array.prototype.copyWithin()</code></a></dt>
 <dd>Copies a sequence of array elements within the array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/copyWithin" title="The copyWithin() method shallow copies part of an array to another location in the same array and returns it, without modifying its size."><code>Array.prototype.copyWithin()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/entries" title="The entries() method returns a new Array Iterator object that contains the key/value pairs for each index in the array."><code>Uint16Array.prototype.entries()</code></a></dt>
 <dd>Returns a new <code>Array Iterator</code> object that contains the key/value pairs for each index in the array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/entries" title="The entries() method returns a new Array Iterator object that contains the key/value pairs for each index in the array."><code>Array.prototype.entries()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/every" title="The every() method tests whether all elements in the typed array pass the test implemented by the provided function. This method has the same algorithm as Array.prototype.every(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.every()</code></a></dt>
 <dd>Tests whether all elements in the array pass the test provided by a function. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every" title="The every() method tests whether all elements in the array pass the test implemented by the provided function."><code>Array.prototype.every()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/fill" title="The fill() method fills all the elements of a typed array from a start index to an end index with a static value. This method has the same algorithm as Array.prototype.fill(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.fill()</code></a></dt>
 <dd>Fills all the elements of an array from a start index to an end index with a static value. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/fill" title="The fill() method fills all the elements of an array from a start index to an end index with a static value."><code>Array.prototype.fill()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/filter" title="The filter() method creates a new typed array with all elements that pass the test implemented by the provided function. This method has the same algorithm as Array.prototype.filter(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.filter()</code></a></dt>
 <dd>Creates a new array with all of the elements of this array for which the provided filtering function returns true. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter" title="The filter() method creates a new array with all elements that pass the test implemented by the provided function."><code>Array.prototype.filter()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/find" title="The find() method returns a value in the typed array, if an element satisfies the provided testing function. Otherwise undefined is returned. TypedArray is one of the typed array types here."><code>Uint16Array.prototype.find()</code></a></dt>
 <dd>Returns the found value in the array, if an element in the array satisfies the provided testing function or <code>undefined</code> if not found. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find" title="The find() method returns a value of the first element in the array that satisfies the provided testing function. Otherwise undefined is returned."><code>Array.prototype.find()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/findIndex" title="The findIndex() method returns an index in the typed array, if an element in the typed array satisfies the provided testing function. Otherwise -1 is returned."><code>Uint16Array.prototype.findIndex()</code></a></dt>
 <dd>Returns the found index in the array, if an element in the array satisfies the provided testing function or -1 if not found. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex" title="The findIndex() method returns an index of the first element in the array that satisfies the provided testing function. Otherwise -1 is returned."><code>Array.prototype.findIndex()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/forEach" title="The forEach() method executes a provided function once per array element. This method has the same algorithm as Array.prototype.forEach(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.forEach()</code></a></dt>
 <dd>Calls a function for each element in the array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach" title="The forEach() method executes a provided function once for each array element."><code>Array.prototype.forEach()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/includes" title="The includes() method determines whether a typed array includes a certain element, returning true or false as appropriate. This method has the same algorithm as Array.prototype.includes(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.includes()</code></a> <span title="This is an experimental API that should not be used in production code."><i class="icon-beaker"> </i></span></dt>
 <dd>Determines whether a typed array includes a certain element, returning <code>true</code> or <code>false</code> as appropriate. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes" title="The includes() method determines whether an array includes a certain element, returning true or false as appropriate."><code>Array.prototype.includes()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/indexOf" title="The indexOf() method returns the first index at which a given element can be found in the typed array, or -1 if it is not present. This method has the same algorithm as Array.prototype.indexOf(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.indexOf()</code></a></dt>
 <dd>Returns the first (least) index of an element within the array equal to the specified value, or -1 if none is found. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf" title="The indexOf() method returns the first index at which a given element can be found in the array, or -1 if it is not present."><code>Array.prototype.indexOf()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/join" title="The join() method joins all elements of an array into a string. This method has the same algorithm as Array.prototype.join(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.join()</code></a></dt>
 <dd>Joins all elements of an array into a string. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join" title="The join() method joins all elements of an array into a string."><code>Array.prototype.join()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/keys" title="The keys() method returns a new Array Iterator object that contains the keys for each index in the array."><code>Uint16Array.prototype.keys()</code></a></dt>
 <dd>Returns a new <code>Array Iterator</code> that contains the keys for each index in the array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/keys" title="The keys() method returns a new Array Iterator that contains the keys for each index in the array."><code>Array.prototype.keys()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/lastIndexOf" title="The lastIndexOf() method returns the last index at which a given element can be found in the typed array, or -1 if it is not present. The typed array is searched backwards, starting at fromIndex. This method has the same algorithm as Array.prototype.lastIndexOf(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.lastIndexOf()</code></a></dt>
 <dd>Returns the last (greatest) index of an element within the array equal to the specified value, or -1 if none is found. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf" title="The lastIndexOf() method returns the last index at which a given element can be found in the array, or -1 if it is not present. The array is searched backwards, starting at fromIndex."><code>Array.prototype.lastIndexOf()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/map" title="The map() method creates a new typed array with the results of calling a provided function on every element in this typed array. This method has the same algorithm as Array.prototype.map(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.map()</code></a></dt>
 <dd>Creates a new array with the results of calling a provided function on every element in this array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map" title="The map() method creates a new array with the results of calling a provided function on every element in this array."><code>Array.prototype.map()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/move" title="The move() method used to copy the sequence of array elements within the array to the position starting at target. However, this non-standard method has been replaced with the standard TypedArray.prototype.copyWithin() method. TypedArray is one of the typed array types here."><code>Uint16Array.prototype.move()</code></a> <span title="This API has not been standardized."><i class="icon-warning-sign"> </i></span> <span class="inlineIndicator unimplemented unimplementedInline">Unimplemented</span></dt>
 <dd>Former non-standard version of <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/copyWithin" title="The copyWithin() method copies the sequence of array elements within the array to the position starting at target. The copy is taken from the index positions of the second and third arguments start and end. The end argument is optional and defaults to the length of the array. This method has the same algorithm as Array.prototype.copyWithin. TypedArray is one of the typed array types here."><code>Uint16Array.prototype.copyWithin()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/reduce" title="The reduce() method applies a function against an accumulator and each value of the typed array (from left-to-right) has to reduce it to a single value. This method has the same algorithm as Array.prototype.reduce(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.reduce()</code></a></dt>
 <dd>Apply a function against an accumulator and each value of the array (from left-to-right) as to reduce it to a single value. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce" title="The reduce() method applies a function against an accumulator and each value of the array (from left-to-right) to reduce it to a single value."><code>Array.prototype.reduce()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/reduceRight" title="The reduceRight() method applies a function against an accumulator and each value of the typed array (from right-to-left) has to reduce it to a single value. This method has the same algorithm as Array.prototype.reduceRight(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.reduceRight()</code></a></dt>
 <dd>Apply a function against an accumulator and each value of the array (from right-to-left) as to reduce it to a single value. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduceRight" title="The reduceRight() method applies a function against an accumulator and each value of the array (from right-to-left) has to reduce it to a single value."><code>Array.prototype.reduceRight()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/reverse" title="The reverse() method reverses a typed array in place. The first typed array element becomes the last and the last becomes the first. This method has the same algorithm as Array.prototype.reverse(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.reverse()</code></a></dt>
 <dd>Reverses the order of the elements of an array&#xA0;&#x2014; the first becomes the last, and the last becomes the first. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse" title="The reverse() method reverses an array in place. The first array element becomes the last, and the last array element becomes the first."><code>Array.prototype.reverse()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/set" title="The set() method stores multiple values in the typed array, reading input values from a specified array."><code>Uint16Array.prototype.set()</code></a></dt>
 <dd>Stores multiple values in the typed array, reading input values from a specified array.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/slice" title="The slice() method returns a shallow copy of a portion of a typed array into a new typed array object. This method has the same algorithm as Array.prototype.slice(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.slice()</code></a></dt>
 <dd>Extracts a section of an array and returns a new array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice" title="The slice() method returns a shallow copy of a portion of an array into a new array object selected from begin to end (end not included). The original array will not be modified."><code>Array.prototype.slice()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/some" title="The some() method tests whether some element in the typed array passes the test implemented by the provided function. This method has the same algorithm as Array.prototype.some(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.some()</code></a></dt>
 <dd>Returns true if at least one element in this array satisfies the provided testing function. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some" title="The some() method tests whether some element in the array passes the test implemented by the provided function."><code>Array.prototype.some()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/sort" title="The sort() method sorts the elements of a typed array in place and returns the typed array. This method has the same algorithm as Array.prototype.sort(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.sort()</code></a></dt>
 <dd>Sorts the elements of an array in place and returns the array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort" title="The sort() method sorts the elements of an array in place and returns the array. The sort is not necessarily stable. The default sort order is according to string Unicode code points."><code>Array.prototype.sort()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/subarray" title="The subarray() method returns a new TypedArray on the same ArrayBuffer store and with the same element types as for this TypedArray object. The begin offset is inclusive and the end offset is exclusive. TypedArray is one of the typed array types."><code>Uint16Array.prototype.subarray()</code></a></dt>
 <dd>Returns a new <code>Uint16Array</code> from the given start and end element index.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/values" title="The values() method returns a new Array Iterator object that contains the values for each index in the array."><code>Uint16Array.prototype.values()</code></a></dt>
 <dd>Returns a new <code>Array Iterator</code> object that contains the values for each index in the array. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/values" title="The values() method returns a new Array Iterator object that contains the values for each index in the array."><code>Array.prototype.values()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/toLocaleString" title="The toLocaleString() method returns a string representing the elements of the typed array. The elements are converted to strings and are separated by a locale-specific string (such as a comma &#x201C;,&#x201D;). This method has the same algorithm as Array.prototype.toLocaleString() and, as the typed array elements are numbers, the same algorithm as&#xA0;Number.prototype.toLocaleString() applies for each element. TypedArray is one of the typed array types here."><code>Uint16Array.prototype.toLocaleString()</code></a></dt>
 <dd>Returns a localized string representing the array and its elements. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/toLocaleString" title="The toLocaleString() method returns a string representing the elements of the array. The elements are converted to Strings using their toLocaleString methods and these Strings are separated by a locale-specific String (such as a comma &#x201C;,&#x201D;)."><code>Array.prototype.toLocaleString()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/toString" title="The toString() method returns a string representing the specified array and its elements. This method has the same algorithm as Array.prototype.toString(). TypedArray is one of the typed array types here."><code>Uint16Array.prototype.toString()</code></a></dt>
 <dd>Returns a string representing the array and its elements. See also <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/toString" title="The toString() method returns a string representing the specified array and its elements."><code>Array.prototype.toString()</code></a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/@@iterator" title="The initial value of the @@iterator property is the same function object as the initial value of the values property."><code>Uint16Array.prototype[@@iterator]()</code></a></dt>
 <dd>Returns a new <code>Array Iterator</code> object that contains the values for each index in the array.</dd>
</dl>

<h2 id="Examples">Examples</h2>

<p>Different ways to create a <code>Uint16Array</code>:</p>

<pre class="brush: js">// From a length
var uint16 = new Uint16Array(2);
uint16[0] = 42;
console.log(uint16[0]); // 42
console.log(uint16.length); // 2
console.log(uint16.BYTES_PER_ELEMENT); // 2

// From an array
var arr = new Uint16Array([21,31]);
console.log(arr[1]); // 31

// From another TypedArray
var x = new Uint16Array([21, 31]);
var y = new Uint16Array(x);
console.log(y[0]); // 21

// From an ArrayBuffer
var buffer = new ArrayBuffer(8);
var z = new Uint16Array(buffer, 0, 4);

// From an iterable
var iterable = function*(){ yield* [1,2,3]; }(); 
var uint16 = new Uint16Array(iterable); 
// Uint16Array[1, 2, 3]
</pre>

<h2 id="Specifications">Specifications</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Status</th>
   <th scope="col">Comment</th>
  </tr>
  <tr>
   <td><a href="https://www.khronos.org/registry/typedarray/specs/latest/" class="external" lang="en" hreflang="en" title="The &apos;Typed Array Specification&apos; specification">Typed Array Specification</a></td>
   <td><span class="spec-Obsolete">Obsolete</span></td>
   <td>Superseded by ECMAScript 2015.</td>
  </tr>
  <tr>
   <td><a href="http://www.ecma-international.org/ecma-262/6.0/#table-49" class="external" lang="en" hreflang="en">ECMAScript 2015 (6th Edition, ECMA-262)<br><small lang="en-US">The definition of &apos;TypedArray constructors&apos; in that specification.</small></a></td>
   <td><span class="spec-Standard">Standard</span></td>
   <td>Initial definition in an ECMA standard. Specified that <code>new</code> is required.</td>
  </tr>
  <tr>
   <td><a href="https://tc39.github.io/ecma262/#table-49" class="external" lang="en" hreflang="en">ECMAScript 2017 Draft (ECMA-262)<br><small lang="en-US">The definition of &apos;TypedArray constructors&apos; in that specification.</small></a></td>
   <td><span class="spec-Draft">Draft</span></td>
   <td>&#xA0;</td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p></p><div class="htab">
    <a name="AutoCompatibilityTable" id="AutoCompatibilityTable"></a>
    <ul>
        <li class="selected"><a>Desktop</a></li>
        <li><a>Mobile</a></li>
    </ul>
</div><p></p>

<div id="compat-desktop">
<table class="compat-table">
 <tbody>
  <tr>
   <th>Feature</th>
   <th>Chrome</th>
   <th>Firefox (Gecko)</th>
   <th>Internet Explorer</th>
   <th>Opera</th>
   <th>Safari</th>
  </tr>
  <tr>
   <td>Basic support</td>
   <td>7.0</td>
   <td><a href="/en-US/Firefox/Releases/4" title="Released on 2011-03-22.">4.0</a> (2)</td>
   <td>10</td>
   <td>11.6</td>
   <td>5.1</td>
  </tr>
  <tr>
   <td><code>new</code> is required</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><a href="/en-US/Firefox/Releases/44" title="Released on 2016-01-26.">44</a> (44)</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
  </tr>
  <tr>
   <td>Iterable in constructor</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><a href="/en-US/Firefox/Releases/52" title="Released on 2017-03-07.">52</a> (52)</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
  </tr>
 </tbody>
</table>
</div>

<div id="compat-mobile">
<table class="compat-table">
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
   <td>4.0</td>
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td>4.0 (2)</td>
   <td>10</td>
   <td>11.6</td>
   <td>4.2</td>
  </tr>
  <tr>
   <td><code>new</code> is required</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td>44.0 (44)</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
  </tr>
  <tr>
   <td>Iterable in constructor</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td>52.0 (52)</td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
  </tr>
 </tbody>
</table>
</div>

<h2 id="Compatibility_notes">Compatibility notes</h2>

<p>Starting with ECMAScript 2015 (ES6), <code>Uint16Array</code> constructors require to be constructed with a <a href="/en-US/docs/Web/JavaScript/Reference/Operators/new" title="The new operator creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function."><code>new</code></a> operator. Calling a <code>Uint16Array</code> constructor as a function without <code>new</code>, will throw a <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError" title="The TypeError object represents an error when a value is not of the expected type."><code>TypeError</code></a> from now on.</p>

<pre class="brush: js example-bad">var dv = Uint16Array([1, 2, 3]);
// TypeError: calling a builtin Uint16Array constructor
// without new is forbidden</pre>

<pre class="brush: js example-good">var dv = new Uint16Array([1, 2, 3]);</pre>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/JavaScript/Typed_arrays" title="en/JavaScript typed arrays">JavaScript typed arrays</a></li>
 <li><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer" title="The ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You cannot directly manipulate the contents of an ArrayBuffer; instead, you create one of the typed array objects or a DataView object which represents the buffer in a specific format, and use that to read and write the contents of the buffer."><code>ArrayBuffer</code></a></li>
 <li><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/DataView" title="The DataView view provides a low-level interface for reading and writing multiple number types&#xA0;in an ArrayBuffer irrespective of the platform&apos;s endianness."><code>DataView</code></a></li>
</ul>
                
              