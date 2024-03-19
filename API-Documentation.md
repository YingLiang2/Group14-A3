# 3040CryptoAPI

## API Description

* Basic API that lets you buy crypto and see your wallet contents.

## Endpoints
GET/wallet (all our assets and money I guess)

    * private key (identifier)

POST/addCrypto (add money to our wallet)

    * $amount in USD
    * coin name (the coin we want to buy / add to?)
    * wallet ID (which wallet we are adding to)

GET/coinPrice (get price of a single coin)

    * coin name 
    * coin id

## Resources

## Sample Request and Response
### Request

GET/coinPrice ? coinName="BitCoin";coinID="123123123qwe"

### Response

```
{
    "coinId":"2131002-V23",
    "coinName": "BitCoin",
    "coinPrice": "$70,000 USD"
} 
```
