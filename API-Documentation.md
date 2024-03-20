# 3040CryptoAPI

## Description

* 3040Crypto provides a simple REST API for querying for wallet information, allows you to buy crypto with USD and check the price of a coin.

## Endpoints
* Method: ``GET`` 
* Endpoint: ``/wallet`` - Returns information about the wallet.
    * Parameters: 
      * walletID (String) - A unique UUID4 that is different for every wallet.

* Method: ``GET``
* Endpoint: ``/coinPrice`` - Returns the price of a coin.
    * Parameters:
      * coinID (String) - A unique UUID4 that indentifies the coin.

* Method: ``POST``
* Endpoint: ``/addCrypto`` - Adds more crypto to your wallet by buying with USD
    * Parameters:
      * amountToPurchase (Int) - The amount of crypto we want to want to buy with USD converted.
      * coinID (String) - A unique UUID4 that identifies the coin.
      * walletID (String) - A unique UUID4 that indentifies the wallet to add the crypto to.


## Resources

* TODO

## Sample Request and Response
### Request

```
https://3040Crypto.com/api/get/coinPrice?coinID=<COIN_ID>
```

### Response
* An JSON object is returned. 

```
{
    "coinId":"2131002-V23",
    "coinName": "BitCoin",
    "coinPrice": "$70,000 USD"
} 
```

### Response Values Descriptions

* ```coinID``` - (String) - A Unique UUID4 that indentifies the coin
* ``coinName`` - (String) - The name of the Coin
* ``coinPrice`` - (String) - The Price of the coin in USD.