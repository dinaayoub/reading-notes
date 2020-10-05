# Read: 01 - SMACSS and Responsive Web Design

* [Shay Howe’s intro to RWD](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)
  * Talks about the difference between responsive and adaptive design, and why we shouldn't use "mobile" design (where a website is designed specifically for mobile) 
  * Gives an intro to flexible layouts where you can use em or % to make the design adapt to the screen size. Caveat is that sometimes doing this might result in illegible stuff on smaller devices, in which case you may need to use "media queries"
  * media queries can be initialized in the html document in the \<link href="style.css" rel="stylesheet" media="all and (max-width: 1024px)"> or they can be initialized in the css file using the media rule: @media all and (max-width: 1024px) {...} or import rule: @import url(styles.css) all and (max-width: 1024px) {...}
    * media query logical operators: and, not, and only. Using comma to list multiple individual media queries is an unofficial "or" operator
    * Media features:
      * height & width, has min/max prefixes
      * orientation: landscape or portrait
      * aspect-ratio and device-aspect-ratio , has min/max prefixes
      * pixel-ratio or device-pixel-ratio, , has min/max prefixes
      * resolution in dpi (dots per inch), dppx (dots per pixel), or dpcm (dots per centimeter),has min/max prefixes
    * Example: @media all and (max-width: 420px) {section,aside {float:none; width:auto;}}  will make it so that on small screens the section and aside will be on top of each other instead of trying to float next to each other on a tiny screen.
    * Caution: bad idea to identify break points and write media queries for them all because the website should work with myriad options and new ones are available every day!
    * Mobile first prioritizes the mobile experience and you can write media queries that avoid downloading unnecessary media assets (bandwidth is costly on mobile). for example, instead of doing @media all and (max-width) we would do @media all and min-width so the default is for the smaller screen size
    * apple invented "viewport" meta tag, so you can set viewport height to device-height and width to device=width. e.g. \<meta name="viewport" content="width=device-width">
    * viewport scale can be controlled with minimum-scale, maximum-scale, initial-scale (usually set to 1) - all of these must be between 0 and 10. You can use user-scalable to disable or enable zooming e.g. \<meta name="viewport" content="initial-scale=2">
    * it's possible to use target-densitydpi which can accept device-dpi, high-dpi, low-dpi, or an actual dpi number. It's rare to use this. e.g. \<meta name="viewport" content="target-densitydpi=device-dpi">
    * you can combile viewport values with commas inbetween. e.g. \<meta name="viewport" content="width=device-width, initial-scale=1">
  * Flexible media: you can use max-width: 100% to let something scale with the container, but it doesn't work well with iframes and embedded media. To make things work with iframes you need to make the iframe absolute positioning with top & left = 0 and height+width=100% within the containing element.
* [All About Floats](https://css-tricks.com/all-about-floats/)
  * valid values for float: left, right, none and inherit
  * floats can be used to design entire web layouts, though now we have Flexbox and Grid that are more useful.
  * it's most useful in small layouts where you want the text size to float depending on the size of the media, so absolute wouldn't work well.
  * to make an item after the floating item start on a new line, you need to give it clear CSS property.
  * valid values for clear: both, left, right, none.
  * parent element of floats only collapses to zero, which we can deal with by clearing the float after the floated elements in the parent element but before the close of the parent element. For example, an empty div can be used. can also use the overflow method on the parent element. There's also something called the "easy clearing method" which uses a psuedo selecter (:after) but I'm not sure how this works. Here's the code snippet:

  ```css
  .clearfix:after {
   content: ".";
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
  }
  ```

  * Some issues with floats:
    * Pushdown if an element inside a floated item is wider than the float itself
    * Double margin bug which you can fix by using display:inline (might only be for IE 6 though? not sure this is relevant anymore)
    * 3px jog is when text floated up next to a floated element is kicked away by 3px. can be fixed by setting a width or height on the affected text.
    * Bottom margin bug: seems like an ie 7 thing, so don't think this is relevant anymore.

* Bookmark/Skim
  * [Don’t Overthink It Grids](https://css-tricks.com/dont-overthink-it-grids/)
    * mostly just reiterates some of the stuff with floats, but adds something called "gutters" and gives examples of clearing with :after and :before
    * references "-webkit-box-sizing" and "-moz-box-sizing" and "box-sizing: border-box" \<---I don't understand these
  * [CSS Floats Explained By Riding An Escalator](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/) - If you took Code 201, review this article. If you did not take Code 201, this is Essential reading.
    * This is brilliant!
    * Floats left and right allow other elements (or people in the escalator example) to flow between them, or fill in the gaps.
    * clear left will align the floated item under the first element floated left. clear both will reset both left and right flows. 
  * [SMACSS Official Documentation](http://smacss.com/)
    * A way to write css that is more structured and organized.
