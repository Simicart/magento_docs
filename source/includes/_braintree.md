# Braintree Payment

## Braintree Properties
merchant_id | string | Merchant ID
public_key | string | Public Key
private_key | string | Private Key
token | string | Token
type | string | Payment Type
payment_list | array | Payment List
apple_merchant | string | Apple Merchant
google_merchant | string | Goole Merchant

## Save Payment via PayPal Mobile

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/braintreeapis" \
  -H "Authorization: Bearer <token>" \
  -d "{
"order_id":"100000015",
"amount":"100000",
"nonce":"100000"
}
"
```

> The above command returns JSON structured like this:

```json
{
    "braintreeapi": {
        "message": "Thank you for your purchase!"
    }
}
```
This API is to save payment via Braintree

### HTTP Request


