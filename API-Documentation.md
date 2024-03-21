# 3040CryptoAPI

## Description

* 3040Crypto provides a simple REST API for querying for wallet information, allows you to buy crypto with USD and check the price of a coin.

## Endpoints

### 1. ``/wallet``
* Method: ``GET`` 
* Endpoint: ``/wallet`` - Returns information about the wallet.
    * Parameters: 
      * walletID (String) - A unique UUID4 that is different for every wallet.

### 2. ``/coinPrice``
* Method: ``GET``
* Endpoint: ``/coinPrice`` - Returns the price of a coin.
    * Parameters:
      * coinID (String) - A unique UUID4 that indentifies the coin.

### 3. ``/addCrypto``
* Method: ``POST``
* Endpoint: ``/addCrypto`` - Adds more crypto to your wallet by buying with USD
    * Parameters:
      * amountToPurchase (Int) - The amount of crypto we want to want to buy with USD converted.
      * coinID (String) - A unique UUID4 that identifies the coin.
      * walletID (String) - A unique UUID4 that indentifies the wallet to add the crypto to.


## Resources

### 1. Wallet Resource
```json
{
  "walletID": "2a4f6e89-326b-4c1d-a9d3-22f6e8b76ab1",
  "balance": "0.05 BTC",
  "transactions": [
    {
      "transactionID": "4567890",
      "amount": "0.01 BTC",
      "type": "deposit",
      "timestamp": "2024-03-20T12:00:00Z"
    },
    {
      "transactionID": "5678901",
      "amount": "0.02 BTC",
      "type": "withdrawal",
      "timestamp": "2024-03-20T12:30:00Z"
    }
  ]
}
```

### 2. Cryptocurrency Resource
```json
{
  "coinID": "2131002-V23",
  "coinName": "BitCoin",
  "coinSymbol": "BTC",
  "coinPrice": "$70,000 USD"
}
```

## Sample Request and Response

### Request coin price:

#### Request

```
https://3040Crypto.com/api/get/coinPrice?coinID=2131002-V23
```

#### Response
* An JSON object is returned. 

```json
{
    "coinId":"2131002-V23",
    "coinName": "BitCoin",
    "coinSymbol": "BTC",
    "coinPrice": "$70,000 USD"
} 
```

#### Response Values Descriptions

* ```coinID``` - (String) - A Unique UUID4 that indentifies the coin
* ``coinName`` - (String) - The name of the Coin
* ``coinSymbol`` - (String) - The symbol of the Coin
* ``coinPrice`` - (String) - The Price of the coin in USD.
