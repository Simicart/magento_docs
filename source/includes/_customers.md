# Customer

## Customer Properties

Attributes| Type| Description
--------- | ------- | -----------
website_id | id | Website Associated with
entity_id | id | Customer Id
entity_type_id | id | Customer Type Id
attribute_set_id | id | Customer Attribute Set
email | string | Customer Email
group_id | id | Customer Group
created_at | datetime | Created time
updated_at | datetime | Updated time
is_active | string | is Actived or Not
created_in | string | Store View Created
firstname | string | First Name
lastname | string | Last Name
password_hash | string | Pasword hash
taxvat | string | Tax Vat Number
dob | datetime | Date Of Birth



## Register

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/customers" \
  -H "Authorization: Bearer <token>" \
  -d "{
	"email":"test11@simicart.com",
	"password":"123456",
	"firstname":"My First Name",
	"lastname":"My Last Name",
	"day":"01",
	"month":"05",
	"year":"1977",
	"taxvat":"mytaxvat",
	"gender":"",
	"prefix":"My Prefix",
	"suffix":"My Suffix"
}"
```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "firstname":"My First Name",
      "lastname":"My Last Name",
      "email":"test11@simicart.com",
      "dob":"1977-05-01 00:00:00",
      "taxvat":"mytaxvat",
      "prefix":"My Prefix",
      "suffix":"My Suffix",
      "password":"123456",
      "password_hash":"d7951e4e12a14f7481e173b048f65c4c:aC6XMnjNFkqbWVUqBSLSNylXcoV2lEyy",
      "password_confirmation":null,
      "store_id":"1",
      "group_id":"1",
      "entity_type_id":"1",
      "parent_id":0,
      "created_at":"2016-05-25 08:04:56",
      "updated_at":"2016-05-25 08:04:56",
      "created_in":"English",
      "website_id":"1",
      "disable_auto_group_change":"0",
      "dob_is_formated":true,
      "confirmation":null,
      "entity_id":"147"
   },
   "message":[  
      "Thank you for registering with English store"
   ]
}
```
This API is to register a customer.

## Login

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/customers/login?email=test@simicart.com&password=123456" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "website_id":"1",
      "entity_id":"137",
      "entity_type_id":"1",
      "attribute_set_id":"0",
      "email":"test@simicart.com",
      "group_id":"1",
      "increment_id":null,
      "store_id":"1",
      "created_at":"2016-05-23T20:22:30-07:00",
      "updated_at":"2016-05-24 03:22:30",
      "is_active":"1",
      "disable_auto_group_change":"0",
      "created_in":"English",
      "firstname":"Cody",
      "lastname":"Nguyen",
      "password_hash":"2bb46761550eeb075761d00eae4e839c:zwtnSXgqdnHdoveyhsmAfrJPfZhAhxVQ",
      "taxvat":null
   }
}
```

This API is to start a customer session.

## Logout

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/customers/logout" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "website_id":"1",
      "entity_id":"137",
      "entity_type_id":"1",
      "attribute_set_id":"0",
      "email":"test@simicart.com",
      "group_id":"1",
      "increment_id":null,
      "store_id":"1",
      "created_at":"2016-05-23T20:22:30-07:00",
      "updated_at":"2016-05-24 03:22:30",
      "is_active":"1",
      "disable_auto_group_change":"0",
      "created_in":"English",
      "firstname":"Cody",
      "lastname":"Nguyen",
      "password_hash":"2bb46761550eeb075761d00eae4e839c:zwtnSXgqdnHdoveyhsmAfrJPfZhAhxVQ",
      "taxvat":null
   }
}
```


This API is to End a Customer Session and return previous Profile.


## View A Customer (get Profile)

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/customers/profile" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "website_id":"1",
      "entity_id":"137",
      "entity_type_id":"1",
      "attribute_set_id":"0",
      "email":"test@simicart.com",
      "group_id":"1",
      "increment_id":null,
      "store_id":"1",
      "created_at":"2016-05-23T20:22:30-07:00",
      "updated_at":"2016-05-24 03:22:30",
      "is_active":"1",
      "disable_auto_group_change":"0",
      "created_in":"English",
      "firstname":"Cody",
      "lastname":"Nguyen",
      "password_hash":"2bb46761550eeb075761d00eae4e839c:zwtnSXgqdnHdoveyhsmAfrJPfZhAhxVQ",
      "taxvat":null
   }
}
```

This one Return Customer profile.


## Edit Customer (Change Profile Information)

```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/customers" \
  -H "Authorization: Bearer <token>" \
  -d '{
		"email":"test2@simicart.com",
		"change_password":"1",
		"old_password":"123456",
		"new_password":"1234567",
		"com_password":"1234567",
		"firstname":"First",
		"lastname":"Last",
		"day":"05",
		"month":"02",
		"year":"1991",
		"taxvat":"",
		"gender":"",
		"prefix":"My Prefix",
		"suffix":"My Suffix"
	}'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "website_id":"1",
      "entity_id":"139",
      "entity_type_id":"1",
      "attribute_set_id":"0",
      "email":"test2@simicart.com",
      "group_id":"1",
      "increment_id":null,
      "store_id":"1",
      "created_at":"2016-05-24T07:30:55+00:00",
      "updated_at":"2016-05-25 08:05:57",
      "is_active":"1",
      "disable_auto_group_change":"0",
      "created_in":"English",
      "firstname":"First",
      "lastname":"Last",
      "password_hash":"7856856c2e67dcd8e093ee0333bf781d:YJhRGRgavrYy1oCMxk6YuwV8ZleaKZVv",
      "rp_token":"4aad212425b7da83027ca69db7581392",
      "dob":"1991-02-05 00:00:00",
      "rp_token_created_at":"2016-05-25 07:53:01",
      "change_password":1,
      "password":"1234567",
      "password_confirmation":"1234567",
      "confirmation":null,
      "parent_id":0,
      "dob_is_formated":true
   },
   "message":[  
      "The account information has been saved."
   ]
}
```

This API is to edit Customer Profile.

### HTTP Request

`GET /rest/products/<id>`


## Forget Password

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/customers/forgetpassword?email=test2@simicart.com" \
  -H "Authorization: Bearer <token>" 
```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "website_id":"1"
   },
   "message":[  
      "If there is an account associated with test2@simicart.com you will receive an email with a link to reset your password."
   ]
}
```

This API is to Send Password reset Email

