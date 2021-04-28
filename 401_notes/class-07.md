# Class 07

## Review, Research, and Discussion

1. Write the following steps in the correct order:
    - Register your application to get a client_id and client_secret
    - Ask the client if they want to sign in via a third party
    - Make a request to a third-party API endpoint
    - Redirect to a third party authentication endpoint
    - Make a request to the access token endpoint
    - Receive access token
    - Receive authorization code
    
2. [What can you do with an authorization code?](https://www.investopedia.com/terms/a/authorization-code.asp)
    - An authorization code is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space. An authorization code is typically a sequence of letters, numbers, or a combination of both, that validates a person's identity, approves a transaction or provides access to a secured area.

3. [What can you do with an access token?](https://www.oauth.com/oauth2-servers/access-tokens/#:~:text=Access%20tokens%20are%20the%20thing,in%20transit%20and%20in%20storage.)
    - Access tokens are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user’s data.
    - Access tokens must be kept confidential in transit and in storage. The only parties that should ever see the access token are the application itself, the authorization server, and resource server.

4. What’s a benefit of using OAuth instead of your own basic authentication?
    - OAuth is more secure

 ## Vocabulary Terms

1. [Client ID](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
    - The client_id is a public identifier for apps. Even though it’s public, it’s best that it isn’t guessable by third parties, so many implementations use something like a 32-character hex string. It must also be unique across all clients that the authorization server handles. If the client ID is guessable, it makes it slightly easier to craft phishing attacks against arbitrary applications.

2. [Client Secret](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
    - The client_secret is a secret known only to the application and the authorization server. It must be sufficiently random to not be guessable, which means you should avoid using common UUID libraries which often take into account the timestamp or MAC address of the server generating it. A great way to generate a secure secret is to use a cryptographically-secure library to generate a 256-bit value and converting it to a hexadecimal representation.

3. [Authentication Endpoint](https://whatis.techtarget.com/definition/endpoint-authentication#:~:text=Endpoint%20authentication%20is%20a%20security,also%20known%20as%20device%20authentication.&text=Authenticating%20both%20the%20user%20and,%2Dfactor%20authentication%20(2FA).)
    - Endpoint authentication is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service.

4. [Access Token Endpoint](https://auth0.com/docs/protocols/protocol-oauth2)
    - The /oauth/token endpoint is used by the application in order to get an access token or a refresh token. It is used by all flows except for the Implicit Flow because in that case an access token is issued directly.

    - In the Authorization Code Flow, the application exchanges the authorization code it got from the authorization endpoint for an access token.

    - In the Client Credentials Flow and Resource Owner Password Credentials Grant Exchange, the application authenticates using a set of credentials and then gets an access token.

5. [API Endpoint](https://smartbear.com/learn/performance-monitoring/api-endpoints/)
    - An endpoint is one end of a communication channel. When an API interacts with another system, the touchpoints of this communication are considered endpoints. For APIs, an endpoint can include a URL of a server or service. Each endpoint is the location from which APIs can access the resources they need to carry out their function.
6. [Authorization Code](https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/)
    - The authorization code is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.

7. [Access Token](https://auth0.com/docs/tokens/access-tokens)
    - Access tokens are used in token-based authentication to allow an application to access an API. The application receives an access token after a user successfully authenticates and authorizes access, then passes the access token as a credential when it calls the target API. The passed token informs the API that the bearer of the token has been authorized to access the API and perform specific actions specified by the scope that was granted during authorization.