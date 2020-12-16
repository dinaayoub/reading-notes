# Read: Class 06 - Bearer Authorization

## Review, Research, and Discussion

1. Write the following steps in the correct order:
  1. Register your application to get a client_id and client_secret
  2. Ask the client if they want to sign in via a third party
  3. Redirect to a third party authentication endpoint
  6. Make a request to a third-party API endpoint
  7. Receive authorization code
  7. Make a request to the access token endpoint
  4. Receive access token
2. What can you do with an authorization code?
exchange it for an access token [src](https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/#:~:text=The%20authorization%20code%20is%20a,approve%20or%20deny%20the%20request.)
3. What can you do with an access token?
use it to make api calls on behalf of the user [src](https://www.oauth.com/oauth2-servers/access-tokens/#:~:text=Access%20tokens%20are%20the%20thing,in%20transit%20and%20in%20storage.)
4. What’s a benefit of using OAuth instead of your own basic authentication?
more secure because you don't have the burden of saving passwords in your own db and then having to worry about liability or being hacked giving away access to user accounts.

## Vocabulary Terms

* Client ID: public identifier for apps unique across all clients that the auth server handles [src](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/#:~:text=The%20client_id%20is%20a%20public%20identifier%20for%20apps.&text=It%20must%20also%20be%20unique,that%20the%20authorization%20server%20handles.)
* Client Secret: Client Secret (OAuth 2.0 client_secret) is a secret used by the OAuth Client to Authenticate to the Authorization Server. The Client Secret is a secret known only to the OAuth Client and the Authorization Server. Client Secret must be sufficiently random to not be guessable. [src](https://ldapwiki.com/wiki/Client%20Secret#:~:text=Client%20Secret%20(OAuth%202.0%20client_secret,random%20to%20not%20be%20guessable.)
* Authentication Endpoint
security mechanism to make sure that only authorized devices can connect [src](https://whatis.techtarget.com/definition/endpoint-authentication#:~:text=Endpoint%20authentication%20is%20a%20security,also%20known%20as%20device%20authentication.&text=Authenticating%20both%20the%20user%20and,%2Dfactor%20authentication%20(2FA).)
* Access Token Endpoint: The token endpoint is where apps make a request to get an access token for a user. [src](https://www.oauth.com/oauth2-servers/access-tokens/#:~:text=The%20token%20endpoint%20is%20where,Client%20Credentials)
* API Endpoint: one end of the communication channel between a client and the api (the api end)[src](https://smartbear.com/learn/performance-monitoring/api-endpoints/#:~:text=Simply%20put%2C%20an%20endpoint%20is,of%20a%20server%20or%20service.&text=The%20place%20that%20APIs%20send,lives%2C%20is%20called%20an%20endpoint.)
* Authorization Code: the code the client sends to the auth api to get an access token. (see questions above for src)
* Access Token: the token we use to to make api calls on behalf of the authenticated user (see questions above for src)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
  - oAuth
  - what bearer auth is and how it works
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - also oAuth...
3. What are you most excited about trying to implement or see how it works?
  - oAuth! Can't wait to implement it and try it out

## Preparation Materials

* [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)
* [Intro to JWT](https://jwt.io/introduction/)
* [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

## Bookmark

* [npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)