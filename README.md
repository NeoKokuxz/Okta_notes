# Okta Notes

## Redirect vs. embedded 

### Redirect 
Redirect authentication: A user sign-in flow that grants authentication control to Okta by redirecting to an Okta hosted sign-in page. This flow uses open protocols like OAuth 2.0 and SAML.

#### Redirect summary
Use it straight out of the box.
Use it easily with no maintenance and no updates as Okta hosts and secures.
XSS (opens new window)(cross-site scripting) attacks on your app don't affect the sign-in experience.
Integrate it easily either manually or with a generic OpenID Connect client.
Customize it through HTML, CSS, and JavaScript.
Complex logic changes that require source code access are limited.
Redirects the user out of the app to Okta, and then back to the app.
Handles most client deployment requirements.

#### Use the redirect deployment model when you
Have multiple apps or use third-party apps and need SSO.
Want Okta to control the authentication flows through policy configuration.
Want Okta to control upgrades to take advantage of new functionality.
Have an app that already uses an OAuth 2.0 or SAML provider to sign in.

### embedded
Embedded authentication: A user sign-in flow where the app retains authentication control without redirection to Okta. This flow uses a client-hosted embedded Sign-In Widget, SDKs, or direct API calls.

#### Embedded summary
Moderate maintenance may be required. If using a CDN, maintenance is more limited as Okta keeps it up to date. NPM packages a specific version of the widget, which means that it may need to be updated in the project periodically. Customized or local versions of the Sign-In Widget source code require regular updating.
A great level of source code customization control is offered while being drastically easier and more secure than building from scratch.
There's a slightly increased risk in security due to Okta not being able to guarantee that the Sign-In Widget has been implemented correctly. The app code may be able to access the credentials that the user enters into the Sign-In Widget, which needs to be kept secure.
XSS (cross-site scripting) attacks on your app may result in stolen sign-in credentials.
A higher level of effort to integrate and maintain is required compared to the Okta-hosted Sign-In Widget.
The user is kept in the app, which reduces redirects to and from Okta.
