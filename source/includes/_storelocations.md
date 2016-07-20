# Storelocations

## Storelocator Properties

Attributes| Type| Description
--------- | ------- | -----------
simistorelocator_id | id | Store Id
website_id | int | id of the Website that Store belongs to
name | string | Store name
address | string | Store's Address
city | string | Store City 
country | string | Store Country
zipcode | string | Zip Code
state | string | Stage
email | string | Store email
phone | string | Store Phone Number
description | string | Store Description
latitude | string | Store Latitute
longtitude | string | Store Longtitude
special_days | array | Special Days
holiday_days | array | Holiday Dates
monday_status | string | Monday status (and so on with week days)
monday_open | string | Monday Open Time
monday_close | string | Monday Close Time
distance | string | Distance to Store (if longtitude and latitude included)


## Get Storelocations

```shell
curl "https://abc.com/simiconnector/rest/v2/storelocations" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1"
   ],
   "storelocations":[  
      {  
         "simistorelocator_id":"1",
         "name":"Store 1",
         "address":"120 E. President St.",
         "city":"St. Louis",
         "country":"AI",
         "zipcode":"1000",
         "state":"4564",
         "state_id":null,
         "email":"abc@bjkj.com",
         "phone":"98878987979",
         "fax":"2121213213",
         "description":"Description",
         "status":"1",
         "sort":"0",
         "link":null,
         "latitude":"18.220554",
         "longtitude":"-63.068615",
         "monday_status":"1",
         "monday_open":"00:00",
         "monday_close":"00:00",
         "tuesday_status":"1",
         "tuesday_open":"02:06",
         "tuesday_close":"00:00",
         "wednesday_status":"1",
         "wednesday_open":"00:00",
         "wednesday_close":"00:00",
         "thursday_status":"1",
         "thursday_open":"00:00",
         "thursday_close":"00:00",
         "friday_status":"1",
         "friday_open":"00:00",
         "friday_close":"00:00",
         "saturday_status":"1",
         "saturday_open":"00:00",
         "saturday_close":"00:00",
         "sunday_status":"1",
         "sunday_open":"00:00",
         "sunday_close":"00:00",
         "zoom_level":"4",
         "image_icon":"photo1468804718500.png",
         "entity_id":"256",
         "content_type":"5",
         "item_id":"1",
         "store_view_id":"1",
         "special_days":[  
            {  
               "date":"2016-07-22",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-23",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-24",
               "time_open":"01:02",
               "time_close":"03:06"
            }
         ],
         "holiday_days":[  
            {  
               "date":"2016-07-17"
            },
            {  
               "date":"2016-07-18"
            },
            {  
               "date":"2016-07-19"
            },
            {  
               "date":"2016-07-20"
            }
         ],
         "country_name":"Anguilla",
         "distance":0,
         "image":"http:\/\/localhost.com\/magento19\/media\/simistorelocator\/images\/1\/1\/1_1.png"
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

Get Storelocations List

### HTTP Request

`GET /simiconnector/rest/v2/storelocations<id>`


## Get Storelocations Tags

```shell
curl "https://abc.com/simiconnector/rest/v2/storelocatortags" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2",
      "3",
      "4",
      "9"
   ],
   "storelocatortags":[  
      {  
         "tag_id":"1",
         "simistorelocator_id":"1",
         "value":"tag1"
      },
      {  
         "tag_id":"2",
         "simistorelocator_id":"1",
         "value":"tag2"
      },
      {  
         "tag_id":"3",
         "simistorelocator_id":"1",
         "value":"tag3"
      },
      {  
         "tag_id":"4",
         "simistorelocator_id":"1",
         "value":"tag4"
      },
      {  
         "tag_id":"9",
         "simistorelocator_id":"2",
         "value":"tag5"
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves a list store location tags.




## Get Storelocations by Locations

```shell
curl "https://abc.com/simiconnector/rest/v2/storelocations?country=AI" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1"
   ],
   "storelocations":[  
      {  
         "simistorelocator_id":"1",
         "name":"Store 1",
         "address":"120 E. President St.",
         "city":"St. Louis",
         "country":"AI",
         "zipcode":"1000",
         "state":"4564",
         "state_id":null,
         "email":"abc@bjkj.com",
         "phone":"98878987979",
         "fax":"2121213213",
         "description":"Description",
         "status":"1",
         "sort":"0",
         "link":null,
         "latitude":"18.220554",
         "longtitude":"-63.068615",
         "monday_status":"1",
         "monday_open":"00:00",
         "monday_close":"00:00",
         "tuesday_status":"1",
         "tuesday_open":"02:06",
         "tuesday_close":"00:00",
         "wednesday_status":"1",
         "wednesday_open":"00:00",
         "wednesday_close":"00:00",
         "thursday_status":"1",
         "thursday_open":"00:00",
         "thursday_close":"00:00",
         "friday_status":"1",
         "friday_open":"00:00",
         "friday_close":"00:00",
         "saturday_status":"1",
         "saturday_open":"00:00",
         "saturday_close":"00:00",
         "sunday_status":"1",
         "sunday_open":"00:00",
         "sunday_close":"00:00",
         "zoom_level":"4",
         "image_icon":"photo1468804718500.png",
         "entity_id":"256",
         "content_type":"5",
         "item_id":"1",
         "store_view_id":"1",
         "special_days":[  
            {  
               "date":"2016-07-22",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-23",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-24",
               "time_open":"01:02",
               "time_close":"03:06"
            }
         ],
         "holiday_days":[  
            {  
               "date":"2016-07-17"
            },
            {  
               "date":"2016-07-18"
            },
            {  
               "date":"2016-07-19"
            },
            {  
               "date":"2016-07-20"
            }
         ],
         "country_name":"Anguilla",
         "distance":0,
         "image":"http:\/\/localhost.com\/magento19\/media\/simistorelocator\/images\/1\/1\/1_1.png"
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

Get Storelocations List By Location, key including:
location country, city, state, zipcode

## Get Storelocations by Longitude and Latitude

```shell
curl "https://abc.com/simiconnector/rest/v2/storelocations?lat=1&lng=2" \
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
   "storelocations":[  
      {  
         "simistorelocator_id":"1",
         "name":"Store 1",
         "address":"120 E. President St.",
         "city":"St. Louis",
         "country":"AI",
         "zipcode":"1000",
         "state":"4564",
         "state_id":null,
         "email":"abc@bjkj.com",
         "phone":"98878987979",
         "fax":"2121213213",
         "description":"Description",
         "status":"1",
         "sort":"0",
         "link":null,
         "latitude":"18.220554",
         "longtitude":"-63.068615",
         "monday_status":"1",
         "monday_open":"00:00",
         "monday_close":"00:00",
         "tuesday_status":"1",
         "tuesday_open":"02:06",
         "tuesday_close":"00:00",
         "wednesday_status":"1",
         "wednesday_open":"00:00",
         "wednesday_close":"00:00",
         "thursday_status":"1",
         "thursday_open":"00:00",
         "thursday_close":"00:00",
         "friday_status":"1",
         "friday_open":"00:00",
         "friday_close":"00:00",
         "saturday_status":"1",
         "saturday_open":"00:00",
         "saturday_close":"00:00",
         "sunday_status":"1",
         "sunday_open":"00:00",
         "sunday_close":"00:00",
         "zoom_level":"4",
         "image_icon":"photo1468804718500.png",
         "entity_id":"256",
         "content_type":"5",
         "item_id":"1",
         "store_view_id":"1",
         "special_days":[  
            {  
               "date":"2016-07-22",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-23",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-24",
               "time_open":"01:02",
               "time_close":"03:06"
            }
         ],
         "holiday_days":[  
            {  
               "date":"2016-07-17"
            },
            {  
               "date":"2016-07-18"
            },
            {  
               "date":"2016-07-19"
            },
            {  
               "date":"2016-07-20"
            }
         ],
         "country_name":"Anguilla",
         "distance":7345445.2709984,
         "image":"http:\/\/localhost.com\/magento19\/media\/simistorelocator\/images\/1\/1\/1_1.png"
      },
      {  
         "simistorelocator_id":"2",
         "name":"Store 2",
         "address":"address1",
         "city":"billing city",
         "country":"GB",
         "zipcode":"post code",
         "state":null,
         "state_id":null,
         "email":null,
         "phone":null,
         "fax":null,
         "description":"",
         "status":"1",
         "sort":"0",
         "link":null,
         "latitude":"51.49542",
         "longtitude":"-3.455298",
         "monday_status":"1",
         "monday_open":"00:00",
         "monday_close":"00:00",
         "tuesday_status":"1",
         "tuesday_open":"00:00",
         "tuesday_close":"00:00",
         "wednesday_status":"1",
         "wednesday_open":"00:00",
         "wednesday_close":"00:00",
         "thursday_status":"1",
         "thursday_open":"00:00",
         "thursday_close":"00:00",
         "friday_status":"1",
         "friday_open":"00:00",
         "friday_close":"00:00",
         "saturday_status":"1",
         "saturday_open":"00:00",
         "saturday_close":"00:00",
         "sunday_status":"1",
         "sunday_open":"00:00",
         "sunday_close":"00:00",
         "zoom_level":"6",
         "image_icon":"photo1468804718629.png",
         "entity_id":"262",
         "content_type":"5",
         "item_id":"2",
         "store_view_id":"1",
         "special_days":[  
            {  
               "date":"2016-07-22",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-23",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-24",
               "time_open":"01:02",
               "time_close":"03:06"
            }
         ],
         "holiday_days":[  
            {  
               "date":"2016-07-17"
            },
            {  
               "date":"2016-07-18"
            },
            {  
               "date":"2016-07-19"
            },
            {  
               "date":"2016-07-20"
            }
         ],
         "country_name":"United Kingdom",
         "distance":5638080.0306908,
         "image":"http:\/\/localhost.com\/magento19\/media\/simistorelocator\/images\/2\/2\/2_1.png"
      },
      {  
         "simistorelocator_id":"3",
         "name":"Store 3",
         "address":"a",
         "city":"2",
         "country":"AD",
         "zipcode":"1",
         "state":null,
         "state_id":null,
         "email":"123@b.com",
         "phone":"123",
         "fax":"123",
         "description":"des 3",
         "status":"1",
         "sort":"0",
         "link":null,
         "latitude":"42.74515296238155",
         "longtitude":"1.9335146611693972",
         "monday_status":"1",
         "monday_open":"00:00",
         "monday_close":"00:00",
         "tuesday_status":"1",
         "tuesday_open":"00:00",
         "tuesday_close":"00:00",
         "wednesday_status":"1",
         "wednesday_open":"00:00",
         "wednesday_close":"00:00",
         "thursday_status":"1",
         "thursday_open":"00:00",
         "thursday_close":"00:00",
         "friday_status":"1",
         "friday_open":"00:00",
         "friday_close":"00:00",
         "saturday_status":"1",
         "saturday_open":"00:00",
         "saturday_close":"00:00",
         "sunday_status":"1",
         "sunday_open":"00:00",
         "sunday_close":"00:00",
         "zoom_level":"9",
         "image_icon":"",
         "entity_id":"250",
         "content_type":"5",
         "item_id":"3",
         "store_view_id":"1",
         "special_days":[  
            {  
               "date":"2016-07-22",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-23",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-24",
               "time_open":"01:02",
               "time_close":"03:06"
            }
         ],
         "holiday_days":[  
            {  
               "date":"2016-07-17"
            },
            {  
               "date":"2016-07-18"
            },
            {  
               "date":"2016-07-19"
            },
            {  
               "date":"2016-07-20"
            }
         ],
         "country_name":"Andorra",
         "distance":4641853.9516521,
         "image":"http:\/\/localhost.com\/magento19\/media\/simistorelocator\/images\/3\/6\/3_6.jpg"
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

Get Storelocations List By Location, key including:
lng, lat



## Get Storelocations by Tag

```shell
curl "https://abc.com/simiconnector/rest/v2/storelocations?tag=tag5" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "2"
   ],
   "storelocations":[  
      {  
         "simistorelocator_id":"2",
         "name":"Store 2",
         "address":"address1",
         "city":"billing city",
         "country":"GB",
         "zipcode":"post code",
         "state":null,
         "state_id":null,
         "email":null,
         "phone":null,
         "fax":null,
         "description":"",
         "status":"1",
         "sort":"0",
         "link":null,
         "latitude":"51.49542",
         "longtitude":"-3.455298",
         "monday_status":"1",
         "monday_open":"00:00",
         "monday_close":"00:00",
         "tuesday_status":"1",
         "tuesday_open":"00:00",
         "tuesday_close":"00:00",
         "wednesday_status":"1",
         "wednesday_open":"00:00",
         "wednesday_close":"00:00",
         "thursday_status":"1",
         "thursday_open":"00:00",
         "thursday_close":"00:00",
         "friday_status":"1",
         "friday_open":"00:00",
         "friday_close":"00:00",
         "saturday_status":"1",
         "saturday_open":"00:00",
         "saturday_close":"00:00",
         "sunday_status":"1",
         "sunday_open":"00:00",
         "sunday_close":"00:00",
         "zoom_level":"6",
         "image_icon":"photo1468804718629.png",
         "entity_id":"262",
         "content_type":"5",
         "item_id":"2",
         "store_view_id":"1",
         "special_days":[  
            {  
               "date":"2016-07-22",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-23",
               "time_open":"01:02",
               "time_close":"03:06"
            },
            {  
               "date":"2016-07-24",
               "time_open":"01:02",
               "time_close":"03:06"
            }
         ],
         "holiday_days":[  
            {  
               "date":"2016-07-17"
            },
            {  
               "date":"2016-07-18"
            },
            {  
               "date":"2016-07-19"
            },
            {  
               "date":"2016-07-20"
            }
         ],
         "country_name":"United Kingdom",
         "distance":0,
         "image":"http:\/\/localhost.com\/magento19\/media\/simistorelocator\/images\/2\/2\/2_1.png"
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

Get Storelocations List By Tag
