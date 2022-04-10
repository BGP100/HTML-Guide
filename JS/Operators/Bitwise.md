<a href="/JS/Operators/Type.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Data-Types.md">Next &gt;</a>
<hr>
<h1>Short Descriptions</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Operator</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>&</code></td>
    <td>And.</td>
  </tr>
  <tr>
    <td><code>|</code></td>
    <td>Or.</td>
  </tr>
  <tr>
    <td><code>~</code></td>
    <td>Not.</td>
  </tr>
  <tr>
    <td><code>^</code></td>
    <td>Xor.</td>
  </tr>
  <tr>
    <td><code>&lt;&lt;</code></td>
    <td>Left shift.</td>
  </tr>
  <tr>
    <td><code>&gt;&gt;</code></td>
    <td>Right shift.</td>
  </tr>
  <tr>
    <td><code>&gt;&gt;&gt;</code></td>
    <td>Unsigned right shift.</td>
  </tr>
</table>
<h1>Long Descriptions</h1>
<h2>AND</h2>
The bitwise AND operator (<code>&</code>) returns a 1 in each bit position for which the corresponding bits of both operands are 1s.
<h2>OR</h2>
The bitwise OR operator (<code>|</code>) returns a 1 in each bit position for which the corresponding bits of either or both operands are 1s.
<h2>NOT</h2>
The bitwise NOT operator (<code>~</code>) inverts the bits of its operand. Like other bitwise operators, it converts the operand to a 32-bit signed integer
<h2>XOR</h2>
The bitwise XOR operator (<code>^</code>) returns a 1 in each bit position for which the corresponding bits of either but not both operands are 1s.
<h2>Left Shift</h2>
The left shift operator (<code>&lt;&lt;</code>) shifts the first operand the specified number of bits to the left. Excess bits shifted off to the left are discarded. Zero bits are shifted in from the right.
<h2>Right Shift</h2>
The right shift operator (<code>&gt;&gt;</code>) shifts the first operand the specified number of bits to the right. Excess bits shifted off to the right are discarded. Copies of the leftmost bit are shifted in from the left. Since the new leftmost bit has the same value as the previous leftmost bit, the sign bit (the leftmost bit) does not change. Hence the name "sign-propagating".
<h2>Unsigned right shift</h2>
The unsigned right shift operator (<code>&gt;&gt;&gt;</code>) (zero-fill right shift) shifts the first operand the specified number of bits to the right. Excess bits shifted off to the right are discarded. Zero bits are shifted in from the left. The sign bit becomes 0, so the result is always non-negative. Unlike the other bitwise operators, zero-fill right shift returns an unsigned 32-bit integer.
