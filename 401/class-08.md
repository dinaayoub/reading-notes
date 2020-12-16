# Read: Class 08 - Access Control (ACL)

## Review, Research, and Discussion

1. When is Basic Authorization used vs. Bearer Authorization?
initially when the user first uses their username and password to log in, we use basic auth. then on subsequent calls to access privileged info we use bearer auth.
2. What does the JSON Web Token package do?
JWT creates a token using a secret that allows us to use bearer auth and make sure the token given by the user is valid (using the secret)
3. What considerations should we make when creating and storing a SECRET?
we could store in a .env file that isn't accessible, though i'm not sure how to make github run tests correctly if secret isn't provided.

## Vocabulary Terms

* encryption: applying an algorithm (or many) to an item to turn it into a more secure text that can't be read or easily accessed. most successful encryption algorithms can't be decrypted.
* token: a string that allows the user and server to communicate while maintaining the identity of the user.
* bearer: identifies the person with the token as the person who is authorized to access the info
* secret: a secret string that is used to create a jwt token.
* JSON Web Token: a standard that defines a way for transmitting information securely as a json object. the info can be verified and trusted because it's signed using a secret that only the server knows. [src](https://jwt.io/introduction/)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
3. What are you most excited about trying to implement or see how it works?

## Preparation Materials

[RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)
[5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)
[wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)