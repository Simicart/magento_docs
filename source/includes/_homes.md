# Home screen

## Home Screen Properties

Attributes| Type| Description
--------- | ------- | -----------
homebanners | array | Home Banners
homecategories | array | Home Categories
homeproductlists | array | Home Product Lists




## View Home Screen Items with Product Lists Details

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homes" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "home":{  
      "homebanners":{  
         "all_ids":[  
            "1"
         ],
         "homebanners":[  
            {  
               "banner_id":"1",
               "banner_name":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/3784554_CV-Grimsel.jpg",
               "banner_url":null,
               "banner_title":"Title",
               "status":"1",
               "website_id":"0",
               "type":"2",
               "category_id":"5",
               "product_id":"0",
               "sort_order":"0",
               "banner_url_tablet":null,
               "banner_name_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/3784368_cv.jpg",
               "entity_id":"23",
               "content_type":"2",
               "item_id":"1",
               "store_view_id":"1",
               "width":960,
               "height":358,
               "width_tablet":2048,
               "height_tablet":893,
               "has_children":true,
               "cat_name":"Men"
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      },
      "homecategories":{  
         "all_ids":[  
            "1"
         ],
         "homecategories":[  
            {  
               "simicategory_id":"1",
               "simicategory_name":"Root Catalog",
               "simicategory_filename":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/3784368_cv.jpg",
               "category_id":"1",
               "status":"1",
               "website_id":"0",
               "storeview_id":"Array",
               "sort_order":"0",
               "simicategory_filename_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/3784554_CV-Grimsel.jpg",
               "entity_id":"9",
               "content_type":"3",
               "item_id":"1",
               "store_view_id":"1",
               "width":2048,
               "height":893,
               "width_tablet":960,
               "height_tablet":358,
               "cat_name":"Root Catalog",
               "has_children":true
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      },
      "homeproductlists":{  
         "all_ids":[  
            "1"
         ],
         "homeproductlists":[  
            {  
               "productlist_id":"1",
               "list_title":"2",
               "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/3784368_cv@2x.jpg",
               "list_type":"1",
               "list_products":"338, 337",
               "list_status":"1",
               "sort_order":"0",
               "list_image_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/3784554_CV-Grimsel@2x.jpg",
               "entity_id":"27",
               "content_type":"4",
               "item_id":"1",
               "store_view_id":"1",
               "width":2048,
               "height":893,
               "width_tablet":960,
               "height_tablet":358,
               "type_name":"Custom Product List",
               "product_array":{  
                  "all_ids":[  
                     "337",
                     "338"
                  ],
                  "products":[  
                     {  
                        "entity_id":"337",
                        "entity_type_id":"4",
                        "attribute_set_id":"11",
                        "type_id":"simple",
                        "sku":"ace000",
                        "has_options":"0",
                        "required_options":"0",
                        "created_at":"2013-03-05 12:48:17",
                        "updated_at":"2013-03-20 23:45:10",
                        "price":"295.0000",
                        "tax_class_id":"2",
                        "final_price":"295.0000",
                        "minimal_price":"295.0000",
                        "min_price":"295.0000",
                        "max_price":"295.0000",
                        "tier_price":null,
                        "name":"Aviator Sunglasses",
                        "small_image":"\/a\/c\/ace000a_1.jpg",
                        "thumbnail":"\/a\/c\/ace000a_1.jpg",
                        "url_key":"aviator-sunglasses",
                        "image_label":null,
                        "small_image_label":null,
                        "thumbnail_label":null,
                        "msrp_enabled":"2",
                        "msrp_display_actual_price_type":"4",
                        "short_description":"A timeless accessory staple, the unmistakable teardrop lenses of our Aviator sunglasses appeal to everyone from suits to rock stars to citizens of the world.",
                        "special_price":null,
                        "msrp":null,
                        "news_from_date":null,
                        "news_to_date":null,
                        "special_from_date":null,
                        "special_to_date":null,
                        "status":"1",
                        "do_not_use_category_id":true,
                        "request_path":"aviator-sunglasses.html",
                        "is_salable":"1",
                        "stock_item":{  
                           "is_in_stock":"1"
                        },
                        "tax_percent":8.25,
                        "images":[  
                           {  
                              "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/ace000a_1.jpg",
                              "position":1
                           }
                        ],
                        "app_prices":{  
                           "has_special_price":0,
                           "show_ex_in_price":0,
                           "price":295
                        }
                     },
                     {  
                        "entity_id":"338",
                        "entity_type_id":"4",
                        "attribute_set_id":"11",
                        "type_id":"simple",
                        "sku":"ace001",
                        "has_options":"0",
                        "required_options":"0",
                        "created_at":"2013-03-05 12:48:17",
                        "updated_at":"2013-03-20 23:45:30",
                        "price":"295.0000",
                        "tax_class_id":"2",
                        "final_price":"225.0000",
                        "minimal_price":"225.0000",
                        "min_price":"225.0000",
                        "max_price":"225.0000",
                        "tier_price":null,
                        "name":"Jackie O Round Sunglasses",
                        "small_image":"\/a\/c\/ace001_1.jpg",
                        "thumbnail":"\/a\/c\/ace001_1.jpg",
                        "url_key":"jackie-o-round-sunglasses",
                        "image_label":null,
                        "small_image_label":null,
                        "thumbnail_label":null,
                        "msrp_enabled":"2",
                        "msrp_display_actual_price_type":"4",
                        "short_description":"These distinct, feminine frames balance a classic Jackie-O styling with a modern look. ",
                        "special_price":"225.0000",
                        "msrp":null,
                        "news_from_date":null,
                        "news_to_date":null,
                        "special_from_date":"2013-03-05 00:00:00",
                        "special_to_date":null,
                        "status":"1",
                        "do_not_use_category_id":true,
                        "request_path":"jackie-o-round-sunglasses.html",
                        "is_salable":"1",
                        "stock_item":{  
                           "is_in_stock":"1"
                        },
                        "tax_percent":8.25,
                        "images":[  
                           {  
                              "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/ace001_1.jpg",
                              "position":1
                           }
                        ],
                        "app_prices":{  
                           "has_special_price":1,
                           "price_label":"Regular Price",
                           "regular_price":295,
                           "show_ex_in_price":0,
                           "special_price_label":"Special Price",
                           "price":225
                        }
                     }
                  ],
                  "total":2,
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
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      }
   }
}
```

This API return Home screen detail with product lists items.

## View Home Screen Items

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homes/lite" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "home":{  
      "homebanners":{  
         "all_ids":[  
            "1"
         ],
         "homebanners":[  
            {  
               "banner_id":"1",
               "banner_name":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/3784554_CV-Grimsel.jpg",
               "banner_url":null,
               "banner_title":"Title",
               "status":"1",
               "website_id":"0",
               "type":"2",
               "category_id":"5",
               "product_id":"0",
               "sort_order":"0",
               "banner_url_tablet":null,
               "banner_name_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/3784368_cv.jpg",
               "entity_id":"23",
               "content_type":"2",
               "item_id":"1",
               "store_view_id":"1",
               "width":960,
               "height":358,
               "width_tablet":2048,
               "height_tablet":893,
               "has_children":true,
               "cat_name":"Men"
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      },
      "homecategories":{  
         "all_ids":[  
            "1"
         ],
         "homecategories":[  
            {  
               "simicategory_id":"1",
               "simicategory_name":"Root Catalog",
               "simicategory_filename":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/3784368_cv.jpg",
               "category_id":"1",
               "status":"1",
               "website_id":"0",
               "storeview_id":"Array",
               "sort_order":"0",
               "simicategory_filename_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/3784554_CV-Grimsel.jpg",
               "entity_id":"9",
               "content_type":"3",
               "item_id":"1",
               "store_view_id":"1",
               "width":2048,
               "height":893,
               "width_tablet":960,
               "height_tablet":358,
               "cat_name":"Root Catalog",
               "has_children":true
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      },
      "homeproductlists":{  
         "all_ids":[  
            "1"
         ],
         "homeproductlists":[  
            {  
               "productlist_id":"1",
               "list_title":"2",
               "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/3784368_cv@2x.jpg",
               "list_type":"1",
               "list_products":"338, 337",
               "list_status":"1",
               "sort_order":"0",
               "list_image_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/3784554_CV-Grimsel@2x.jpg",
               "entity_id":"27",
               "content_type":"4",
               "item_id":"1",
               "store_view_id":"1",
               "width":2048,
               "height":893,
               "width_tablet":960,
               "height_tablet":358,
               "type_name":"Custom Product List"
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      }
   }
}
```

This API return Home screen detail with no Product list included.