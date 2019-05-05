# moneris
A wrapper to access the Moneris API.

## Installation

With [npm](https://npmjs.org/):

```bash
npm install moneris --save
```

## Usage

**`moneris(credentials, req[, extended])`**

Queries the Moneris API with the information provided.

- `credentials`: **Required.** An object with the following fields.
  - `api_token`: **Required.** Your API token.
  - `store_id`: **Required.** Your store ID.
  - `test`: Optional. If true, uses Moneris Test endpoints. You can get a `api_token` and `store_id` for this endpoint from Moneris's Documentation. `false` by default.
- `req`: **Required.** An object with the following fields.
  - `type`: **Required.** The type of the request you wish to post.
  - ...All other fields that pertain to that type of request.
- `extended`: Optional. Certain types of requests require additional parameters, including but not limited to CVD, AVS, etc. This is an object that will add directly to the sent data (whereas `req` will create its own child element)

## testing

Run `tests/testPurchase.js`
