# Read: Class 06 - Authentication

## Review, Research, and Discussion

* Explain what a “Singleton” is (in Computer Science terms)
  A class that you can only have one instance of.
* Explain how the Singleton pattern can be used with Node modules, specifically with classes
  Make the constructor private and have a getInstance method. [src](https://medium.com/swlh/node-js-and-singleton-pattern-7b08d11c726a)
* If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
  I don't really understand this question and I don't know how i would go about building another express, but I guess the first thing i'd do is study node extensively so i know how to intercept requests to run the middleware on.

## Vocabulary Terms

* Router Middleware
  Functions that have access to the request and response objects (and the next middleware function) so that they can be run on a route before it goes on to do the work the user requested. [src](https://expressjs.com/en/guide/using-middleware.html)
* Dynamic Module Loading:
  allows us to dynamically load modules in our js code such as importing ES modules with import(), which we use as a function with a string param that can be any code that leads to a string. the function call is a promise, once the module is loaded, the promise is fulfilled. [src](https://medium.com/@leonardobrunolima/javascript-tips-dynamically-importing-es-modules-with-import-f0093dbba8e1)
* Singleton Pattern
  restricts instantiation of a class to only one instance. [src](https://en.wikipedia.org/wiki/Singleton_pattern)
* CRUD -> REST Method Matches
  Create read update delete -> POST GET PUT DELETE (or DESTROY).
* Mock Testing
  Using a mock server to run your tests on without using the actual server (so that you don't add testing load to it).

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  * Singletons
  * Encryption algorithms and how to make them more resilient against today's fast computers
* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  * what dynamic module loading is used for
* What are you most excited about trying to implement or see how it works?
  * can't wait to try authentication!

## Preparation Materials

* [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
  * General purpose cryptographic hash algorithms such as MD5, SHA1. SHA256, SHA512 and SHA-3 are susceptible to brute force attacks. A 16 letter strong password can be cracked in an hour.
  * A Hash Collision attack is possible because hash functions take in infinite input length and produce same output length, which means some words will end up with the same hash. Salting your password (whatever that means) can foil dictionary attacks, but an attacker can stil use a wordlist to crack the hashes.
  * PBKDF2 and Bcrypt are slow and very strong because they make brute force attacks slower by Key stretching. When computers get faster next year, we can increase the work factor to balance it out (to make the attack slower again).
    * [Key stretching](https://en.wikipedia.org/wiki/Key_stretching): "key stretching techniques are used to make a possibly weak key, typically a password or passphrase, more secure against a brute-force attack by increasing the resources (time and possibly space) it takes to test each possible key."
    * Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algoritm and introdcues a work factor (aka a security factor) that allows you too determine how expensive the hash function will be.
    * Implemented in PHP, Java, Ruby, C# and C... etc.

* [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)
  * simplest technique for access control
  * no cookies, session identifiers or login pages. 
  * uses http header Authorization: Basic <credentials> 
  * credentials is encoding of username:password. For example, if the browser uses Aladdin as the username and OpenSesame as the password, then the field's value is the Base64 encoding of Aladdin:OpenSesame, or QWxhZGRpbjpPcGVuU2VzYW1l. Then the Authorization header will appear as: Authorization: Basic QWxhZGRpbjpPcGVuU2VzYW1l
  * Does not have hashing or encryption so should only be used over https.
  
* [OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)
* [bcrypt docs](https://www.npmjs.com/package/bcrypt)