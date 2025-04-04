<details>
  <summary> <h3> 01)  .a + .b {  } </h3> </summary>
<small>
+ work only with first sibling
  
  ```
<div class="a"></div>
<div class="b"></div> <!-- This .b will be selected -->
<div class="b"></div> <!-- This .b will NOT be selected --> */
```
</small>
</details>


<details>
  <summary> <h3> 02) .a ~ .b {  }  </h3> </summary>

<small> Selects all .b elements that come after .a (not necessarily immediately).
  ```
<div class="a"></div>
<div class="x"></div>
<div class="b"></div> <!-- This .b will be selected -->
<div class="b"></div> <!-- This .b will also be selected --> */
```
</small>
</details>

<details>
  <summary> <h3> 03)  .a > p { } </h3> </summary>
  <small> It’s a child combinator selector. It selects only the <p> elements that are direct children of any element with the class .a. </small>
  
  ```
  
  <style>
  .a > p {
    color: red;
    font-weight: bold;
  }
</style>

<div class="a">
  <p>This paragraph will be red and bold ✔</p>
  <div>
    <p>This one WON'T be affected ❌</p>
  </div>
</div>
```
</details>

<details>
  <summary> <h3> 04)  abc[xyz*=foo] {  } </h3></summary>
  <small>
The CSS selector abc[xyz*=foo] targets all <abc> elements with an xyz attribute that contains the string "foo". For example, <abc xyz="foobar"></abc> matches.

```

<abc xyz="foobar"></abc> <!-- This matches: contains 'foo' -->
<abc xyz="hellofoo"></abc> <!-- This matches: contains 'foo' -->
<abc xyz="foobarbaz"></abc> <!-- This matches: contains 'foo' -->
<abc xyz="barbaz"></abc> <!-- This does NOT match: 'foo' is not present -->
<xyz xyz="foobar"></xyz> <!-- This does NOT match: tag name is not 'abc' --> */

```
    
  </small>
</details>
