# Reward Points (Loyalty)

## Rewardpoints Account Properties

Attributes| Type| Description
--------- | ------- | -----------
reward_id | id | Rewardpoint Account Id
loyalty_point | float | Point Balance
loyalty_balance | string | Point Balance String Display
loyalty_redeem | string | Redeem (Loyalty Point Equal To)
loyalty_hold | float | Holding Balance
loyalty_image | string | Loyalty Image URL
is_notification | boolean | Is Notification
expire_notification | boolean | Expire Notification
earning_label | string | Earning Label
earning_policy | string | Earning Policy
spending_label | string | Spending Label
spending_policy | string | Spending Policy
spending_point | string | Spending Point (Each point equal when Earning)
spending_discount | string | Spending Discount (Each point equal when Spending)
start_discount | int | Start Discount
spending_min | int | Minimum Spending
policies | array | Policies

## View Customer Rewardpoint Information

```shell
curl "https://abc.com/simiconnector/rest/v2/simirewardpoints/home" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "simirewardpoint":{  
      "reward_id":"1",
      "customer_id":"137",
      "point_balance":"789",
      "holding_balance":"0",
      "spent_balance":"211",
      "is_notification":0,
      "expire_notification":0,
      "loyalty_point":789,
      "loyalty_balance":"789 Codypoints",
      "loyalty_redeem":"$78.90",
      "loyalty_image":"http:\/\/localhost.com\/magento19\/skin\/frontend\/base\/default\/images\/simirewardpoints\/point.png",
      "earning_label":"How you can earn points",
      "earning_policy":"Each $2.00 spent for your order will earn 1 Codypoint.",
      "spending_label":"How you can spend points",
      "spending_policy":"Each 1 Codypoint can be redeemed for $0.10.",
      "spending_point":1,
      "spending_discount":"$0.10",
      "start_discount":"$0.10",
      "spending_min":1,
      "policies":[  
         "A transaction will be withheld for 11 days since creation."
      ]
   }
}
```

This endpoint retrieves Customer Rewardpoint Information




## View Rewardpoint History

```shell
curl "https://abc.com/simiconnector/rest/v2/simirewardpointstransactions" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2",
      "1"
   ],
   "simirewardpointstransactions":[  
      {  
         "transaction_id":"2",
         "reward_id":"1",
         "customer_id":"137",
         "customer_email":"test@simicart.com",
         "title":"Spend points to purchase order #145000013",
         "action":"spending_order",
         "action_type":"2",
         "store_id":"1",
         "point_amount":-211,
         "point_used":"0",
         "real_point":"0",
         "status":"completed",
         "created_time":"2016-07-05 01:44:52",
         "updated_time":"2016-07-05 01:44:52",
         "expiration_date":"",
         "expire_email":"0",
         "order_id":"202",
         "order_increment_id":"145000013",
         "order_base_amount":"735.4800",
         "order_amount":"735.4800",
         "base_discount":"21.1000",
         "discount":"21.1000",
         "extra_content":null,
         "point_label":"-211 Codypoints"
      },
      {  
         "transaction_id":"1",
         "reward_id":"1",
         "customer_id":"137",
         "customer_email":"test@simicart.com",
         "title":"title",
         "action":"admin",
         "action_type":"0",
         "store_id":"0",
         "point_amount":1000,
         "point_used":"211",
         "real_point":"1000",
         "status":"completed",
         "created_time":"2016-07-05 01:16:27",
         "updated_time":"2016-07-05 01:16:27",
         "expiration_date":"2016-10-13 01:16:27",
         "expire_email":"0",
         "order_id":null,
         "order_increment_id":null,
         "order_base_amount":null,
         "order_amount":null,
         "base_discount":null,
         "discount":null,
         "extra_content":"admin",
         "point_label":"1000 Codypoints"
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves Reward point History

## Product Detail Reward Label

```shell
curl "https://abc.com/simiconnector/rest/v2/products/890" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"890",      
      "wishlist_item_id":null,
      "loyalty_image":"http:\/\/localhost.com\/magento19\/skin\/frontend\/base\/default\/images\/simirewardpoints\/point.png",
      "loyalty_label":"You could receive some Codypoints for purchasing this product"
   }
}
```

On product Detail, there will be Label and Point image if available


## Quoteitems (Cart) Reward Label

```shell
curl "https://abc.com/simiconnector/rest/v2/quoteitems" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2602"
   ],
   "quoteitems":[  
      {  
         "item_id":"2602",         
         "option":[  

         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/ace000a_1.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":295,
      "subtotal_incl_tax":295,
      "tax":0,
      "discount":3.25,
      "grand_total_excl_tax":291.75,
      "grand_total_incl_tax":291.75
   },
   "page_size":15,
   "from":0,
   "loyalty":{  
      "loyalty_image":"http:\/\/localhost.com\/magento19\/skin\/frontend\/base\/default\/images\/simirewardpoints\/point.png",
      "loyalty_label":"Checkout now and earn 146 Codypoints in rewards"
   }
}
```

On Cart (Quoteitems), there will be Loyalty image and Label if available


## Order Detail (One Page) Reward Information

```shell
curl "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{           
         "latlng":""
      },
      "shipping_address":{           
         "latlng":""
      },
      "shipping":[           
         {  
            "s_method_id":"17051",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         
      ],
      "total":{  
         "subtotal_excl_tax":295,
         "subtotal_incl_tax":295,
         "tax":0,
         "discount":3.25,
         "grand_total_excl_tax":266.35,
         "grand_total_incl_tax":266.35,
         "custom_rows":[  
            {  
               "title":"You will spend",
               "sort_order":5,
               "value":254,
               "value_string":"254 Codypoints"
            },
            {  
               "title":"You will earn",
               "sort_order":6,
               "value":133,
               "value_string":"133 Codypoints"
            },
            {  
               "title":"Use point",
               "sort_order":7,
               "value":25.4
            }
         ]
      }
   },
   "loyalty":{  
      "loyalty_rules":[  
         {  
            "id":"rate",
            "minPoints":0,
            "pointStep":1,
            "maxPoints":789,
            "pointStepLabel":"1 Codypoint",
            "pointStepDiscount":"$0.10",
            "optionType":"slider"
         }
      ]
   }
}
```

On Order Detail, there will be Loyalty rules for Spending if available


## Send Point on Order Screen

```shell
curl PUT "https://abc.com/simiconnector/rest/v2/simirewardpoints/spend" \
  -H "Authorization: Bearer <token>"
  -d "{  
"usepoint":"8",
"ruleid":"rate"
}"
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "billing_address": {            
            "latlng": ""
        },
        "shipping_address": {            
            "latlng": ""
        },
        "shipping": [            
            {
                "s_method_id": "17061",
                "s_method_code": "flatrate_flatrate",
                "s_method_title": "Flat Rate",
                "s_method_fee": 10,
                "s_method_name": "Fixed",
                "s_method_selected": false
            }
        ],
        "payment": [
            {
                "cc_types": [
                    {
                        "cc_code": "AE",
                        "cc_name": "American Express"
                    },
                    {
                        "cc_code": "VI",
                        "cc_name": "Visa"
                    },
                    {
                        "cc_code": "MC",
                        "cc_name": "MasterCard"
                    },
                    {
                        "cc_code": "DI",
                        "cc_name": "Discover"
                    }
                ],
                "payment_method": "CCSAVE",
                "title": "Credit Card (saved)",
                "useccv": "0",
                "show_type": 1,
                "p_method_selected": false
            }
        ],
        "total": {
            "subtotal_excl_tax": 295,
            "subtotal_incl_tax": 295,
            "tax": 0,
            "discount": 3.25,
            "grand_total_excl_tax": 290.95,
            "grand_total_incl_tax": 290.95,
            "custom_rows": [
                {
                    "title": "You will spend",
                    "sort_order": 5,
                    "value": 8,
                    "value_string": "8 Codypoints"
                },
                {
                    "title": "You will earn",
                    "sort_order": 6,
                    "value": 145,
                    "value_string": "145 Codypoints"
                },
                {
                    "title": "Use point",
                    "sort_order": 7,
                    "value": 0.8
                }
            ]
        }
    },
    "loyalty": {
        "loyalty_rules": [
            {
                "id": "rate",
                "minPoints": 0,
                "pointStep": 1,
                "maxPoints": 789,
                "pointStepLabel": "1 Codypoint",
                "pointStepDiscount": "$0.10",
                "optionType": "slider"
            }
        ]
    }
}
```

This API is to Apply Point balance to be Spend, it will return Order Onepage Information to show on Screen

## Save Rewardpoint Settings

```shell
curl PUT "https://abc.com/simiconnector/rest/v2/simirewardpoints/savesetting" \
  -H "Authorization: Bearer <token>"
  -d "{  
"is_notification":"0",
"expire_notification":"1"
}"
```

> The above command returns JSON structured like this:

```json
{
    "simirewardpoint": {
        "reward_id": "1",
        "customer_id": "137",
        "point_balance": "789",
        "holding_balance": "0",
        "spent_balance": "211",
        "is_notification": 0,
        "expire_notification": 1,
        "loyalty_point": 789,
        "loyalty_balance": "789 Codypoints",
        "loyalty_redeem": "$78.90",
        "loyalty_image": "http://localhost.com/magento19/skin/frontend/base/default/images/simirewardpoints/point.png",
        "earning_label": "How you can earn points",
        "earning_policy": "Each $2.00 spent for your order will earn 1 Codypoint.",
        "spending_label": "How you can spend points",
        "spending_policy": "Each 1 Codypoint can be redeemed for $0.10.",
        "spending_point": 1,
        "spending_discount": "$0.10",
        "start_discount": "$0.10",
        "spending_min": 1,
        "policies": [
            "A transaction will be withheld for 11 days since creation."
        ]
    }
}
```

This API is to Save Rewardpoint Settings


