# PayPal Express

## PayPal Express Properties


## Start Paypal Express Checkout

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/ppexpressapis/start" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "ppexpressapi": 
      {  
         "url":"https:\/\/www.sandbox.paypal.com\/cgi-bin\/webscr?cmd=_express-checkout&token=EC-4PS62653C2068842V&useraction=commit",
         "review_address":"1"
      }
   
}
```
This API is to Start Paypal express payment

Open the link from url.

Check when webview open the url contain simiconnector/rest/v2/ppexpressapis/return

(example http://localhost.com/magento18/index.php/simiconnector/rest/v2/ppexpressapis/return/?token=EC-3CF98368P25276342&PayerID=6AHCYJCNWT368)

If review_address is 1, then open Address Select/Edit screen, if not, open Shipping select screen instead.

## Get Paypal Express Addresses

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/ppexpressapis/checkout_address" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "ppexpressapi":  
      {  
         "billing_address":{  
            "firstname":"Cody",
            "lastname":"Nguyen",
            "prefix":null,
            "suffix":null,
            "vat_id":null,
            "street":"",
            "city":null,
            "region":null,
            "region_id":null,
            "region_code":null,
            "postcode":null,
            "country_name":"United States",
            "country_id":"US",
            "telephone":null,
            "email":"test@simicart.com",
            "company":null,
            "fax":null,
            "latlng":"",
            "address_id":"21"
         },
         "shipping_address":{  
            "firstname":"Cody",
            "lastname":"Nguyen",
            "prefix":null,
            "suffix":null,
            "vat_id":null,
            "street":"1 Main St",
            "city":"San Jose",
            "region":"California",
            "region_id":"12",
            "region_code":"CA",
            "postcode":"95131",
            "country_name":"United States",
            "country_id":"US",
            "telephone":null,
            "email":"cody2@simicart.com",
            "company":null,
            "fax":null,
            "latlng":""
         }
      }
   
}
```
It's the same with Address editing from Onepage/Checkout as guest screen.


## Save Paypal Express Addresses

```shell
  curl -X PUT "https://abc.com/simiconnector/rest/v2/ppexpressapis/checkout_address" \
  -H "Authorization: Bearer <token>" \
  -d '{  
"b_address":{
    "firstname":"My First NameB",
    "lastname":"My Last Name",
    "prefix":"My Prefix",
    "suffix":"My Suffix",
    "street":"Cedar Street",
    "city":"Berkeley",
    "region":"12",
    "region_id":"12",
    "postcode":"94709",
    "country_name":"Bolivia",
    "country_id":"US",
    "company":"Company",
    "telephone":"0987123456",
    "fax":"123456",
    "vat_id":"123"
   },
"s_address":{
    "firstname":"My First NameB",
    "lastname":"My Last Name",
    "prefix":"My Prefix",
    "suffix":"My Suffix",
    "street":"Cedar Street",
    "city":"Berkeley",
    "region":"12",
    "region_id":"12",
    "postcode":"94709",
    "country_name":"Bolivia",
    "country_id":"US",
    "company":"Company",
    "telephone":"0987123456",
    "fax":"123456",
    "vat_id":"123"
   }
} '
  "
```

> The above command returns JSON structured like this:

```json
{
    "ppexpressapi": 
        {
            "billing_address": {
                "firstname": "My First NameB",
                "lastname": "My Last Name",
                "prefix": null,
                "suffix": null,
                "vat_id": "123",
                "street": "Cedar Street",
                "city": "Berkeley",
                "region": "California",
                "region_id": "12",
                "region_code": "CA",
                "postcode": "94709",
                "country_name": "United States",
                "country_id": "US",
                "telephone": "0987123456",
                "email": "test@simicart.com",
                "company": "Company",
                "fax": "123456",
                "latlng": "",
                "address_id": "21"
            },
            "shipping_address": {
                "firstname": "My First NameB",
                "lastname": "My Last Name",
                "prefix": null,
                "suffix": null,
                "vat_id": "123",
                "street": "Cedar Street",
                "city": "Berkeley",
                "region": "California",
                "region_id": "12",
                "region_code": "CA",
                "postcode": "94709",
                "country_name": "United States",
                "country_id": "US",
                "telephone": "0987123456",
                "email": "cody2@simicart.com",
                "company": "Company",
                "fax": "123456",
                "latlng": ""
            }
        }
    
}

```
It's the same with Address editing from Onepage/Checkout as guest screen.


## Get Paypal Express Shipping Methods

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/ppexpressapis/shipping_methods" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "ppexpressapi":{  
      "methods":[  
         {  
            "s_method_id":"58",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":5,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ]
   }
}
```
It's the same with Order screen.


## Place Paypal Express

```shell
  curl -X POST "https://abc.com/simiconnector/rest/v2/ppexpressapis/place" \
  -H "Authorization: Bearer <token>" \
  -d '{  
"s_method":{
   "method":"flatrate_flatrate"
   }   
} '
  "
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "message": "Thank you for your purchase!"
    }
}
```
Select shipping method and place Order then.
