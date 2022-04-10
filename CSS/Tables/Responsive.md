<a href="/CSS/Tables/Style.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Display.md">Next &gt;</a>
<hr>
A responsive table will display a horizontal scroll bar if the screen is too small to display the full content:
<table class="ws-table-all notranslate">
  <tr>
    <th>Name</th>
    <th>Last Name</th>
    <th>Game 1</th>
    <th>Game 2</th>
    <th>Game 3</th>
    <th>Game 4</th>
    <th>Game 5</th>
    <th>Game 6</th>
    <th>Game 7</th>
    <th>Game 8</th>
    <th>Game 9</th>
    <th>Game 10</th>
    <th>Game 11</th>
    <th>Game 12</th>
    <th>Game 13</th>
    <th>Game 14</th>
    <th>Game 15</th>
    <th>Total</th>
  </tr>
  <tr>
    <th>John</th>
    <th>Smith</th>
    <th>11</th>
    <th>4</th>
    <th>25</th>
    <th>8</th>
    <th>5</th>
    <th>9</th>
    <th>16</th>
    <th>3</th>
    <th>21</th>
    <th>10</th>
    <th>13</th>
    <th>7</th>
    <th>3</th>
    <th>11</th>
    <th>26</th>
    <th>172</th>
  </tr>
  <tr>
    <th>Eve</th>
    <th>Compet</th>
    <th>4</th>
    <th>6</th>
    <th>18</th>
    <th>16</th>
    <th>26</th>
    <th>3</th>
    <th>15</th>
    <th>8</th>
    <th>17</th>
    <th>13</th>
    <th>1</th>
    <th>17</th>
    <th>1</th>
    <th>25</th>
    <th>10</th>
    <th>162</th>
  </tr>
  <tr>
    <th>Jack</th>
    <th>Adams</th>
    <th>6</th>
    <th>4</th>
    <th>10</th>
    <th>2</th>
    <th>25</th>
    <th>8</th>
    <th>11</th>
    <th>18</th>
    <th>22</th>
    <th>5</th>
    <th>10</th>
    <th>24</th>
    <th>16</th>
    <th>4</th>
    <th>1</th>
    <th>166</th>
  </tr>
</table>
Add a container element (like <b>&lt;div&gt;</b>) with <b>overflow-x:auto</b> around the <b>&lt;table&gt;</b> element to make it responsive:
<pre>
&lt;div style="overflow-x:auto;"&gt;
&lt;table&gt;
... table content ...
&lt;/table&gt;
&lt;/div&gt;
</pre>
