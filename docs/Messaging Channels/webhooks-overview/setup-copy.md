---
title: Setup (COPY)
excerpt: Learn how to set up webhooks.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Set Up Webhooks

Webhooks send an HTTP API request to a specified endpoint on your server, including information about the user, such as event details or user properties. As part of the setup, you will configure this endpoint on your server to receive and process the webhook requests.

To set up your first CleverTap webhook:

1. Navigate to _Settings_ > _Engage_ > _Channels_> _Webhooks_ from the CleverTap dashboard.
2. Click **+ Add Webhook**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a6763a789646a09f0de7c85469f74d6c6abf2bf49c1b03cac5cab31e44919df1-Add_a_Webhook.png",
        "",
        "Add a Webhook"
      ],
      "align": "center",
      "border": true,
      "caption": "Add a Webhook"
    }
  ]
}
[/block]


3. Configure the webhook template.

> 📘 HTTP Methods
> 
> The following four HTTP methods are available for webhooks templates:
> 
> - POST
> - GET
> - DELETE 
> - PUT

4. Add a webhook _Name_ and _Destination URL_. If you currently do not have an endpoint created on your server to receive the webhook, you can use [requestcatcher.com](https://requestcatcher.com) to create and test endpoint.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8326c7fdc753b9b70359152cd3de88d4b63ef0b00734c539460e719dacb0c0fa-Create_Webhook_Template.png",
        "",
        "Configure Webhook Template"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Configure Webhook Template"
    }
  ]
}
[/block]


Select _[Authenticaton type](doc:setup-webhooks#authentication-type)_  from the _Authentication_ tab.

4. Click **Create**. CleverTap sends the following payload to your configured endpoint:

```json
{
   "is_test":true,
   "targetId":1234,
   "key_values":{
      "key":"value"
   },
   "profiles":[
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      }
   ]
}
```

CleverTap saves the template if your endpoint responds with an **HTTP status 200 OK**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bff36a1-CreateWebhookTemplate.jpg",
        "Sample Webhook Campaign Setup",
        606
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Sample Webhook Setup"
    }
  ]
}
[/block]


> 🚧 Webhook Errors
> 
> CleverTap sends the request and waits for three seconds for a response from the endpoint. If the endpoint URL fails to respond then CleverTap retries the request. If the retry attempt fails, the campaign stats page is updated with the error "Webhook Dispatch Failed." 
> 
> Also, another probable cause for the error is if the webhook endpoint is temporarily unavailable or down.

<br />

# Partner Tool for Setup

Another option besides setting up an endpoint on your server to listen to CleverTap webhooks is using a partner tool to report certain events. Let us consider a sample use case for better understanding.

For your recently published [In-App rating](doc:create-message-inapp#ratings-template) campaign, you want to capture details of customers who provide negative feedback. You can configure a webhook that captures details of all the customers submitting less than or equal to three ratings and create a support ticket for it on Zendesk. Creating the support ticket will help your customer support team to reach out to them.

For more information about how to set up a webhook and create a CleverTap webhook campaign to report tickets on Zendesk based on customer ratings submitted, refer to the detailed [integration guide](https://docs.clevertap.com/docs/zendesk#integrate-clevertap-with-zendesk).

# Authentication Type

Webhook authorization on CleverTap ensures that only verified sources can send data through your Webhooks. It uses one of the following methods:

- **No authentication**: Authenticate users by adding credentials such as a password or token via the _Headers_ tab.
- **Basic Authorization**: Authenticate using a username and password in the request headers to verify the sender’s identity.
- **OAuth 2.0**: Authenticate requests by obtaining an access token from CleverTap and adding the token to the request headers to ensure that only authorized systems can send data.

## Basic Authentication

Basic Authentication is a simple authentication method where the client sends an HTTP request with the following:

- Key: `Authorization` 
- Value: 'Basic '+ base 64 encoding of a user ID and password separated by a colon. 

> 📘 Security Advisory
> 
> The Basic authentication method suits webhooks sent to internal systems behind a firewall or secure infrastructure.

### Set Up Webhooks Using Basic Authentication

When setting up a webhook with Basic Authentication, CleverTap includes an _Authorization_ header in every HTTP request sent to your server. The header follows the format shown below:

```css
"Basic " + base64 encoding('YOUR_USERNAME:YOUR_PASSWORD')
```

## OAuth 2.0

OAuth is a secure authentication framework that lets CleverTap access resources for you without sharing your credentials. This method involves authenticating requests using an access token, which is added to the request headers to ensure that only authorized systems can access resources. 

This ensures that CleverTap securely accesses third-party data or services by obtaining proper authorization from customers and leveraging secure tokens to manage API requests without exposing sensitive customer credentials by leveraging secure tokens.

### Configure OAuth 2.0

CleverTap recommends using this method when you need a more secure and scalable approach to managing webhook authentication, especially when interacting with external APIs or services. To configure OAuth 2.0 on the CleverTap dashboard:

1. Navigate to _Settings_ > _Channels_ > _Webhooks_ and click **+ Webhook**. The _Create webhook template _ window opens on the right.
2. Add a webhook _Name_ and _Destination URL_. If you currently do not have an endpoint created on your server to receive the webhook, you can use [requestcatcher.com](https://requestcatcher.com) to create an endpoint for testing purposes.
3. Select OAuth 2.0 from the _Authenticaton Type_  list.
4. Select either from the following _Grant Type_ list:  

- [Password Credentials](doc:setup-webhooks#using-password-credentials) 
- [Client Credentials without JWT](doc:setup-webhooks#using-client-credentials)
- [Client Credentials with JWT](https://staging.docs.user.clevertap.net/docs/setup-webhooks#client-credentials-with-jwt)

### Grant Type

Grant Type in OAuth refers to the method CleverTap uses to obtain an access token from the authorization server. In CleverTap, there are two methods to obtain the access token:

#### Using Password Credentials

This method involves providing a username and password to obtain an access token. It is typically used when the application has direct access to user credentials. Here is the detailed flow:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50dbc41f055a335a6a001efa517efc3e067fb98366104439e88aa7918fd00f85-Password_Credentials.png",
        null,
        "Password Credentials Flow"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Password Credentials Flow"
    }
  ]
}
[/block]


1. _Provide User Credentials_: The user provides their credentials (username and password) to CleverTap.
2. _Send Credentials to Authentication Server_: CleverTap sends the user credentials to the authorization server. This request must include the following in the request header: Client ID and Client Secret Key.
3. _Receive Access Token_: If the user credentials are correct, the authorization tool responds with an access token.
4. _Use Access Token_: CleverTap uses this access token to make authorized requests to the resource server.
5. _Validate Access Token_: The resource server validates the access token before responding to your application's request.

#### Configure Password Credentials

1. Enter the following details after setting up the Grant Type as Password Credentials: 

| Field                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Client ID                  | <ul><li> A unique identifier issued to the requesting application (here, CleverTap) when it registers with an authorization server.</li> <li> It helps the authorization server recognize the application that makes the request and applies relevant authorization policies.</li></ul>                                                                                                                                                                                                                                                           |
| Secret                     | <ul> <li>A confidential key issued to CleverTap during registration.</li><li>It is used to authenticate the identity of the client application (here, CleverTap) and must be kept secure.</li> <li> It works alongside the Client ID to authenticate the identity of the requesting application and to prevent unauthorized parties from impersonating the requesting application.</li></ul>                                                                                                                                                      |
| Username\*                 | <ul> <li>A unique identifier issued to the resource owner, which is necessary when the OAuth flow requires a user’s credentials. </li> <li>It is required when you are using the _Password Credentials_ grant type, where the application needs to directly authenticate the user. </li></ul>                                                                                                                                                                                                                                                     |
| Password\*                 | <ul> <li>It works alongside the username to authenticate the resource owner (user) directly when the OAuth flow requires a user’s credentials.</li> <li>It is required when you are using the _Password Credentials_ grant type, where the application needs to directly authenticate the user. </li></ul>                                                                                                                                                                                                                                        |
| Scopes                     | <ul> <li> The parameters in OAuth that define the specific permissions requested by the client application.</li> <li> They control what parts of a user's account the client (here, CleverTap) has access to, such as reading profile data and so on.</li></ul>                                                                                                                                                                                                                                                                                   |
| Access Token URL           | The endpoint on the authorization server where a client application (CleverTap) sends a request to obtain an access token.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Refresh Token URL\*        | The endpoint on an authorization server where a client application sends a request to obtain a new access token using a refresh token. This field is available only when using _Password Credentials_ grant type.                                                                                                                                                                                                                                                                                                                                 |
| Client Authentication Type | <ul> <li>The method used by a client application to prove its identity to the authorization server in OAuth 2.0 flows. </li> <li> This ensures that only the authorized client can request tokens or access protected resources. </li> <li> The following are the available options:<ul><li> _Send Basic Authentication in Header_: Include an Authorization header with encoded username and password. </li><li>_Send Bearer Authentication in Header_: Include an Authorization header with an access token obtained from OAuth.</li></ul></ul> |

<br />

2. Click **Generate**. This creates the Access Token using the provided credentials, which are displayed below: 
   1. Map the Access Token and Refresh Token (when using the Password Credentials grant type).
   2. Select an expiry option from the _Expiry_ dropdown.

The generated OAuth response includes a key with an expiry, which is not encoded.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d586260c10a6f55de0a73a0663819884a3d7107e00f3f77852fd19a0a88bedff-Select_Expiry_for_the_Token.png",
        "",
        "Select Expiry from Expiry Dropdown"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Select Expiry from Expiry Dropdown"
    }
  ]
}
[/block]


3. Click **+ Key-Value Pair** and enter the headers for the API.
4. Click **Save** to create a webhook.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/95b5dfc019affcfc50e89eeff114f94738f1a1d04101495d1f31a9ba501f1d93-Configure_OAuth_2.0.png",
        "",
        "Configure OAuth 2.0"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Configure OAuth 2.0"
    }
  ]
}
[/block]


#### Using Client Credentials without JWT

This method involves providing a client ID and client secret key to obtain an access token. This method does not require a username and password for the OAuth flow; instead, it relies on these credentials to authenticate the application and generate a token for secure interactions. Here are the detailed steps:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e139311bd9f0c65bbf95749855a9af4dc8c643d01b9c2fd3599e8eb34e494f9-Client_Credentials.png",
        null,
        "Client Credentials Flow"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Client Credentials Flow"
    }
  ]
}
[/block]


1. _Send Authorization Request to Authorization Server_: CleverTap makes an authorization request to the authorization server using the Client Credentials, such as Client ID and Secret Key.
2. _Receive Access Token_: The authorization tool responds with an access token if the client credentials are accurate.
3. _Use Access Token_: CleverTap uses this access token to make authorized requests to the resource server (for example, accessing user data).
4. _Validate Access Token_: The resource server validates the access token before responding to the request.

#### Configure Client Credentials without JWT

1. Enter the following details after setting up the Grant Type as Client Credentials without JWT:

| Field                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Client ID                  | <ul><li> A unique identifier issued to the requesting application (here, CleverTap) when it registers with an authorization server.</li> <li> It helps the authorization server recognize the application that makes the request and applies relevant authorization policies.</li></ul>                                                                                                                                                                                                                                                           |
| Secret                     | <ul> <li>A confidential key issued to CleverTap during registration.</li><li>It is used to authenticate the identity of the client application (here, CleverTap) and must be kept secure.</li> <li> It works alongside the Client ID to authenticate the identity of the requesting application and to prevent unauthorized parties from impersonating the requesting application.</li></ul>                                                                                                                                                      |
| Scopes                     | <ul> <li> The parameters in OAuth that define the specific permissions requested by the client application.</li> <li> They control what parts of a user's account the client (here, CleverTap) has access to, such as reading profile data and so on.</li></ul>                                                                                                                                                                                                                                                                                   |
| Access Token URL           | The endpoint on the authorization server where a client application (CleverTap) sends a request to obtain an access token.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Client Authentication Type | <ul> <li>The method used by a client application to prove its identity to the authorization server in OAuth 2.0 flows. </li> <li> This ensures that only the authorized client can request tokens or access protected resources. </li> <li> The following are the available options:<ul><li> _Send Basic Authentication in Header_: Include an Authorization header with encoded username and password. </li><li>_Send Bearer Authentication in Header_: Include an Authorization header with an access token obtained from OAuth.</li></ul></ul> |

<br />

2. Click **Generate**. This creates the Access Token using the provided credentials, which are displayed below: 
   1. Map the Access Token and Refresh Token (when using the Password Credentials grant type).
   2. Select an expiry option from the _Expiry_ dropdown.

The generated OAuth response includes a key with an expiry, which is not encoded.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d586260c10a6f55de0a73a0663819884a3d7107e00f3f77852fd19a0a88bedff-Select_Expiry_for_the_Token.png",
        "",
        "Select Expiry from Expiry Dropdown"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Select Expiry from Expiry Dropdown"
    }
  ]
}
[/block]


3. Click **+ Key-Value Pair** and enter the headers for the API.
4. Click **Save** to create a webhook.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/95b5dfc019affcfc50e89eeff114f94738f1a1d04101495d1f31a9ba501f1d93-Configure_OAuth_2.0.png",
        "",
        "Configure OAuth 2.0"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Configure OAuth 2.0"
    }
  ]
}
[/block]


#### Using Client Credentials with JWT

JSON Web Tokens (JWT) OAuth 2.0 offers a secure way to authenticate and authorize third-party applications while protecting sensitive data. In CleverTap, this integration allows marketers to securely manage access to resources and send/receive identity claims via webhooks. CleverTap uses JWT for webhooks, ensuring that the data transmitted is encrypted, verifiable, and secure.

While OAuth 2.0 helps secure API access, there is still the risk of token theft. If an attacker intercepts an access token, they can impersonate the legitimate client and make unauthorized requests to the CleverTap APIs. This is where JWT (JSON Web Token) comes in, enhancing security. With an added layer of security, JWT secures data as follows.

- **Tamper-Proof**: JWTs are signed using a private key, ensuring that the signature becomes invalid if an attacker tries to modify the token.
- **Compact and Self-Contained**: JWTs contain all the necessary information (claims) in the token itself, reducing the need for constant database checks.
- **Portable**: JWTs can be passed between systems easily and are ideal for authentication in distributed environments like webhooks.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7d6d2ce41a7cee5ee410b52b9e2e0902d655d176594dab6076968e28a6ea332-JWT_1.png",
        "",
        "Client Credentials with JWT"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Client Credentials with JWT"
    }
  ]
}
[/block]


1. **CleverTap Generates Public and Private Keys**:  
   CleverTap generates a private key and a corresponding public key. The private key is kept secure by CleverTap, and the public key is shared with the client to validate JWTs.

2. **Client Assertion (JWT)**:  
   The client creates a client assertion a JWT that contains key information such as:
   - **Header**: Specifies the signing algorithm (e.g., RSA).
   - **Payload**: Contains the client's credentials (`client_id`), audience (`aud`), expiration (`exp`), and other claims.
   - **Signature**: The JWT is signed using the issuesprivate key generated by CleverTap, ensuring its integrity.

3. **Client Sends JWT to Auth Server**:  
   The client sends the client assertion (JWT) to the Auth Server to request an access token.

4. **Auth Server Validates the JWT**:  
   The Auth Server uses the public key to verify the JWT's signature. If the token is valid and unaltered, the server proceeds to issue an access token.

5. **Access Token Issued**:  
   Once validated, the Auth Server issues an access token to the client. The access token is then used for secure communication with the CleverTap API.

##### Securing OAuth 2.0 with JWT

Using JWT adds an extra layer of security to OAuth 2.0. Here’s how it works:

- **Signature Verification**: Only CleverTap holds the private key to sign the JWT. The Auth Server uses the public key to verify the signature. Any modification to the JWT will cause the signature to mismatch, leading to rejection.
- **Preventing Token Theft**: Even if intercepted, the JWT can't be altered or reused without the private key. It’s self-contained with necessary info (e.g., client identity, permissions, expiration), reducing the risk of sensitive data exposure.
- **No Repeated `client_secret` Transmission**: The client doesn't need to send the `client_secret` with each request. Instead, the signed JWT proves its identity and authorization, minimizing secret exposure.
- **Short-Lived Tokens**: Access tokens are short-lived (minutes or hours), limiting damage if compromised. Once it expires, the client must request a new token securely.

#### Configure Client Credentials with JWT

The public key must be configured on the client's OAuth server for the verification process to work. This allows the server to verify the authenticity of the JWS. The JWT cannot be trusted if the signature verification fails and should be discarded. On the other hand, if both the signature verification and claims validation are successful, CleverTap will receive the access token from their OAuth server.

> 📘 Note
> 
> CleverTap cryptographically signs the JWT to ensure its authenticity and integrity. This guarantees that the JWT is authentic and that it has not been altered or tampered with after creation. To sign the JWTs, CleverTap currently supports the following signature algorithms:
> 
> - `RS256`
> - `RS384`
> - `RS512`
> 
> Each of these algorithms requires the generation of RSA public-private key pairs. The private key is used to create the signed JWT (also referred to as a JWS), and the public key is used to verify the cryptographic signature of the JWS.

1. The following are steps to generate a Public Key: 
   1. **Generate Public Key**: Click **Generate Public Key**. The public key will encrypt sensitive data, such as access tokens, ensuring that only the intended recipient (your server) can decrypt and access this information using the corresponding private key.
   2. **Paste the Public Key to Your Server**: Copy the generated public key and paste it into the relevant configuration on your server. This allows your server to decrypt the data received from CleverTap securely.
   3. (Optional) **Regenerate Public Key**: Click **Regenerate Public Key** to enhance security. This will invalidate any previously generated keys, providing additional protection if you suspect that a key has been compromised or if you need to rotate keys periodically for security purposes.
2. **Set Up Client Assertion**.  
   After generating the Public Key, you must set up the Client Assertion. The Client Assertion is a JWT that authenticates your application and proves it is authorized to access CleverTap resources. It includes a Header, Payload, and Signature to ensure the integrity and authenticity of the request.

   - Header: The Header of a JWT contains metadata about the token, such as the signing algorithm and the type of token. The header is typically composed of two parts: the **algorithm** used to sign the token (for example, `RS256` for RSA) and the **type** of the token (usually `JWT`). The header also optionally contains other fields, such as a **key identifier** (`kid`) to indicate which public key should be used for signature verification. These details help CleverTap as a recipient understand how to process and verify the JWT.

   <br />

   | **Field**            | **Description**                                                                             | **Example Value** | **Reason/Purpose**                                                                                                           |
   | -------------------- | ------------------------------------------------------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------- |
   | Algorithm (`alg`)    | Specifies the algorithm used to sign the JWT. Possible values: `RS384`, `RS512`, or `RS256` | `RS256`           | Defines how the signature is created. The recipient (CleverTap) uses it to verify the token integrity.                       |
   | Type (`typ`)         | Defines the type of token.                                                                  | `JWT`             | Helps the system identify the token format, ensuring it is treated correctly as a JWT.                                       |
   | Key ID (`kid`)       | Identifies which public key should be used to verify the signature.                         | `12345`           | Allows CleverTap to find and use the correct public key for signature verification, especially with rotating keys.           |
   | Content Type (`cty`) | Specifies the content type of the JWT.                                                      | `JWT`             | Indicates that the JWT contains JWT data, ensuring correct handling by the recipient.                                        |
   | Critical (`crit`)    | Lists headers that must be processed by the recipient.                                      | `["exp", "aud"]`  | Ensures the recipient processes critical headers, such as **expiration** and **audience**, which are important for security. |

   <br />

   - Payload: The Payload of a JWT contains the claims - statements about an entity (typically the user) and additional data. The claims are categorized into three types: registered, public, and private. In the case of CleverTap's OAuth 2.0 integration, the **Issuer** (`iss`), **Subject** (`sub`), **Audience** (`aud`), **Issued At** (`iat`), and **Expiration Time** (`exp`) are the most commonly used claims. The Payload carries important information that validates the authenticity of the token and ensures its intended use. 

   <br />

   | **Field**               | **Description**                                                             | **Example Value**                       | **Reason/Purpose**                                                                                         |
   | ----------------------- | --------------------------------------------------------------------------- | --------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
   | Issuer (`iss`)          | The client ID that created and sent the JWT.                                | `your-client-id`                        | Identifies the entity that issued the token, allowing CleverTap to verify the source.                      |
   | Subject (`sub`)         | The client ID or user the token is issued for.                              | `your-client-id`                        | Identifies the client or user the token is issued for, ensuring the correct permissions are applied.       |
   | Audience (`aud`)        | Indicates the intended recipient of the token (CleverTap API endpoint).     | `https://api.clevertap.com/oauth/token` | Ensures that the token is sent to the correct recipient (CleverTap), used only for that specific audience. |
   | Issued At (`iat`)       | The timestamp when the token was created.                                   | `1626784891` (Unix timestamp)           | Ensures the token is fresh and helps manage the token lifecycle.                                           |
   | Expiration Time (`exp`) | Specifies when the token expires and is no longer valid.                    | `1626788491` (Unix timestamp)           | Prevents replay attacks by making the token invalid after a certain time.                                  |
   | JWT ID (`jti`)          | A unique identifier for the token, used to prevent reuse of the same token. | `unique-jwt-id-123`                     | Helps prevent replay attacks by ensuring each token is unique.                                             |
   | Use Issued At (`iat`)   | Whether the Issued At claim should be used.                                 | `Yes`                                   | Recommended to use to track when the token was issued, ensuring it’s not used prematurely or too late.     |
3. Click **Generate Client Assertion** to create the JWT after filling out the **Header** and **Payload** details.
4. Enter the required details after generating the Client Assertion.

   | Field                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
   | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
   | Client ID                  | <ul><li> A unique identifier issued to the requesting application (here, CleverTap) when it registers with an authorization server.</li> <li> It helps the authorization server recognize the application that makes the request and applies relevant authorization policies.</li></ul>                                                                                                                                                                                                                                                           |
   | Client Assertion Type      | <ul><li>The method used by the client (CleverTap) to authenticate itself to the authorization server using a JWT (JSON Web Token).</li><li>The JWT is sent in the request, and the server validates it to confirm the client's identity.</li><li>Commonly used in Client Credentials Flow and JWT Authorization Grant of OAuth 2.0.</li><li>More secure than basic authentication, as it relies on cryptographic signatures and short-lived tokens.</li></ul>                                                                                     |
   | Scopes                     | <ul> <li> The parameters in OAuth that define the specific permissions requested by the client application.</li> <li> They control what parts of a user's account the client (here, CleverTap) has access to, such as reading profile data and so on.</li></ul>                                                                                                                                                                                                                                                                                   |
   | Access Token URL           | The endpoint on the authorization server where a client application (CleverTap) sends a request to obtain an access token.                                                                                                                                                                                                                                                                                                                                                                                                                        |
   | Refresh Token URL\*        | The endpoint on an authorization server where a client application sends a request to obtain a new access token using a refresh token. This field is available only when using _Password Credentials_ grant type.                                                                                                                                                                                                                                                                                                                                 |
   | Client Authentication Type | <ul> <li>The method used by a client application to prove its identity to the authorization server in OAuth 2.0 flows. </li> <li> This ensures that only the authorized client can request tokens or access protected resources. </li> <li> The following are the available options:<ul><li> _Send Basic Authentication in Header_: Include an Authorization header with encoded username and password. </li><li>_Send Bearer Authentication in Header_: Include an Authorization header with an access token obtained from OAuth.</li></ul></ul> |

<br />

5. Click **Generate**. This creates the Access Token using the provided credentials, which are displayed below: 
   1. Map the Access Token and Refresh Token (when using the Password Credentials grant type).
   2. Select an expiry option from the _Expiry_ dropdown.

The generated OAuth response includes a key with an expiry, which is not encoded.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d586260c10a6f55de0a73a0663819884a3d7107e00f3f77852fd19a0a88bedff-Select_Expiry_for_the_Token.png",
        "",
        "Select Expiry from Expiry Dropdown"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Select Expiry from Expiry Dropdown"
    }
  ]
}
[/block]


6. Click **+ Key-Value Pair** and enter the headers for the API.
7. Click **Save** to create a webhook.

# FAQs

### Q. What are the timeouts and retry limits for Webhook?

A. The timeout for Webhook is 5 seconds with a retry limit of 2 times. For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).