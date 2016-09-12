# Store Views

## Store View Properties

Attributes| Type| Description
--------- | ------- | -----------
store_id | string | Store View id <code>read only</code>
code | string | Store View code
base_url | string | Store View Base URL
website_id | int | id of the Website that Store View belongs to
group_id | int | id of the Store (Group) that Store View belongs to
name | string | Store View name
base_url | string | Store View Base URL
sort_order | int | display sort order
is_active | int | "1" for active, "0" for inactive
base | array | Store View base information
sales | array | Store View sales configuration
checkout | array | Store View checkout configuration
tax | array | Store View tax configuration
google_analytics | array | Google API configuration values
customer | array | Customer Address and Account configuration
wishlist | array | Website Wishlist configuration
catalog | array | Catalog frontend display and review configuration values
cms | array | CMS pages


## View Default Store View

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews/default" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "storeview":{  
      "base":{  
         "country_code":"AL",
         "country_name":"Albania",
         "locale_identifier":"en_US",
         "store_id":"1",
         "store_name":"English",
         "store_code":"default",
         "group_id":"1",
         "base_url":"",
         "use_store":"0",
         "is_rtl":"0",
         "is_show_sample_data":"1",
         "android_sender":"",
         "currency_symbol":"$",
         "currency_code":"USD",
         "currency_position":"before",
         "thousand_separator":",",
         "decimal_separator":".",
         "min_number_of_decimals":"0",
         "max_number_of_decimals":"2",
         "currencies":[  
            {  
               "value":"USD",
               "title":"US Dollar"
            }
         ],
         "is_show_home_title":"1"
      },
      "sales":{  
         "sales_reorder_allow":"1",
         "sales_totals_sort_subtotal":"10",
         "sales_totals_sort_discount":"20",
         "sales_totals_sort_shipping":"30",
         "sales_totals_sort_weee":"50",
         "sales_totals_sort_tax":"40",
         "sales_totals_sort_grand_total":"100"
      },
      "checkout":{  
         "enable_guest_checkout":"1",
         "enable_agreements":0
      },
      "tax":{  
         "tax_display_type":"1",
         "tax_display_shipping":"1",
         "tax_cart_display_price":"1",
         "tax_cart_display_subtotal":"1",
         "tax_cart_display_shipping":"1",
         "tax_cart_display_grandtotal":"0",
         "tax_cart_display_full_summary":"0",
         "tax_cart_display_zero_tax":"0"
      },
      "google_analytics":{  
         "google_analytics_active":null,
         "google_analytics_type":null,
         "google_analytics_account":null,
         "google_analytics_anonymization":null
      },
      "customer":{  
         "address_option":{  
            "prefix_show":"",
            "middlename_show":"",
            "suffix_show":"",
            "dob_show":"",
            "taxvat_show":null,
            "gender_show":"",
            "gender_value":[  
               {  
                  "label":"Male",
                  "value":"123"
               },
               {  
                  "label":"Female",
                  "value":"124"
               }
            ]
         },
         "account_option":{  
            "taxvat_show":"0"
         }
      },
      "wishlist":{  
         "wishlist_general_active":"1",
         "wishlist_wishlist_link_use_qty":null
      },
      "catalog":{  
         "frontend":{  
            "view_products_default":"0",
            "is_show_zero_price":"1",
            "is_show_link_all_product":"1",
            "catalog_frontend_list_mode":"grid-list",
            "catalog_frontend_grid_per_page_values":"9,15,30",
            "catalog_frontend_list_per_page":"10",
            "catalog_frontend_list_allow_all":null,
            "catalog_frontend_default_sort_by":"position",
            "catalog_frontend_flat_catalog_category":"0",
            "catalog_frontend_flat_catalog_product":null,
            "catalog_frontend_parse_url_directives":"1"
         },
         "review":{  
            "catalog_review_allow_guest":"1"
         }
      },
      "cms":{  
         "all_ids":[  

         ],
         "cmspages":[  

         ],
         "total":0,
         "page_size":15,
         "from":0
      },
      "category_cmspages":[  

      ],
      "zopim_config":{  
         "enable":"0",
         "account_key":"",
         "show_profile":"0",
         "name":"3",
         "email":"3",
         "phone":"3"
      },
      "mixpanel_config":{  
         "token":""
      },
      "allowed_countries":[  
         {  
            "country_code":"AL",
            "country_name":"Albania",
            "states":[  

            ]
         },
         {  
            "country_code":"DZ",
            "country_name":"Algeria",
            "states":[  

            ]
         }
      ],
      "stores":{  
         "all_ids":[  
            "1"
         ],
         "stores":[  
            {  
               "group_id":"1",
               "website_id":"1",
               "name":"Main Store",
               "root_category_id":"3",
               "default_store_id":"1",
               "storeviews":{  
                  "all_ids":[  
                     "1",
                     "2",
                     "3"
                  ],
                  "storeviews":[  
                     {  
                        "store_id":"1",
                        "code":"default",
                        "website_id":"1",
                        "group_id":"1",
                        "name":"English",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":""
                     },
                     {  
                        "store_id":"2",
                        "code":"german",
                        "website_id":"1",
                        "group_id":"1",
                        "name":"German",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":""
                     },
                     {  
                        "store_id":"3",
                        "code":"french",
                        "website_id":"1",
                        "group_id":"1",
                        "name":"French",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":""
                     }
                  ],
                  "total":3,
                  "page_size":15,
                  "from":0
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

Get default Store View



## View A Store View

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews/3" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON the Same structure with "View Default Store View" API

```json
{
   "_comment": "The above command returns JSON the Same structure with View Default Store View API"
}
```

This endpoint retrieves a specific Store View.

### HTTP Request

`GET /rest/storeviews/<id>`


## View List Of Store Views

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2",
      "3"
   ],
   "storeviews":[  
      {  
         "store_id":"1",
         "code":"default",
         "website_id":"1",
         "group_id":"1",
         "name":"English",
         "sort_order":"0",
         "is_active":"1",
         "base_url":"http:\/\/default.com\/magento19"
      },
      {  
         "store_id":"2",
         "code":"french",
         "website_id":"1",
         "group_id":"1",
         "name":"French",
         "sort_order":"0",
         "is_active":"1",
         "base_url":"http:\/\/localhost.com\/magento19\/index.php"
      },
      {  
         "store_id":"3",
         "code":"german",
         "website_id":"1",
         "group_id":"1",
         "name":"German",
         "sort_order":"0",
         "is_active":"1",
         "base_url":""
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves a list of Store Views.



## Change Currency

```shell
curl GET "https://abc.com/simiconnector/rest/v2/storeviews/default?currency=KMF" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON the Same structure with "View Default Store View" API

```json
{
   "_comment": "The above command returns JSON the Same structure with View Default Store View API"
}
```

This request is to Change customer Currency.