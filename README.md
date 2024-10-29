# Constant Product Algorithm Trading on Bybit and Native ADA Wallet
=============================================================

Table of Contents
-----------------

1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Configuration](#configuration)
7. [Algorithms](#algorithms)
8. [Bybit Integration](#bybit-integration)
9. [Native ADA Wallet Integration](#native-ada-wallet-integration)
10. [License](#license)

## Overview
-----------

This project implements a constant product algorithm for trading USDT on Bybit and ADA on a native wallet. The algorithm adjusts the prices based on the current market conditions to maximize profit.

## Project Structure
---------------------

The project consists of the following directories:

* `bybit`: Contains the Bybit API client and trading logic.
* `ada_wallet`: Contains the native ADA wallet integration.
* `algorithm`: Contains the constant product algorithm implementation.
* `config`: Contains the project configuration files.

## Requirements
------------

* Python 3.8+
* `ccxt` library for Bybit API integration
* `cardanoserializationlib` library for ADA native wallet integration

## Installation
------------

To install the required libraries, run the following command:

```bash
pip install ccxt cardanoserializationlib
```

## Usage
-----

To run the project, execute the following command:

```bash
python main.py
```

## Configuration
-------------

The project uses a configuration file (`config.json`) to store the API keys, wallet information, and other settings. Modify the file to suit your needs.

```json
{
    "bybit": {
        "api_key": "your_bybit_api_key",
        "api_secret": "your_bybit_api_secret"
    },
    "ada_wallet": {
        "mnemonic": "your_ada_wallet_mnemonic",
        "passphrase": "your_ada_wallet_passphrase"
    },
    "algorithm": {
        "constant_product": 0.05
    }
}
```

## Algorithms
-------------

The project uses a constant product algorithm to adjust the prices based on the current market conditions.

```python
def constant_product(price, quantity, constant):
    return price * quantity * (1 + constant)
```

## Bybit Integration
-------------------

The project uses the `ccxt` library to integrate with the Bybit API.

```python
import ccxt

bybit = ccxt.bybit({
    'apiKey': config['bybit']['api_key'],
    'apiSecret': config['bybit']['api_secret']
})
```

## Native ADA Wallet Integration
--------------------------------

The project uses the `cardanoserializationlib` library to integrate with the native ADA wallet.

```python
import cardanoserializationlib as csl

wallet = csl deserializationMnemonic(
    mnemonic=config['ada_wallet']['mnemonic'],
    passphrase=config['ada_wallet']['passphrase']
)
```

## License
-------

This project is licensed under the MIT License.
