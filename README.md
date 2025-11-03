# PPCP v3 vaulted flows demo
A simple PPCP server built in NodeJS with express framework and using the PayPal REST API and client-side JavaScript SDK. The Demo shows how a customers PayPal payment method can be stored and used for future purchases using the v3 vaulted payment flow. It also shows a returning customer present flow and how a stored PayPal payment method can be used for a one-click checkout experience.

The developer documentation for this flow can be viewed from [this link on the paypal developer website](https://developer.paypal.com/docs/checkout/save-payment-methods/purchase-later/js-sdk/paypal/).

This is a proof of concept Demo and not a production ready solution.

## Setup instructions
Install the packages from the package-json file by typing into terminal:
```
npm install
```

Make sure to create a .env file with your gateway credentials in it. An example is provided ('example.env').

## Start the server
Start the server by typing into terminal:
```
node server.js
```

## Testing
Testing in the PayPal sandbox environment can be done by creating test Sandbox personal and business accounts as described here in the [official developer documentation here](https://developer.paypal.com/tools/sandbox/accounts/).

## Payment flow
First, visit the index page at http://localhost:8000 and click the new customer button. Login to your test personal account and complete the flow. After, return to the index page and select the returning customer button. Click the one-click button to experience the returning customer flow.
## Disclaimer
This repository is for illustrative purposes only and shouldn't be used directly in a live environment.
