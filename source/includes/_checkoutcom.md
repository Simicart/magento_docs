# Checkout.com Payment

## Checkout.com Payment Properties


Attributes| Type| Description
--------- | ------- | -----------
public_key | string | Public Key
private_key | string | Private (Secret) Key
is_sandbox | string | 1 - sanbox, 0 - live

## Onepage Payment Info

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "billing_address": {
        },
        "shipping_address": {
        },
        "shipping": [
            {
                "s_method_id": "345",
                "s_method_code": "freeshipping_freeshipping",
                "s_method_title": "Free Shipping",
                "s_method_fee": 0,
                "s_method_name": "Free",
                "s_method_selected": true
            },
            {
                "s_method_id": "344",
                "s_method_code": "flatrate_flatrate",
                "s_method_title": "Flat Rate",
                "s_method_fee": 5,
                "s_method_name": "Fixed",
                "s_method_selected": false
            }
        ],
        "payment": [
            {
                "payment_method": "SIMIAVENUE",
                "title": "CC Avenue",
                "show_type": 3,
                "p_method_selected": false
            },
            {
                "payment_method": "SIMICHECKOUTCOM",
                "title": "Checkout.com",
                "show_type": 3,
                "p_method_selected": false,
                "public_key": "pk_test_SPECIMEN-111",
                "private_key": "sk_093F4C8D-E608-4B8D-9B39-8C2491345864",
                "is_sandbox": "1"
            },
            {
                "payment_method": "SIMIPAYU",
                "title": "PayU",
                "show_type": 3,
                "p_method_selected": false
            }
        ],
        "total": {
            "shipping_hand_incl_tax": 0,
            "shipping_hand_excl_tax": 0,
            "subtotal_excl_tax": 399.99,
            "subtotal_incl_tax": 399.99,
            "grand_total_excl_tax": 399.99,
            "grand_total_incl_tax": 399.99
        },
        "loyalty": {
            "loyalty_spend": 0,
            "loyalty_discount": 0,
            "loyalty_earn": 0,
            "loyalty_spending": "0 Point",
            "loyalty_earning": "0 Point",
            "loyalty_rules": []
        }
    }
}
```
Use is_sandbox for the following action

## After Payment completed

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/checkoutcomapis/update_payment?invoice_number=100000041&transaction_id=1102" \
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
Use this API to update payment with invoice number and checkout.com transaction_id.

