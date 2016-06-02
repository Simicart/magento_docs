# Devices

## Device Properties

Attributes| Type| Description
--------- | ------- | -----------
device_id | id | Device Id
user_email | email | Customer Email
is_demo | int | 1 - Demo app, 0 - Live App
latitude | string | Device Latitude
longitude | string | Device Longtitude


## Register

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/devices" \
  -H "Authorization: Bearer <token>" \
  -d "{
"device_token":"456456456",
"is_demo":"1",
"latitude":"10.100",
"longitude":"20.10",
"user_email":"test123123@jkjkj.com"
}
"
```

> The above command returns JSON structured like this:

```json
{  
   "device":{  
      "device_id":"1",
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
      "created_time":"2016-06-02 08:46:30",
      "user_email":"test123123@jkjkj.com",
      "is_demo":"1"
   }
}
```
This API is to register a device.

