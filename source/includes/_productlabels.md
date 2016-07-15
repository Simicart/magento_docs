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

