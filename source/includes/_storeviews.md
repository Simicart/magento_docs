# Store Views

## Store View Properties

Attributes| Type| Description
--------- | ------- | -----------
store_id | string | Store View id <code>read only</code>
code | string | Store View code
website_id | int | id of the Website that Store View belongs to
group_id | int | id of the Store (Group) that Store View belongs to
name | string | Store View name
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

## View A Store View

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews/3" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json

{  
   "storeview":{  
      "base":{  
         "country_code":"US",
         "country_name":"United States",
         "locale_identifier":"en_US",
         "currency_symbol":"$",
         "currency_code":"USD",
         "currency_position":"before",
         "store_id":"3",
         "store_name":"French",
         "store_code":"french",
         "use_store":"0",
         "is_rtl":"0",
         "android_sender":"518903118242"
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
         "is_reload_payment_method":"0",
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
      }
   }
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
         "is_active":"1"
      },
      {  
         "store_id":"2",
         "code":"german",
         "website_id":"1",
         "group_id":"1",
         "name":"German",
         "sort_order":"0",
         "is_active":"0"
      },
      {  
         "store_id":"3",
         "code":"french",
         "website_id":"1",
         "group_id":"1",
         "name":"French",
         "sort_order":"0",
         "is_active":"1"
      }
   ],
   "total":4,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves a list of Store Views.
