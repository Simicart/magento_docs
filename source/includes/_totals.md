# Cart/Order Total

## Cart/Order Total Properties

Attributes| Type| Description
--------- | ------- | -----------
subtotal_excl_tax | string | Subtotal excluded Tax
subtotal_incl_tax | string | Subtotal included Tax
shipping_hand_incl_tax | float | Shipping and Handling included Tax
shipping_hand_excl_tax | float | Shipping and Handling excluded Tax
tax | float | Tax value
coupon_code | string | Coupon Code Applying
discount | float | Discount Value
grand_total_excl_tax | float | Grand Total Excluded Tax
grand_total_incl_tax | float | Grand Total Included Tax
custom_rows | array | Custom Row (added manually)
custom_rows.title | string | Custom Row Title
custom_rows.value | float | Custom Row value
custom_rows.sort_order | int | Sort Order on Total Row


## Display Total Row

```shell
curl "https://abc.com/simiconnector/rest/v2/quoteitems" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
   "total":{  
         "subtotal_excl_tax":340,
         "subtotal_incl_tax":340,
         "shipping_hand_incl_tax":25.27,
         "shipping_hand_excl_tax":25.27,
         "tax":0,
         "discount":5,
         "grand_total_excl_tax":372.27,
         "grand_total_incl_tax":372.27,
         "coupon_code":"MYCOUPON",
         "custom_rows":[  
            {  
               "title":"Nachnahmegeb\u00fchr",
               "sort_order":"31",
               "value":12
            },
         {
            "title": "You will earn",
            "sort_order": 6,
            "value": 145,
            "value_string": "145 Codypoints"
            }
         ]
      }
}
```

Base on Store View Configuration:


Subtotal: tax_cart_display_subtotal (tax_sales_display_subtotal on order history screen)

- If 1: Show subtotal_excl_tax with Label "Subtotal".

- If 2: Show subtotal_incl_tax with Label "Subtotal".

- If 3: Show both subtotal_excl_tax and subtotal_incl_tax with Labels "Subtotal (Excl. Tax)" and "Subtotal (Incl. Tax)".

Shipping and Handling: tax_cart_display_shipping (tax_sales_display_shipping on order history screen)

- If 1: Show shipping_hand_excl_tax with Label "Shipping".

- If 2: Show shipping_hand_incl_tax with Label "Shipping".

- If 3: Show both shipping_hand_excl_tax and shipping_hand_incl_tax with Labels "Shipping Excl. Tax" and "Shipping Incl. Tax".


Discount: Label: "Discount"

Tax: If there's tax value included, show it with label "Tax"

Grand Total: tax_cart_display_grandtotal (tax_sales_display_grandtotal on order history screen)

- If 1: Display both grand_total_excl_tax and grand_total_incl_tax with Labels "Grand Total Excl. Tax" and "Grand Total Incl. Tax"

- If 0: Display  grand_total_incl_tax with Label "Grand Total"

All these above Rows are sorted by storeview.sales setting array (from Store View Configuration request)

eg.

{

   "storeview":{  

      "sales":{  

         "sales_reorder_allow":"1",

         "sales_totals_sort_subtotal":"10",

         "sales_totals_sort_discount":"20",

         "sales_totals_sort_shipping":"30",

         "sales_totals_sort_weee":"50",

         "sales_totals_sort_tax":"40",

         "sales_totals_sort_grand_total":"100"

      }

   }

}

Custom Rows: Sort Order counted the same with other Total Items, for Example it's 31, it'd be below Shipping row

If there's no "value_string" on custom row, show the "value" with Store currency format


## Tax Summary

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
   "total":{  
      "subtotal_excl_tax":295,
      "subtotal_incl_tax":321.55,
      "tax":26.26,
      "tax_summary":[  
         {  
            "title":"US-CA-*-Rate 1 (9%)",
            "amount":26.26
         }
      ],
      "discount":3.25,
      "grand_total_excl_tax":291.75,
      "grand_total_incl_tax":318.01,
      "custom_rows":[  
         {  
            "title":"You will earn",
            "sort_order":6,
            "value":146,
            "value_string":"146 Codypoints"
         }
      ]
   },
   "page_size":15,
   "from":0,
   "loyalty":{  
      "loyalty_image":"http:\/\/localhost.com\/magento19\/skin\/frontend\/base\/default\/images\/simirewardpoints\/point.png",
      "loyalty_label":"Checkout now and earn 146 Codypoints in rewards"
   }
}
```

If Store Configuration for tax on Cart (tax_cart_display_full_summary) or on Order (tax_sales_display_full_summary) is '1', and there's tax_summary on total information, then the Summary needs to be shown.

The 'amount' can be empty, in that case, the value row is blank.

