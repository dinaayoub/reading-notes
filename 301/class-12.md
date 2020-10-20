# Read: 12 - Components

* [EJS Partials](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)
  * very useful for repeated assets like navigation and footers. 
  * in a new "views/partials" file create the partial html, e.g. the div. 
  * to include the partial file in another ejs use <%-include(PARTIAL_FILE_NAME)%> 
  * notice the dash before the include to make it unescaped so it can put the html in

Videos
* [Watch EJS tutorial from WalkThroughCode on YouTube, Video 7, Partials](https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt&ab_channel=WalkThroughCode)
This is a short, 3-minute video.
  * partials are native to ejs, so easy to put in