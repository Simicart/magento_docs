# PayU India (PayUbiz)

## PayU India Properties


## After Order Placed

```shell
curl POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000011",
        "payment_method": "simipayuindia",
        "url_action": "http://localhost.com/magento18/index.php/simipayuindia/api/checkout/invoice_number/100000011/"
    }
}
```

Open the url on url_action

Success url contain: simipayuindia/api/canceled

Failure url contain: simipayuindia/api/failure

Canceled url contain: simipayuindia/api/canceled

Demo Merchant Information:

Merchant Id: gtKFFx

Salt: eCwWELxi

### HTTP Request


