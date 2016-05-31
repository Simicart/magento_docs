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

