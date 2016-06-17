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


## View Default Store View

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
               "sort_order":4,
               "value":12
            }
         ]
      }
}
```

Base on Store View Configuration:


Subtotal: tax_cart_display_subtotal

- If 1: Show subtotal_excl_tax with Label "Subtotal".

- If 2: Show subtotal_incl_tax with Label "Subtotal".

- If 3: Show both subtotal_excl_tax and subtotal_incl_tax with Labels "SUBTOTAL (EXCL. TAX)" and "SUBTOTAL (INCL. TAX)".

Shipping and Handling: tax_cart_display_shipping

- If 1: Show shipping_hand_excl_tax with Label "Shipping".

- If 2: Show shipping_hand_incl_tax with Label "Shipping".

- If 3: Show both shipping_hand_excl_tax and shipping_hand_incl_tax with Labels "SHIPPING EXCL. TAX" and "SHIPPING INCL. TAX".


Discount: Label: "Discount"

Tax: If there's tax value included, show it with label "TAX"

Grand Total: tax_cart_display_grandtotal

- If 1: Display both grand_total_excl_tax and grand_total_incl_tax with Labels "GRAND TOTAL EXCL. TAX" and "GRAND TOTAL INCL. TAX"

- If 2: Display  grand_total_incl_tax with Label "Grand Total"

Custom Rows: Sort Order calculated by counting from Top (with Top count as 1) and under the row with sort order value, for example:

Show  Subtotal(1), Shipping Excl. Tax (2), Shipping Incl. Tax (3), Discount (4), GrandTotal (5).
if Sort Order = 4, then it's under Discount. Then add The new row to that array and go to next Custom Row until there's no Custom Row left.