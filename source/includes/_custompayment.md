# Customize Payment

## Customize payment Properties

Attributes| Type| Description
--------- | ------- | -----------
title_url_action | string | Customized Payment Key to get URL
paymentmethod | string | Customized Payment method Code
url_success | string | Url when the payment failed and open popup with message_success
url_fail | string | Url when the payment failed and open popup with message_fail
url_cancel | string | Url when the payment failed and open popup with message_cancel
url_error | string | Url when the payment failed and open popup with message_error

## Get Customize Payments

```shell
curl GET "https://abc.com/simiconnector/rest/v2/customizepayments" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "all_ids": [
        "1"
    ],
    "customizepayments": [
        {
            "paymentmethod": "bankpayment",
            "title_url_action": "url_action",
            "url_redirect": "http://localhost.com/magento18/index.php/",
            "url_success": "checkout/onepage/success",
            "url_fail": "checkout/onepage/failure",
            "url_cancel": "checkout/onepage/cancel",
            "url_error": "checkout/onepage/failure ",
            "message_success": "Thank you for purchasing",
            "message_fail": "Sorry, payment failed",
            "message_cancel": "Your order has been canceled",
            "message_error": "Sorry, Your order has an error",
            "ischeckurl": "0",
            "url_check": "checkout/onepage/failure"
        }
    ],
    "total": 1,
    "page_size": 15,
    "from": 0
}
```

This endpoint retrieves a specific Store.

### HTTP Request

`GET /rest/stores/<id>`


## After Placed Order Information

```shell
curl POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000009",
        "payment_method": "bankpayment",
        "url_action": "http://localhost.com/magento18/index.php/simicustompaymentadmin/api/placement/OrderID/MTAwMDAwMDA5/LastRealOrderId/MTAwMDAwMDA5/"
    }
}
```

Use the URL from key (url_action) if payment method is the one on list Customized Payment.
