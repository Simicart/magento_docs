# Klarna Checkout Payment

## Klarna Checkout Properties

## Save Payment via PayPal Mobile

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/simiklarnaapis/get_params" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "simiklarnaapi": [
        {
            "reference": "27",
            "name": "CLOUDY NIGHT",
            "quantity": 1,
            "unit_price": 7576,
            "tax_rate": 825
        },
        {
            "reference": "26",
            "name": "ARTIFICE STRASS",
            "quantity": 1,
            "unit_price": 9732,
            "tax_rate": 825
        }
    ]
}
```
Use this json for Data on the webview content. Under the 'data' param
(https://abc.com/simiklarna/api/checkout)

eg.

demo.magestore.com/simicart/simipos1/index.php/simiklarna/api/checkout/data/{"simiklarnaapi":[{"reference":"27","name":"CLOUDY NIGHT","quantity":1,"unit_price":7576,"tax_rate":825},{"reference":"26","name":"ARTIFICE STRASS","quantity":1,"unit_price":9732,"tax_rate":825}]}

When the webview contain checkout/cart, show error and return to Cart Screen.

If resonse contain  "simiconnector/rest/v2/simiklarnaapis/success/", follow the following API

### HTTP Request

## Klarna Checkout Completed

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/simiklarnaapis/success/" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "simiklarnaapi": {
        "klarna_order": "FZLQ2IWHUYJVN7IYW4OQ8IXAN5R"
    }
}
```
Get the klarna_order value and paste it to the 'PUSH' action.

### HTTP Request

## Klarna Order Pushing

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/simiklarnaapis/push?klarna_order=FZLQ2IWHUYJVN7IYW4OQ8IXAN5R" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "simiklarnaapi": {
        "message": "Order Placed"
    }
}
```

### HTTP Request
