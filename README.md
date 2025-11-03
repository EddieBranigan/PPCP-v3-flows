# PPCP v3 vaulted flows demo
A simple PPCP server built in NodeJS with express framework and using the PayPal REST API and client-side JavaScript SDK. The Demo shows how a customers PayPal payment method can be stored and used for future purchases using the v3 vaulted payment flow. It also shows a returning customer present flow and how a stored PayPal payment method can be used for a one-click checkout experience.

The developer documentation for this flow can be viewed from [this link on the paypal developer website](https://developer.paypal.com/docs/checkout/save-payment-methods/purchase-later/js-sdk/paypal/).

This is a proof of concept Demo and not a production ready solution.

## Setup instructions
Install the packages from the package-json file by typing into terminal:
```
npm install
```

Create a .env file in the route of your project folder with your PPCP credentials in it, [following this guide](https://developer.paypal.com/api/rest/#link-getclientidandclientsecret). See example below:

```
PAYPAL_CLIENT_ID='YOUR CLIENT ID GOES HERE'
PAYPAL_CLIENT_SECRET='YOUR CLIENT SECRET GOES HERE'
MERCHANT_ID='MERCHANT ID FOR your sandbox business account'
```

## Start the server
Start the server by typing into terminal:
```
node server.js
```

## Testing
Testing in the PayPal sandbox environment can be done by creating test Sandbox personal and business accounts as described here in the [official developer documentation here](https://developer.paypal.com/tools/sandbox/accounts/).
_ From index.html page, click the new customer button and login to your personal sandbox account.
_ After logging into your account and agreeing to have your payment method stored, make note of the stored payment id, which is needed for the next step.
Next, go back to the index.html page and click the returning customer button.
_ Enter the stored payment id into the form and click submit. This will initialise the client-side sdk with the customers stored payment method and provide the one-click checkout button.
_ Click the PayPal button to see the server response.

## Payment flow
First, visit the index page at http://localhost:8000 and click the new customer button. Login to your test personal account and complete the flow. After, return to the index page and select the returning customer button. Click the one-click button to experience the returning customer flow.
## Disclaimer
This repository is for illustrative purposes only and shouldn't be used directly in a live environment.
