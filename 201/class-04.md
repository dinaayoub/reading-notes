# Read: 04 - HTML Links, CSS Layout, JS Functions

* From the Duckett HTML book:
  * Chapter 4: Ch.4 “Links” (pp.74-93)
    * Links using the a tag
    * relative links using the file structure
    * links to on-page anchors using the id tag and # in the href
    * [Chapter 15: “Layout” (pp.358-404)](http://htmlandcssbook.com/code-samples/chapter-15/)
      * types of positioning for block elements:
        * normal flow (new line) using position: static;
        * relative position using position:relative and setting the top / left / right / bottom attributes which will be from the spot where it would have been in normal flow
        * absolute positioning using the position:absolute and setting top/left/right/bottom which will be from the top of the page
        * fixed positioning (like absolute but relative to the page) using position: fixed to keep something in the position of whatever the page is displaying (like sticky headers)
        * z-index: higher index shoes up above lower index. can use this instead of following strict code-order where lower elements in the html file will sit on top of higher up elements. 
        * floating: float the element and all other elements will flow around it. it floats to the left or right of whatever container it's in.
          * it can be used to sit elements side by side (e.g. float: left; on all of the boxes)
          * To stop it from adding a floating item where it shouldn't be, you might have to use clear: left or clear: right. This just means it will be placed so that no other elements touch its left or right side.
          * Potential issue: browser might treat a container as 0px tall if it only has floated elements in it. Solution: use overflow: auto; and width: 100%;
        * Layouts: Fixed vs Liquid
        * You can link multiple sheets in your css by using \@import url('blah.css'), or you can use the regular \<link rel=""> in the html

Note: This layout chapter is BIG. Focus your attention on understanding the core concepts presented on pp.358-364, and look at the code samples on the website that accompanies the textbook. You will have another reading assignment on this chapter, so do not try to digest it all now.

* From the Duckett JS book:
  * Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)
    * anonymous functions are when you set a variable to function(blah) then you can use that variable name to run that function (?)
    * IIFE * i didn't really understand this. It seems like an abbreviation thing by adding outer parentheses and running the function by adding () at the end of the function.
    * [Article: “6 Reasons for Pair Programming”](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)
