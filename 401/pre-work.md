# Read

* [Solving Problems](https://simpleprogrammer.com/solving-problems-breaking-it-down/)
  * Don't dive right in. Measure twice, cut once.
  * Steps - as much of 70% of your time should be spent in steps 1-3:
    * Read the problem completely twice. Understand the problem very well.
    * Solve the problem manually with 3 sets of sample data.
      * Use mathematical induction approach: Solve for 1, then for 2, then for n.
      * Think of edge cases.
      * Write down every step that your brain is doing but glossing over
      * Use divide and conquer for larger problems.
    * Optimize the manual steps. Much easier to do than to rearrange or reconstruct code. Figure out if there's an easier way to solve it, things to cut.
    * Write the manual steps as comments or psuedo-code. Can skip this if you have a really good handle on the problem, or the previous steps created detailed description such that coding will be 1 to 1 translation.
    * Replace the comments or psuedo code with real code. If you struggle here, then it's usually one of these 2 reasons:
      * You didn't break down the problem into small enough steps.
      * You don't know your programming language well enough to do the conversion. You should be able to at least do the following in the language:
        * Create a list
        * Sort a list or array
        * Create a map or dictionary
        * Loop through a list, or dictionary
        * Parse strings
        * Convert from string to int, int to string, etc
    * Optimize the real code. Worth a look to see if you can cut out anything or make it simpler.

* [Act like you make $1000/hr](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d)
  * Imagine that your time was worth $1000/hr, what people would you stop putting up with? what problems would you stop wasting time on? what things would you stop or start doing?
  * The most successful people aren't busy, they're focused. Being busy but on autopilot is mental laziness.
  * Say no more often.

* [How to think like a programmer](https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/)
  * Trial and error is a waste of time. Better to have a framework.
  * Steps:
    * Understand. Write down the problem, doodle a diagram, or tell it to someone else. Can help you see the holes in the logic.
    * Plan. Don't dive into solving without a plan. Write down the exact steps.
    * Divide. Break it into sub problems that are easier to solve, then connect the dots when those are all solved. Similarly, you can reduce the problem until it's easy, then expand it bit by bit to get where you need to be.
    * Stuck? Don't get irritated, be curious:
      * Debug, step by step.
      * Re-assess, take a step back and look at it from another perspective - can it be abstracted in a more general approach? Sometimes, delete everything and start new.
      * Research, Google is your friend. Find solutions to the subproblems not the big problem, or else you won't learn anything
    * Practice.

* [The 5 Whys](https://www.mindtools.com/pages/article/newTMC_5W.htm)
  * Invented by the founder of Toyota, Sakichi Toyoda
  * Most effective when used to resolve simple or moderately difficult problems.
  * For more complex problems, use ["Cause and Effect Analysis"](https://www.mindtools.com/pages/article/newTMC_03.htm) or ["Failure Mode and Effects Analysis"](https://www.mindtools.com/pages/article/newTMC_82.htm)
  * How to use:
    * Assemble a team, with a facilitator.
    * Define the problem with a clear problem statement that you all agree on
    * Ask the first why regarding the problem statement. Answers must be grounded in fact.
    * Ask Why four more times, each time as a question in response to the answer you've just recorded
    * Stop when asking why does not produce any more useful responses
    * Address the root cause
    * Monitor your measures
    * Example: ![Example](https://www.mindtools.com/media/Diagrams/5_Whys_Figure_1_Single_Lane.jpg)
