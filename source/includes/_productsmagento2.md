# Product Price on Magento 2

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

It's the same with 1.x version

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
      "attribute_set_id":"10",
      "type_id":"configurable",
      "sku":"WP06",
      "has_options":"1",
      "required_options":"1",
      "created_at":"2016-08-24 04:58:18",
      "updated_at":"2016-09-12 03:51:52",
      "name":"Diana Tights",
      "image":"\/w\/p\/wp06-black_main.jpg",
      "small_image":"\/w\/p\/wp06-black_main.jpg",
      "thumbnail":"\/w\/p\/wp06-black_main.jpg",
      "options_container":"container2",
      "url_key":"diana-tights",
      "msrp_display_actual_price_type":"0",
      "gift_message_available":"2",
      "material":"150,38,151",
      "style_bottom":"107,109",
      "pattern":"197",
      "climate":"202,204,205,206,208,209",
      "description":"<p>Perfect for hot bikram session or cool-down stretching. 8-percent stretch means you'll feel like anything is possible in the capri-style Diana Tights.<\/p>\r\n<p>&bull; Black legging with slate details.<br \/>&bull; Flat-lock, chafe-free side seams.<br \/>&bull; Vented gusset.<br \/>&bull; Secret interior pocket.<br \/>&bull; Sustainable and recycled fabric.<\/p>",
      "price":"59.0000",
      "status":"1",
      "visibility":"4",
      "quantity_and_stock_status":{  
         "is_in_stock":true,
         "qty":0
      },
      "tax_class_id":"2",
      "eco_collection":"0",
      "performance_fabric":"0",
      "erin_recommends":"1",
      "new":"0",
      "sale":"0",
      "options":[  
         {  

         }
      ],
      "media_gallery":{  
         "images":{  
            "3115":{  
               "value_id":"3115",
               "file":"\/w\/p\/wp06-black_alt1.jpg",
               "media_type":"image",
               "entity_id":"1859",
               "label":"",
               "position":"1",
               "disabled":"0",
               "label_default":null,
               "position_default":"1",
               "disabled_default":"0"
            },
            "3118":{  
               "value_id":"3118",
               "file":"\/w\/p\/wp06-black_main.jpg",
               "media_type":"image",
               "entity_id":"1859",
               "label":"",
               "position":"1",
               "disabled":"0",
               "label_default":null,
               "position_default":"1",
               "disabled_default":"0"
            },
            "3116":{  
               "value_id":"3116",
               "file":"\/w\/p\/wp06-black_back.jpg",
               "media_type":"image",
               "entity_id":"1859",
               "label":"",
               "position":"2",
               "disabled":"0",
               "label_default":null,
               "position_default":"2",
               "disabled_default":"0"
            },
            "3117":{  
               "value_id":"3117",
               "file":"\/w\/p\/wp06-black_outfit.jpg",
               "media_type":"image",
               "entity_id":"1859",
               "label":"",
               "position":"3",
               "disabled":"0",
               "label_default":null,
               "position_default":"3",
               "disabled_default":"0"
            }
         }
      },
      "extension_attributes":{  

      },
      "category_ids":[  
         "27",
         "32",
         "34",
         "2"
      ],
      "tier_price":[  

      ],
      "tier_price_changed":0,
      "is_salable":"1",
      "additional":{  
         "style_bottom":{  
            "label":"Style",
            "value":"Capri, Leggings",
            "code":"style_bottom"
         },
         "material":{  
            "label":"Material",
            "value":"Microfiber, Polyester, Spandex",
            "code":"material"
         },
         "pattern":{  
            "label":"Pattern",
            "value":"Solid",
            "code":"pattern"
         },
         "climate":{  
            "label":"Climate",
            "value":"All-Weather, Cool, Indoor, Mild, Spring, Warm",
            "code":"climate"
         }
      },
      "images":[  
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_alt1.jpg",
            "position":"1"
         },
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_main.jpg",
            "position":"1"
         },
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_back.jpg",
            "position":"2"
         },
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/w\/p\/wp06-black_outfit.jpg",
            "position":"3"
         }
      ],
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
      "attribute_set_id":"11",
      "type_id":"bundle",
      "sku":"24-WG080",
      "has_options":"1",
      "required_options":"1",
      "created_at":"2016-08-24 04:56:52",
      "updated_at":"2016-08-24 04:56:52",
      "name":"Sprite Yoga Companion Kit",
      "image":"\/l\/u\/luma-yoga-kit-2.jpg",
      "small_image":"\/l\/u\/luma-yoga-kit-2.jpg",
      "thumbnail":"\/l\/u\/luma-yoga-kit-2.jpg",
      "options_container":"container2",
      "url_key":"sprite-yoga-companion-kit",
      "activity":"8,11",
      "gender":"80,81,84",
      "category_gear":"87",
      "description":"<p>A well-rounded yoga workout takes more than a mat. The Sprite Yoga Companion Kit helps stock your studio with the basics you need for a full-range workout. The kit is composed of four best-selling Luma Sprite accessories in one easy bundle: statis ball, foam block, yoga strap, and foam roller. Choose sizes and colors and leave the rest to us. The kit includes:<\/p>\n<ul>\n<li> Sprite Statis Ball\n<li> Sprite Foam Yoga Brick\n<li> Sprite Yoga Strap\n<li> Sprite Foam Roller\n<\/ul>",
      "status":"1",
      "visibility":"4",
      "quantity_and_stock_status":{  
         "is_in_stock":true,
         "qty":0
      },
      "price_type":"0",
      "tax_class_id":"2",
      "options":[  

      ],
      "media_gallery":{  
         "images":{  
            "57":{  
               "value_id":"57",
               "file":"\/l\/u\/luma-yoga-kit-2.jpg",
               "media_type":"image",
               "entity_id":"51",
               "label":"Image",
               "position":"1",
               "disabled":"0",
               "label_default":"Image",
               "position_default":"1",
               "disabled_default":"0"
            }
         }
      },
      "_cache_instance_store_filter":"1",
      "_cache_instance_options_collection":{  

      },
      "_cache_instance_selections_collection1":{  

      },
      "_cache_instance_selections_collection2":{  

      },
      "_cache_instance_selections_collection3":{  

      },
      "_cache_instance_selections_collection4":{  

      },
      "extension_attributes":{  

      },
      "category_ids":[  
         "3",
         "5"
      ],
      "tier_price":[  

      ],
      "tier_price_changed":0,
      "is_salable":"1",
      "additional":{  
         "activity":{  
            "label":"Activity",
            "value":"Yoga, Gym",
            "code":"activity"
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
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/l\/u\/luma-yoga-kit-2.jpg",
            "position":"1"
         }
      ],
      "app_prices":{  
         "minimal_price":0,
         "show_from_to_tax_price":0,
         "show_ex_in_price":1,
         "product_from_label":"From",
         "product_to_label":"To",
         "from_price":0,
         "to_price":0,
         "configure":{  
            "product_label":"Price as configured",
            "show_ex_in_price":1
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

Price values for each options are oldPrice (no discount, excluded tax), basePrice (applied discount, excluded tax), finalPrice (applied discount, tax included)


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
The same with 1.x version.



## View Downloadable Product

```shell
curl "https://abc.com/simiconnector/rest/v2/products/2046" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "product":{  
      "entity_id":"50",
      "attribute_set_id":"14",
      "type_id":"downloadable",
      "sku":"240-LV09",
      "has_options":"0",
      "required_options":"0",
      "created_at":"2016-08-24 04:56:50",
      "updated_at":"2016-08-24 04:56:50",
      "name":"Luma Yoga For Life",
      "meta_description":"You'll learn to use yoga to relax, control stress and increase your calorie-burning capacity, all while exploring traditional and new yoga poses that lengthen and strengthen your full muscular structure.",
      "image":"\/l\/t\/lt06.jpg",
      "small_image":"\/l\/t\/lt06.jpg",
      "thumbnail":"\/l\/t\/lt06.jpg",
      "options_container":"container2",
      "url_key":"luma-yoga-for-life",
      "samples_title":"Trailers",
      "links_title":"Downloads",
      "activity":"8,16",
      "description":"<ul><li>Increase strength + flexibility + metabolism<\/li><li>Burn calories + feel great<\/li><li>Gain energy + youthfulness + mental wellness<\/li> <\/ul><h3 style=\"margin-top: 30px;\">Download description<\/h3><p><strong style=\"display: block; margin: 20px 0 5px;\">Tone up mind and body<\/strong>Pro Yoga Instructor and Master Practitioner Marie Peale helps tone and sculpt your physique with her invigorating yet gentle approach.<\/p><p>You'll learn to use yoga to relax, control stress and increase your calorie-burning capacity, all while exploring traditional and new yoga poses that lengthen and strengthen your full muscular structure.  <\/p><ul><li>Easy download<\/li><li>Audio options: Music and instruction or instruction only<\/li><li>Heart rate techniques explained<\/li><li>Breathing techniques explained<\/li><li>Move through exercises at your own pace<\/li><\/ul><p>Two 25-minute workout episodes and one 40-minute workout episode with warm-up and cool down:<\/p><p><strong style=\"display: block; margin: 20px 0 5px;\">Episode 1<\/strong>Creative, fun session geared toward opening your lungs. Combines stretching and breathing with a focus on hips and shoulders. <\/p><p><strong style=\"display: block; margin: 20px 0 5px;\">Episode 2<\/strong>Ramp up the tempo and energy with calorie-burning flows. A stimulating workout introducing the body-sculpting power of yoga.<\/p><p><strong style=\"display: block; margin: 20px 0 5px;\">Episode 3<\/strong>Push your fitness reach and stamina with an intense series of standing and floor exercises and poses. End this extra-length session with a meditative cool down.<\/p><h3 style=\"margin-top: 30px;\">instructor bio<\/h3><p><strong style=\"display: block; margin: 20px 0 5px;\">About Marie<\/strong>Marie is a trained martial artist and dancer with a BS in Biological Engineering and over 10 years as a certified yoga teacher. Marie has studied yoga in England, India and, in 2009, at the Ashraqat Ashram Yoga Farm in the United States. She has been teaching full time since then. Her focus on strength and wellness combines a deep knowledge of human biology and motivation guided by unconditional love for her audience.<\/p>",
      "short_description":"<p>\nLuma founder Erin Renny on yoga and longevity: \"I won't promise you'll live longer with yoga. No one can promise that. But your life will be healthier, less stressful, and more physically in tune when you focus on connecting your mind and body or a regular basis. Yoga is my favorite way to express this connection. I want to share the secrets of lifelong yoga with anyone willing to breathe and learn with me.\"\n<\/p>",
      "price":"0.0000",
      "status":"1",
      "visibility":"4",
      "quantity_and_stock_status":{  
         "is_in_stock":true,
         "qty":null
      },
      "links_purchased_separately":"1",
      "tax_class_id":"2",
      "format":"102",
      "options":[  

      ],
      "media_gallery":{  
         "images":{  
            "56":{  
               "value_id":"56",
               "file":"\/l\/t\/lt06.jpg",
               "media_type":"image",
               "entity_id":"50",
               "label":"Image",
               "position":"1",
               "disabled":"0",
               "label_default":"Image",
               "position_default":"1",
               "disabled_default":"0"
            }
         }
      },
      "downloadable_links":{  
         "6":{  

         },
         "7":{  

         },
         "8":{  

         }
      },
      "extension_attributes":{  

      },
      "downloadable_samples":{  

      },
      "category_ids":[  
         "9",
         "10"
      ],
      "tier_price":[  

      ],
      "tier_price_changed":0,
      "is_salable":"1",
      "additional":{  
         "format":{  
            "label":"Format",
            "value":"Download",
            "code":"format"
         },
         "activity":{  
            "label":"Activity",
            "value":"Yoga, Athletic",
            "code":"activity"
         }
      },
      "images":[  
         {  
            "url":"http:\/\/magento2.jajahub.com\/pub\/media\/catalog\/product\/cache\/1\/image\/600x600\/beff4985b56e3afdbeabfc89641a4582\/l\/t\/lt06.jpg",
            "position":"1"
         }
      ],
      "app_prices":{  
         "has_special_price":0,
         "show_ex_in_price":1,
         "price_excluding_tax":{  
            "label":"Excl. Tax",
            "price":0
         },
         "price_including_tax":{  
            "label":"Incl. Tax",
            "price":0
         }
      },
      "app_options":{  
         "download_sample":[  
            {  
               "title":"Trailers",
               "value":[  
                  {  
                     "url":"http:\/\/magento2.jajahub.com\/downloadable\/download\/sample\/sample_id\/16\/",
                     "title":"Trailer #1"
                  }
               ]
            },
            {  
               "title":"Trailers",
               "value":[  
                  {  
                     "url":"http:\/\/magento2.jajahub.com\/downloadable\/download\/sample\/sample_id\/16\/",
                     "title":"Trailer #1"
                  },
                  {  
                     "url":"http:\/\/magento2.jajahub.com\/downloadable\/download\/sample\/sample_id\/17\/",
                     "title":"Trailer #2"
                  }
               ]
            },
            {  
               "title":"Trailers",
               "value":[  
                  {  
                     "url":"http:\/\/magento2.jajahub.com\/downloadable\/download\/sample\/sample_id\/16\/",
                     "title":"Trailer #1"
                  },
                  {  
                     "url":"http:\/\/magento2.jajahub.com\/downloadable\/download\/sample\/sample_id\/17\/",
                     "title":"Trailer #2"
                  },
                  {  
                     "url":"http:\/\/magento2.jajahub.com\/downloadable\/download\/sample\/sample_id\/18\/",
                     "title":"Trailer #3"
                  }
               ]
            }
         ],
         "download_options":[  
            {  
               "title":"Downloads",
               "type":"checkbox",
               "position":"0",
               "links_purchased_separately":"1",
               "isRequired":"1",
               "value":[  
                  {  
                     "id":"6",
                     "title":"Episode 1",
                     "price_excluding_tax":{  
                        "label":"Excl. Tax",
                        "price":9
                     },
                     "price_including_tax":{  
                        "label":"Incl. Tax",
                        "price":9.74
                     }
                  },
                  {  
                     "id":"7",
                     "title":"Episode 2",
                     "price_excluding_tax":{  
                        "label":"Excl. Tax",
                        "price":9
                     },
                     "price_including_tax":{  
                        "label":"Incl. Tax",
                        "price":9.74
                     }
                  },
                  {  
                     "id":"8",
                     "title":"Episode 3",
                     "price_excluding_tax":{  
                        "label":"Excl. Tax",
                        "price":9
                     },
                     "price_including_tax":{  
                        "label":"Incl. Tax",
                        "price":9.74
                     }
                  }
               ]
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
The same with 1.x version.

