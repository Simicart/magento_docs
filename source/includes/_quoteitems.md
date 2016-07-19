# Quote Items (Cart)

## Quote Properties

Attributes| Type| Description
--------- | ------- | -----------
quote_id | id | Quote Id
cart_total | int | Total Cart Items (show on Cart icon Badge)

## Items Properties

Attributes| Type| Description
--------- | ------- | -----------
item_id | id | Item Id
product_id | id | Product Id
sku | string | Product SKU
name | string | Item Name
price | float | Item Price
price_incl_tax | float | Item Price Included Tax
base_price | float | Item Price (Base Currency)
base_price_incl_tax | float | Item Price Included Tax (Base Currency)
row_total | float | Row Price
row_total_incl_tax | float | Row Price Included Tax
base_row_total | float | Row Price (Base Currency)
base_row_total_incl_tax | float | Row Price Included Tax(Base Currency)
qty | int | Item Qty
product_type | string | Product Type
option | array | Item Options
total | array | Cart Total
total.subtotal_excl_tax | float | Subtotal Excluded Tax
total.subtotal_incl_tax | float | Subtotal Included Tax
total.grand_total_excl_tax | float | Grand Total Excluded Tax
total.grand_total_incl_tax | float | Grand Total Included Tax
total.shipping_hand_excl_tax | float | Shipping/Handling Excluded Tax
total.shipping_hand_incl_tax | float | Shipping/Handling Included Tax
total.discount | float | Discount value
total.coupon_code | string | Coupon Value

## View Quote Items

```shell
curl GET "https://abc.com/simiconnector/rest/v2/quoteitems" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2477",
      "2479"
   ],
   "quoteitems":[  
      {  
         "item_id":"2477",
         "quote_id":"681",
         "created_at":"2016-05-31 07:07:08",
         "updated_at":"2016-06-02 07:46:18",
         "product_id":"421",
         "store_id":"1",
         "parent_item_id":null,
         "is_virtual":"0",
         "sku":"wbk013",
         "name":"Elizabeth Knit Top",
         "description":null,
         "applied_rule_ids":"6,29",
         "additional_data":null,
         "free_shipping":"0",
         "is_qty_decimal":"0",
         "no_discount":"0",
         "weight":"1.0000",
         "qty":1,
         "price":"210.0000",
         "base_price":"210.0000",
         "custom_price":null,
         "discount_percent":"0.0000",
         "discount_amount":"2.0800",
         "base_discount_amount":"2.0800",
         "tax_percent":"0.0000",
         "tax_amount":"0.0000",
         "base_tax_amount":"0.0000",
         "row_total":"210.0000",
         "base_row_total":"210.0000",
         "row_total_with_discount":"0.0000",
         "row_weight":"0.0000",
         "product_type":"configurable",
         "base_tax_before_discount":null,
         "tax_before_discount":null,
         "original_custom_price":null,
         "redirect_url":null,
         "base_cost":null,
         "price_incl_tax":"210.0000",
         "base_price_incl_tax":"210.0000",
         "row_total_incl_tax":"210.0000",
         "base_row_total_incl_tax":"210.0000",
         "hidden_tax_amount":"0.0000",
         "base_hidden_tax_amount":"0.0000",
         "gift_message_id":null,
         "weee_tax_disposition":"0.0000",
         "weee_tax_row_disposition":"0.0000",
         "base_weee_tax_disposition":"0.0000",
         "base_weee_tax_row_disposition":"0.0000",
         "weee_tax_applied":"a:0:{}",
         "weee_tax_applied_amount":"0.0000",
         "weee_tax_applied_row_amount":"0.0000",
         "base_weee_tax_applied_amount":"0.0000",
         "base_weee_tax_applied_row_amnt":null,
         "event_id":null,
         "giftregistry_item_id":null,
         "gw_id":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "qty_options":{  
            "295":{  

            }
         },
         "product":{  
            "entity_id":"421",
            "entity_type_id":"4",
            "attribute_set_id":"13",
            "type_id":"configurable",
            "sku":"wbk012c",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2013-03-05 13:25:11",
            "updated_at":"2013-04-15 14:59:03",
            "name":"Elizabeth Knit Top",
            "small_image":"\/w\/b\/wbk012t.jpg",
            "thumbnail":"\/w\/b\/wbk012t.jpg",
            "url_key":"elizabeth-knit-top",
            "url_path":"elizabeth-knit-top-582.html",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"2",
            "price":"210.0000",
            "special_price":null,
            "msrp":null,
            "special_from_date":"2013-03-01 00:00:00",
            "special_to_date":null,
            "is_salable":"1",
            "stock_item":{  
               "item_id":"691",
               "product_id":"421",
               "stock_id":"1",
               "qty":"0.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"configurable",
               "stock_status":"1",
               "product_name":"Elizabeth Knit Top",
               "store_id":"1",
               "product_type_id":"configurable",
               "product_status_changed":true,
               "product_changed_websites":null
            },
            "do_not_use_category_id":true,
            "request_path":"elizabeth-knit-top-582.html",
            "tier_price":[  

            ],
            "is_in_stock":"1",
            "store_id":"1",
            "customer_group_id":"1",
            "final_price":null,
            "_cache_instance_products":[  
               {  

               },
               {  

               },
               {  

               },
               {  

               },
               {  

               }
            ],
            "_cache_instance_configurable_attributes":{  

            },
            "_cache_instance_used_attributes":{  
               "92":{  

               },
               "180":{  

               }
            },
            "_cache_instance_used_product_attributes":{  
               "92":{  

               },
               "180":{  

               }
            },
            "_cache_instance_used_product_attribute_ids":[  
               "92",
               "180"
            ]
         },
         "tax_class_id":"2",
         "is_recurring":null,
         "has_error":false,
         "converted_price":210,
         "calculation_price":210,
         "option":[  
            {  
               "option_title":"Color",
               "option_value":"White",
               "option_price":0
            },
            {  
               "option_title":"Size",
               "option_value":"M",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/w\/b\/wbk012t.jpg"
      },
      {  
         "item_id":"2479",
         "quote_id":"681",
         "created_at":"2016-05-31 08:28:54",
         "updated_at":"2016-06-02 07:46:18",
         "product_id":"337",
         "store_id":"1",
         "parent_item_id":null,
         "is_virtual":"0",
         "sku":"ace000",
         "name":"Aviator Sunglasses",
         "description":null,
         "applied_rule_ids":"6,29",
         "additional_data":null,
         "free_shipping":"0",
         "is_qty_decimal":"0",
         "no_discount":"0",
         "weight":"1.0000",
         "qty":1,
         "price":"295.0000",
         "base_price":"295.0000",
         "custom_price":null,
         "discount_percent":"0.0000",
         "discount_amount":"2.9200",
         "base_discount_amount":"2.9200",
         "tax_percent":"0.0000",
         "tax_amount":"0.0000",
         "base_tax_amount":"0.0000",
         "row_total":"295.0000",
         "base_row_total":"295.0000",
         "row_total_with_discount":"0.0000",
         "row_weight":"0.0000",
         "product_type":"simple",
         "base_tax_before_discount":null,
         "tax_before_discount":null,
         "original_custom_price":null,
         "redirect_url":null,
         "base_cost":null,
         "price_incl_tax":"295.0000",
         "base_price_incl_tax":"295.0000",
         "row_total_incl_tax":"295.0000",
         "base_row_total_incl_tax":"295.0000",
         "hidden_tax_amount":"0.0000",
         "base_hidden_tax_amount":"0.0000",
         "gift_message_id":null,
         "weee_tax_disposition":"0.0000",
         "weee_tax_row_disposition":"0.0000",
         "base_weee_tax_disposition":"0.0000",
         "base_weee_tax_row_disposition":"0.0000",
         "weee_tax_applied":"a:0:{}",
         "weee_tax_applied_amount":"0.0000",
         "weee_tax_applied_row_amount":"0.0000",
         "base_weee_tax_applied_amount":"0.0000",
         "base_weee_tax_applied_row_amnt":null,
         "event_id":null,
         "giftregistry_item_id":null,
         "gw_id":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "qty_options":[  

         ],
         "product":{  
            "entity_id":"337",
            "entity_type_id":"4",
            "attribute_set_id":"11",
            "type_id":"simple",
            "sku":"ace000",
            "has_options":"0",
            "required_options":"0",
            "created_at":"2013-03-05 12:48:17",
            "updated_at":"2013-03-20 23:45:10",
            "name":"Aviator Sunglasses",
            "small_image":"\/a\/c\/ace000a_1.jpg",
            "thumbnail":"\/a\/c\/ace000a_1.jpg",
            "url_key":"aviator-sunglasses",
            "url_path":"aviator-sunglasses.html",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"2",
            "is_recurring":"0",
            "weight":"1.0000",
            "price":"295.0000",
            "special_price":null,
            "msrp":null,
            "special_from_date":null,
            "special_to_date":null,
            "is_salable":"1",
            "stock_item":{  
               "item_id":"472",
               "product_id":"337",
               "stock_id":"1",
               "qty":"7.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"1",
               "stock_status_changed_automatically":"1",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Aviator Sunglasses",
               "store_id":"1",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null,
               "ordered_items":1
            },
            "do_not_use_category_id":true,
            "request_path":"aviator-sunglasses.html",
            "tier_price":[  

            ],
            "is_in_stock":"1",
            "store_id":"1",
            "customer_group_id":"1",
            "final_price":null
         },
         "tax_class_id":"2",
         "is_recurring":"0",
         "has_error":false,
         "converted_price":295,
         "calculation_price":295,
         "option":[  

         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/ace000a_1.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":505,
      "subtotal_incl_tax":505,
      "grand_total_excl_tax":500,
      "grand_total_incl_tax":500,
      "shipping_hand_incl_tax":"0.0000",
      "shipping_hand_excl_tax":"0.0000",
      "discount":5,
      "coupon_code":"MYCOUPON"
   },
   "page_size":15,
   "from":0,
   "cart_total":2,
   "quote_id": "729"
}
```
Base on Store View Tax Config to Show Row Price and Total Information:

If tax_cart_display_price is:

- 1: Excluding Tax  - Show Excluded tax value (row_total) with No title
 
- 2: Including Tax - Show Included Tax value (row_total_incl_tax) with No title

- 3: Including and Excluding Tax - Show both Including tax (with Title "Incl. Tax") and Excluding Tax (with title "Excl. Tax")



## Apply Coupon Code

```shell
curl PUT "https://abc.com/simiconnector/rest/v2/quoteitems" \
  -H "Authorization: Bearer <token>"
  -d "{
"coupon_code":"MYCOUPON"
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2557"
   ],
   "quoteitems":[  
      {  
         "item_id":"2557",
         "quote_id":"690",
         "created_at":"2016-06-09 04:54:09",
         "updated_at":"2016-06-09 06:20:37",
         "product_id":"888",
         "store_id":"1",
         "parent_item_id":null,
         "is_virtual":false,
         "sku":"testcustom-option1",
         "name":"Test Custom Option Simple Product",
         "description":null,
         "applied_rule_ids":"6",
         "additional_data":null,
         "free_shipping":false,
         "is_qty_decimal":"0",
         "no_discount":"0",
         "weight":"1.0000",
         "qty":100,
         "price":2,
         "base_price":2,
         "custom_price":null,
         "discount_percent":0,
         "discount_amount":5,
         "base_discount_amount":5,
         "tax_percent":0,
         "tax_amount":0,
         "base_tax_amount":0,
         "row_total":200,
         "base_row_total":200,
         "row_total_with_discount":"0.0000",
         "row_weight":100,
         "product_type":"simple",
         "base_tax_before_discount":null,
         "tax_before_discount":null,
         "original_custom_price":null,
         "redirect_url":null,
         "base_cost":null,
         "price_incl_tax":2,
         "base_price_incl_tax":2,
         "row_total_incl_tax":200,
         "base_row_total_incl_tax":200,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "gift_message_id":null,
         "weee_tax_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_applied":"a:0:{}",
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amnt":null,
         "event_id":null,
         "giftregistry_item_id":null,
         "gw_id":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "qty_options":[  

         ],
         "product":{  
            "entity_id":"888",
            "entity_type_id":"4",
            "attribute_set_id":"4",
            "type_id":"simple",
            "sku":"testcustom",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2016-06-07 07:49:15",
            "updated_at":"2016-06-07 07:51:17",
            "name":"Test Custom Option Simple Product",
            "small_image":"no_selection",
            "thumbnail":"no_selection",
            "url_key":"test-custom-option-simple-product",
            "url_path":"test-custom-option-simple-product.html",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"0",
            "is_recurring":"0",
            "price":"1.0000",
            "special_price":null,
            "weight":"1.0000",
            "msrp":null,
            "special_from_date":null,
            "special_to_date":null,
            "is_salable":"1",
            "stock_item":{  
               "item_id":"1867",
               "product_id":"888",
               "stock_id":"1",
               "qty":"88888.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Test Custom Option Simple Product",
               "store_id":"1",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null,
               "ordered_items":100
            },
            "do_not_use_category_id":true,
            "request_path":"test-custom-option-simple-product.html",
            "tier_price":[  

            ],
            "is_in_stock":"1",
            "store_id":"1",
            "customer_group_id":"1",
            "final_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "quote_item_qty":100,
            "quote_item_price":2,
            "quote_item_row_total":200,
            "category_ids":[  
               "2"
            ]
         },
         "tax_class_id":"0",
         "is_recurring":"0",
         "has_error":false,
         "is_nominal":false,
         "base_calculation_price":2,
         "calculation_price":2,
         "converted_price":2,
         "base_original_price":2,
         "taxable_amount":200,
         "base_taxable_amount":200,
         "is_price_incl_tax":false,
         "base_weee_tax_applied_row_amount":0,
         "original_price":2,
         "applied_rates":[  

         ],
         "original_discount_amount":5,
         "base_original_discount_amount":2,
         "discount_tax_compensation":0,
         "option":[  
            {  
               "option_title":"mydropdownoption",
               "option_value":"option1 title",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":200,
      "subtotal_incl_tax":200,
      "grand_total_excl_tax":195,
      "grand_total_incl_tax":195,
      "tax":0,
      "discount":5,
      "coupon_code":"MYCOUPON"
   },
   "page_size":15,
   "from":0,
   "cart_total":2,
   "quote_id": "729",
   "message":[  
      "Coupon code \"MYCOUPON\" was applied."
   ]
}
```
Apply Coupon to Quote.


## Remove Coupon

```shell
curl PUT "https://abc.com/simiconnector/rest/v2/quoteitems" \
  -H "Authorization: Bearer <token>"
  -d "{
"coupon_code":""
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2557"
   ],
   "quoteitems":[  
      {  
         "item_id":"2557",
         "quote_id":"690",
         "created_at":"2016-06-09 04:54:09",
         "updated_at":"2016-06-09 06:22:02",
         "product_id":"888",
         "store_id":"1",
         "parent_item_id":null,
         "is_virtual":false,
         "sku":"testcustom-option1",
         "name":"Test Custom Option Simple Product",
         "description":null,
         "applied_rule_ids":"",
         "additional_data":null,
         "free_shipping":false,
         "is_qty_decimal":"0",
         "no_discount":"0",
         "weight":"1.0000",
         "qty":100,
         "price":2,
         "base_price":2,
         "custom_price":null,
         "discount_percent":0,
         "discount_amount":0,
         "base_discount_amount":0,
         "tax_percent":0,
         "tax_amount":0,
         "base_tax_amount":0,
         "row_total":200,
         "base_row_total":200,
         "row_total_with_discount":"0.0000",
         "row_weight":100,
         "product_type":"simple",
         "base_tax_before_discount":null,
         "tax_before_discount":null,
         "original_custom_price":null,
         "redirect_url":null,
         "base_cost":null,
         "price_incl_tax":2,
         "base_price_incl_tax":2,
         "row_total_incl_tax":200,
         "base_row_total_incl_tax":200,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "gift_message_id":null,
         "weee_tax_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_applied":"a:0:{}",
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amnt":null,
         "event_id":null,
         "giftregistry_item_id":null,
         "gw_id":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "qty_options":[  

         ],
         "product":{  
            "entity_id":"888",
            "entity_type_id":"4",
            "attribute_set_id":"4",
            "type_id":"simple",
            "sku":"testcustom",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2016-06-07 07:49:15",
            "updated_at":"2016-06-07 07:51:17",
            "name":"Test Custom Option Simple Product",
            "small_image":"no_selection",
            "thumbnail":"no_selection",
            "url_key":"test-custom-option-simple-product",
            "url_path":"test-custom-option-simple-product.html",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"0",
            "is_recurring":"0",
            "price":"1.0000",
            "special_price":null,
            "weight":"1.0000",
            "msrp":null,
            "special_from_date":null,
            "special_to_date":null,
            "is_salable":"1",
            "stock_item":{  
               "item_id":"1867",
               "product_id":"888",
               "stock_id":"1",
               "qty":"88888.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Test Custom Option Simple Product",
               "store_id":"1",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null,
               "ordered_items":100
            },
            "do_not_use_category_id":true,
            "request_path":"test-custom-option-simple-product.html",
            "tier_price":[  

            ],
            "is_in_stock":"1",
            "store_id":"1",
            "customer_group_id":"1",
            "final_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "quote_item_qty":100,
            "quote_item_price":2,
            "quote_item_row_total":200,
            "category_ids":[  
               "2"
            ]
         },
         "tax_class_id":"0",
         "is_recurring":"0",
         "has_error":false,
         "is_nominal":false,
         "base_calculation_price":2,
         "calculation_price":2,
         "converted_price":2,
         "base_original_price":2,
         "taxable_amount":200,
         "base_taxable_amount":200,
         "is_price_incl_tax":false,
         "base_weee_tax_applied_row_amount":0,
         "original_price":2,
         "applied_rates":[  

         ],
         "discount_tax_compensation":0,
         "option":[  
            {  
               "option_title":"mydropdownoption",
               "option_value":"option1 title",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":200,
      "subtotal_incl_tax":200,
      "grand_total_excl_tax":200,
      "grand_total_incl_tax":200,
      "tax":0
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id": "729",
   "message":[  
      "Coupon code was canceled."
   ]
}
```
Cancel Coupon Code.



## Add Product To Quote

```shell
curl POST "https://abc.com/simiconnector/rest/v2/quoteitems " \
  -H "Authorization: Bearer <token>"
  -d "{
"product":"888",
"qty":"1",
"options":{"7":"3"}
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2575"
   ],
   "quoteitems":[  
      {  
         "quote_id":"689",
         "store_id":"2",
         "product":{  
            "store_id":"2",
            "entity_id":"888",
            "entity_type_id":"4",
            "attribute_set_id":"4",
            "type_id":"simple",
            "sku":"testcustom",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2016-06-07T00:49:15-07:00",
            "updated_at":"2016-06-07 07:51:17",
            "price":"1.0000",
            "special_price":null,
            "weight":"1.0000",
            "msrp":null,
            "gift_wrapping_price":null,
            "name":"Test Custom Option Simple Product",
            "meta_title":null,
            "meta_description":null,
            "image":"no_selection",
            "small_image":"no_selection",
            "thumbnail":"no_selection",
            "url_key":"test-custom-option-simple-product",
            "url_path":"test-custom-option-simple-product.html",
            "custom_design":null,
            "page_layout":null,
            "options_container":"container2",
            "country_of_manufacture":null,
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "gift_wrapping_available":"0",
            "status":"1",
            "is_recurring":"0",
            "visibility":"4",
            "tax_class_id":"0",
            "description":"Test Custom Option Simple Product",
            "short_description":"Test Custom Option Simple Product",
            "meta_keyword":null,
            "custom_layout_update":null,
            "special_from_date":null,
            "special_to_date":null,
            "news_from_date":null,
            "news_to_date":null,
            "custom_design_from":null,
            "custom_design_to":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "media_gallery":{  
               "images":[  

               ],
               "values":[  

               ]
            },
            "tier_price":[  

            ],
            "tier_price_changed":0,
            "stock_item":{  
               "item_id":"1867",
               "product_id":"888",
               "stock_id":"1",
               "qty":"88888.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status_changed_automatically":"0",
               "use_config_enable_qty_increments":"1",
               "product_name":"Test Custom Option Simple Product",
               "store_id":"2",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null,
               "ordered_items":1
            },
            "is_in_stock":"1",
            "is_salable":"1",
            "website_ids":[  
               "1"
            ],
            "cart_qty":"1",
            "qty":"1",
            "stick_within_parent":null,
            "customer_group_id":"0",
            "final_price":null,
            "quote_item_qty":1,
            "quote_item_price":2,
            "quote_item_row_total":2
         },
         "product_id":"888",
         "product_type":"simple",
         "sku":"testcustom-option1",
         "name":"Test Custom Option Simple Product",
         "weight":"1.0000",
         "tax_class_id":"0",
         "base_cost":null,
         "is_recurring":"0",
         "is_qty_decimal":"0",
         "is_nominal":false,
         "qty_to_add":1,
         "qty":1,
         "qty_options":[  

         ],
         "base_calculation_price":2,
         "calculation_price":2,
         "converted_price":2,
         "price":2,
         "base_original_price":2,
         "row_total":2,
         "base_row_total":2,
         "free_shipping":false,
         "tax_percent":0,
         "base_price":2,
         "price_incl_tax":2,
         "base_price_incl_tax":2,
         "row_total_incl_tax":2,
         "base_row_total_incl_tax":2,
         "taxable_amount":2,
         "base_taxable_amount":2,
         "is_price_incl_tax":false,
         "weee_tax_applied":"a:0:{}",
         "base_weee_tax_disposition":0,
         "weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amount":0,
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "row_weight":1,
         "discount_amount":0,
         "base_discount_amount":0,
         "discount_percent":0,
         "original_price":2,
         "applied_rule_ids":"",
         "tax_amount":0,
         "base_tax_amount":0,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "discount_tax_compensation":0,
         "is_virtual":false,
         "created_at":"2016-06-08 02:33:53",
         "updated_at":"2016-06-08 02:33:53",
         "item_id":"2575",
         "option":[  
            {  
               "option_title":"mydropdownoption",
               "option_value":"option1 title",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/2\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":2,
      "subtotal_incl_tax":2,
      "grand_total_excl_tax":2,
      "grand_total_incl_tax":2
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id": "729",
   "message":[  
      "Test Custom Option Simple Product was added to your shopping cart."
   ]
}
```
Add Products with Custom Options (Simple/Downloadable/Virtual Products)

## Add Configurable Product To Quote

```shell
curl POST "https://abc.com/simiconnector/rest/v2/quoteitems " \
  -H "Authorization: Bearer <token>"
  -d "{
"product":"406",
"qty":"5",
"super_attribute":{"92":"22","180":"79"}
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2573"
   ],
   "quoteitems":[  
      {  
         "quote_id":"689",
         "store_id":"2",
         "product":{  
            "store_id":"2",
            "entity_id":"406",
            "entity_type_id":"4",
            "attribute_set_id":"13",
            "type_id":"configurable",
            "sku":"msj012c",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2013-03-05T05:25:10-08:00",
            "updated_at":"2013-03-19 05:12:44",
            "name":"Linen Blazer",
            "meta_title":null,
            "meta_description":null,
            "image":"\/m\/s\/msj012t_2.jpg",
            "small_image":"\/m\/s\/msj012t_2.jpg",
            "thumbnail":"\/m\/s\/msj012t_2.jpg",
            "media_gallery":{  
               "images":[  
                  {  
                     "value_id":"688",
                     "file":"\/m\/s\/msj012t_2.jpg",
                     "product_id":"406",
                     "label":"",
                     "position":"1",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"1",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"689",
                     "file":"\/m\/s\/msj012a_2.jpg",
                     "product_id":"406",
                     "label":"",
                     "position":"2",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"2",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"813",
                     "file":"\/m\/s\/msj012b.jpg",
                     "product_id":"406",
                     "label":"",
                     "position":"3",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"3",
                     "disabled_default":"0"
                  }
               ],
               "values":[  

               ]
            },
            "gallery":null,
            "url_key":"linen-blazer",
            "url_path":"linen-blazer-580.html",
            "custom_design":null,
            "page_layout":"one_column",
            "options_container":"container1",
            "image_label":null,
            "small_image_label":null,
            "thumbnail_label":null,
            "country_of_manufacture":null,
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "gift_wrapping_available":null,
            "color":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"2",
            "occasion":"31",
            "apparel_type":"211",
            "sleeve_length":"47",
            "fit":"49",
            "size":null,
            "gender":"93",
            "description":"Single vented, notched lapels. Flap pockets. Tonal stitching. Fully lined. Linen. Dry clean.",
            "short_description":"In airy lightweight linen, this blazer is classic tailoring with a warm weather twist.",
            "meta_keyword":null,
            "custom_layout_update":null,
            "special_from_date":null,
            "special_to_date":null,
            "news_from_date":"2013-03-01 00:00:00",
            "news_to_date":null,
            "custom_design_from":null,
            "custom_design_to":null,
            "price":"455.0000",
            "special_price":null,
            "msrp":null,
            "gift_wrapping_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "tier_price":[  

            ],
            "tier_price_changed":0,
            "stock_item":{  
               "item_id":"676",
               "product_id":"406",
               "stock_id":"1",
               "qty":"0.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"configurable",
               "stock_status_changed_automatically":"0",
               "use_config_enable_qty_increments":"1",
               "product_name":"Linen Blazer",
               "store_id":"2",
               "product_type_id":"configurable",
               "product_status_changed":true,
               "product_changed_websites":null
            },
            "is_in_stock":"1",
            "is_salable":"1",
            "website_ids":[  
               "1"
            ],
            "cart_qty":"5",
            "qty":"5",
            "_cache_instance_products":[  
               {  

               },
               {  

               },
               {  

               },
               {  

               },
               {  

               }
            ],
            "_cache_instance_configurable_attributes":{  

            },
            "stick_within_parent":null,
            "customer_group_id":"0",
            "final_price":null,
            "_cache_instance_store_filter":{  

            },
            "parent_id":true,
            "quote_item_qty":5,
            "quote_item_price":455,
            "quote_item_row_total":2275,
            "_cache_instance_used_attributes":{  
               "92":{  

               },
               "180":{  

               }
            },
            "_cache_instance_used_product_attributes":{  
               "92":{  

               },
               "180":{  

               }
            },
            "_cache_instance_used_product_attribute_ids":[  
               "92",
               "180"
            ]
         },
         "product_id":"406",
         "product_type":"configurable",
         "sku":"msj013",
         "name":"Linen Blazer",
         "weight":null,
         "tax_class_id":"2",
         "base_cost":null,
         "is_recurring":null,
         "is_qty_decimal":"0",
         "is_nominal":false,
         "qty_to_add":5,
         "qty":5,
         "qty_options":{  
            "244":{  

            }
         },
         "has_children":true,
         "base_calculation_price":455,
         "calculation_price":455,
         "converted_price":455,
         "price":455,
         "base_original_price":455,
         "row_total":2275,
         "base_row_total":2275,
         "free_shipping":false,
         "tax_percent":8.25,
         "base_price":455,
         "price_incl_tax":492.54,
         "base_price_incl_tax":492.54,
         "row_total_incl_tax":2462.69,
         "base_row_total_incl_tax":2462.69,
         "taxable_amount":2275,
         "base_taxable_amount":2275,
         "is_price_incl_tax":false,
         "weee_tax_applied":"a:0:{}",
         "base_weee_tax_disposition":0,
         "weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amount":0,
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "row_weight":0,
         "discount_amount":0,
         "base_discount_amount":0,
         "discount_percent":0,
         "original_price":455,
         "original_discount_amount":0,
         "base_original_discount_amount":0,
         "applied_rule_ids":"29",
         "tax_amount":187.69,
         "base_tax_amount":187.69,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "discount_tax_compensation":0,
         "is_virtual":false,
         "created_at":"2016-06-08 02:33:12",
         "updated_at":"2016-06-08 02:33:12",
         "item_id":"2573",
         "option":[  
            {  
               "option_title":"Color",
               "option_value":"White",
               "option_price":0
            },
            {  
               "option_title":"Size",
               "option_value":"M",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/2\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/m\/s\/msj012t_2.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":2275,
      "subtotal_incl_tax":2462.69,
      "grand_total_excl_tax":2275,
      "grand_total_incl_tax":2462.69,
      "tax":187.69
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id": "729",
   "message":[  
      "Linen Blazer was added to your shopping cart."
   ]
}
```
Add Configurable Product To Quote

## Add Group Product To Quote

```shell
curl POST "https://abc.com/simiconnector/rest/v2/quoteitems " \
  -H "Authorization: Bearer <token>"
  -d "{
"product":"555",
"super_group":{"548":"3","551":"2"}
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2571",
      "2572"
   ],
   "quoteitems":[  
      {  
         "quote_id":"689",
         "store_id":"2",
         "product":{  
            "entity_id":"548",
            "entity_type_id":"4",
            "attribute_set_id":"17",
            "type_id":"simple",
            "sku":"acj00124",
            "has_options":"0",
            "required_options":"0",
            "created_at":"2013-03-19 22:59:37",
            "updated_at":"2016-06-08 02:23:32",
            "status":"1",
            "link_id":"614",
            "position":"2",
            "qty":1,
            "name":"Pearl Strand Necklace-24\"",
            "country_of_manufacture":"ID",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "meta_title":null,
            "meta_description":null,
            "custom_design":null,
            "page_layout":null,
            "options_container":"container2",
            "gift_message_available":null,
            "gift_wrapping_available":"0",
            "url_key":"pearl-strand-necklace-24",
            "url_path":"pearl-strand-necklace-24.html",
            "image":"\/a\/c\/acj001_1_4.jpg",
            "small_image":"\/a\/c\/acj001_1_4.jpg",
            "thumbnail":"\/a\/c\/acj001_1_4.jpg",
            "image_label":null,
            "small_image_label":null,
            "thumbnail_label":null,
            "visibility":"1",
            "tax_class_id":"2",
            "is_recurring":"0",
            "necklace_length":"212",
            "style":"205",
            "color":null,
            "gender":null,
            "jewelry_type":null,
            "description":"AA& quality 6.0-6.5mm pearls. Double knotted on silk thread. 24\" strand. 14K gold hook-and-eye clasp. Made in Indonesia.",
            "short_description":"For a discreet display of pure elegance. Layer multi strands or compliment with pearl or diamond studs. 18\" or 24\"",
            "meta_keyword":null,
            "recurring_profile":null,
            "custom_layout_update":null,
            "news_from_date":null,
            "news_to_date":null,
            "special_from_date":null,
            "special_to_date":null,
            "custom_design_from":null,
            "custom_design_to":null,
            "weight":"0.5000",
            "price":"250.0000",
            "special_price":null,
            "msrp":null,
            "gift_wrapping_price":null,
            "stock_item":{  
               "item_id":"1160",
               "product_id":"548",
               "stock_id":"1",
               "qty":"1000.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Pearl Strand Necklace-24\"",
               "store_id":"2",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null
            },
            "is_in_stock":"1",
            "is_salable":"1",
            "cart_qty":"3",
            "stick_within_parent":null,
            "store_id":"2",
            "customer_group_id":"0",
            "final_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "tier_price":[  

            ],
            "tier_price_changed":0,
            "quote_item_qty":3,
            "quote_item_price":250,
            "quote_item_row_total":750
         },
         "product_id":"548",
         "product_type":"simple",
         "sku":"acj00124",
         "name":"Pearl Strand Necklace-24\"",
         "weight":"0.5000",
         "tax_class_id":"2",
         "base_cost":null,
         "is_recurring":"0",
         "is_qty_decimal":"0",
         "is_nominal":false,
         "qty_to_add":3,
         "qty":3,
         "qty_options":[  

         ],
         "base_calculation_price":250,
         "calculation_price":250,
         "converted_price":250,
         "price":250,
         "base_original_price":250,
         "row_total":750,
         "base_row_total":750,
         "free_shipping":false,
         "tax_percent":8.25,
         "base_price":250,
         "price_incl_tax":270.63,
         "base_price_incl_tax":270.63,
         "row_total_incl_tax":811.88,
         "base_row_total_incl_tax":811.88,
         "taxable_amount":750,
         "base_taxable_amount":750,
         "is_price_incl_tax":false,
         "weee_tax_applied":"a:0:{}",
         "base_weee_tax_disposition":0,
         "weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amount":0,
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "row_weight":0,
         "discount_amount":0,
         "base_discount_amount":0,
         "discount_percent":0,
         "original_price":250,
         "original_discount_amount":0,
         "base_original_discount_amount":0,
         "applied_rule_ids":"29",
         "tax_amount":61.88,
         "base_tax_amount":61.88,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "discount_tax_compensation":0,
         "is_virtual":false,
         "created_at":"2016-06-08 02:32:05",
         "updated_at":"2016-06-08 02:32:05",
         "item_id":"2571",
         "option":[  

         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/2\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/acj001_1_4.jpg"
      },
      {  
         "quote_id":"689",
         "store_id":"2",
         "product":{  
            "entity_id":"551",
            "entity_type_id":"4",
            "attribute_set_id":"17",
            "type_id":"simple",
            "sku":"acj003",
            "has_options":"0",
            "required_options":"0",
            "created_at":"2013-03-20 01:03:10",
            "updated_at":"2013-03-21 01:36:49",
            "status":"1",
            "link_id":"615",
            "position":"3",
            "qty":1,
            "name":"Pearl Stud Earrings",
            "url_key":"pearl-stud-earrings",
            "country_of_manufacture":null,
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "meta_title":null,
            "meta_description":null,
            "image":"\/a\/c\/acj003_2.jpg",
            "small_image":"\/a\/c\/acj003_2.jpg",
            "thumbnail":"\/a\/c\/acj003_2.jpg",
            "custom_design":null,
            "page_layout":null,
            "options_container":"container2",
            "gift_message_available":null,
            "gift_wrapping_available":null,
            "url_path":"pearl-stud-earrings.html",
            "image_label":null,
            "small_image_label":null,
            "thumbnail_label":null,
            "visibility":"4",
            "tax_class_id":"2",
            "is_recurring":"0",
            "necklace_length":null,
            "color":"13",
            "gender":"94",
            "jewelry_type":"164",
            "style":"200",
            "description":"AA& quality 6.5mm pearl. 14K gold post. Made in Indonesia.",
            "short_description":"Prim and demure, pearl studs are a cross cultural symbol of style and refinement.",
            "meta_keyword":null,
            "custom_layout_update":null,
            "news_from_date":null,
            "news_to_date":null,
            "special_from_date":null,
            "special_to_date":null,
            "custom_design_from":null,
            "custom_design_to":null,
            "weight":"0.2500",
            "price":"110.0000",
            "special_price":null,
            "msrp":null,
            "gift_wrapping_price":null,
            "stock_item":{  
               "item_id":"1163",
               "product_id":"551",
               "stock_id":"1",
               "qty":"15.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Pearl Stud Earrings",
               "store_id":"2",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null
            },
            "is_in_stock":"1",
            "is_salable":"1",
            "cart_qty":"2",
            "stick_within_parent":null,
            "store_id":"2",
            "customer_group_id":"0",
            "final_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "tier_price":[  

            ],
            "tier_price_changed":0,
            "quote_item_qty":2,
            "quote_item_price":110,
            "quote_item_row_total":220
         },
         "product_id":"551",
         "product_type":"simple",
         "sku":"acj003",
         "name":"Pearl Stud Earrings",
         "weight":"0.2500",
         "tax_class_id":"2",
         "base_cost":null,
         "is_recurring":"0",
         "is_qty_decimal":"0",
         "is_nominal":false,
         "qty_to_add":2,
         "qty":2,
         "qty_options":[  

         ],
         "base_calculation_price":110,
         "calculation_price":110,
         "converted_price":110,
         "price":110,
         "base_original_price":110,
         "row_total":220,
         "base_row_total":220,
         "free_shipping":false,
         "tax_percent":8.25,
         "base_price":110,
         "price_incl_tax":119.08,
         "base_price_incl_tax":119.08,
         "row_total_incl_tax":238.15,
         "base_row_total_incl_tax":238.15,
         "taxable_amount":220,
         "base_taxable_amount":220,
         "is_price_incl_tax":false,
         "weee_tax_applied":"a:0:{}",
         "base_weee_tax_disposition":0,
         "weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amount":0,
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "row_weight":0,
         "discount_amount":0,
         "base_discount_amount":0,
         "discount_percent":0,
         "original_price":110,
         "original_discount_amount":0,
         "base_original_discount_amount":0,
         "applied_rule_ids":"29",
         "tax_amount":18.15,
         "base_tax_amount":18.15,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "discount_tax_compensation":0,
         "is_virtual":false,
         "created_at":"2016-06-08 02:32:05",
         "updated_at":"2016-06-08 02:32:05",
         "item_id":"2572",
         "option":[  

         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/2\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/acj003_2.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":970,
      "subtotal_incl_tax":1050.03,
      "grand_total_excl_tax":970,
      "grand_total_incl_tax":1050.03,
      "tax":80.03
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id": "729",
   "message":[  
      "Pearl Necklace Set was added to your shopping cart."
   ]
}
```
Add Group Product To Cart.

## Add Bundle Product To Quote

```shell
curl POST "https://abc.com/simiconnector/rest/v2/quoteitems " \
  -H "Authorization: Bearer <token>"
  -d "{
"product":"447",
"bundle_option":{"23":"89","24":"91"},
"bundle_option_qty":{"23":"3","24":"2"}
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2568"
   ],
   "quoteitems":[  
      {  
         "quote_id":"689",
         "store_id":"2",
         "product":{  
            "store_id":"2",
            "entity_id":"447",
            "entity_type_id":"4",
            "attribute_set_id":"16",
            "type_id":"bundle",
            "sku":"hdb010",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2013-03-05T06:10:53-08:00",
            "updated_at":"2013-03-21 01:17:25",
            "name":"Pillow and Throw Set",
            "meta_title":null,
            "meta_description":null,
            "image":"\/h\/d\/hdb010.jpg",
            "small_image":"\/h\/d\/hdb010.jpg",
            "thumbnail":"\/h\/d\/hdb010.jpg",
            "url_key":"pillow-and-throw-set",
            "url_path":"pillow-and-throw-set.html",
            "custom_design":null,
            "page_layout":"one_column",
            "options_container":"container1",
            "image_label":null,
            "small_image_label":null,
            "thumbnail_label":null,
            "country_of_manufacture":null,
            "msrp_enabled":"0",
            "gift_message_available":null,
            "gift_wrapping_available":null,
            "bedding_pattern":null,
            "status":"1",
            "visibility":"4",
            "price_type":"0",
            "sku_type":"0",
            "weight_type":"0",
            "price_view":"0",
            "shipment_type":"0",
            "bed_bath_type":"184",
            "decor_type":"217",
            "home_decor_type":"191",
            "description":"Includes a choice between Titian Raw Silk Pillow or Shay Printed Pillow and our Carnegia Alpaca Throw or Park Row Throw or Gramercy Throw.\r\n",
            "short_description":"A conveniently packaged pairing of our pillows and throws.\r\n",
            "meta_keyword":null,
            "custom_layout_update":null,
            "special_from_date":null,
            "special_to_date":null,
            "news_from_date":null,
            "news_to_date":null,
            "custom_design_from":null,
            "custom_design_to":null,
            "special_price":null,
            "gift_wrapping_price":null,
            "media_gallery":{  
               "images":[  
                  {  
                     "value_id":"824",
                     "file":"\/h\/d\/hdb009_2.jpg",
                     "product_id":"447",
                     "label":"",
                     "position":"1",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"1",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"825",
                     "file":"\/h\/d\/hdb008_2.jpg",
                     "product_id":"447",
                     "label":"",
                     "position":"2",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"2",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"826",
                     "file":"\/h\/d\/hdb006_2.jpg",
                     "product_id":"447",
                     "label":"",
                     "position":"3",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"3",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"827",
                     "file":"\/h\/d\/hdb007_2.jpg",
                     "product_id":"447",
                     "label":"",
                     "position":"4",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"4",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"828",
                     "file":"\/h\/d\/hdb005_2.jpg",
                     "product_id":"447",
                     "label":"",
                     "position":"5",
                     "disabled":"0",
                     "label_default":null,
                     "position_default":"5",
                     "disabled_default":"0"
                  },
                  {  
                     "value_id":"880",
                     "file":"\/h\/d\/hdb010.jpg",
                     "product_id":"447",
                     "label":"",
                     "position":"6",
                     "disabled":"1",
                     "label_default":null,
                     "position_default":"6",
                     "disabled_default":"1"
                  }
               ],
               "values":[  

               ]
            },
            "group_price":[  

            ],
            "group_price_changed":0,
            "tier_price":[  

            ],
            "tier_price_changed":0,
            "stock_item":{  
               "item_id":"717",
               "product_id":"447",
               "stock_id":"1",
               "qty":"0.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"bundle",
               "stock_status_changed_automatically":"0",
               "use_config_enable_qty_increments":"1",
               "product_name":"Pillow and Throw Set",
               "store_id":"2",
               "product_type_id":"bundle",
               "product_status_changed":true,
               "product_changed_websites":null
            },
            "is_in_stock":"1",
            "is_salable":"1",
            "website_ids":[  
               "1"
            ],
            "cart_qty":1,
            "qty":1,
            "_cache_instance_store_filter":"2",
            "_cache_instance_options_collection":{  

            },
            "_cache_instance_used_selections":{  

            },
            "_cache_instance_used_selections_ids":[  
               "89",
               "91"
            ],
            "stick_within_parent":null,
            "customer_group_id":"0",
            "final_price":null,
            "_cache_instance_selections_collection23_24":{  

            },
            "quote_item_qty":1,
            "quote_item_price":580,
            "quote_item_row_total":580,
            "_cache_instance_used_options":{  

            },
            "_cache_instance_used_options_ids":[  
               23,
               24
            ]
         },
         "product_id":"447",
         "product_type":"bundle",
         "sku":"hdb010-hdb008-hdb005",
         "name":"Pillow and Throw Set",
         "weight":5,
         "tax_class_id":null,
         "base_cost":null,
         "is_recurring":null,
         "is_qty_decimal":"0",
         "is_nominal":false,
         "qty_to_add":1,
         "qty":1,
         "qty_options":{  
            "381":{  

            },
            "384":{  

            }
         },
         "has_children":true,
         "base_calculation_price":null,
         "calculation_price":580,
         "converted_price":580,
         "price":580,
         "base_original_price":580,
         "row_total":580,
         "base_row_total":580,
         "free_shipping":false,
         "price_incl_tax":627.85,
         "base_price_incl_tax":627.85,
         "row_total_incl_tax":627.85,
         "base_row_total_incl_tax":627.85,
         "row_tax":0,
         "base_row_tax":0,
         "weee_tax_applied":"a:0:{}",
         "base_weee_tax_disposition":0,
         "weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amount":0,
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "row_weight":0,
         "tax_amount":47.85,
         "base_tax_amount":47.85,
         "is_virtual":false,
         "created_at":"2016-06-08 02:31:27",
         "updated_at":"2016-06-08 02:31:27",
         "item_id":"2568",
         "option":[  
            {  
               "option_title":"Accent Pillow",
               "option_value":"2 x Titian Raw Silk Pillow",
               "option_price":110
            },
            {  
               "option_title":"Decorative Throw",
               "option_value":"3 x Park Row Throw",
               "option_price":120
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/2\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/h\/d\/hdb010.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":580,
      "subtotal_incl_tax":627.85,
      "grand_total_excl_tax":580,
      "grand_total_incl_tax":627.85,
      "tax":47.85
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id": "729",
   "message":[  
      "Pillow and Throw Set was added to your shopping cart."
   ]
}
```
Add Bundle Product To Cart.

## Edit Quote Items Qty

```shell
curl PUT "https://abc.com/simiconnector/rest/v2/quoteitems " \
  -H "Authorization: Bearer <token>"
  -d "{
"2575":"4"
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2575"
   ],
   "quoteitems":[  
      {  
         "item_id":"2575",
         "quote_id":"689",
         "created_at":"2016-06-08 02:33:53",
         "updated_at":"2016-06-08 04:34:23",
         "product_id":"888",
         "store_id":"2",
         "parent_item_id":null,
         "is_virtual":false,
         "sku":"testcustom-option1",
         "name":"Test Custom Option Simple Product",
         "description":null,
         "applied_rule_ids":"",
         "additional_data":null,
         "free_shipping":false,
         "is_qty_decimal":"0",
         "no_discount":"0",
         "weight":"1.0000",
         "qty":4,
         "price":2,
         "base_price":2,
         "custom_price":null,
         "discount_percent":0,
         "discount_amount":0,
         "base_discount_amount":0,
         "tax_percent":0,
         "tax_amount":0,
         "base_tax_amount":0,
         "row_total":8,
         "base_row_total":8,
         "row_total_with_discount":"0.0000",
         "row_weight":4,
         "product_type":"simple",
         "base_tax_before_discount":null,
         "tax_before_discount":null,
         "original_custom_price":null,
         "redirect_url":null,
         "base_cost":null,
         "price_incl_tax":2,
         "base_price_incl_tax":2,
         "row_total_incl_tax":8,
         "base_row_total_incl_tax":8,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "gift_message_id":null,
         "weee_tax_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_applied":"a:0:{}",
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amnt":null,
         "event_id":null,
         "giftregistry_item_id":null,
         "gw_id":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "qty_options":[  

         ],
         "product":{  
            "entity_id":"888",
            "entity_type_id":"4",
            "attribute_set_id":"4",
            "type_id":"simple",
            "sku":"testcustom",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2016-06-07 07:49:15",
            "updated_at":"2016-06-07 07:51:17",
            "name":"Test Custom Option Simple Product",
            "small_image":"no_selection",
            "thumbnail":"no_selection",
            "url_key":"test-custom-option-simple-product",
            "url_path":"test-custom-option-simple-product.html",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"0",
            "is_recurring":"0",
            "price":"1.0000",
            "special_price":null,
            "weight":"1.0000",
            "msrp":null,
            "special_from_date":null,
            "special_to_date":null,
            "is_salable":"1",
            "stock_item":{  
               "item_id":"1867",
               "product_id":"888",
               "stock_id":"1",
               "qty":"88888.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Test Custom Option Simple Product",
               "store_id":"1",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null,
               "ordered_items":6
            },
            "do_not_use_category_id":true,
            "request_path":"test-custom-option-simple-product.html",
            "tier_price":[  

            ],
            "is_in_stock":"1",
            "store_id":"1",
            "customer_group_id":"0",
            "final_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "quote_item_qty":4,
            "quote_item_price":2,
            "quote_item_row_total":8
         },
         "tax_class_id":"0",
         "is_recurring":"0",
         "has_error":false,
         "is_nominal":false,
         "base_calculation_price":2,
         "calculation_price":2,
         "converted_price":2,
         "base_original_price":2,
         "taxable_amount":8,
         "base_taxable_amount":8,
         "is_price_incl_tax":false,
         "base_weee_tax_applied_row_amount":0,
         "original_price":2,
         "applied_rates":[  

         ],
         "discount_tax_compensation":0,
         "option":[  
            {  
               "option_title":"mydropdownoption",
               "option_value":"option1 title",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":8,
      "subtotal_incl_tax":8,
      "grand_total_excl_tax":8,
      "grand_total_incl_tax":8,
      "tax":0
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id": "729"
}
```
Edit Quote Item Qty.

## Remove Item From Quote

```shell
curl PUT "https://abc.com/simiconnector/rest/v2/quoteitems " \
  -H "Authorization: Bearer <token>"
  -d "{
"2575":"0"
}"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  

   ],
   "quoteitems":[  

   ],
   "total":{  
      "subtotal_excl_tax":0,
      "subtotal_incl_tax":0,
      "grand_total_excl_tax":0,
      "grand_total_incl_tax":0,
      "tax":0
   },
   "page_size":15,
   "from":0
}
```
Remove Quote Item.

## Continue Cart Session with Quote Id

```shell
curl GET "https://abc.com/simiconnector/rest/v2/quoteitems?quote_id=729 " \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2603"
   ],
   "quoteitems":[  
      {  
         "item_id":"2603",
         "quote_id":"729",
         "created_at":"2016-07-19 03:11:15",
         "updated_at":"2016-07-19 03:11:15",
         "product_id":"888",
         "store_id":"1",
         "parent_item_id":null,
         "is_virtual":"0",
         "sku":"testcustom-option1",
         "name":"Test Custom Option Simple Product",
         "description":null,
         "applied_rule_ids":"44",
         "additional_data":null,
         "free_shipping":false,
         "is_qty_decimal":"0",
         "no_discount":"0",
         "weight":"1.0000",
         "qty":1,
         "price":2,
         "base_price":2,
         "custom_price":null,
         "discount_percent":1.1,
         "discount_amount":0.02,
         "base_discount_amount":0.02,
         "tax_percent":0,
         "tax_amount":0,
         "base_tax_amount":0,
         "row_total":2,
         "base_row_total":2,
         "row_total_with_discount":"0.0000",
         "row_weight":1,
         "product_type":"simple",
         "base_tax_before_discount":null,
         "tax_before_discount":null,
         "original_custom_price":null,
         "redirect_url":null,
         "base_cost":null,
         "price_incl_tax":2,
         "base_price_incl_tax":2,
         "row_total_incl_tax":2,
         "base_row_total_incl_tax":2,
         "hidden_tax_amount":0,
         "base_hidden_tax_amount":0,
         "gift_message_id":null,
         "weee_tax_disposition":0,
         "weee_tax_row_disposition":0,
         "base_weee_tax_disposition":0,
         "base_weee_tax_row_disposition":0,
         "weee_tax_applied":"a:0:{}",
         "weee_tax_applied_amount":0,
         "weee_tax_applied_row_amount":0,
         "base_weee_tax_applied_amount":0,
         "base_weee_tax_applied_row_amnt":null,
         "event_id":null,
         "giftregistry_item_id":null,
         "gw_id":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "qty_options":[  

         ],
         "product":{  
            "entity_id":"888",
            "entity_type_id":"4",
            "attribute_set_id":"4",
            "type_id":"simple",
            "sku":"testcustom",
            "has_options":"1",
            "required_options":"1",
            "created_at":"2016-06-07 07:49:15",
            "updated_at":"2016-06-17 06:59:04",
            "name":"Test Custom Option Simple Product",
            "small_image":"no_selection",
            "thumbnail":"no_selection",
            "url_key":"test-custom-option-simple-product",
            "url_path":"test-custom-option-simple-product.html",
            "msrp_enabled":"2",
            "msrp_display_actual_price_type":"4",
            "gift_message_available":null,
            "status":"1",
            "visibility":"4",
            "tax_class_id":"0",
            "is_recurring":"0",
            "price":"1.0000",
            "special_price":null,
            "weight":"1.0000",
            "msrp":null,
            "special_from_date":null,
            "special_to_date":null,
            "is_salable":"1",
            "stock_item":{  
               "item_id":"1867",
               "product_id":"888",
               "stock_id":"1",
               "qty":"88884.0000",
               "min_qty":"0.0000",
               "use_config_min_qty":"1",
               "is_qty_decimal":"0",
               "backorders":"0",
               "use_config_backorders":"1",
               "min_sale_qty":"1.0000",
               "use_config_min_sale_qty":"1",
               "max_sale_qty":"0.0000",
               "use_config_max_sale_qty":"1",
               "is_in_stock":"1",
               "low_stock_date":null,
               "notify_stock_qty":null,
               "use_config_notify_stock_qty":"1",
               "manage_stock":"0",
               "use_config_manage_stock":"1",
               "stock_status_changed_auto":"0",
               "stock_status_changed_automatically":"0",
               "use_config_qty_increments":"1",
               "qty_increments":"0.0000",
               "use_config_enable_qty_inc":"1",
               "use_config_enable_qty_increments":"1",
               "enable_qty_increments":"0",
               "is_decimal_divided":"0",
               "type_id":"simple",
               "stock_status":"1",
               "product_name":"Test Custom Option Simple Product",
               "store_id":"1",
               "product_type_id":"simple",
               "product_status_changed":true,
               "product_changed_websites":null,
               "ordered_items":1
            },
            "do_not_use_category_id":true,
            "request_path":"test-custom-option-simple-product.html",
            "tier_price":[  

            ],
            "is_in_stock":"1",
            "store_id":"1",
            "customer_group_id":"0",
            "final_price":null,
            "group_price":[  

            ],
            "group_price_changed":0,
            "quote_item_qty":1,
            "quote_item_price":2,
            "quote_item_row_total":2
         },
         "tax_class_id":"0",
         "is_recurring":"0",
         "has_error":false,
         "is_nominal":false,
         "simirewardpoints_base_discount":0,
         "simirewardpoints_discount":0,
         "simi_base_discount":0,
         "simirewardpoints_spent":0,
         "base_calculation_price":2,
         "calculation_price":2,
         "converted_price":2,
         "base_original_price":2,
         "taxable_amount":2,
         "base_taxable_amount":2,
         "is_price_incl_tax":false,
         "base_weee_tax_applied_row_amount":0,
         "original_price":2,
         "applied_rates":[  

         ],
         "original_discount_amount":0.022,
         "base_original_discount_amount":0.022,
         "discount_tax_compensation":0,
         "simirewardpoints_earn":1,
         "option":[  
            {  
               "option_title":"mydropdownoption",
               "option_value":"option1 title",
               "option_price":0
            }
         ],
         "image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg"
      }
   ],
   "total":{  
      "subtotal_excl_tax":2,
      "subtotal_incl_tax":2,
      "tax":0,
      "discount":0.02,
      "grand_total_excl_tax":1.98,
      "grand_total_incl_tax":1.98,
      "custom_rows":[  
         {  
            "title":"You will earn",
            "sort_order":6,
            "value":1,
            "value_string":"1 Codypoint"
         }
      ]
   },
   "page_size":15,
   "from":0,
   "cart_total":1,
   "quote_id":"729",
   "loyalty":{  
      "loyalty_image":"http:\/\/localhost.com\/magento19\/skin\/frontend\/base\/default\/images\/simirewardpoints\/point.png",
      "loyalty_label":"Checkout now and earn 1 Codypoint in rewards"
   }
}
```
This API is to Continue Cart Session with Quote Id
