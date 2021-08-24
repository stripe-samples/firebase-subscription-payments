# Run Subscription Payments with the Stripe Firebase Extension

This is an example web client for usage with the [Stripe Subscriptions Firebase Extension](https://firebase.google.com/products/extensions/firestore-stripe-subscriptions).

**Features:**

- Renders product and pricing details from your Cloud Firestore.
- Creates Stripe Checkout Sessions to start subscriptions for your customers.
- Syncs your subscription statuses with Firebase Authentication for access control management.
- Gives your users access to the Stripe Customer Portal.

## Demo

- https://stripe-subs-ext.web.app/

The design for Stripe Checkout and the customer portal can be customized in your Stripe Dashboard [branding settings](https://dashboard.stripe.com/settings/branding). See this example which is customized to match the Firebase color scheme:

## Setup

If you haven't already, [install the Firebase CLI](https://firebase.google.com/docs/cli):

```bash
npm install -g firebase-tools
```

### Install and configure the Firebase Extension

1. Install the [Stripe Subscriptions Firebase Extension](https://firebase.google.com/products/extensions/firestore-stripe-subscriptions).
2. Configure the extension in your Firebase Console.

### Configure the example web client

- In the [/public/javascript/app.js](/public/javascript/app.js) file set your
  - `STRIPE_PUBLISHABLE_KEY` from the [Stripe Dashboard](https://dashboard.stripe.com/apikeys).
  - `taxRates` array from the [Stripe Dashboard](https://dashboard.stripe.com/tax-rates).
  - `firebaseConfig` object from your Firebase console project settings.
  - `functionLocation` from your Cloud Functions location setting.

## Run locally

```bash
firebase serve --project {your Firebase project name}
# or
npm run dev
```

## Deploy to Firebase Hosting

```bash
firebase deploy
# or
npm run deploy
```

## Author

- [@thorsten-stripe](https://twitter.com/thorwebdev)
