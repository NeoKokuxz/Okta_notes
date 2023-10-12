# Sign users in to your SPA using the redirect model

- Create an integration that represents your app in your Okta org.
- Add dependencies and configure your app to use Okta redirect authentication.
- Add sign-in and sign-out actions.
- Require authentication on protected routes.
- Get authenticated user info.
- Make an HTTP call with the access token.
- Check the integration by signing in a user.

## Step 1: Install Okta CLI

```bash
# Install Okta CLI on terminal
brew install --cask oktadeveloper/tap/okta
```

```bash
# Register Okta
~ % okta register
First name: Neo
Last name: AvoMD
Email address: neo@avomd.io
Country: USA
Creating new Okta Organization, this may take a minute:
An account activation email has been sent to you.

Check your email
New Okta Account created!
Your Okta Domain: https://dev-05801763.okta.com <- This is the URL to Okta admin console
                                                    
```

## Step 2: Set up new app integration
1. Create a new app integration
2. OIDC - OpenID Connect
  - Token-based OAuth 2.0 authentication for Single Sign-On (SSO) through API endpoints. Recommended if you intend to build a custom app integration with the Okta Sign-In Widget.
3. Single-Page Application
  - Single-page web applications that run in the browser where the client receives tokens (for example, Javascript, Angular, React, Vue)


