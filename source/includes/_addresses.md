# Addresses

## Address Properties

Attributes| Type| Description
--------- | ------- | -----------
entity_id | id | Address Id
firstname | string | First Name
lastname | string | Last Name
prefix | string | Prefix
suffix | string | Suffix
vat_id | string | Vat ID
street | string | Street Name
city | string | City
region | string | State/Province Name
region_id | string | State/Provice Id
postcode | string | Zip Code
country_name | string | Country Name
country_id | string | Country Id
company | string | Company
telephone | string | Telephone
fax | string | Fax Number
telephone | string | Telephone

## Address Fields Managements (Checkout Information Management)

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/storeviews/1" \
  -H "Authorization: Bearer <token>" \
  "

```

> The above command returns JSON structured like this:

```json
{  
   "storeview":{  
      "customer":{  
         "address_option": {
            "prefix_show": "",
            "middlename_show": "",
            "suffix_show": "",
            "dob_show": "",
            "taxvat_show": null,
            "gender_show": "",
            "gender_value": [
               {
                  "label": "Male",
                  "value": "123"
               },
               {
                  "label": "Female",
                  "value": "124"
               }
            ],
            "region_state_required": "AT,CA,CH,DE,EE,ES,FI,FR,LT,LV,RO,US",
            "region_display_all": "1"
         },
         "account_option":{  
            "taxvat_show":"0"
         },
         "address_fields_config":{  
            "company_show":"opt",
            "street_show":"opt",
            "country_id_show":"opt",
            "region_id_show":"opt",
            "city_show":"opt",
            "zipcode_show":"opt",
            "telephone_show":"opt",
            "fax_show":"opt",
            "prefix_show":"opt",
            "suffix_show":"opt",
            "dob_show":"opt",
            "gender_show":"opt",
            "taxvat_show":"opt",
            "custom_fields":[  
               {  
                  "code":"text_field_sample",
                  "title":"Text Field",
                  "type":"text",
                  "required":"opt",
                  "position":"7"
               },
               {  
                  "code":"number_field_sample",
                  "title":"Number Field",
                  "type":"number",
                  "required":"req",
                  "position":"8"
               },
               {  
                  "code":"single_option_sample",
                  "title":"Sample Field Single Option",
                  "type":"single_option",
                  "required":"",
                  "option_array":[  
                     "Option Single 1",
                     "Option Single 2",
                     "Option Single 3"
                  ],
                  "position":"9"
               },
               {  
                  "code":"multi_option_sample",
                  "title":"Sample Field Multi Option",
                  "type":"multi_option",
                  "required":"opt",
                  "option_array":[  
                     "Option Multi 1",
                     "Option Multi 2",
                     "Option Multi 3",
                     "Option Multi 4",
                     "Option Multi 5"
                  ],
                  "separated_by":"%",
                  "position":"10"
               }
            ]
         }
      }
   }
}
```
Value of region_state_required:

-  If Country Id is one of the listed Values, show the state fields and make it required.

-  If not, if the value of region_display_all is 1: show the state (optional) else: hide the state field


Address fields is configured on the Storeview Config setting result. (storeview.customer.address_option)

If customer chooses to hide some fields, there will be one more field named storeview.customer.address_fields_config :

1. "opt" - Optional

2. "" - Hidden

3. "req" - Required

If there's Custom Address Fields, there'd be one more arrray at storeview.customer.address_fields_config.custom_fields

1. text : Show Text field, send with address adding/editing request, use value added with key is 'code', e g. "text_field_sample":"What Customer Type In"

2. Number Field : Show Number field, send with address adding/editing request, use value added with key is 'code', e g. "number_field_sample":"0987654321"

3. single_option : Show Single Choice Option, send with address adding/editing request, use value added with key is 'code', e g. "single_option_sample":"Option Single 1"

4. multi_option : Show Multi Choice Option, send with address adding/editing request, use value added with key is 'code', separated by the "separated_by" value, e g. "multi_option_sample":"Option Multi 1%Option Multi 3%Option Multi 5"



## Add Addresses

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/addresses" \
  -H "Authorization: Bearer <token>" \
  -d "{
		"firstname":"My First Name",
		"lastname":"My Last Name",
		"prefix":"My Prefix",
		"suffix":"My Suffix",
		"street":"Street",
		"city":"City",
		"region":"56",
		"region_id":"5",
		"postcode":"123456",
		"country_name":"Bolivia",
		"country_id":"UK",
		"company":"Company",
		"telephone":"0987123456",
		"fax":"123456",
		"vat_id":"123",
      "is_default_billing":"1",
      "is_default_shipping":"1"
}"
```

> The above command returns JSON structured like this:

```json
{  
   "Address":{  
      "entity_id":"109",
      "entity_type_id":"2",
      "firstname":"My First Name",
      "lastname":"My Last Name",
      "company":"Company",
      "street":"Street",
      "city":"City",
      "country_id":"UK",
      "region":"56",
      "postcode":"123456",
      "telephone":"0987123456",
      "fax":"123456",
      "vat_id":"123",
      "parent_id":137,
      "customer_id":"137",
      "created_at":"2016-05-27 08:02:23",
      "updated_at":"2016-05-27 08:02:23"
   }
}
```
This API is to add an address.

is_default_billing and  is_default_shipping is to set it to be the default billing/shipping address.




## View Addresses

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/addresses" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "93",
      "94",
      "95"
   ],
   "addresses":[  
      {  
         "entity_id":"93",
         "entity_type_id":"2",
         "attribute_set_id":"0",
         "increment_id":null,
         "parent_id":"137",
         "created_at":"2016-05-27 17:49:31",
         "updated_at":"2016-05-27 08:09:20",
         "is_active":"1",
         "firstname":"Cody",
         "lastname":"Nguyen",
         "prefix":null,
         "suffix":null,
         "vat_id":"vat num",
         "street":"street",
         "city":"city",
         "region":"Alabama",
         "region_id":1,
         "region_code":"AL",
         "postcode":"10000",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"098765412321",
         "email":"test@simicart.com",
         "company":"company",
         "latlng":""
      },
      {  
         "entity_id":"94",
         "entity_type_id":"2",
         "attribute_set_id":"0",
         "increment_id":null,
         "parent_id":"137",
         "created_at":"2016-05-27 10:51:01",
         "updated_at":"2016-05-27 08:09:20",
         "is_active":"1",
         "firstname":"Cody",
         "lastname":"Nguyen",
         "prefix":null,
         "suffix":null,
         "vat_id":null,
         "street":"str",
         "city":"city",
         "region":null,
         "region_id":0,
         "region_code":null,
         "postcode":"12121",
         "country_name":"United Arab Emirates",
         "country_id":"AE",
         "telephone":"01996996",
         "email":"test@simicart.com",
         "company":null,
         "latlng":""
      },
      {  
         "entity_id":"95",
         "entity_type_id":"2",
         "attribute_set_id":"0",
         "increment_id":null,
         "parent_id":"137",
         "created_at":"2016-05-28 08:57:48",
         "updated_at":"2016-05-27 08:09:20",
         "is_active":"1",
         "firstname":"Add 3",
         "lastname":"Add 3 Last",
         "prefix":null,
         "suffix":null,
         "vat_id":null,
         "street":"str 3",
         "city":"city",
         "region":"Alabama",
         "region_id":1,
         "region_code":"AL",
         "postcode":"456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"tel",
         "email":"test@simicart.com",
         "company":"company",
         "latlng":""
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

This one Return Customer Addresses.


## Edit Address

```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/addresses" \
  -H "Authorization: Bearer <token>" \
  -d '{
		"entity_id":"107",
		"firstname":"My First Name",
		"lastname":"My Last Name2",
		"prefix":"My Prefix",
		"suffix":"My Suffix",
		"vat_id":"My Vat ID1",
		"street":"Street",
		"city":"City",
		"region":"56",
		"region_id":"5",
		"postcode":"123456",
		"country_name":"USA",
		"country_id":"AT",
		"company":"Company",
		"telephone":"0987123456",
		"fax":"123456",
		"vat_id":"123",
      "created_at":"2016-05-27 08:02:23",
      "updated_at":"2016-05-27 08:02:23"
	}'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "Address":{  
      "entity_id":"107",
      "entity_type_id":"2",
      "firstname":"My First Name",
      "lastname":"My Last Name2",
      "company":"Company",
      "street":"Street",
      "city":"City",
      "country_id":"AT",
      "region":"56",
      "postcode":"123456",
      "telephone":"0987123456",
      "fax":"123456",
      "vat_id":"123",
      "parent_id":137,
      "customer_id":"137",
      "updated_at":"2016-05-27 08:07:19"
   }
}
```

This API is to edit Customer Address.

## Geocoding (Address Autofill)

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/addresses/geocoding?longitude=-99.9&latitude=38.1" \
  -H "Authorization: Bearer <token>" \
  "

```

> The above command returns JSON structured like this:

```json
{  
   "address":{  
      "street":" U.S. 283, Jetmore",
      "city":"Hodgeman County",
      "region":"Kansas",
      "region_id":"KS",
      "country_name":"United States",
      "country_id":"US",
      "postcode":"67854"
   }
}
```

This API is to get Address Information from Longtitude and Latitude
