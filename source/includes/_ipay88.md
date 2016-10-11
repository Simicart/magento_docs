# Ipay88 Payment

## Ipay88 Payment Properties

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
                "s_method_id": "375",
                "s_method_code": "freeshipping_freeshipping",
                "s_method_title": "Free Shipping",
                "s_method_fee": 0,
                "s_method_name": "Free",
                "s_method_selected": true
            },
            {
                "s_method_id": "374",
                "s_method_code": "flatrate_flatrate",
                "s_method_title": "Flat Rate",
                "s_method_fee": 5,
                "s_method_name": "Fixed",
                "s_method_selected": false
            }
        ],
        "payment": [
            {
                "is_sandbox": "1",
                "payment_method": "SIMIIPAY88",
                "title": "iPay88 Checkout",
                "show_type": 2,
                "p_method_selected": false,
                "merchant_key": "54xlV4aIf4",
                "merchant_code": "M05268"
            }
        ],
        "total": {
            "shipping_hand_incl_tax": 0,
            "shipping_hand_excl_tax": 0,
            "subtotal_excl_tax": 15,
            "subtotal_incl_tax": 15,
            "grand_total_excl_tax": 15,
            "grand_total_incl_tax": 15
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

## After Order Placed

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000043",
        "payment_method": "simiipay88",
        "amount": 399.99,
        "currency_code": "INR",
        "name": "abc Company",
        "contact": "66784318",
        "email": "test@simicart.com",
        "product_des": "sw810i,",
        "country_id": "IN"
    }
}
```

Use those information for iPay88 checkout.

## Update Payment

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/simiipay88apis/update_payment?order_id=100000043&transaction_id=1102&status=processing&auth_code=xyz&ref_no=123" \
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
Use this API to update payment.

