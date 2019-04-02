# Product on Magento 2

## Product Price Properties

Attributes| Type| Description
--------- | ------- | -----------
entity_id | string | product id <code>read only</code>
entity_type_id | int | type id of product
attribute_set_id | string | product attribute set
type_id | int | type of product ( simple, grouped, bundle, downloadable)
sku | string | stock keeping unit
name | string | product name
created_at | datetime | created time
updated_at | datetime | updated time
has_options | string | "0" or "1" has options?
required_options| string | "0" or "1" is required options when do add cart
cat_index_position| string | position of session cart
price | string | original price of product
tax_class_id | string | tax_id of product
final_price | string | sale price of product
description | string | product description
short_description | string | product short description
images | JSON Array | list images of product
is_salable | string | product is salable

## View Simple Product

```shell
curl "https://abc.com/simiconnector/rest/v2/products/1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"1",
      "attribute_set_id":"15",
      "type_id":"simple",
      "sku":"24-MB01",
      "has_options":"0",
      "required_options":"0",
      "created_at":"2016-08-24 04:56:36",
      "updated_at":"2016-08-24 04:56:36",
      "name":"Joust Duffle Bag",
      "image":"\/m\/b\/mb01-blue-0.jpg",
      "small_image":"\/m\/b\/mb01-blue-0.jpg",
      "thumbnail":"\/m\/b\/mb01-blue-0.jpg",
      "url_key":"joust-duffle-bag",
      "description":"<p>The sporty Joust Duffle Bag can't be beat - not in the gym, not on the luggage carousel, not anywhere. Big enough to haul a basketball or soccer ball and some sneakers with plenty of room to spare, it's ideal for athletes with places to go.<p>\n<ul>\n<li>Dual top handles.<\/li>\n<li>Adjustable shoulder strap.<\/li>\n<li>Full-length zipper.<\/li>\n<li>L 29\" x W 13\" x H 11\".<\/li>\n<\/ul>",
      "price":"34.0000",
      "status":"1",
      "visibility":"4",
      "options":[  

      ],
      "media_gallery":{  
         "images":{  
            "1":{  
               "value_id":"1",
               "file":"\/m\/b\/mb01-blue-0.jpg",
               "media_type":"image",
               "entity_id":"1",
               "label":"Image",
               "position":"1",
               "disabled":"0",
               "label_default":"Image",
               "position_default":"1",
               "disabled_default":"0"
            }
         }
      },
      "category_ids":[  
         "3",
         "4"
      ],
      "quantity_and_stock_status":{  
         "is_in_stock":true,
         "qty":null
      },
      "tier_price":[  

      ],
      "tier_price_changed":0,
      "is_salable":"1",
      "extension_attributes":{  

      },
      "additional":[  

      ],
      "images":[  
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/m\/b\/mb01-blue-0.jpg",
            "position":"1"
         }
      ],
      "app_prices":{  
         "has_special_price":0,
         "show_ex_in_price":1,
         "price_excluding_tax":{  
            "label":"Excl. Tax",
            "price":34
         },
         "price_including_tax":{  
            "label":"Incl. Tax",
            "price":34
         }
      },
      "app_options":{  
         "custom_options":[  

         ]
      },
      "app_reviews":{  
         "rate":2.5,
         "number":2
      }
   }
}
```

It's the same with 1.x version:

-- 1. If has_special_price = 0, then there is no special price. If price_excluding_tax and price_including_tax returned, use storeview config to decide to show include tax / excluded tax or both.

Sample API with tax (price_excluding_tax and price_including_tax);

"app_prices":{  
      "has_special_price":0,
      "show_ex_in_price":1,
      "price_excluding_tax":{  
         "label":"Excl. Tax",
         "price":34
      },
      "price_including_tax":{  
         "label":"Incl. Tax",
         "price":34
      }
}

-- 2. If has_special_price = 1, then there is special price. If price_excluding_tax and price_including_tax returned, use storeview config to decide to show include tax / excluded tax or both and add the special price with value from price and label from special_price_label.

Sample API:

"app_prices": {

      "has_special_price": 1,

      "price_label": "Normalpreis",

      "regular_price": 35,

      "show_ex_in_price": 0,

      "special_price_label": "Special Price",

      "price": 29.97
}

-- 3. If is_low_price = 1, then ONLY show label from low_price_label with value from low_price

Sample API:

"app_prices": {

      "has_special_price": 1,

      "price_label": "Regular Price",

      "regular_price": 45,

      "show_ex_in_price": 0,

      "special_price_label": "Special Price",

      "price": 22,

      "is_low_price": 1,

      "low_price_label": "As low as",

      "low_price": 22
}

## View Configurable Product

```shell
curl "https://abc.com/simiconnector/rest/v2/products/1859" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"1859",
      "app_prices":{  
         "has_special_price":1,
         "price_label":"Regular Price",
         "regular_price":63.87,
         "show_ex_in_price":1,
         "special_price_label":"Special Price",
         "price_excluding_tax":{  
            "label":"Excl. Tax",
            "price":51.09
         },
         "price_including_tax":{  
            "label":"Incl. Tax",
            "price":55.3
         }
      },
      "app_options":{  
         "configurable_options":{  
            "attributes":{  
               "93":{  
                  "id":"93",
                  "code":"color",
                  "label":"Color",
                  "options":[  
                     {  
                        "id":"49",
                        "label":"Black",
                        "products":[  
                           "1853",
                           "1856"
                        ]
                     },
                     {  
                        "id":"50",
                        "label":"Blue",
                        "products":[  
                           "1854",
                           "1857"
                        ]
                     },
                     {  
                        "id":"56",
                        "label":"Orange",
                        "products":[  
                           "1855",
                           "1858"
                        ]
                     }
                  ],
                  "position":"0"
               },
               "142":{  
                  "id":"142",
                  "code":"size",
                  "label":"Size",
                  "options":[  
                     {  
                        "id":"172",
                        "label":"28",
                        "products":[  
                           "1853",
                           "1854",
                           "1855"
                        ]
                     },
                     {  
                        "id":"173",
                        "label":"29",
                        "products":[  
                           "1856",
                           "1857",
                           "1858"
                        ]
                     }
                  ],
                  "position":"1"
               }
            },
            "template":"$<%- data.price %>",
            "optionPrices":{  
               "1853":{  
                  "oldPrice":{  
                     "amount":"63.867501"
                  },
                  "basePrice":{  
                     "amount":"47.2"
                  },
                  "finalPrice":{  
                     "amount":"51.094001"
                  }
               },
               "1856":{  
                  "oldPrice":{  
                     "amount":"66.032501"
                  },
                  "basePrice":{  
                     "amount":"48.8"
                  },
                  "finalPrice":{  
                     "amount":"52.826001"
                  }
               },
               "1854":{  
                  "oldPrice":{  
                     "amount":"68.197501"
                  },
                  "basePrice":{  
                     "amount":"50.4"
                  },
                  "finalPrice":{  
                     "amount":"54.558001"
                  }
               },
               "1857":{  
                  "oldPrice":{  
                     "amount":"70.362501"
                  },
                  "basePrice":{  
                     "amount":"52"
                  },
                  "finalPrice":{  
                     "amount":"56.290001"
                  }
               },
               "1855":{  
                  "oldPrice":{  
                     "amount":"72.527501"
                  },
                  "basePrice":{  
                     "amount":"53.6"
                  },
                  "finalPrice":{  
                     "amount":"58.022001"
                  }
               },
               "1858":{  
                  "oldPrice":{  
                     "amount":"86.600001"
                  },
                  "basePrice":{  
                     "amount":"64"
                  },
                  "finalPrice":{  
                     "amount":"69.280001"
                  }
               }
            },
            "prices":{  
               "oldPrice":{  
                  "amount":"63.867501"
               },
               "basePrice":{  
                  "amount":"47.2"
               },
               "finalPrice":{  
                  "amount":"51.094001"
               }
            },
            "productId":"1859",
            "chooseText":"Choose an Option...",
            "images":{  
               "1853":[  
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_alt1.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_alt1.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_alt1.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  },
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_main.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_main.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_main.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  },
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_back.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_back.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_back.jpg",
                     "caption":"",
                     "position":"2",
                     "isMain":false
                  },
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_outfit.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_outfit.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_outfit.jpg",
                     "caption":"",
                     "position":"3",
                     "isMain":false
                  }
               ],
               "1856":[  
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_alt1.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_alt1.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_alt1.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  },
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_main.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_main.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_main.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  },
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_back.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_back.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_back.jpg",
                     "caption":"",
                     "position":"2",
                     "isMain":false
                  },
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_outfit.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_outfit.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-black_outfit.jpg",
                     "caption":"",
                     "position":"3",
                     "isMain":false
                  }
               ],
               "1854":[  
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-blue_main.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-blue_main.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-blue_main.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  }
               ],
               "1857":[  
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-blue_main.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-blue_main.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-blue_main.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  }
               ],
               "1855":[  
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-orange_main.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-orange_main.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-orange_main.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  }
               ],
               "1858":[  
                  {  
                     "thumb":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/thumbnail\/88x110\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-orange_main.jpg",
                     "img":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/700x560\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-orange_main.jpg",
                     "full":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/e9c3970ab036de70892d86c6d221abfe\/w\/p\/wp06-orange_main.jpg",
                     "caption":"",
                     "position":"1",
                     "isMain":false
                  }
               ]
            },
            "index":{  
               "1853":{  
                  "93":"49",
                  "142":"172"
               },
               "1856":{  
                  "93":"49",
                  "142":"173"
               },
               "1854":{  
                  "93":"50",
                  "142":"172"
               },
               "1857":{  
                  "93":"50",
                  "142":"173"
               },
               "1855":{  
                  "93":"56",
                  "142":"172"
               },
               "1858":{  
                  "93":"56",
                  "142":"173"
               }
            }
         },
         "custom_options":[  
            {  
               "id":"4",
               "title":"Sample Option Hainh",
               "type":"multiple",
               "position":"1",
               "isRequired":"1",
               "values":[  
                  {  
                     "id":"10",
                     "title":"Test Option 1",
                     "price_excluding_tax":{  
                        "label":"Excl. Tax",
                        "price":10
                     },
                     "price_including_tax":{  
                        "label":"Incl. Tax",
                        "price":10.83
                     }
                  },
                  {  
                     "id":"11",
                     "title":"Test Option 2",
                     "price_excluding_tax":{  
                        "label":"Excl. Tax",
                        "price":20
                     },
                     "price_including_tax":{  
                        "label":"Incl. Tax",
                        "price":21.65
                     }
                  },
                  {  
                     "id":"12",
                     "title":"Test Option 3",
                     "price_excluding_tax":{  
                        "label":"Excl. Tax",
                        "price":30
                     },
                     "price_including_tax":{  
                        "label":"Incl. Tax",
                        "price":32.48
                     }
                  }
               ]
            }
         ]
      },
      "app_reviews":{  
         "rate":3.3333333333333,
         "number":3
      }
   }
}
```
Before customer selected ALL configurable options, show the price displayed on product.app_prices plus Selected custom option prices, like a normal simple product.

For configurable product, for each bunch of selectable options, a simple product would be created, each Simple products created by configurable options mapped on "app_options.index"

From the Simple product Id got from index array, get the configurable price from "app_options.optionPrices" with value below: 

1. oldPrice.amount: Regular price with NO discount and NO tax.

2. basePrice.amount: Price with discount APPLIED (special price) and NO tax included

3. finalPrice.amount: Price with discount APPLIED and Tax INCLUDED

After get the price with configurable options, plus the value of custom_options. For example with the product above, price for 1858 ("93":"56","142":"173") and "Test Option 1" for "Sample Option Hainh" is:

- Regular Price: 86.600001 + 10 = 96.600001

- Excl tax: 64 + 10 = 74

- Incl tax: 69.280001 + 10.83 = 80.11

Images for each Configurable Options are listed under "app_options.images"


## View Bundle Product

```shell
curl "https://abc.com/simiconnector/rest/v2/products/51" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"51",
      "app_prices":{  
         "minimal_price": 0,
         "product_from_label": "From",
         "product_to_label": "To",
         "show_from_to_tax_price": 1,
         "show_ex_in_price": 0,
         "from_price": 56.2,
         "to_price": 72.2,
         "configure": {
            "product_label": "Price as configured"
         }
      },
      "app_options":{  
         "bundle_options":{  
            "options":{  
               "1":{  
                  "selections":{  
                     "1":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"26",
                        "prices":{  
                           "oldPrice":{  
                              "amount":23
                           },
                           "basePrice":{  
                              "amount":23
                           },
                           "finalPrice":{  
                              "amount":24.897501
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Stasis Ball 55 cm",
                        "canApplyMsrp":false
                     },
                     "2":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"29",
                        "prices":{  
                           "oldPrice":{  
                              "amount":27
                           },
                           "basePrice":{  
                              "amount":27
                           },
                           "finalPrice":{  
                              "amount":29.227501
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Stasis Ball 65 cm",
                        "canApplyMsrp":false
                     },
                     "3":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"32",
                        "prices":{  
                           "oldPrice":{  
                              "amount":32
                           },
                           "basePrice":{  
                              "amount":32
                           },
                           "finalPrice":{  
                              "amount":34.640001
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Stasis Ball 75 cm",
                        "canApplyMsrp":false
                     }
                  },
                  "title":"Sprite Stasis Ball",
                  "isMulti":false,
                  "position":0
               },
               "2":{  
                  "selections":{  
                     "4":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"21",
                        "prices":{  
                           "oldPrice":{  
                              "amount":5
                           },
                           "basePrice":{  
                              "amount":5
                           },
                           "finalPrice":{  
                              "amount":5.412501
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Foam Yoga Brick",
                        "canApplyMsrp":false
                     }
                  },
                  "title":"Sprite Foam Yoga Brick",
                  "isMulti":false,
                  "position":1
               },
               "3":{  
                  "selections":{  
                     "5":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"33",
                        "prices":{  
                           "oldPrice":{  
                              "amount":14
                           },
                           "basePrice":{  
                              "amount":14
                           },
                           "finalPrice":{  
                              "amount":15.155001
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Yoga Strap 6 foot",
                        "canApplyMsrp":false
                     },
                     "6":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"34",
                        "prices":{  
                           "oldPrice":{  
                              "amount":17
                           },
                           "basePrice":{  
                              "amount":17
                           },
                           "finalPrice":{  
                              "amount":18.402501
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Yoga Strap 8 foot",
                        "canApplyMsrp":false
                     },
                     "7":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"35",
                        "prices":{  
                           "oldPrice":{  
                              "amount":21
                           },
                           "basePrice":{  
                              "amount":21
                           },
                           "finalPrice":{  
                              "amount":22.732501
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Yoga Strap 10 foot",
                        "canApplyMsrp":false
                     }
                  },
                  "title":"Sprite Yoga Strap",
                  "isMulti":false,
                  "position":2
               },
               "4":{  
                  "selections":{  
                     "8":{  
                        "qty":1,
                        "customQty":"1",
                        "optionId":"22",
                        "prices":{  
                           "oldPrice":{  
                              "amount":19
                           },
                           "basePrice":{  
                              "amount":19
                           },
                           "finalPrice":{  
                              "amount":20.567501
                           }
                        },
                        "priceType":"0",
                        "tierPrice":[  

                        ],
                        "name":"Sprite Foam Roller",
                        "canApplyMsrp":false
                     }
                  },
                  "title":"Sprite Foam Roller",
                  "isMulti":false,
                  "position":3
               }
            },
            "selected":{  
               "1":[  
                  "1"
               ],
               "2":[  
                  "4"
               ],
               "3":[  
                  "5"
               ],
               "4":[  
                  "8"
               ]
            },
            "bundleId":"51",
            "priceFormat":{  
               "pattern":"$%s",
               "precision":2,
               "requiredPrecision":2,
               "decimalSymbol":".",
               "groupSymbol":",",
               "groupLength":3,
               "integerRequired":1
            },
            "prices":{  
               "oldPrice":{  
                  "amount":0
               },
               "basePrice":{  
                  "amount":0
               },
               "finalPrice":{  
                  "amount":0
               }
            },
            "priceType":"0",
            "isFixedPrice":false
         }
      },
      "app_reviews":{  
         "rate":0,
         "number":0
      }
   }
}
```

Similar with 1.x version, under app_options.bundle_options.

Price values for each options are oldPrice (no discount, excluded tax), basePrice (applied discount, excluded tax), finalPrice (applied discount, tax included).

For pricing display before selecting options:

-- 1. If show_from_to_tax_price = 1, show 'from price' and 'to price' with value from from_price and to_price with label from product_from_label and product_to_label

Example API

"app_prices": {
   "minimal_price": 0,
   "product_from_label": "From",
   "product_to_label": "To",
   "show_from_to_tax_price": 1,
   "show_ex_in_price": 0,
   "from_price": 56.2,
   "to_price": 72.2,
   "configure": {
      "product_label": "Price as configured"
   }
}

-- 2. If show_from_to_tax_price = 1, which mean the from and to price is the same, use price from key 'price' for value. If minimal_price = 1, add the label from price_label

Example API

"app_prices": {
   "minimal_price": 0,
   "show_from_to_tax_price": 0,
   "price": 56.2,
   "configure": {
      "product_label": "Price as configured"
   }
}


"app_prices": {
   "price_label": "As low as",
   "minimal_price": 1,
   "show_ex_in_price": 0,
   "price": 56.2,
   "configure": {
      "product_label": "Price as configured"
   }
}

-- 3. With from_price_excluding_tax, from_price_including_tax, to_price_excluding_tax, to_price_including_tax included in the API, use the configuration from storeview to show the price.

Sample API:

"app_prices": {
   "minimal_price": 0,
   "product_from_label": "From",
   "product_to_label": "To",
   "show_from_to_tax_price": 1,
   "show_ex_in_price": 1,
   "from_price_excluding_tax": {
      "label": "Excl. Tax",
      "price": 56.2
   },
   "from_price_including_tax": {
      "label": "Incl. Tax",
      "price": 56.2
   },
   "to_price_excluding_tax": {
      "label": "Excl. Tax",
      "price": 72.2
   },
   "to_price_including_tax": {
      "label": "Incl. Tax",
      "price": 72.2
   },
   "configure": {
      "product_label": "Price as configured"
   }
}

## View Grouped Product

```shell
curl "https://abc.com/simiconnector/rest/v2/products/2046" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"2046",
      "attribute_set_id":"11",
      "type_id":"grouped",
      "sku":"24-WG085_Group",
      "has_options":"0",
      "required_options":"0",
      "created_at":"2016-08-24 04:58:56",
      "updated_at":"2016-08-24 04:58:56",
      "name":"Set of Sprite Yoga Straps",
      "image":"\/l\/u\/luma-yoga-strap-set.jpg",
      "small_image":"\/l\/u\/luma-yoga-strap-set.jpg",
      "thumbnail":"\/l\/u\/luma-yoga-strap-set.jpg",
      "options_container":"container2",
      "url_key":"set-of-sprite-yoga-straps",
      "activity":"8",
      "material":"32,44",
      "gender":"80,81,84",
      "category_gear":"87",
      "description":"<p>Great set of Sprite Yoga Straps for every stretch and hold you need. There are three straps in this set: 6', 8' and 10'.<\/p>\n<ul>\n<li> 100% soft and durable cotton.\n<li> Plastic cinch buckle is easy to use.\n<li> Choice of three natural colors made from phthalate and heavy metal free dyes.\n<\/ul>",
      "status":"1",
      "visibility":"4",
      "quantity_and_stock_status":{  
         "is_in_stock":true,
         "qty":0
      },
      "options":[  

      ],
      "media_gallery":{  
         "images":{  
            "3422":{  
               "value_id":"3422",
               "file":"\/l\/u\/luma-yoga-strap-set.jpg",
               "media_type":"image",
               "entity_id":"2046",
               "label":"Image",
               "position":"1",
               "disabled":"0",
               "label_default":"Image",
               "position_default":"1",
               "disabled_default":"0"
            }
         }
      },
      "category_ids":[  
         "3",
         "5"
      ],
      "is_salable":"1",
      "extension_attributes":{  

      },
      "additional":{  
         "activity":{  
            "label":"Activity",
            "value":"Yoga",
            "code":"activity"
         },
         "material":{  
            "label":"Material",
            "value":"Canvas, Plastic",
            "code":"material"
         },
         "gender":{  
            "label":"Gender",
            "value":"Men, Women, Unisex",
            "code":"gender"
         },
         "category_gear":{  
            "label":"Category",
            "value":"Exercise",
            "code":"category_gear"
         }
      },
      "images":[  
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/l\/u\/luma-yoga-strap-set.jpg",
            "position":"1"
         }
      ],
      "app_prices":[  

      ],
      "app_options":{  
         "grouped_options":[  
            {  
               "id":"33",
               "name":"Sprite Yoga Strap 6 foot",
               "is_salable":"1",
               "has_special_price":0,
               "show_ex_in_price":1,
               "price_excluding_tax":{  
                  "label":"Excl. Tax",
                  "price":14
               },
               "price_including_tax":{  
                  "label":"Incl. Tax",
                  "price":14
               }
            },
            {  
               "id":"34",
               "name":"Sprite Yoga Strap 8 foot",
               "is_salable":"1",
               "has_special_price":0,
               "show_ex_in_price":1,
               "price_excluding_tax":{  
                  "label":"Excl. Tax",
                  "price":17
               },
               "price_including_tax":{  
                  "label":"Incl. Tax",
                  "price":17
               }
            },
            {  
               "id":"35",
               "name":"Sprite Yoga Strap 10 foot",
               "is_salable":"1",
               "has_special_price":0,
               "show_ex_in_price":1,
               "price_excluding_tax":{  
                  "label":"Excl. Tax",
                  "price":21
               },
               "price_including_tax":{  
                  "label":"Incl. Tax",
                  "price":21
               }
            }
         ]
      },
      "app_reviews":{  
         "rate":0,
         "number":0
      }
   }
}
```
Same with Simple product.

For option prices, each group product item has it own pricing values and configurations, there is 2 cases: show both included and excluded tax or just show one, with each case, there would be special price or not.

