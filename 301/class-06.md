# Read: 06 - Node, Express, and APIs

* [An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js/)
  * What is node.js? a javascript runtime built on google chrome's "v8 javascript engine" which is responsible for compiling js to native machine code that your computer can handle. the creator of node took that v8 engine and enhanced it with file system api, an http library, and some other OS related utility methods.
  * npm comes bundled with node and is the package manager which has over a million packages you can install.
  * Node.js allows us to run javascript code on the server. It is single-threaded (?) and handles things asynchronously so that longer operations don't block it, using callbacks. It uses an event loop.
  * To scale node.js, you clone it and have the cloned instances share the workload, which there's a built-in module for.
  * Potential issues because of node being single-threaded: blocking i/o calls should be avoided. cpu- intensive operations should be handed off to a worker thread, and errors should always be handled correctly so they don't crash the entire process.
  * It doesn't have as many bells and whistles as frameworks like Rails or Laravel. It's bare bones, and you can add Express to have more but even that is still rather bare bones.
  * Node advantages:
    * You don't have to switch langauges or frameworks between client and server work and can even share code. Supposed to make you more productive.
    * speed and scalability.
    * it speaks json!
    * can be used for more than server code.
