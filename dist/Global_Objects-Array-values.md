
                
                  
                    <div><section class="Quick_links" id="Quick_Links"><!-- --></section>&#xA0;</div>

<p><strong><code>values()</code></strong> &#x65B9;&#x6CD5;&#x8FD4;&#x56DE;&#x4E00;&#x4E2A;&#x65B0;&#x7684;&#xA0;<strong><code>Array Iterator</code></strong>&#xA0;&#x5BF9;&#x8C61;&#xFF0C;&#x8BE5;&#x5BF9;&#x8C61;&#x5305;&#x542B;&#x6570;&#x7EC4;&#x6BCF;&#x4E2A;&#x7D22;&#x5F15;&#x7684;&#x503C;&#x3002;</p>

<div class="warning">
<p>PS:&#xA0;<strong>Chrome &#x672A;&#x5B9E;&#x73B0;&#xA0;</strong></p>
</div>

<h2 id="&#x8BED;&#x6CD5;">&#x8BED;&#x6CD5;</h2>

<pre class="syntaxbox"><code><var>arr</var>.values()</code></pre>

<h2 id="&#x793A;&#x4F8B;">&#x793A;&#x4F8B;</h2>

<h3 id="&#x4F7F;&#x7528;_for...of_&#x5FAA;&#x73AF;&#x8FDB;&#x884C;&#x8FED;&#x4EE3;"><code>&#x4F7F;&#x7528; for...of</code> &#x5FAA;&#x73AF;&#x8FDB;&#x884C;&#x8FED;&#x4EE3;</h3>

<pre class="brush: js">var arr = [&apos;w&apos;, &apos;y&apos;, &apos;k&apos;, &apos;o&apos;, &apos;p&apos;];
var eArr = arr.values();
// &#x60A8;&#x7684;&#x6D4F;&#x89C8;&#x5668;&#x5FC5;&#x987B;&#x652F;&#x6301; for..of &#x5FAA;&#x73AF;
// &#x4EE5;&#x53CA; let &#x2014;&#x2014; &#x5C06;&#x53D8;&#x91CF;&#x4F5C;&#x7528;&#x57DF;&#x9650;&#x5B9A;&#x5728; for &#x5FAA;&#x73AF;&#x4E2D;
for (let letter of eArr) {
  console.log(letter);
}
</pre>

<h3 id="&#x53E6;&#x4E00;&#x79CD;&#x8FED;&#x4EE3;&#x65B9;&#x5F0F;">&#x53E6;&#x4E00;&#x79CD;&#x8FED;&#x4EE3;&#x65B9;&#x5F0F;</h3>

<pre class="brush: js">var arr = [&apos;w&apos;, &apos;y&apos;, &apos;k&apos;, &apos;o&apos;, &apos;p&apos;];
var eArr = arr.values();
console.log(eArr.next().value); // w
console.log(eArr.next().value); // y
console.log(eArr.next().value); // k
console.log(eArr.next().value); // o
console.log(eArr.next().value); // p
</pre>

<h2 id="&#x89C4;&#x8303;">&#x89C4;&#x8303;</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <th scope="col">&#x89C4;&#x8303;&#x540D;&#x79F0;</th>
   <th scope="col">&#x89C4;&#x8303;&#x72B6;&#x6001;</th>
   <th scope="col">&#x5907;&#x6CE8;</th>
  </tr>
  <tr>
   <td><a href="http://www.ecma-international.org/ecma-262/6.0/#sec-array.prototype.values" class="external" lang="en" hreflang="en">ECMAScript 2015 (6th Edition, ECMA-262)<br><small lang="zh-CN">Array.prototype.values</small></a></td>
   <td><span class="spec-Standard">Standard</span></td>
   <td>&#x9996;&#x6B21;&#x5B9A;&#x4E49;</td>
  </tr>
  <tr>
   <td><a href="https://tc39.github.io/ecma262/#sec-array.prototype.values" class="external" lang="en" hreflang="en">ECMAScript 2017 Draft (ECMA-262)<br><small lang="zh-CN">Array.prototype.values</small></a></td>
   <td><span class="spec-Draft">Draft</span></td>
   <td>&#xA0;</td>
  </tr>
 </tbody>
</table>

<h2 id="&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;">&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;</h2>

<div><div class="htab">
    <a name="AutoCompatibilityTable" id="AutoCompatibilityTable"></a>
    <ul>
        <li class="selected"><a>Desktop</a></li>
        <li><a>Mobile</a></li>
    </ul>
</div></div>

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
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span>&#xA0;[1]</td>
   <td><a href="/en-US/Firefox/Releases/48" title="Released on 2016-08-02.">48</a> (48)</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td>9</td>
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
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span>[1]</td>
   <td>48.0 (48)</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
  </tr>
 </tbody>
</table>
</div>

<div>[1] See&#xA0;<a href="https://bugs.chromium.org/p/chromium/issues/detail?id=615873" class="external">bug 615873</a>.</div>

<div>&#xA0;</div>

<h2 id="&#x76F8;&#x5173;&#x94FE;&#x63A5;">&#x76F8;&#x5173;&#x94FE;&#x63A5;</h2>

<ul>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/keys" title="keys()&#xA0;&#x65B9;&#x6CD5;&#x8FD4;&#x56DE;&#x4E00;&#x4E2A;&#x65B0;&#x7684;Array&#x8FED;&#x4EE3;&#x5668;&#xFF0C;&#x5B83;&#x5305;&#x542B;&#x6570;&#x7EC4;&#x4E2D;&#x6BCF;&#x4E2A;&#x7D22;&#x5F15;&#x7684;&#x952E;&#x3002;"><code>Array.prototype.keys()</code></a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/entries" title="entries() &#x65B9;&#x6CD5;&#x8FD4;&#x56DE;&#x4E00;&#x4E2A;&#xA0;Array Iterator &#x5BF9;&#x8C61;&#xFF0C;&#x8BE5;&#x5BF9;&#x8C61;&#x5305;&#x542B;&#x6570;&#x7EC4;&#x4E2D;&#x6BCF;&#x4E00;&#x4E2A;&#x7D22;&#x5F15;&#x7684;&#x952E;&#x503C;&#x5BF9;&#x3002;"><code>Array.prototype.entries()</code></a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach" title="forEach() &#x65B9;&#x6CD5;&#x5BF9;&#x6570;&#x7EC4;&#x7684;&#x6BCF;&#x4E2A;&#x5143;&#x7D20;&#x6267;&#x884C;&#x4E00;&#x6B21;&#x63D0;&#x4F9B;&#x7684;&#x51FD;&#x6570;(&#x56DE;&#x8C03;&#x51FD;&#x6570;)&#x3002;"><code>Array.prototype.forEach()</code></a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/every" title="every() &#x65B9;&#x6CD5;&#x6D4B;&#x8BD5;&#x6570;&#x7EC4;&#x7684;&#x6240;&#x6709;&#x5143;&#x7D20;&#x662F;&#x5426;&#x90FD;&#x901A;&#x8FC7;&#x4E86;&#x6307;&#x5B9A;&#x51FD;&#x6570;&#x7684;&#x6D4B;&#x8BD5;&#x3002;"><code>Array.prototype.every()</code></a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/some" title="some()&#xA0;&#x65B9;&#x6CD5;&#x6D4B;&#x8BD5;&#x6570;&#x7EC4;&#x4E2D;&#x7684;&#x67D0;&#x4E9B;&#x5143;&#x7D20;&#x662F;&#x5426;&#x901A;&#x8FC7;&#x4E86;&#x6307;&#x5B9A;&#x51FD;&#x6570;&#x7684;&#x6D4B;&#x8BD5;&#x3002;"><code>Array.prototype.some()</code></a></li>
</ul>
                  
                
              