# Checkout.com Payment

## Checkout.com Payment Properties


Attributes| Type| Description
--------- | ------- | -----------
public_key | string | Public Key
private_key | string | Private (Secret) Key
is_sandbox | string | 1 - sanbox, 0 - live

## Redirect url sent after placed URL

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000047",
        "payment_method": "simicheckoutcom",
        "redirect_url": "http://localhost.com/magento18/index.php/simicheckoutcom/index/startCheckoutcom/?order_id=100000047",
        "success_url": "https://www.simicart.com/pricing.html"
    }
}
```

Use the Use the redirect_url to open Webview.

Checkout with sample card:

4242 4242 4242 4242

06/18

100

When the url on webview contain 'success_url', complete order with the following API.

## After Payment completed

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/checkoutcomapis/update_payment?invoice_number=100000047" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "checkoutcomapi": {
        "status": "SUCCESS",
        "message": [
            "Thank you for your purchase!"
        ]
    }
}
```
Use this API to update payment with invoice number.

