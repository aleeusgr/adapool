**Adapool: Centralized Market Maker for Cardano**
=====================================================

**Overview**
------------

Adapool is a centralized market maker (CMM) library designed for the Cardano blockchain. It provides a simple and efficient way to interact with the Cardano blockchain, allowing users to retrieve token balances and calculate constant product and conversion rates.

**Features**
------------

* **Token Balance Retrieval**: Retrieve the amounts of ADA and USDT tokens in a user's wallet.
* **Constant Product Calculation**: Calculate the constant product of a liquidity pool based on the token balances.
* **Conversion Rate Calculation**: Calculate the conversion rate between ADA and USDT tokens.

**Installation**
------------

To use Adapool, you'll need to have Node.js installed on your system. You can install Adapool using npm:
```bash
npm install adapool
```
**Usage**
-----

```javascript
const Adapool = require('adapool');

// Initialize the Adapool instance with your wallet address and credentials
const adapool = new Adapool({
  walletAddress: 'addr123',
  credentials: {
    user: 'username',
    password: 'password',
  },
});

// Retrieve the ADA balance of the wallet
adapool.getAdaBalance()
  .then((balance) => console.log(`ADA balance: ${balance}`))
  .catch((error) => console.error(`Error: ${error}`));

// Retrieve the USDT balance of the wallet
adapool.getUsdtBalance()
  .then((balance) => console.log(`USDT balance: ${balance}`))
  .catch((error) => console.error(`Error: ${error}`));

// Calculate the constant product of a liquidity pool
adapool.calculateConstantProduct(1000, 1000)
  .then((product) => console.log(`Constant product: ${product}`))
  .catch((error) => console.error(`Error: ${error}`));

// Calculate the conversion rate between ADA and USDT
adapool.calculateConversionRate(1000, 1000)
  .then((rate) => console.log(`Conversion rate: ${rate}`))
  .catch((error) => console.error(`Error: ${error}`));
```
**API Documentation**
--------------------

### `Adapool`

* `new Adapool(options)`: Initializes a new Adapool instance with the given options.
	+ `options.walletAddress`: The address of the wallet to interact with.
	+ `options.credentials`: An object containing the username and password for the wallet.

### `getAdaBalance()`

* Retrieves the ADA balance of the wallet.
* Returns a promise that resolves with the ADA balance.

### `getUsdtBalance()`

* Retrieves the USDT balance of the wallet.
* Returns a promise that resolves with the USDT balance.

### `calculateConstantProduct(adaBalance, usdtBalance)`

* Calculates the constant product of a liquidity pool based on the given ADA and USDT balances.
* Returns a promise that resolves with the constant product.

### `calculateConversionRate(adaBalance, usdtBalance)`

* Calculates the conversion rate between ADA and USDT based on the given ADA and USDT balances.
* Returns a promise that resolves with the conversion rate.

**License**
----------

Adapool is available under the MIT License.

**Contributing**
---------------

Contributions to Adapool are welcome! Please open an issue or submit a pull request to discuss changes or submit new features.

**Disclaimer**
--------------

Adapool is provided "as is" without warranty of any kind. Use at your own risk.
