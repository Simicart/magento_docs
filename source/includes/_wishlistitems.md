# Wishlist

## Wishlist Item Properties

Attributes| Type| Description
--------- | ------- | -----------
wishlist_item_id | id | Item Id
wishlist_id | id | Wishlist Id
product_id | id | Product Id
name | string | Item Name
price | float | Item Price
qty | int | Item Qty
product_sku | string | Product SKU
product_sharing_message | string | Product Sharing Message
product_sharing_url | string | Product Sharing URL
product_image | string | Item Image
selected_all_required_options  | boolean | Item is available to be Added To Cart


## Add to Wishlist

```shell
curl POST "https://abc.com/simiconnector/rest/v2/wishlistitems " \
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
   "wishlistitem":{  
      "wishlist_item_id":"160",
      "wishlist_id":"63",
      "product_id":"406",
      "store_id":"1",
      "added_at":"2016-06-24 07:48:19",
      "description":null,
      "qty":5,
      "product":{  },
      "product_name":"Linen Blazer",
      "name":"Linen Blazer",
      "price":"455.0000",
      "wishlist":{  

      }
   }
}
```

This request is to Add product To Wishlist

Parameters are the same with Adding Products To Cart

## Get Wishlist Items

```shell
curl GET "https://abc.com/simiconnector/rest/v2/wishlistitems " \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "161"
   ],
   "wishlistitems":[  
      {  
         "wishlist_item_id":"161",
         "wishlist_id":"63",
         "product_id":"406",
         "store_id":"1",
         "added_at":"2016-06-24 08:05:36",
         "description":null,
         "qty":"5.0000",
         "product":{  

         },
         "product_name":"Linen Blazer",
         "name":"Linen Blazer",
         "price":"455.0000",
         "product_type":"configurable",
         "product_regular_price":455,
         "product_price":455,
         "stock_status":true,
         "product_image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/040ec09b1e35df139433887a97daa66f\/m\/s\/msj012t_2.jpg",
         "is_show_price":true,
         "options":[  
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
         "selected_all_required_options":true,
         "product_sharing_message":" http:\/\/localhost.com\/magento19\/linen-blazer-585.html",
         "product_sharing_url":"http:\/\/localhost.com\/magento19\/linen-blazer-585.html"
      }
   ],
   "total":{  
      "subtotal_excl_tax":3235,
      "subtotal_incl_tax":3235,
      "tax":0,
      "discount":35.59,
      "grand_total_excl_tax":3199.41,
      "grand_total_incl_tax":3199.41
   },
   "page_size":15,
   "from":0,
   "message":[  
      " http:\/\/localhost.com\/magento19\/wishlist\/shared\/index\/code\/c5e33effa6ce62930592e8de3b46e166\/"
   ]
}
```

This request is to get Wishlist Items


## Wishlist Item Id on Product Detail

```shell
curl GET "https://abc.com/simiconnector/rest/v2/products/392" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"392",
      "entity_type_id":"4",
      "attribute_set_id":"14",
      "type_id":"simple",
      "sku":"hde001",
      "images":[  
         {  
            "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/thumbnail\/600x600\/040ec09b1e35df139433887a97daa66f\/h\/d\/hde001a.jpg",
            "position":"2"
         },
         {  
            "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/thumbnail\/600x600\/040ec09b1e35df139433887a97daa66f\/h\/d\/hde001b.jpg",
            "position":"3"
         },
         {  
            "url":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/thumbnail\/600x600\/040ec09b1e35df139433887a97daa66f\/h\/d\/hde001t_2.jpg",
            "position":"4"
         }
      ],
      "app_prices":{  
         "has_special_price":0,
         "show_ex_in_price":0,
         "price":425
      },
      "app_options":{  
         "custom_options":[  

         ]
      },
      "wishlist_item_id":"162"
   }
}
```

If on product is already on Wishlist, there would be wishlist_item_id value, if not, it's NULL.


## Remove Wishlist Item

```shell
curl DELETE "https://abc.com/simiconnector/rest/v2/wishlistitems/161" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "162"
   ],
   "wishlistitems":[  
      {  
         "wishlist_item_id":"162",
         "wishlist_id":"63",
         "product_id":"392",
         "store_id":"1",
         "added_at":"2016-06-24 08:10:20",
         "description":null,
         "qty":"1.0000",
         "product":{  

         },
         "product_name":"Madison LX2200",
         "name":"Madison LX2200",
         "price":"425.0000",
         "product_type":"simple",
         "product_regular_price":425,
         "product_price":425,
         "stock_status":true,
         "product_image":"http:\/\/localhost.com\/magento19\/media\/catalog\/product\/cache\/1\/small_image\/040ec09b1e35df139433887a97daa66f\/h\/d\/hde001t_2.jpg",
         "is_show_price":true,
         "options":[  

         ],
         "selected_all_required_options":true,
         "product_sharing_message":" http:\/\/localhost.com\/magento19\/madison-lx2200.html",
         "product_sharing_url":"http:\/\/localhost.com\/magento19\/madison-lx2200.html"
      }
   ],
   "total":{  
      "subtotal_excl_tax":3235,
      "subtotal_incl_tax":3235,
      "tax":0,
      "discount":35.59,
      "grand_total_excl_tax":3199.41,
      "grand_total_incl_tax":3199.41
   },
   "page_size":15,
   "from":0,
   "message":[  
      " http:\/\/localhost.com\/magento19\/wishlist\/shared\/index\/code\/c5e33effa6ce62930592e8de3b46e166\/"
   ]
}
```

This request is to remove product from wishlist

## Add Product From Wishlist To Cart

```shell
curl GET "https://abc.com/simiconnector/rest/v2/wishlistitems/164?add_to_cart=1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  

   ],
   "wishlistitems":[  

   ],
   "total":0,
   "page_size":15,
   "from":0,
   "message":[  
      " http:\/\/localhost.com\/magento19\/wishlist\/shared\/index\/code\/c5e33effa6ce62930592e8de3b46e166\/"
   ]
}
```

This request is to add Wishlist Item To Cart, after that the Item would be removed from wishlist, then the result is Wishlist Items List.




