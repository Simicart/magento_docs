# CMS Pages

## CMS Page Properties

Attributes| Type| Description
--------- | ------- | -----------
cms_id | id | CMS Pages Id
cms_title | string | CMS Page Title
cms_image | string | CMS Icon
cms_content | string | Content To Display
cms_status | int | CMS Status


## View CMS Pages

```shell
curl GET "https://abc.com/simiconnector/rest/v2/cmspages" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2"
   ],
   "cmspages":[  
      {  
         "cms_id":"1",
         "cms_title":"Title 1",
         "cms_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/cms\/photo1464572154470@2x.png",
         "cms_content":"Content 1",
         "cms_status":"0",
         "website_id":"0",
         "sort_order":"1",
         "entity_id":"50",
         "content_type":"1",
         "item_id":"1",
         "store_view_id":"1"
      },
      {  
         "cms_id":"2",
         "cms_title":"Title 2",
         "cms_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/cms\/photo1464572154555@2x.png",
         "cms_content":"Content 2",
         "cms_status":"1",
         "website_id":"0",
         "sort_order":"2",
         "entity_id":"52",
         "content_type":"1",
         "item_id":"2",
         "store_view_id":"1"
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

Return Home CMS Pages


## Category as CMS Page

```shell
curl "https://abc.com/simiconnector/rest/v2/categories/4" \
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
         "store_id":"1",
         "store_name":"English",
         "store_code":"default",
         "group_id":"1",
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
      "cms":{  
         "all_ids":[  
            "1"
         ],
         "cmspages":[  
            {  
               "cms_id":"1",
               "cms_title":"b",
               "cms_image":"",
               "cms_content":"<p>a<\/p>",
               "cms_status":"1",
               "website_id":"0",
               "type":"1",
               "category_id":"0",
               "sort_order":"1",
               "entity_id":"4",
               "content_type":"1",
               "item_id":"1",
               "store_view_id":"1"
            }
         ],
         "total":1,
         "page_size":15,
         "from":0
      },
      "category_cmspages":[  
         {  
            "cms_id":"2",
            "cms_title":"c",
            "cms_image":"",
            "cms_content":"d",
            "cms_status":"0",
            "website_id":"0",
            "type":"2",
            "category_id":"15",
            "sort_order":"0",
            "entity_id":"7",
            "content_type":"1",
            "item_id":"2",
            "store_view_id":"1"
         }
      ],
      "zopim_config":{  
         "enable":"0",
         "account_key":"",
         "show_profile":"0",
         "name":"3",
         "email":"3",
         "phone":"3"
      },
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

On Store View Configuration setting, the category_cmspages shows the Categories that would be shown as CMS page.
