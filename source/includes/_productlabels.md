# Product Labels

## Product Labels Properties

Attributes| Type| Description
--------- | ------- | -----------
label_id | id | Label Id
name | string | Label Name
description | string | Label Description
text | string | Label Text
image | string | Label Image Url
position | int | Label Position


## Labels on Product List

```shell
curl "https://abc.com/simiconnector/rest/v2/products" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "883",
      "887",
      "891"
   ],
   "products":[  
      {  
         "entity_id":"883",
         "entity_type_id":"4",
         "attribute_set_id":"20",
         "type_id":"configurable",
         "sku":"ABC456",
         "has_options":"1",
         "required_options":"1",
         "created_at":"2014-05-01 02:59:57",
         "updated_at":"2016-06-22 07:07:21",
         "cat_index_position":"1",
         "price":"50.0000",
         "tax_class_id":"2",
         "final_price":"50.0000",
         "minimal_price":"50.0000",
         "min_price":"50.0000",
         "max_price":"50.0000",
         "tier_price":null,
         "name":"My Configurable Product",
         "small_image":"no_selection",
         "thumbnail":"no_selection",
         "url_key":"my-configurable-product",
         "msrp_enabled":"2",
         "msrp_display_actual_price_type":"4",
         "short_description":"Short Description",
         "special_price":null,
         "msrp":null,
         "news_from_date":null,
         "news_to_date":null,
         "special_from_date":null,
         "special_to_date":null,
         "status":"1",
         "do_not_use_category_id":true,
         "request_path":"my-configurable-product.html",
         "is_salable":"1",
         "stock_item":{  
            "is_in_stock":"1"
         },
         "tax_percent":8.25,
         "images":[  
            {  
               "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg",
               "position":1
            }
         ],
         "app_prices":{  
            "has_special_price":0,
            "show_ex_in_price":0,
            "price":50
         },
         "product_label":{  
            "name":"Name",
            "label_id":"1",
            "description":"Description",
            "text":"abc",
            "image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlabel\/thermovape-single.jpg",
            "position":"1"
         }
      }
   ],
   "total":3,
   "page_size":15,
   "from":0,
   "layers":[  

   ],
   "orders":[  
      {  
         "key":"position",
         "value":"Position",
         "direction":"asc",
         "default":"1"
      },
      {  
         "key":"position",
         "value":"Position",
         "direction":"desc",
         "default":"0"
      },
      {  
         "key":"name",
         "value":"Name",
         "direction":"asc",
         "default":"0"
      },
      {  
         "key":"name",
         "value":"Name",
         "direction":"desc",
         "default":"0"
      },
      {  
         "key":"price",
         "value":"Price",
         "direction":"asc",
         "default":"0"
      },
      {  
         "key":"price",
         "value":"Price",
         "direction":"desc",
         "default":"0"
      }
   ]
}
```

Position table:

1 - 'Top-left'

2 - 'Top-center'

3 - 'Top-right'

4 - 'Middle-left'

5 - 'Middle-center'

6 - 'Middle-right'

7 - 'Bottom-left'

8 - 'Bottom-center'

9 - 'Bottom-right'


## Label On Product Details

```shell
curl "https://abc.com/simiconnector/rest/v2/products/883" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"883",
      "entity_type_id":"4",
      "attribute_set_id":"20",
      "type_id":"configurable",
      "sku":"ABC456",  
      "wishlist_item_id":null,
      "product_label":{  
         "name":"Name",
         "label_id":"1",
         "description":"Description",
         "text":"abc",
         "image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlabel\/thermovape-single.jpg",
         "position":"1"
      },
      "loyalty_image":"http:\/\/localhost.com\/magento19\/skin\/frontend\/base\/default\/images\/simirewardpoints\/point.png",
      "loyalty_label":"You could receive some Codypoints for purchasing this product"
   }
}
```
On product Detail API, the label would be added the same way with on the Product Listing

## Multi Label On Product List

```shell
curl "https://abc.com/simiconnector/rest/v2/products" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"906",
      "entity_type_id":"4",
      "attribute_set_id":"4",
      "type_id":"simple",
      "sku":"cody",
      "has_options":"0",
      "required_options":"0",
      "created_at":"2017-06-10T00:33:04-07:00",
      "updated_at":"2017-12-01 12:53:23",
      "price":"0.1000",
      "special_price":null,
      "weight":"1.0000",
      "msrp":null,
      "gift_wrapping_price":null,
      "name":"cody",
      "meta_title":null,
      "meta_description":null,
      "image":"no_selection",
      "small_image":"no_selection",
      "thumbnail":"no_selection",
      "url_key":"cody",
      "url_path":"cody.html",
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
      "description":"nooo",
      "short_description":"123213",
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
         "item_id":"1885",
         "product_id":"906",
         "stock_id":"1",
         "qty":"110.0000",
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
         "product_name":"cody",
         "store_id":"1",
         "product_type_id":"simple",
         "product_status_changed":true,
         "product_changed_websites":null
      },
      "is_in_stock":"1",
      "is_salable":"1",
      "additional":[  

      ],
      "images":[  
         {  
            "url":"http://localhost.com/magento19/media/catalog/product/cache/1/small_image/600x/040ec09b1e35df139433887a97daa66f/images/catalog/product/placeholder/small_image.jpg",
            "position":1
         }
      ],
      "app_prices":{  
         "has_special_price":0,
         "show_ex_in_price":0,
         "price_label":"Regular Price",
         "price":0.1
      },
      "app_tier_prices":[  

      ],
      "app_reviews":{  
         "rate":0,
         "number":0,
         "5_star_number":0,
         "4_star_number":0,
         "3_star_number":0,
         "2_star_number":0,
         "1_star_number":0,
         "form_add_reviews":[  
            {  
               "rates":[  
                  {  
                     "rate_code":"Quality",
                     "rate_options":[  
                        {  
                           "key":"1",
                           "value":"1"
                        },
                        {  
                           "key":"1",
                           "value":"2"
                        },
                        {  
                           "key":"1",
                           "value":"3"
                        },
                        {  
                           "key":"1",
                           "value":"4"
                        },
                        {  
                           "key":"1",
                           "value":"5"
                        }
                     ]
                  },
                  {  
                     "rate_code":"Price",
                     "rate_options":[  
                        {  
                           "key":"3",
                           "value":"11"
                        },
                        {  
                           "key":"3",
                           "value":"12"
                        },
                        {  
                           "key":"3",
                           "value":"13"
                        },
                        {  
                           "key":"3",
                           "value":"14"
                        },
                        {  
                           "key":"3",
                           "value":"15"
                        }
                     ]
                  },
                  {  
                     "rate_code":"Value",
                     "rate_options":[  
                        {  
                           "key":"2",
                           "value":"6"
                        },
                        {  
                           "key":"2",
                           "value":"7"
                        },
                        {  
                           "key":"2",
                           "value":"8"
                        },
                        {  
                           "key":"2",
                           "value":"9"
                        },
                        {  
                           "key":"2",
                           "value":"10"
                        }
                     ]
                  }
               ],
               "form_review":{  
                  "key_1":"nickname",
                  "key_2":"title",
                  "key_3":"detail",
                  "form_key":[  
                     {  
                        "key":"nickname",
                        "value":"Nickname"
                     },
                     {  
                        "key":"title",
                        "value":"Title"
                     },
                     {  
                        "key":"detail",
                        "value":"Detail"
                     }
                  ]
               }
            }
         ]
      },
      "app_options":{  
         "custom_options":[  

         ]
      },
      "wishlist_item_id":null,
      "product_labels":[  
         {  
            "name":"Cody",
            "label_id":"1",
            "description":"Sample",
            "text":"",
            "image":"http://localhost.com/magento19/media/simi/simiconnector/productlabel/49a6898b8a3837679be1a06c5e51e2c3.png",
            "position":"1"
         },
         {  
            "name":"13",
            "label_id":"2",
            "description":"1",
            "text":"1",
            "image":"",
            "position":"1"
         }
      ],
      "product_video":null
   }
}
```
On product Listing API, if there is NO product_label, there could be product_labels which contain multi labels for one product.


## Multi Label On Product Detail

```shell
curl "https://abc.com/simiconnector/rest/v2/products/906" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"906",
      "entity_type_id":"4",
      "attribute_set_id":"4",
      "type_id":"simple",
      "sku":"cody",
      "has_options":"0",
      "required_options":"0",
      "created_at":"2017-06-10T00:33:04-07:00",
      "updated_at":"2017-12-01 12:53:23",
      "price":"0.1000",
      "special_price":null,
      "weight":"1.0000",
      "msrp":null,
      "gift_wrapping_price":null,
      "name":"cody",
      "meta_title":null,
      "meta_description":null,
      "image":"no_selection",
      "small_image":"no_selection",
      "thumbnail":"no_selection",
      "url_key":"cody",
      "url_path":"cody.html",
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
      "description":"nooo",
      "short_description":"123213",
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
         "item_id":"1885",
         "product_id":"906",
         "stock_id":"1",
         "qty":"110.0000",
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
         "product_name":"cody",
         "store_id":"1",
         "product_type_id":"simple",
         "product_status_changed":true,
         "product_changed_websites":null
      },
      "is_in_stock":"1",
      "is_salable":"1",
      "additional":[  

      ],
      "images":[  
         {  
            "url":"http://localhost.com/magento19/media/catalog/product/cache/1/small_image/600x/040ec09b1e35df139433887a97daa66f/images/catalog/product/placeholder/small_image.jpg",
            "position":1
         }
      ],
      "app_prices":{  
         "has_special_price":0,
         "show_ex_in_price":0,
         "price_label":"Regular Price",
         "price":0.1
      },
      "app_tier_prices":[  

      ],
      "app_reviews":{  
         "rate":0,
         "number":0,
         "5_star_number":0,
         "4_star_number":0,
         "3_star_number":0,
         "2_star_number":0,
         "1_star_number":0,
         "form_add_reviews":[  
            {  
               "rates":[  
                  {  
                     "rate_code":"Quality",
                     "rate_options":[  
                        {  
                           "key":"1",
                           "value":"1"
                        },
                        {  
                           "key":"1",
                           "value":"2"
                        },
                        {  
                           "key":"1",
                           "value":"3"
                        },
                        {  
                           "key":"1",
                           "value":"4"
                        },
                        {  
                           "key":"1",
                           "value":"5"
                        }
                     ]
                  },
                  {  
                     "rate_code":"Price",
                     "rate_options":[  
                        {  
                           "key":"3",
                           "value":"11"
                        },
                        {  
                           "key":"3",
                           "value":"12"
                        },
                        {  
                           "key":"3",
                           "value":"13"
                        },
                        {  
                           "key":"3",
                           "value":"14"
                        },
                        {  
                           "key":"3",
                           "value":"15"
                        }
                     ]
                  },
                  {  
                     "rate_code":"Value",
                     "rate_options":[  
                        {  
                           "key":"2",
                           "value":"6"
                        },
                        {  
                           "key":"2",
                           "value":"7"
                        },
                        {  
                           "key":"2",
                           "value":"8"
                        },
                        {  
                           "key":"2",
                           "value":"9"
                        },
                        {  
                           "key":"2",
                           "value":"10"
                        }
                     ]
                  }
               ],
               "form_review":{  
                  "key_1":"nickname",
                  "key_2":"title",
                  "key_3":"detail",
                  "form_key":[  
                     {  
                        "key":"nickname",
                        "value":"Nickname"
                     },
                     {  
                        "key":"title",
                        "value":"Title"
                     },
                     {  
                        "key":"detail",
                        "value":"Detail"
                     }
                  ]
               }
            }
         ]
      },
      "app_options":{  
         "custom_options":[  

         ]
      },
      "wishlist_item_id":null,
      "product_labels":[  
         {  
            "name":"Cody",
            "label_id":"1",
            "description":"Sample",
            "text":"",
            "image":"http://localhost.com/magento19/media/simi/simiconnector/productlabel/49a6898b8a3837679be1a06c5e51e2c3.png",
            "position":"1"
         },
         {  
            "name":"13",
            "label_id":"2",
            "description":"1",
            "text":"1",
            "image":"",
            "position":"1"
         }
      ],
      "product_video":null
   }
}
```
On product Detail API, if there is NO product_label, there could be product_labels which contain multi labels for one product.