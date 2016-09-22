# Polymer App with Auth0

How to add Auth0 [Lock](https://auth0.com/docs/libraries/lock) authentication to a Polymer web app.

## Dependencies

* [Node.js](http://nodejs.org)
* [Bower](http://bower.io) `npm install bower -g`
* [Auth0 account](https://auth0.com/pricing) (free)

## Setup

1. Install the Polymer CLI: `npm install -g polymer-CLI`.
2. Clone this repo into the folder of your choice.
3. Run `bower install` to install Bower components.

## Integrate Your Auth0 Account

1. Sign up for a [free Auth0 account](https://auth0.com/signup).
2. In your **Auth0 Dashboard**, [create a new client](https://manage.auth0.com/#/clients/create).
3. Name your new app and select "Single Page Web Applications".
4. In the **Settings** section for your newly created app, add `http://localhost:8080` to the Allowed Callback URLs and Allowed Logout URLs.
5. Open the `/src/my-app.html` file and replace the following with your app domain and client ID (found in **Settings** for your Auth0 app):
```
<auth0-login 
	client-id="[YOUR_CLIENT_ID]" 
	domain="[YOUR_DOMAIN].auth0.com" 
	redirect-url="http://localhost:8080"></auth0-login>
```

## Serve

Serve the Polymer project from the project folder: `polymer serve` (can be accessed in browser at [http://localhost:8080](http://localhost:8080), or add the `--open` flag to auto-launch in your default browser)

## What is Auth0?

Auth0 helps you to:

* Add authentication with [multiple authentication sources](https://docs.auth0.com/identityproviders), either social like **Google, Facebook, Microsoft Account, LinkedIn, GitHub, Twitter, Box, Salesforce, amont others**, or enterprise identity systems like **Windows Azure AD, Google Apps, Active Directory, ADFS or any SAML Identity Provider**.
* Add authentication through more traditional **[username/password databases](https://docs.auth0.com/mysql-connection-tutorial)**.
* Add support for **[linking different user accounts](https://docs.auth0.com/link-accounts)** with the same user.
* Support for generating signed [Json Web Tokens](https://docs.auth0.com/jwt) to call your APIs and **flow the user identity** securely.
* Analytics of how, when and where users are logging in.
* Pull data from other sources and add it to the user profile, through [JavaScript rules](https://docs.auth0.com/rules).

## Create a free Auth0 account

1. Go to [Auth0](https://auth0.com/signup).
2. Use Google, GitHub or Microsoft Account to log in.

## Issue Reporting

If you have found a bug or if you have a feature request, please report them at this repository issues section. Please do not report security vulnerabilities on the public GitHub issue tracker. The [Responsible Disclosure Program](https://auth0.com/whitehat) details the procedure for disclosing security issues.

## Author

[Auth0](auth0.com)

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE) file for more info.