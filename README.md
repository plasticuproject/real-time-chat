# Example App Using Node, TypeScript, and React

## Requirements

* Install [Node.js](https://nodejs.org)

## Development setup

* Clone or download this repository
* Install modules using `npm install`
* Copy `.env.sample` to `.env`
* Install the [Okta CLI](https://cli.okta.com/) and run `okta register` to sign up for a new account, or if you already have an account, run `okta login`.
* Set up a new Okta application

    1. Run `okta apps create`. Select the default app name, or change it as you see fit.
    2. Choose **Single Page App** and press **Enter**.
    3. Press **Enter** to set the Redirect URI to `http://localhost:8080/callback` and accept the default Logout Redirect URI of `http://localhost:8080`.
    4. Press **Enter** to set the Post Logout Redirect URI to `http://localhost:8080/`
    5. Save your OKTA_ORG_URL and OKTA_CLIENT_ID

You'll also need to create a token in Okta.
* To create the token:

    1. Sign in to your Okta organization using the OKTA_ORG_URL
    2. Access the API page: In the Admin Console, select **API** from the **Security** menu and then select the **Tokens** tab.
    3. Click **Create Token**.
    4. Name your token and click **Create Token**.
    5. Record the token value. This is the only opportunity to see it and record it.

* Copy and paste your `OKTA_CLIENT_ID`, `OKTA_TOKEN`, and `OKTA_ORG_URL` into the `.env` file as such.
```
OKTA_ORG_URL=https://{yourOktaOrgUrl}
OKTA_CLIENT_ID={yourClientId}
OKTA_TOKEN={yourToken}
```

Now you can run both the Node backend and the React frontend with the following command:

```
npm start
```

## License

Apache 2.0, see [LICENSE](LICENSE).

