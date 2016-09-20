# Downloadable Products

## Downloadable Item Properties

Attributes| Type| Description
--------- | ------- | -----------
order_id | id | Order Id
order_date | date | Order Date
order_name | string | Order Name
order_link | string | Item Link
order_file | string | Item File Name
order_status | string | Order Status
order_remain | string | Download Remaining


## Get Downloadable Products

```shell
curl GET "https://abc.com/simiconnector/rest/v2/downloadableproducts " \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1"
   ],
   "downloadableproducts":[  
      {  
         "item_id":"1",
         "purchased_id":"1",
         "order_item_id":"1",
         "product_id":"177",
         "link_hash":"MC44NjExODQwMCAxNDc0MzU0NDkzMTExNzc,",
         "number_of_downloads_bought":"0",
         "number_of_downloads_used":"1",
         "link_id":"1",
         "link_title":"Links",
         "is_shareable":"0",
         "link_url":null,
         "link_file":"\/f\/a\/fashionone_user_guide.pdf",
         "link_type":"file",
         "status":"available",
         "created_at":"2016-09-20 06:54:51",
         "updated_at":"2016-09-20 06:54:51",
         "order_id":"100000001",
         "order_date":"2016-09-20 06:54:51",
         "order_name":"Downloadable Product",
         "order_link":"http:\/\/localhost.com\/magento18\/index.php\/downloadable\/download\/link\/id\/MC44NjExODQwMCAxNDc0MzU0NDkzMTExNzc,\/",
         "order_file":"fashionone_user_guide.pdf",
         "order_status":"available",
         "order_remain":"Unlimited"
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```


