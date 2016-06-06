# Stores

## Store Properties

Attributes| Type| Description
--------- | ------- | -----------
group_id | string | Store (Group) id <code>read only</code>
website_id | int | id of the Website that Store belongs to
name | string | Store name
root_category_id | int | Store's Root category
default_store_id | int | Default Store View of this Store (Group) 
storeviews | array | Store Views

## View A Store

```shell
curl "https://abc.com/simiconnector/rest/v2/stores/1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "store":{  
      "group_id":"1",
      "website_id":"1",
      "name":"Madison Island",
      "root_category_id":"2",
      "default_store_id":"1"
   }
}
```

This endpoint retrieves a specific Store.

### HTTP Request

`GET /rest/stores/<id>`


## View List Of Stores

```shell
curl "https://abc.com/simiconnector/rest/v2/stores" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2"
   ],
   "stores":[  
      {  
         "group_id":"1",
         "website_id":"1",
         "name":"Madison Island",
         "root_category_id":"2",
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
      },
      {  
         "group_id":"2",
         "website_id":"1",
         "name":"Store 2",
         "root_category_id":"2",
         "default_store_id":"4",
         "storeviews":{  
            "all_ids":[  
               "4"
            ],
            "storeviews":[  
               {  
                  "store_id":"4",
                  "code":"storeview2",
                  "website_id":"1",
                  "group_id":"2",
                  "name":"Storeview 2",
                  "sort_order":"0",
                  "is_active":"1",
                  "base_url":""
               }
            ],
            "total":1,
            "page_size":15,
            "from":0
         }
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves a list of Stores.
