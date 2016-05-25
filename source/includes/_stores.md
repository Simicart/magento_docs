# Stores

## Store Properties

Attributes| Type| Description
--------- | ------- | -----------
group_id | string | Store (Group) id <code>read only</code>
website_id | int | id of the Website that Store belongs to
name | string | Store name
root_category_id | int | Store's Root category
default_store_id | int | Default Store View of this Store (Group) 

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
      "1"
   ],
   "stores":[  
      {  
         "group_id":"1",
         "website_id":"1",
         "name":"Madison Island",
         "root_category_id":"2",
         "default_store_id":"1"
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves a list of Stores.
