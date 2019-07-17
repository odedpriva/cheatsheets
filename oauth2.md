# oauth2

## Authorization Code Grant

     +----------+
     | Resource |
     |   Owner  |
     |          |
     +----------+
          ^
          |
         (B)
     +----|-----+          Client Identifier      +---------------+
     |         -+----(A)-- & Redirection URI ---->|               |
     |  User-   |                                 | Authorization |
     |  Agent  -+----(B)-- User authenticates --->|     Server    |
     |          |                                 |               |
     |         -+----(C)-- Authorization Code ---<|               |
     +-|----|---+                                 +---------------+
       |    |                                         ^      v
      (A)  (C)                                        |      |
       |    |                                         |      |
       ^    v                                         |      |
     +---------+                                      |      |
     |         |>---(D)-- Authorization Code ---------'      |
     |  Client |          & Redirection URI                  |
     |         |                                             |
     |         |<---(E)----- Access Token -------------------'
     +---------+       (w/ Optional Refresh Token)

## Oauth2 terminalogy

* Resource Owner (user) - The user capable of granting access to a protected resource.
* Client - An application making protected resource requests on behalf of the resource owner and     with its authorization
* Authorization server - The server issuing access tokens to the client after successfully
  authenticating the resource owner and obtaining authorization
* Resource server
* Authorization grant
* Redirect URI
* Access token
* Back channel
* Front channel

## external links

* [oauth debugger](https://oauthdebugger.com/)
* [openid connect debugger](https://oidcdebugger.com/)
