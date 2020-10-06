# Read: 02 - jQuery, Events, and The DOM

* JavaScript and jQuery book by Jon Duckett pages 293-301, 306-331 and 354-357
  * gives some examples of jquery to manipulate the dom in less code.
  * reasons to use jquery over pure javascript:
    * simple selectors, super specific.
    * less code for common tasks like loops (e.g. you can just set properties for a bunch of selected elements instead of looping through them), adding or removing elements from the dom, chaining methods... etc
    * cross browser compat because it deals with the funkiness of some browsers by using the best method to accomplish what you want that is available for that browser. So again, less code for you to write!
    * syntax is like $('htmlElement')
    * can get and set the html using html()
    * you can cache jquery elements in variables, usually they start with a $ to differentiate them from other variables in your code.
    * to update elements, use .html() and .text(). difference betweenthem is that .html() includes the html tags inside the element but .text() returns only the text, ignoring the html tags.
    * Can use .replaceWith() and .remove() so you can change the content of the page
    * to insert elements, can use .before(), .after(). .prepend() and .append()
    * can get or set attributes of an element using .attr(), .removeAttr(), .addClass(), .removeClass()
    * can get or set css properties using .css('attribute name','optionalNewValue')
    * To loop through a selection of items (similar to foreach): .each() goes through every element in a selection, and inside of it you can access the current element using this or $(this)
    * use the .on('action', function(){blah;}) to add event listeners such as click, dblclick, focus, submit... etc. this function receives an event object so you can add a parameter to the function then use that to access the event type, target, pageX, pageY... etc. .on() has extra parameters you can send in such as selector and data (placed inbetween the action an the function parameters).
    * you can load jquery from a content delivery network (CDN)
    * where the script tag is affects the loading speed of the page. best to put it before the closing of the body tag.

* [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)
  * greater efficiency due to cleaner code, even if it takes a bit longer to write
  * more engaging and collaborative - can figure out problems together faster, avoid wasting time on personal stuff (like facebook!) and procrastinating
  * learning from each other - exposing us to different styles and thought processes. teaching each other in our strengths.
  * social skills - improves your communication because you're forced to find the words. can't just grab the keyboard and take over. it helps with career growth overall.
  * job interview readiness: some interviews will pair you up with one of their own employees to work on a code challenge or something, so having this skill is important for those interviews.
  * work environment readiness: if the company you are going to work for practices pair programming, they won't have to teach you how to do it! you'll hit the ground running.

Bookmark/Skim

* JavaScript and jQuery book by Jon Duckett pages 332-335
  * this introduces some cool effects you can use, such as fadeIn and fadeOut... etc
  * a bit of info about using .animate to animate css properties that you want to change
* JavaScript and jQuery book by Jon Duckett pages 302-305
  * shows some selectors for finding elements. covered by the jquery sololearn class as well.
  * has a nice list of functions to reference.
