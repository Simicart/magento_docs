# Devices

## Device Properties

Attributes| Type| Description
--------- | ------- | -----------
device_id | id | Device Id
user_email | email | Customer Email
is_demo | int | 1 - Demo app, 0 - Live App
latitude | string | Device Latitude
longitude | string | Device Longtitude
app_id | string | Application Id (Package Id)
build_version | string | Application Build Version
plaform_id | int | Platform: 1- iPhone, 2- iPad, 3- Android


## Register

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/devices" \
  -H "Authorization: Bearer <token>" \
  -d "{
"device_token":"456456456",
"is_demo":"1",
"latitude":"10.100",
"longitude":"20.10",
"user_email":"test123123@jkjkj.com",
"build_version":"1.0.1",
"plaform_id":"1",
"app_id":"com.simicart.demo"
}
"
```

> The above command returns JSON structured like this:

```json
{  
   "device":{  
      "device_id":"2",
      "address":"",
      "city":"\u0633\u0644\u0645\u0627\u062a",
      "state":"Barh Azoum",
      "country":"TD",
      "zipcode":null,
      "device_token":"456456456",
      "plaform_id":1,
      "website_id":"1",
      "latitude":"10.100",
      "longitude":"20.10",
      "created_time":"2016-06-20 07:18:57",
      "user_email":"test123123@jkjkj.com",
      "app_id":"com.simicart.demo",
      "build_version":"1.0.1",
      "is_demo":"1"
   }
}
```
This API is to register a device.

## Show Notification List

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/notifications?device_token=45646546546545623" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2",
      "3"
   ],
   "notifications":[  
      {  
         "notice_id":"1",
         "notice_title":"Test Notification iOS 01",
         "notice_url":null,
         "notice_content":"Customize your mobile store design in just a few clicks. Make your app completely stand out with two beautiful themes inspired by modern & flat design. Each button optimized. Seeing is believing - give customers that extra vote of confidence in your business.",
         "notice_sanbox":"1",
         "storeview_id":"1",
         "device_id":"1",
         "type":"1",
         "category_id":"0",
         "product_id":"107",
         "image_url":"http:\/\/demo.magestore.com\/simicart\/simipos1\/media\/simi\/simiconnector\/notification\/images\/6bdede43932e3564de8f55685d42d943.png",
         "location":"",
         "distance":"",
         "address":"",
         "city":"",
         "country":"",
         "zipcode":"",
         "state":"",
         "show_popup":"1",
         "devices_pushed":"1",
         "created_time":"2016-08-29 03:31:01",
         "width":500,
         "height":500,
         "product_name":"CLOUDY NIGHT"
      },
      {  
         "notice_id":"2",
         "notice_title":"Test Notification iOS 02",
         "notice_url":null,
         "notice_content":"Customize your mobile store design in just a few clicks. Make your app completely stand out with two beautiful themes inspired by modern & flat design. Each button optimized. Seeing is believing - give customers that extra vote of confidence in your business.",
         "notice_sanbox":"1",
         "storeview_id":"1",
         "device_id":"1",
         "type":"2",
         "category_id":"5",
         "product_id":"0",
         "image_url":"http:\/\/demo.magestore.com\/simicart\/simipos1\/media\/simi\/simiconnector\/notification\/images\/0f61cda55910f0dd54e983d8c87ff319.png",
         "location":"",
         "distance":"",
         "address":"",
         "city":"",
         "country":"",
         "zipcode":"",
         "state":"",
         "show_popup":"1",
         "devices_pushed":"1",
         "created_time":"2016-08-29 03:41:41",
         "width":500,
         "height":500,
         "category_name":"Shoes",
         "has_child":1
      },
      {  
         "notice_id":"3",
         "notice_title":"Test Notification iOS 03",
         "notice_url":"https:\/\/www.simicart.com\/",
         "notice_content":"Understand your customer insights and get more engagement through optimization with Real-time mobile app Analytics!\r\n\r\nGet close to potential customers in multichannel. You can promote your social media marketing activities and run promotional campaign together to assist sales.",
         "notice_sanbox":"1",
         "storeview_id":"1",
         "device_id":"1",
         "type":"3",
         "category_id":"0",
         "product_id":"0",
         "image_url":"",
         "location":"",
         "distance":"",
         "address":"",
         "city":"",
         "country":"",
         "zipcode":"",
         "state":"",
         "show_popup":"0",
         "devices_pushed":"1, 2",
         "created_time":"2016-08-29 03:42:22"
      }
   ],
   "total":3,
   "page_size":"24",
   "from":0
}
```
This API is to show Notification list

