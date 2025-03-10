1) All Types of Css -  3 main (Inline, Internal, External) and 4th optional (CSS Preprocessors) like - SCSS, Less
2) box modal in css
3) psudo class and element



/* 1) _________ SCSS vs CSS ____________ */

/* CSS (Cascading Style Sheets)
Definition: CSS is a style sheet language used for describing the presentation of a document written in HTML or XML. It provides the ability to apply styles such as fonts, colors, and spacing to web pages.


SCSS (Sassy CSS)
Definition: SCSS is a syntax of SASS (Syntactically Awesome Stylesheets) that extends CSS with features like variables, nested rules, mixins, inheritance, and more, allowing for more dynamic and maintainable stylesheets. It is fully compatible with all versions of CSS. */


/* 2) .a + .b {  }
+ work only with first sibling
<div class="a"></div>
<div class="b"></div> <!-- This .b will be selected -->
<div class="b"></div> <!-- This .b will NOT be selected --> */




/* 3) .a ~ .b {  } 
Selects all .b elements that come after .a (not necessarily immediately).
<div class="a"></div>
<div class="x"></div>
<div class="b"></div> <!-- This .b will be selected -->
<div class="b"></div> <!-- This .b will also be selected --> */


/* 4) abc[xyz*=foo] {  }


The CSS selector abc[xyz*=foo] targets all <abc> elements with an xyz attribute that contains the string "foo". For example, <abc xyz="foobar"></abc> matches.


<abc xyz="foobar"></abc> <!-- This matches: contains 'foo' -->
<abc xyz="hellofoo"></abc> <!-- This matches: contains 'foo' -->
<abc xyz="foobarbaz"></abc> <!-- This matches: contains 'foo' -->
<abc xyz="barbaz"></abc> <!-- This does NOT match: 'foo' is not present -->
<xyz xyz="foobar"></xyz> <!-- This does NOT match: tag name is not 'abc' --> */
