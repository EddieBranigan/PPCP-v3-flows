# PPCP v3 vaulted flows demo
A simple PPCP server built in NodeJS with express framework and using the PayPal client-side JavaScript SDK. This is a proof of concept Demo and not a production ready solution.

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
Testing in the PayPal sandbox environment can be done by creating test Sandbox personal and business accounts as described here in the ['https://developer.paypal.com/tools/sandbox/accounts/'](#official developer documentation here).

## Payment flow
First, visit the index page at http://localhost:8000 and click the new customer button. Login to your test personal account and complete the flow. After, return to the index page and select the returning customer button. Click the one-click button to experience the returning customer flow.
## Disclaimer
This repository is for illustrative purposes only and shouldn't be used directly in a live environment.
