# PayU International

## PayU Properties


## After Order Placed

```shell
curl POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000012",
        "payment_method": "simipayu",
        "url_action": "https://stg.gateway.payulatam.com/ppp-web-gateway?merchantId=500238&referenceCode=100000012&description=The Only Children: Paisley T-Shirt&amount=115.00&tax=0.00&taxReturnBase=0&signature=20e5c2e1d8b95df72869521dcfbcee69&accountId=509171&currency=USD&buyerEmail=test@simicart.com&test=1&confirmationUrl=http://localhost.com/magento18/index.php/simipayu/api/notify/&responseUrl=http://localhost.com/magento18/index.php/simipayu/api/success/&"
    }
}
```

Open the url on url_action

Demo Merchant Information:

Merchant Id: 500238

Sercure key: 6u39nqhq8ftd0hlvnjfs66eh8c

Account Id: 509171

Gateway URL: https://sandbox.gateway.payulatam.com/ppp-web-gateway

### HTTP Request


