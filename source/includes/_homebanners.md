# Home Banners

## Home Banners Properties

Attributes| Type| Description
--------- | ------- | -----------
banner_id | id | Banner Id
banner_name | string | Banner Image URL
banner_title | string | Banner Title
status | int | Banner Status
type | int | Banner Type (1- Product In-App, 2- Category In-App, 3- Website Page)
banner_url | string | Banner URL (open WebView)
category_id | int | Category to be Opened
product_id | int | Products to be Opened
width | int | Banner width
height | int | Banner height
width_tablet | int | Banner width Tablet
height_tablet | int | Banner height Tablet
cat_name | string | Category Name (when type = 2)
has_children | boolean | Category Has Children Or Not (when type = 2)


## View Home screen Banners

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homebanners" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2"
   ],
   "homebanners":[  
      {  
         "banner_id":"1",
         "banner_name":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/cat5.jpg",
		 "banner_name_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/3784368_cv.jpg",               
         "banner_url":null,
         "banner_title":"Banner1",
         "status":"1",
         "website_id":"0",
         "type":"2",
         "category_id":"4",
         "product_id":"0",
         "sort_order":"1",
         "entity_id":"25",
         "content_type":"2",
         "item_id":"1",
         "store_view_id":"1",
         "width":960,
         "height":358,
         "width_tablet":2048,
         "height_tablet":893,
         "has_children":true,
         "cat_name":"Women"
      },
      {  
         "banner_id":"2",
         "banner_name":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/cat6.jpg",
		 "banner_name_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/banner\/3784368_cv.jpg",               
         "banner_url":null,
         "banner_title":"2",
         "status":"1",
         "website_id":"0",
         "type":"1",
         "category_id":"0",
         "product_id":"337",
         "sort_order":"1",
         "entity_id":"30",
         "content_type":"2",
         "item_id":"2",
         "store_view_id":"1",
         "width":960,
         "height":358,
         "width_tablet":2048,
         "height_tablet":893
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

Return Home Banners

