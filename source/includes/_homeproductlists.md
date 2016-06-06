# Home Product Lists

## Home Product List Properties

Attributes| Type| Description
--------- | ------- | -----------
productlist_id | id | Product List Id
list_title | string | Product list Title
list_image | string | Product list Image URL
list_status | int | Product list Status
list_products | array | Products of this List
product_array | array | Products Details Listed

## View Product Lists

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homeproductlists" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "5",
      "1"
   ],
   "homeproductlists":[  
      {  
         "productlist_id":"5",
         "list_title":"Recently Added",
         "list_image":"",
         "list_type":"5",
         "list_products":null,
         "list_status":"0",
         "sort_order":"0",
         "entity_id":"47",
         "content_type":"4",
         "item_id":"5",
         "store_view_id":"1",
         "width":null,
         "height":null,
         "type_name":"Recently Added",
         "product_array":{  
            "all_ids":[  
               "881",
               "880",
               "879",
               "878",
               "877",
               "564",
               "563",
               "561",
               "560",
               "559",
               "558",
               "557",
               "555",
               "554",
               "553"
            ],
            "products":[  
               {  
                  "entity_id":"881",
                  "entity_type_id":"4",
                  "attribute_set_id":"13",
                  "type_id":"simple",
                  "sku":"wbk002c-Black-S",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-05-09 02:20:17",
                  "updated_at":"2014-03-07 22:40:41",
                  "price":"150.0000",
                  "tax_class_id":"2",
                  "final_price":"150.0000",
                  "minimal_price":"150.0000",
                  "min_price":"150.0000",
                  "max_price":"150.0000",
                  "tier_price":null,
                  "name":"Black Nolita Cami-Black-S",
                  "small_image":"\/w\/b\/wbk002t_5.jpg",
                  "thumbnail":"\/w\/b\/wbk002t_5.jpg",
                  "url_key":"black-nolita-cami-black-s",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Cut from tissue-weight silk crepe de chine, this airy style features a ruched neckline with tie and an unfinished hem for a contrastinly rugged feel. Compliment yours with skinny jeans.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":"2013-05-08 00:00:00",
                  "news_to_date":null,
                  "special_from_date":"2013-05-08 00:00:00",
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"black-nolita-cami-black-s.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/w\/b\/wbk002t_5.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":150
                  }
               },
               {  
                  "entity_id":"880",
                  "entity_type_id":"4",
                  "attribute_set_id":"13",
                  "type_id":"simple",
                  "sku":"wbk002c-Black-XS",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-05-09 02:20:04",
                  "updated_at":"2014-03-07 22:39:44",
                  "price":"150.0000",
                  "tax_class_id":"2",
                  "final_price":"150.0000",
                  "minimal_price":"150.0000",
                  "min_price":"150.0000",
                  "max_price":"150.0000",
                  "tier_price":null,
                  "name":"Black Nolita Cami-Black-XS",
                  "small_image":"\/w\/b\/wbk002t_4.jpg",
                  "thumbnail":"\/w\/b\/wbk002t_4.jpg",
                  "url_key":"black-nolita-cami-black-xs",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Cut from tissue-weight silk crepe de chine, this airy style features a ruched neckline with tie and an unfinished hem for a contrastinly rugged feel. Compliment yours with skinny jeans.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":"2013-05-08 00:00:00",
                  "news_to_date":null,
                  "special_from_date":"2013-05-08 00:00:00",
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"black-nolita-cami-black-xs.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/w\/b\/wbk002t_4.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":150
                  }
               },
               {  
                  "entity_id":"879",
                  "entity_type_id":"4",
                  "attribute_set_id":"13",
                  "type_id":"simple",
                  "sku":"wbk000c-Pink-L",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-05-09 02:18:12",
                  "updated_at":"2014-03-07 22:37:34",
                  "price":"150.0000",
                  "tax_class_id":"2",
                  "final_price":"150.0000",
                  "minimal_price":"150.0000",
                  "min_price":"150.0000",
                  "max_price":"150.0000",
                  "tier_price":null,
                  "name":"NoLIta Cami-Pink-L",
                  "small_image":"\/w\/b\/wbk000t_6.jpg",
                  "thumbnail":"\/w\/b\/wbk000t_6.jpg",
                  "url_key":"nolita-cami-pink-l",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Cut from tissue-weight silk crepe de chine, this airy style features a ruched neckline with tie and an unfinished hem for a contrastinly rugged feel. Compliment yours with skinny jeans.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":"2013-03-20 00:00:00",
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"nolita-cami-pink-l.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/w\/b\/wbk000t_6.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":150
                  }
               },
               {  
                  "entity_id":"878",
                  "entity_type_id":"4",
                  "attribute_set_id":"13",
                  "type_id":"simple",
                  "sku":"wbk002M",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-05-08 22:11:59",
                  "updated_at":"2014-03-07 22:38:43",
                  "price":"150.0000",
                  "tax_class_id":"2",
                  "final_price":"120.0000",
                  "minimal_price":"120.0000",
                  "min_price":"120.0000",
                  "max_price":"120.0000",
                  "tier_price":null,
                  "name":"Black Nolita Cami",
                  "small_image":"\/w\/b\/wbk002t_3.jpg",
                  "thumbnail":"\/w\/b\/wbk002t_3.jpg",
                  "url_key":"black-nolita-cami",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Cut from tissue-weight silk crepe de chine, this airy style features a ruched neckline with tie and an unfinished hem for a contrastinly rugged feel. Compliment yours with skinny jeans.",
                  "special_price":"120.0000",
                  "msrp":null,
                  "news_from_date":"2013-05-08 00:00:00",
                  "news_to_date":null,
                  "special_from_date":"2013-05-08 00:00:00",
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"black-nolita-cami-880.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/w\/b\/wbk002t_3.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":1,
                     "price_label":"Regular Price",
                     "price":120,
                     "show_ex_in_price":0,
                     "special_price_label":"Special Price"
                  }
               },
               {  
                  "entity_id":"877",
                  "entity_type_id":"4",
                  "attribute_set_id":"13",
                  "type_id":"configurable",
                  "sku":"wbk002c",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-05-08 22:10:35",
                  "updated_at":"2013-05-17 03:20:12",
                  "price":"150.0000",
                  "tax_class_id":"2",
                  "final_price":"150.0000",
                  "minimal_price":"150.0000",
                  "min_price":"150.0000",
                  "max_price":"150.0000",
                  "tier_price":null,
                  "name":"Black Nolita Cami",
                  "small_image":"\/w\/b\/wbk002t_2.jpg",
                  "thumbnail":"\/w\/b\/wbk002a_3.jpg",
                  "url_key":"black-nolita-cami",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Cut from tissue-weight silk crepe de chine, this airy style features a ruched neckline with tie and an unfinished hem for a contrastinly rugged feel. Compliment yours with skinny jeans.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":"2013-05-08 00:00:00",
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"black-nolita-cami.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/w\/b\/wbk002t_2.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":150
                  }
               },
               {  
                  "entity_id":"564",
                  "entity_type_id":"4",
                  "attribute_set_id":"4",
                  "type_id":"virtual",
                  "sku":"mem000",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-03-26 21:00:31",
                  "updated_at":"2016-05-30 07:21:09",
                  "price":"350.0000",
                  "tax_class_id":"0",
                  "final_price":"350.0000",
                  "minimal_price":"350.0000",
                  "min_price":"350.0000",
                  "max_price":"350.0000",
                  "tier_price":null,
                  "name":"Madison Island VIP Membership - 1 Year",
                  "small_image":"\/v\/i\/vip_membership.jpg",
                  "thumbnail":"\/v\/i\/vip_membership.jpg",
                  "url_key":"madison-island-vip-membership-1-year",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Gain insider access to the best styles for fashion and home at up to 40% off. Join and discover some fabulous finds. \r\n\r\nMembership will be reviewed and approved by a Sales Associate.\r\n",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"madison-island-vip-membership-1-year.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/v\/i\/vip_membership.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":350
                  }
               },
               {  
                  "entity_id":"563",
                  "entity_type_id":"4",
                  "attribute_set_id":"10",
                  "type_id":"downloadable",
                  "sku":"hbm010",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-03-26 03:20:16",
                  "updated_at":"2013-04-03 14:43:49",
                  "price":"2.0000",
                  "tax_class_id":"0",
                  "final_price":"2.0000",
                  "minimal_price":"2.0000",
                  "min_price":"2.0000",
                  "max_price":"2.0000",
                  "tier_price":null,
                  "name":"Fire [Kalima remix] by Unannounced Guest",
                  "small_image":"\/u\/n\/unannouncedguest_.jpg",
                  "thumbnail":"\/u\/n\/unannouncedguest_.jpg",
                  "url_key":"fire-kalima-remix-by-unannounced-guest",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Tunes for the trip.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "links_purchased_separately":"1",
                  "links_exist":"1",
                  "do_not_use_category_id":true,
                  "request_path":"fire-kalima-remix-by-unannounced-guest.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/u\/n\/unannouncedguest_.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":2
                  }
               },
               {  
                  "entity_id":"561",
                  "entity_type_id":"4",
                  "attribute_set_id":"10",
                  "type_id":"downloadable",
                  "sku":"hbm008",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-03-26 02:47:45",
                  "updated_at":"2013-03-27 10:57:11",
                  "price":"2.0000",
                  "tax_class_id":"0",
                  "final_price":"2.0000",
                  "minimal_price":"2.0000",
                  "min_price":"2.0000",
                  "max_price":"2.0000",
                  "tier_price":null,
                  "name":"Love is an Eternal Lie by The Sleeping Tree",
                  "small_image":"\/s\/l\/sleepingtree_.jpg",
                  "thumbnail":"\/s\/l\/sleepingtree_.jpg",
                  "url_key":"love-is-an-eternal-lie-by-the-sleeping-tree",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Music to Accompany the World Traveller.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "links_purchased_separately":"1",
                  "links_exist":"1",
                  "do_not_use_category_id":true,
                  "request_path":"love-is-an-eternal-lie-by-the-sleeping-tree.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/s\/l\/sleepingtree_.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":2
                  }
               },
               {  
                  "entity_id":"560",
                  "entity_type_id":"4",
                  "attribute_set_id":"10",
                  "type_id":"downloadable",
                  "sku":"hbm007",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-03-26 02:37:53",
                  "updated_at":"2013-05-15 01:52:18",
                  "price":"2.0000",
                  "tax_class_id":"0",
                  "final_price":"2.0000",
                  "minimal_price":"2.0000",
                  "min_price":"2.0000",
                  "max_price":"2.0000",
                  "tier_price":null,
                  "name":"Can't Stop It by Shearer",
                  "small_image":"\/s\/h\/shearer__2.jpg",
                  "thumbnail":"\/s\/h\/shearer__2.jpg",
                  "url_key":"can-t-stop-it-by-shearer",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Tunes for the trip.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "links_purchased_separately":"1",
                  "links_exist":"1",
                  "do_not_use_category_id":true,
                  "request_path":"can-t-stop-it-by-shearer.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/s\/h\/shearer__2.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":2
                  }
               },
               {  
                  "entity_id":"559",
                  "entity_type_id":"4",
                  "attribute_set_id":"10",
                  "type_id":"downloadable",
                  "sku":"hbm006",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-03-26 02:21:40",
                  "updated_at":"2013-05-15 01:51:55",
                  "price":"2.0000",
                  "tax_class_id":"0",
                  "final_price":"2.0000",
                  "minimal_price":"2.0000",
                  "min_price":"2.0000",
                  "max_price":"2.0000",
                  "tier_price":null,
                  "name":"If You Were by Keshco",
                  "small_image":"\/k\/e\/keshco_.jpg",
                  "thumbnail":"\/k\/e\/keshco_.jpg",
                  "url_key":"if-you-were-by-keshco",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Tunes for the trip.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "links_purchased_separately":"1",
                  "links_exist":"1",
                  "do_not_use_category_id":true,
                  "request_path":"if-you-were-by-keshco.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/k\/e\/keshco_.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":2
                  }
               },
               {  
                  "entity_id":"558",
                  "entity_type_id":"4",
                  "attribute_set_id":"10",
                  "type_id":"downloadable",
                  "sku":"hbm005",
                  "has_options":"1",
                  "required_options":"0",
                  "created_at":"2013-03-26 02:06:32",
                  "updated_at":"2013-05-15 01:49:42",
                  "price":"2.0000",
                  "tax_class_id":"0",
                  "final_price":"2.0000",
                  "minimal_price":"2.0000",
                  "min_price":"2.0000",
                  "max_price":"2.0000",
                  "tier_price":null,
                  "name":"Falling by I Am Not Lefthanded",
                  "small_image":"\/l\/e\/lefthanded_.jpg",
                  "thumbnail":"\/l\/e\/lefthanded_.jpg",
                  "url_key":"falling-by-i-am-not-lefthanded",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Single off the album Yes Means No.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "links_purchased_separately":"0",
                  "links_exist":"1",
                  "do_not_use_category_id":true,
                  "request_path":"falling-by-i-am-not-lefthanded.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/l\/e\/lefthanded_.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":2
                  }
               },
               {  
                  "entity_id":"557",
                  "entity_type_id":"4",
                  "attribute_set_id":"10",
                  "type_id":"downloadable",
                  "sku":"hbm001",
                  "has_options":"1",
                  "required_options":"1",
                  "created_at":"2013-03-25 23:07:06",
                  "updated_at":"2013-05-15 01:47:02",
                  "price":"5.0000",
                  "tax_class_id":"2",
                  "final_price":"5.0000",
                  "minimal_price":"5.0000",
                  "min_price":"5.0000",
                  "max_price":"5.0000",
                  "tier_price":null,
                  "name":"Around the World in 80 Days",
                  "small_image":"\/8\/0\/80_days_.jpg",
                  "thumbnail":"\/8\/0\/80_days_.jpg",
                  "url_key":"around-the-world-in-80-days",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"A classic adventure novel in which a Londoner and his French valet take a bet to circumnavigate the world in 80 days.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "links_purchased_separately":"1",
                  "links_exist":"1",
                  "do_not_use_category_id":true,
                  "request_path":"around-the-world-in-80-days.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/8\/0\/80_days_.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":5
                  }
               },
               {  
                  "entity_id":"555",
                  "entity_type_id":"4",
                  "attribute_set_id":"17",
                  "type_id":"grouped",
                  "sku":"acj007",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-03-20 01:37:46",
                  "updated_at":"2013-03-20 05:36:21",
                  "price":null,
                  "tax_class_id":"2",
                  "final_price":null,
                  "minimal_price":"110.0000",
                  "min_price":"110.0000",
                  "max_price":"110.0000",
                  "tier_price":null,
                  "name":"Pearl Necklace Set",
                  "small_image":"\/a\/c\/acj007_1_2.jpg",
                  "thumbnail":"\/a\/c\/acj007_1_2.jpg",
                  "url_key":"pearl-necklace-set-test",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "short_description":"Fresh Water Pearl Necklaces",
                  "news_from_date":null,
                  "news_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"pearl-necklace-set-test.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/acj007_1_2.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "price_label":"Starting at:",
                     "show_ex_in_price":0,
                     "price":110
                  }
               },
               {  
                  "entity_id":"554",
                  "entity_type_id":"4",
                  "attribute_set_id":"17",
                  "type_id":"simple",
                  "sku":"acj005",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-03-20 01:32:13",
                  "updated_at":"2013-04-16 13:01:28",
                  "price":"500.0000",
                  "tax_class_id":"2",
                  "final_price":"500.0000",
                  "minimal_price":"500.0000",
                  "min_price":"500.0000",
                  "max_price":"500.0000",
                  "tier_price":null,
                  "name":"Swiss Movement Sports Watch",
                  "small_image":"\/a\/c\/acj005_2.jpg",
                  "thumbnail":"\/a\/c\/acj005_2.jpg",
                  "url_key":"swiss-movement-sports-watch",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"A traditional timepiece with edgy detailing.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"swiss-movement-sports-watch.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/acj005_2.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":500
                  }
               },
               {  
                  "entity_id":"553",
                  "entity_type_id":"4",
                  "attribute_set_id":"17",
                  "type_id":"simple",
                  "sku":"acj000",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-03-20 01:16:45",
                  "updated_at":"2013-03-29 01:42:32",
                  "price":"210.0000",
                  "tax_class_id":"2",
                  "final_price":"210.0000",
                  "minimal_price":"210.0000",
                  "min_price":"210.0000",
                  "max_price":"210.0000",
                  "tier_price":null,
                  "name":"Silver Desert Necklace",
                  "small_image":"\/a\/c\/acj000_2.jpg",
                  "thumbnail":"\/a\/c\/acj000_2.jpg",
                  "url_key":"silver-desert-necklace",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"1",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Wear your passport by adding an edgy and artistic statement necklace. Ethnic design on hand-hammered and chiseled silver.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"silver-desert-necklace.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/c\/acj000_2.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":210
                  }
               }
            ],
            "total":272,
            "page_size":15,
            "from":0,
            "layers":[  

            ]
         }
      },
      {  
         "productlist_id":"1",
         "list_title":"Product List",
         "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/cat6@2x.jpg",
         "list_type":"1",
         "list_products":"372, 379, 382",
         "list_status":"1",
         "sort_order":"1",
         "entity_id":"35",
         "content_type":"4",
         "item_id":"1",
         "store_view_id":"1",
         "width":1170,
         "height":759,
         "type_name":"Custom Product List",
         "product_array":{  
            "all_ids":[  
               "372",
               "382"
            ],
            "products":[  
               {  
                  "entity_id":"372",
                  "entity_type_id":"4",
                  "attribute_set_id":"11",
                  "type_id":"simple",
                  "sku":"abl002",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-03-05 12:48:18",
                  "updated_at":"2013-03-21 00:03:32",
                  "price":"150.0000",
                  "tax_class_id":"2",
                  "final_price":"150.0000",
                  "minimal_price":"150.0000",
                  "min_price":"150.0000",
                  "max_price":"150.0000",
                  "tier_price":null,
                  "name":"Flatiron Tablet Sleeve",
                  "small_image":"\/a\/b\/abl002b_1.jpg",
                  "thumbnail":"\/a\/b\/abl002b_1.jpg",
                  "url_key":"leather-tablet-sleeve",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"Protect your tablet with our minimal tablet sleeve.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"leather-tablet-sleeve.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/b\/abl002b_1.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":150
                  }
               },
               {  
                  "entity_id":"382",
                  "entity_type_id":"4",
                  "attribute_set_id":"16",
                  "type_id":"simple",
                  "sku":"hdb006",
                  "has_options":"0",
                  "required_options":"0",
                  "created_at":"2013-03-05 12:48:19",
                  "updated_at":"2013-03-21 01:18:01",
                  "price":"210.0000",
                  "tax_class_id":"2",
                  "final_price":"210.0000",
                  "minimal_price":"210.0000",
                  "min_price":"210.0000",
                  "max_price":"210.0000",
                  "tier_price":null,
                  "name":"Shay Printed Pillow",
                  "small_image":"\/h\/d\/hdb006_1.jpg",
                  "thumbnail":"\/h\/d\/hdb006_1.jpg",
                  "url_key":"shay-printed-pillow",
                  "image_label":null,
                  "small_image_label":null,
                  "thumbnail_label":null,
                  "msrp_enabled":"2",
                  "msrp_display_actual_price_type":"4",
                  "short_description":"A distinctive printed pillow that fills any room with classic appeal.",
                  "special_price":null,
                  "msrp":null,
                  "news_from_date":null,
                  "news_to_date":null,
                  "special_from_date":null,
                  "special_to_date":null,
                  "status":"1",
                  "do_not_use_category_id":true,
                  "request_path":"shay-printed-pillow.html",
                  "is_salable":"1",
                  "stock_item":{  
                     "is_in_stock":"1"
                  },
                  "images":[  
                     {  
                        "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/h\/d\/hdb006_1.jpg",
                        "position":1
                     }
                  ],
                  "app_price":{  
                     "has_special_price":0,
                     "show_ex_in_price":0,
                     "price":210
                  }
               }
            ],
            "total":2,
            "page_size":15,
            "from":0,
            "layers":[  

            ]
         }
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

Return Home Product lists

### HTTP Request

`GET simiconnector/rest/v2/homes/default`


## View Detail Of a Product List

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homeproductlists/3" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "homeproductlist":{  
      "productlist_id":"1",
      "list_title":"Product List",
      "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/cat6@2x.jpg",
      "list_type":"1",
      "list_products":"372, 379, 382",
      "list_status":"1",
      "sort_order":"1",
      "width":1170,
      "height":759,
      "type_name":"Custom Product List",
      "product_array":{  
         "all_ids":[  
            "372",
            "382"
         ],
         "":[  
            {  
               "entity_id":"372",
               "entity_type_id":"4",
               "attribute_set_id":"11",
               "type_id":"simple",
               "sku":"abl002",
               "has_options":"0",
               "required_options":"0",
               "created_at":"2013-03-05 12:48:18",
               "updated_at":"2013-03-21 00:03:32",
               "price":"150.0000",
               "tax_class_id":"2",
               "final_price":"150.0000",
               "minimal_price":"150.0000",
               "min_price":"150.0000",
               "max_price":"150.0000",
               "tier_price":null,
               "name":"Flatiron Tablet Sleeve",
               "small_image":"\/a\/b\/abl002b_1.jpg",
               "thumbnail":"\/a\/b\/abl002b_1.jpg",
               "url_key":"leather-tablet-sleeve",
               "image_label":null,
               "small_image_label":null,
               "thumbnail_label":null,
               "msrp_enabled":"2",
               "msrp_display_actual_price_type":"4",
               "short_description":"Protect your tablet with our minimal tablet sleeve.",
               "special_price":null,
               "msrp":null,
               "news_from_date":null,
               "news_to_date":null,
               "special_from_date":null,
               "special_to_date":null,
               "status":"1",
               "do_not_use_category_id":true,
               "request_path":"leather-tablet-sleeve.html",
               "is_salable":"1",
               "stock_item":{  
                  "is_in_stock":"1"
               },
               "images":[  
                  {  
                     "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/a\/b\/abl002b_1.jpg",
                     "position":1
                  }
               ],
               "app_price":{  
                  "has_special_price":0,
                  "show_ex_in_price":0,
                  "price":150
               }
            },
            {  
               "entity_id":"382",
               "entity_type_id":"4",
               "attribute_set_id":"16",
               "type_id":"simple",
               "sku":"hdb006",
               "has_options":"0",
               "required_options":"0",
               "created_at":"2013-03-05 12:48:19",
               "updated_at":"2013-03-21 01:18:01",
               "price":"210.0000",
               "tax_class_id":"2",
               "final_price":"210.0000",
               "minimal_price":"210.0000",
               "min_price":"210.0000",
               "max_price":"210.0000",
               "tier_price":null,
               "name":"Shay Printed Pillow",
               "small_image":"\/h\/d\/hdb006_1.jpg",
               "thumbnail":"\/h\/d\/hdb006_1.jpg",
               "url_key":"shay-printed-pillow",
               "image_label":null,
               "small_image_label":null,
               "thumbnail_label":null,
               "msrp_enabled":"2",
               "msrp_display_actual_price_type":"4",
               "short_description":"A distinctive printed pillow that fills any room with classic appeal.",
               "special_price":null,
               "msrp":null,
               "news_from_date":null,
               "news_to_date":null,
               "special_from_date":null,
               "special_to_date":null,
               "status":"1",
               "do_not_use_category_id":true,
               "request_path":"shay-printed-pillow.html",
               "is_salable":"1",
               "stock_item":{  
                  "is_in_stock":"1"
               },
               "images":[  
                  {  
                     "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/h\/d\/hdb006_1.jpg",
                     "position":1
                  }
               ],
               "app_price":{  
                  "has_special_price":0,
                  "show_ex_in_price":0,
                  "price":210
               }
            }
         ],
         "total":2,
         "page_size":15,
         "from":0,
         "layers":[  

         ]
      }
   }
}
```

This API returns Product Lists with detailed list.
