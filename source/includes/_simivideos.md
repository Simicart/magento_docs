# Product Videos

## Product Videos Properties

Attributes| Type| Description
--------- | ------- | -----------
video_id | id | Video Id
video_url | string | Video URL
video_key | string | Video Key (for Youtube SDK)
video_title | string | Video Title
status | int | Video Enabled or Not


## Get Videos of a Product

```shell
curl "https://abc.com/simiconnector/rest/v2/simivideos?product_id=397" \
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
   "simivideos":[  
      {  
         "video_id":"1",
         "video_url":"https:\/\/www.youtube.com\/watch?v=AfgX7GB_Rkc",
         "video_key":"AfgX7GB_Rkc",
         "video_title":"Test 1",
         "product_ids":"338, 372, 374, 378, 339, 397",
         "status":"1"
      },
      {  
         "video_id":"2",
         "video_url":"https:\/\/www.youtube.com\/watch?v=6SXYovVYvOQ&t=1474s",
         "video_key":"6SXYovVYvOQ",
         "video_title":"Test 2",
         "product_ids":"378, 339, 397",
         "status":"1"
      },
      {  
         "video_id":"3",
         "video_url":"http:\/\/www.sample-videos.com\/video\/mp4\/720\/big_buck_bunny_720p_1mb.mp4",
         "video_key":null,
         "video_title":"Test 3",
         "product_ids":"337, 397",
         "status":"1"
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

This request is to get Videos of Product.
If the Video key is NULL, then it's not a Valid Youtube URL, Use Webview to Open Video URL instead.