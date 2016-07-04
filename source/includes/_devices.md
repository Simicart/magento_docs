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
    "all_ids": [
        "1"
    ],
    "notifications": [
        {
            "notice_id": "1",
            "notice_title": "First One",
            "notice_url": null,
            "notice_content": "Message Test",
            "notice_sanbox": "2",
            "website_id": "1",
            "device_id": "0",
            "type": "1",
            "category_id": "0",
            "product_id": "1",
            "image_url": "simi/simicart/notification/images/0fdf1e42cc46e5ca1cf5e33b9501655c.png",
            "location": "",
            "distance": "",
            "address": "",
            "city": "",
            "country": "",
            "zipcode": "",
            "state": "",
            "show_popup": "0",
            "created_time": "2016-07-04 09:23:19",
            "devices_pushed": "8, 9, 10, 11",
            "storeview_id": "3"
        }
    ],
    "total": 1,
    "page_size": 15,
    "from": 0
}
```
This API is to show Notification list

