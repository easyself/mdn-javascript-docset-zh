
                
                  <div><section class="Quick_links" id="Quick_Links"><!-- --></section> <div class="notice experimental">
    <p><span title="This is an experimental API that should not be used in production code."><i class="icon-beaker"> </i></span> <strong>This is an experimental technology</strong><br>Because this technology&apos;s specification has not stabilized, check the <a href="#Browser_compatibility">compatibility table</a> for usage in various browsers. Also note that the syntax and behavior of an experimental technology is subject to change in future versions of browsers as the specification changes.</p>
</div></div>

<p>The <strong><code>SIMD.Int32x4</code></strong> data type is a 128-bit vector divided into 4 lanes storing 32-bit signed integer values.</p>

<div><img src="https://mdn.mozillademos.org/files/11257/int32x4.png" alt="SIMD.Int32x4">
<p>Figure 1: SIMD.Int32x4 in a 128-bit SIMD register.</p>
</div>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox">SIMD.Int32x4(x, y, z, w);</pre>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt><code>x</code> <span class="inlineIndicator optional optionalInline">Optional</span></dt>
 <dd>An integer specifying the value of the first lane. Defaults to 0.</dd>
 <dt><code>y</code> <span class="inlineIndicator optional optionalInline">Optional</span></dt>
 <dd>An integer specifying the value of the second lane. Defaults to 0.</dd>
 <dt><code>z</code> <span class="inlineIndicator optional optionalInline">Optional</span></dt>
 <dd>An integer specifying the value of the third lane. Defaults to 0.</dd>
 <dt><code>w</code> <span class="inlineIndicator optional optionalInline">Optional</span></dt>
 <dd>An integer specifying the value of the fourth lane. Defaults to 0.</dd>
</dl>

<h2 id="Constructor_functions">Constructor functions</h2>

<p>In addition to the simple creator functions, the SIMD API provides the following constructor functions.</p>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/splat" title="The static SIMD.%type%.splat() method creates a new SIMD data type with all lanes set to a given value."><code>SIMD.Int32x4.splat()</code></a></dt>
 <dd>Creates an Int32x4 with all lanes set to a given value.</dd>
</dl>

<p>You can also <a href="#Data_conversions">convert from another SIMD data type to Int32x4</a>.</p>

<div class="note">
<p><strong>Note:</strong> SIMD types don&apos;t work with <code>new</code>, as SIMD values are no &quot;boxed&quot; objects (comparable to <code>String(s)</code> vs. <code>new String(s)</code>, which creates a String object).</p>

<pre class="brush: js example-bad">var v = new SIMD.Int32x4(1, 2, 3, 4); 
// TypeError: SIMD.Int32x4 is not a constructor
var w = new SIMD.Int32x4.splat(3); 
// TypeError: SIMD.Int32x4.splat is not a constructor</pre>

<p>Instead, you just write:</p>

<pre class="brush: js example-good">var v = SIMD.Int32x4(1, 2, 3, 4);
var w = SIMD.Int32x4.splat(3);</pre>
</div>

<h2 id="Operations">Operations</h2>

<p>To actually do something with SIMD types, SIMD operations are needed that work on SIMD data types.</p>

<h3 id="Checking_SIMD_types">Checking SIMD types</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/check" title="The static SIMD.%type%.check() method returns a SIMD data type if the parameter is a valid SIMD data type and the same as %type%. Otherwise, a TypeError is thrown."><code>SIMD.Int32x4.check()</code></a></dt>
 <dd>Returns a new Int32x4 if the parameter is a valid Int32x4 data type. Throws a <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError" title="The TypeError object represents an error when a value is not of the expected type."><code>TypeError</code></a> otherwise.</dd>
</dl>

<h3 id="Accessing_and_mutating_lanes">Accessing and mutating lanes</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/extractLane" title="The static SIMD.%type%.extractLane() method returns the value of a given lane."><code>SIMD.Int32x4.extractLane()</code></a></dt>
 <dd>Returns the value of the given lane.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/replaceLane" title="The static SIMD.%type%.replaceLane() method returns a new SIMD data type with the given lane value replaced."><code>SIMD.Int32x4.replaceLane()</code></a></dt>
 <dd>Returns a new Int32x4 with the given lane value replaced.</dd>
</dl>

<h3 id="Loading_from_and_storing_into_typed_arrays">Loading from and storing into typed arrays</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/load" title="The static SIMD.%type%.load() methods create a new SIMD data type with the lane values loaded from a typed array."><code>SIMD.Int32x4.load()</code></a></dt>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/load" title="The static SIMD.%type%.load() methods create a new SIMD data type with the lane values loaded from a typed array."><code>SIMD.Int32x4.load1()</code></a></dt>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/load" title="The static SIMD.%type%.load() methods create a new SIMD data type with the lane values loaded from a typed array."><code>SIMD.Int32x4.load2()</code></a></dt>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/load" title="The static SIMD.%type%.load() methods create a new SIMD data type with the lane values loaded from a typed array."><code>SIMD.Int32x4.load3()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values loaded from a <a href="/en-US/docs/Web/JavaScript/Typed_arrays">typed array</a>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/store" title="The static SIMD.%type%.store() methods store a SIMD data type into a typed array."><code>SIMD.Int32x4.store()</code></a><br>
 <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/store" title="The static SIMD.%type%.store() methods store a SIMD data type into a typed array."><code>SIMD.Int32x4.store1()</code></a><br>
 <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/store" title="The static SIMD.%type%.store() methods store a SIMD data type into a typed array."><code>SIMD.Int32x4.store2()</code></a><br>
 <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/store" title="The static SIMD.%type%.store() methods store a SIMD data type into a typed array."><code>SIMD.Int32x4.store3()</code></a></dt>
 <dd>Stores an Int32x4 into a <a href="/en-US/docs/Web/JavaScript/Typed_arrays">typed array</a>.</dd>
</dl>

<h3 id="Arithmetic_operations">Arithmetic operations</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/add" title="The static SIMD.%type%.add() method returns a new instance with the lane values added (a + b)."><code>SIMD.Int32x4.add()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values added (<code>a + b</code>).</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/mul" title="The static SIMD.%type%.mul() method returns a new instance with the lane values multiplied (a * b)."><code>SIMD.Int32x4.mul()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values multiplied (<code>a * b</code>).</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/neg" title="The static SIMD.%type%.mul() method returns a new instance with the lane values negated."><code>SIMD.Int32x4.neg()</code></a></dt>
 <dd>Returns a new Int32x4 with the negated lane values.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/sub" title="The static SIMD.%type%.sub() method returns a new instance with the lane values subtracted (a - b)."><code>SIMD.Int32x4.sub()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values subtracted (<code>a - b</code>).</dd>
 <dt>
 <h3 id="Shuffling_and_swizzling">Shuffling and swizzling</h3>
 </dt>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/shuffle" title="The static SIMD.%type%.shuffle() method creates a new SIMD data type instance with the lane values shuffled."><code>SIMD.Int32x4.shuffle()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values shuffled.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/swizzle" title="The static SIMD.%type%.swizzle() method creates a new SIMD data type instance with the lane values swizzled (re-ordered)."><code>SIMD.Int32x4.swizzle()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values swizzled.</dd>
</dl>

<h3 id="Selections">Selections</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/select" title="The static SIMD.%type%.select() method creates a new integer SIMD data type with the lane values being a selection match from a selector mask."><code>SIMD.Int32x4.select()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values being a mix of the lanes depending on the selector mask.</dd>
</dl>

<h3 id="Comparisons">Comparisons</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/equal" title="The static SIMD.%type%.equal() method returns a selection mask with values depending on a strict equality comparison (a === b) in each lane."><code>SIMD.Int32x4.equal()</code></a></dt>
 <dd>Returns a selection mask depending on <code>a == b</code>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/notEqual" title="The static SIMD.%type%.notEqual() method returns a selection mask with values depending on an inequality comparison (a != b) in each lane."><code>SIMD.Int32x4.notEqual()</code></a></dt>
 <dd>Returns a&#xA0;selection mask depending on <code>a != b</code>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/lessThan" title="The static SIMD.%type%.lessThan() method returns a selection mask with values depending on a less-than comparison (a &lt; b) in each lane."><code>SIMD.Int32x4.lessThan()</code></a></dt>
 <dd>Returns a selection mask depending on <code>a &lt; b</code>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/lessThanOrEqual" title="The static SIMD.%type%.lessThanOrEqual() method returns a selection mask with values depending on a less-than-or-equal comparison (a &lt;= b) in each lane."><code>SIMD.Int32x4.lessThanOrEqual()</code></a></dt>
 <dd>Returns a selection mask depending on <code>a &lt;= b</code>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/greaterThan" title="The static SIMD.%type%.greaterThan() method returns a selection mask with values depending on a greater-than comparison (a &gt; b) in each lane."><code>SIMD.Int32x4.greaterThan()</code></a></dt>
 <dd>Returns a selection mask depending on <code>a &gt; b</code>.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/greaterThanOrEqual" title="The static SIMD.%type%.greaterThanOrEqual() method returns a selection mask with values depending on a greater-than-or-equal comparison (a &gt;= b) in each lane."><code>SIMD.Int32x4.greaterThanOrEqual()</code></a></dt>
 <dd>Returns a selection mask depending on <code>a &gt;= b</code>.</dd>
</dl>

<h3 id="Bitwise_logical_operations">Bitwise logical operations</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/and" title="The static SIMD.%type%.and() method returns a new instance with the logical AND of the lane values (a &amp; b). This operation exists only on integer and boolean SIMD types."><code>SIMD.Int32x4.and()</code></a></dt>
 <dd>Returns a new Int32x4 with the logical AND of the lane values (<code>a &amp; b</code>).</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/or" title="The static SIMD.%type%.or() method returns a new instance with the logical OR of the lane values (a | b). This operation exists only on integer and boolean SIMD types."><code>SIMD.Int32x4.or()</code></a></dt>
 <dd>Returns a new Int32x4 with the logical OR of the lane values (<code>a | b</code>).</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/xor" title="The static SIMD.%type%.xor() method returns a new instance with the logical XOR of the lane values (a ^ b)."><code>SIMD.Int32x4.xor()</code></a></dt>
 <dd>Returns a new Int32x4 with the logical XOR of the lane values (<code>a ^ b</code>).</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/not" title="The static SIMD.%type%.not() method returns a new instance with the bitwise logical NOT of the lane values (~a). This operation exists only on integer and boolean SIMD types."><code>SIMD.Int32x4.not()</code></a></dt>
 <dd>Returns a new Int32x4 with lane with the logical NOT of the lane values (<code>~a</code>).</dd>
</dl>

<h3 id="Bitwise_shift_operations">Bitwise shift operations</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/shiftLeftByScalar" title="The static SIMD.%type%.shiftLeftByScalar() method returns a new instance with the lane values shifted left by a given bit count (a &lt;&lt; bits)."><code>SIMD.Int32x4.shiftLeftByScalar()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values shifted left by a given bit count (<code>a &lt;&lt; bits</code>).</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/shiftRightByScalar" title="The static SIMD.%type%.shiftRightByScalar() method returns a new instance with the lane values shifted right. Depending on the type, these operations are used:"><code>SIMD.Int32x4.shiftRightByScalar()</code></a></dt>
 <dd>Returns a new Int32x4 with the lane values shifted right.</dd>
</dl>

<h3 id="Data_conversions">Data conversions</h3>

<dl>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/fromFloat32x4" title="The static SIMD.%type%.fromFloat32x4() method creates a new SIMD data type with a float conversion from a Float32x4."><code>SIMD.Int32x4.fromFloat32x4()</code></a></dt>
 <dd>Creates a new Int32x4 data type with a float conversion from a float32x4.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/fromFloat32x4Bits" title="The static SIMD.%type%.fromFloat32x4Bits() method creates a new SIMD data type with a bit-wise copy from a Float32x4."><code>SIMD.Int32x4.fromFloat32x4Bits()</code></a></dt>
 <dd>Creates a new Int32x4 data type with a bit-wise copy from a float32x4.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/fromFloat64x2Bits" title="The static SIMD.%type%.fromFloat64x2Bits() method creates a new SIMD data type with a bit-wise copy from a Float64x2."><code>SIMD.Int32x4.fromFloat64x2Bits()</code></a></dt>
 <dd>Creates a new Int32x4 data type with a bit-wise copy from a float64x2.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/fromInt16x8Bits" title="The static SIMD.%type%.fromInt16x8Bits() method creates a new SIMD data type with a bit-wise copy from an int16x8."><code>SIMD.Int32x4.fromInt16x8Bits()</code></a></dt>
 <dd>Creates a new Int32x4 data type with a bit-wise copy from an Int16x8.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/fromInt8x16Bits" title="The static SIMD.%type%.fromInt8x16Bits() method creates a new SIMD data type with a bit-wise copy from an Int8x16."><code>SIMD.Int32x4.fromInt8x16Bits()</code></a></dt>
 <dd>Creates a new Int32x4 data type with a bit-wise copy from an Int8x16.</dd>
</dl>

<h2 id="SIMD_prototype">SIMD prototype</h2>

<p>The following methods and properties are installed on the <code>SIMD.Int32x4.prototype</code>.</p>

<dl>
 <dt><code>SIMD.Int32x4.prototype.constructor</code></dt>
 <dd>Specifies the function that creates a SIMD object&apos;s prototype.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/toLocaleString" class="new" title="The documentation about this has not yet been written; please consider contributing!"><code>SIMD.Int32x4.prototype.toLocaleString()</code></a></dt>
 <dd>Returns a localized string representing the SIMD type and its elements. Overrides the <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/toLocaleString" title="The toLocaleString() method returns a string representing the object. This method is meant to be overridden by derived objects for locale-specific purposes."><code>Object.prototype.toLocaleString()</code></a> method.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/toString" title="The SIMD.%type%.toString() method returns a String representing a SIMD object."><code>SIMD.Int32x4.prototype.toString()</code></a></dt>
 <dd>Returns a string representing the SIMD type and its elements. Overrides the <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/toString" title="The toString() method returns a string representing the object."><code>Object.prototype.toString()</code></a> method.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/valueOf" title="The SIMD.%type%.valueOf() method performs a type check returns the this value."><code>SIMD.Int32x4.prototype.valueOf()</code></a></dt>
 <dd>Returns the primitive value of a SIMD object.</dd>
 <dt><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD/toSource" title="The non-standard SIMD.%type%.toSource() method returns a string representing the source code of the object."><code>SIMD.Int32x4.prototype.toSource()</code></a> <span title="This API has not been standardized."><i class="icon-warning-sign"> </i></span></dt>
 <dd>Returns a string representing the source code of the object. Overrides the <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/toSource" title="The toSource() method returns a string representing the source code of the object."><code>Object.prototype.toSource()</code></a> method.</dd>
</dl>

<h2 id="Examples">Examples</h2>

<h3 id="Constructing_an_Int32x4">Constructing an Int32x4</h3>

<pre class="brush: js">SIMD.Int32x4(1, 2, 3, 4); // Int32x4[1, 2, 3, 4]
SIMD.Int32x4(1, 2);       // Int32x4[1, 2, 0, 0]
SIMD.Int32x4();           // Int32x4[0, 0, 0, 0]
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
   <td><a href="https://tc39.github.io/ecmascript_simd/#int32x4" class="external" lang="en" hreflang="en">SIMD<br><small lang="en-US">The definition of &apos;Int32x4&apos; in that specification.</small></a></td>
   <td><span class="spec-Draft">Draft</span></td>
   <td>Initial definition.</td>
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
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><em><a href="http://nightly.mozilla.org/" class="external">Nightly build</a></em></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
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
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><em><a href="http://nightly.mozilla.org/" class="external">Nightly build</a></em></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
   <td><span style="color: #f00;">No&#xA0;support</span></td>
  </tr>
 </tbody>
</table>
</div>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/SIMD" title="SIMD (pronounced &quot;sim-dee&quot;) is short for Single Instruction/Multiple Data which is one classification of computer architectures. SIMD operations perform the same computation on multiple data points resulting in data level parallelism and thus performance gains, for example for 3D graphics and video processing, physics simulations or cryptography, and other domains."><code>SIMD</code></a></li>
</ul>
                
              