The numeric functions are used to manipulate numeric values.
<br>
The following table lists all numeric functions in SASS:
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>abs(<em>number</em>)</td>
    <td>Returns the absolute value of <em>number</em>.<br><br>
    <strong>Example:</strong><br>abs(15)<br>Result: 15<br>abs(-15)<br>Result: 15</td>
  </tr>
  <tr>
    <td>ceil(<em>number</em>)</td>
    <td>Rounds <em>number</em> up to the nearest integer.<br><br>
    <strong>Example:</strong><br>ceil(15.20)<br>Result: 16</td>
  </tr>
  <tr>
    <td>comparable(<em>num1</em>, <em>num2</em>)</td>
    <td>Returns whether <em>num1</em> and <em>num2</em> are comparable.<br><br>
    <strong>Example:</strong><br>comparable(15px, 10px)<br>Result: true<br>comparable(20mm, 1cm)<br>Result: 
    true<br>comparable(35px, 2em)<br>Result: false</td>
  </tr>
  <tr>
    <td>floor(<em>number</em>)</td>
    <td>Rounds <em>number</em> down to the nearest integer.<br><br>
    <strong>Example:</strong><br>floor(15.80)<br>Result: 15</td>
  </tr>
  <tr>
    <td>max(<em>number...</em>)</td>
    <td>Returns the highest value of several numbers.<br><br>
    <strong>Example:</strong><br>max(5, 7, 9, 0, -3, -7)<br>Result: 9</td>
  </tr>
  <tr>
    <td>min(<em>number...</em>)</td>
    <td>Returns the lowest value of several numbers.<br><br>
    <strong>Example:</strong><br>min(5, 7, 9, 0, -3, -7)<br>Result: -7</td>
  </tr>
  <tr>
    <td>percentage(<em>number</em>)</td>
    <td>Converts <em>number</em> to a percentage (multiplies the number with 100).<br>
    <br>
    <strong>Example:</strong><br>percentage(1.2)<br>Result: 120</td>
  </tr>
  <tr>
    <td>random()</td>
    <td>Returns a random number between 0 and 1.<br><br>
    <strong>Example:</strong><br>random()<br>Result: 0.45673</td>
  </tr>
  <tr>
    <td>random(<em>number</em>)</td>
    <td>Returns a random integer between 1 and <em>number</em>.<br><br>
    <strong>Example:</strong><br>random(6)<br>Result: 4</td>
  </tr>
  <tr>
    <td>round(<em>number</em>)</td>
    <td>Rounds <em>number</em> to the nearest integer.<br><br>
    <strong>Example:</strong><br>round(15.20)<br>Result: 15<br>round(15.80)<br>Result: 16</td>
  </tr>
</table>
