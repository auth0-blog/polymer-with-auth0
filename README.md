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

1. Sign up for a [free Auth0 account](https://auth0.com/pricing) and log in.
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