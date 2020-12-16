# Read: Class 06 - Bearer Authorization

## Review, Research, and Discussion

1. Write the following steps in the correct order:
  1. Register your application to get a client_id and client_secret
  2. Receive access token
  3. Ask the client if they want to sign in via a third party
  3. Redirect to a third party authentication endpoint
  6. Receive authorization code
  4. Make a request to a third-party API endpoint
  7. Make a request to the access token endpoint
2. What can you do with an authorization code?
exchange it for an access token [src](https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/#:~:text=The%20authorization%20code%20is%20a,approve%20or%20deny%20the%20request.)
3. What can you do with an access token?
maintain your login without having to input your username and password every time.
4. What’s a benefit of using OAuth instead of your own basic authentication?
more secure because you don't have the burden of saving passwords in your own db and then having to worry about liability or being hacked giving away access to user accounts.

## Vocabulary Terms

* Client ID: public identifier for apps unique across all clients that the auth server handles [src](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/#:~:text=The%20client_id%20is%20a%20public%20identifier%20for%20apps.&text=It%20must%20also%20be%20unique,that%20the%20authorization%20server%20handles.)
* Client Secret: the secret used by the server to make sure that the jwt is valid, so the client can't tamper with it and gain access. [src](https://whatis.techtarget.com/definition/endpoint-authentication#:~:text=Endpoint%20authentication%20is%20a%20security,also%20known%20as%20device%20authentication.&text=Authenticating%20both%20the%20user%20and,%2Dfactor%20authentication%20(2FA).)
* Authentication Endpoint
security mechanism to make sure that only authorized devices can connect 
* Access Token Endpoint
* API Endpoint
* Authorization Code
* Access Token

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
3. What are you most excited about trying to implement or see how it works?

## Preparation Materials

* [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)
* [Intro to JWT](https://jwt.io/introduction/)
* [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

## Bookmark

* [npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)