
1. Client Creation
	1. Client Type (Identity Protocols):
		1. OpenID Connect
			- Used for modern application, mostly used for web and mobile application.
			- Its a extension of OAuth 2 and uses JWT.
		2.  SAML
			 - Uses XML for its identity data format and simple HTTP or SOAP for data transport mechanisms
	2. Always display in UI
		- To enable/show client on the admin console, even if the client is not active. Helps to manage client easily.
	 3. Client Authentication
		 - When turned on, clients are required to authenticate themselves when making requests to Keycloak. Done via credentials like a client secret, a client certificate, or other methods depending on the configuration.
	  4. Authorization
		  - Used to fine grained control for authorization.
	  5. Authentication Flow
		  - Standard Flow - activates Authorization Code Flow
			  - Authorization Code Flow (with PKCE)
				**Description:** The Authorization Code Flow with Proof Key for Code Exchange (PKCE) is highly recommended for Single Page Applications (SPAs) like those built with Angular or React.
				**How It Works:** The application redirects the user to the Keycloak login page. After authentication, Keycloak redirects back to the application with an authorization code. The application then exchanges this code for an access token and refresh token.
				Advantages:
				**Security:** Tokens are not exposed in URLs, reducing the risk of token leakage.
				Support for SPAs: PKCE enhances security for public clients (like SPAs) that cannot securely store client secrets.
				**Standard Approach:** Widely supported and recommended for modern web applications.
				Use Case: Ideal for applications where you need secure token handling and are using front-end frameworks like Angular or React.
		