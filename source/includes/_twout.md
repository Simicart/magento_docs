# 2Checkout

## 2Checkout Properties


## Onepage Payment Info

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  },
      "shipping_address":{  },
      "shipping":[  
         {  
            "s_method_id":"73",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":5,
            "s_method_name":"Fixed",
            "s_method_selected":true
         }
      ],
      "payment":[  
         {  
            "email":null,
            "client_id":null,
            "is_sandbox":"1",
            "payment_method":"TWOUT",
            "title":"2Checkout",
            "bncode":"Magestore_SI_MagentoCE",
            "show_type":2,
            "p_method_selected":false,
            "url_action":"simiconnector/rest/v2/twoutapis/update_order",
            "url_back":"https://sandbox.2checkout.com/checkout/purchase"
         },
         {  },
         {  },
         {  },
         {  }
      ],
      "total":{  },
      "loyalty":{  }
   }
}
```
Use url_back for the following action

## After Order placed

```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000007",
        "payment_method": "twout",
        "params": "sid=901328799&purchase_step=payment-method&merchant_order_id=100000007&email=test@simicart.com&first_name=abc&last_name=Company&phone=123&country=AL&street_address=Tan Mai, Hoang Mai&street_address2=Tan Mai, Hoang Mai&city=Ha Noi&state=XX&zip=10000&ship_name=abc Company&ship_country=AL&ship_street_address=Tan Mai, Hoang Mai&ship_street_address2=Tan Mai, Hoang Mai&ship_city=Ha Noi&ship_state=&ship_zip=10000&sh_cost=5&sh_weight=2&ship_method=Flat Rate - Fixed&2co_tax=0&2co_cart_type=magento&currency_code=USD&mode=2CO&li_0_type=product&li_0_product_id=750&li_0_quantity=1&li_0_name= Olympus Stylus 750 7.1MP Digital Camera&li_0_description=&li_0_price=161.94&li_1_type=shipping&li_1_name=Flat Rate - Fixed&li_1_price=5"
    }
}
```
Use the params with the url_back.

Eg. https://sandbox.2checkout.com/checkout/purchase?sid=901328799&purchase_step=payment-method&merchant_order_id=100000007

when URL of webview contain jsessionid, use that for transaction_id for the next API (update Order transaction)

## Update Order and Transation

```shell
  curl -X PUT "https://abc.com/simiconnector/rest/v2/twoutapis/update_order" \
  -H "Authorization: Bearer <token>" \
  -d '{  
"invoice_number":"100000006",
"transaction_id":"100000006",
"payment_status":"1"
} '
  "
```

> The above command returns JSON structured like this:

```json
{
    "twoutapi": {
        "message": "Thank you for your purchase!"
    }
}

```
payment_status == 1 is completed

when need to cancel order, use cancel Order API

