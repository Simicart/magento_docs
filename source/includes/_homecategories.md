# Home Categories

## Home Categories Properties

Attributes| Type| Description
--------- | ------- | -----------
simicategory_id | id | Home Category Id
simicategory_name | string | Home Category Name
simicategory_filename | string | Home Category Image URL
category_id | int | Home Category ID
status | int | Home Category Status
width | int | Category Image Width
height | int | Category Image Height

## View Home Scren Categories

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homecategories" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1"
   ],
   "homecategories":[  
      {  
         "simicategory_id":"1",
         "simicategory_name":null,
         "simicategory_filename":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/cat6.jpg",
         "category_id":"123",
         "status":"1",
         "website_id":"0",
         "storeview_id":"Array",
         "sort_order":"123",
         "entity_id":"17",
         "content_type":"3",
         "item_id":"1",
         "store_view_id":"1",
         "width":1170,
         "height":759
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

Return Home Categories

