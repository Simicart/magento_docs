# Home Product Lists

## Home Product List Properties

Attributes| Type| Description
--------- | ------- | -----------
productlist_id | id | Product List Id
list_title | string | Product list Title
list_image | string | Product list Image URL
list_status | int | Product list Status
list_products | array | Products of this List


## View A Default Home Screen

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homeproductlists" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "5",
      "1",
      "2",
      "3",
      "4"
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
         "height":null
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
         "height":759
      },
      {  
         "productlist_id":"2",
         "list_title":"Best seller",
         "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/cat5@2x.jpg",
         "list_type":"2",
         "list_products":"338",
         "list_status":"1",
         "sort_order":"2",
         "entity_id":"38",
         "content_type":"4",
         "item_id":"2",
         "store_view_id":"1",
         "width":1170,
         "height":759
      },
      {  
         "productlist_id":"3",
         "list_title":"Most Viewed",
         "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/cat3@2x.png",
         "list_type":"3",
         "list_products":"379, 374, 371, 378, 375, 373, 372, 370, 339, 338, 337, 380, 381, 382, 383, 384, 385",
         "list_status":"1",
         "sort_order":"3",
         "entity_id":"41",
         "content_type":"4",
         "item_id":"3",
         "store_view_id":"1",
         "width":1434,
         "height":711
      },
      {  
         "productlist_id":"4",
         "list_title":"Newly Updated",
         "list_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/productlist\/cat3@2x.png",
         "list_type":"4",
         "list_products":null,
         "list_status":"1",
         "sort_order":"3",
         "entity_id":"44",
         "content_type":"4",
         "item_id":"4",
         "store_view_id":"1",
         "width":1434,
         "height":711
      }
   ],
   "total":5,
   "page_size":15,
   "from":0
}
```

Return Home Product lists

### HTTP Request

`GET simiconnector/rest/v2/homes/default`


## View list products and Details of a Product List

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
