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
wishlist_count | int | Number of wishlist items



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
	"suffix":"My Suffix",
	"news_letter":"1"
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
      "taxvat":null,
      "wishlist_count": 1
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
      "taxvat":null,
      "wishlist_count": 1
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


## Create Password (Reset password)

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/customers/createpassword?password=123456&rptoken=mIUKneTlRwJIIQVKL9TYPdeUkVhvahXs" \
  -H "Authorization: Bearer <token>" 
```

> The above command returns JSON structured like this:

```json
{  
   "customer":{  
      "website_id":"1"
   },
   "message":[  
      "You updated your password."
   ]
}
```

This API is to Reset password, with new password filled by user, and rptoken get from the email sent to user after user clicked reset password button.

## Renew Customer Session

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/addresses?email=test@simicart.com&simi_hash=123456" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like the normal request with no user name/password.

```json

```

Add customer email and simi_hash (get from login/register/profile/social login APIs) to renew customer session with any request.

## Social Platform Login/Register


```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/sociallogins?email=cody@gmail.com&uid=11771924354773903187&firstname=Hai&lastname=Nguyen&providerId=google.com&hash=UzqZwpV6WMXzuP2GhnHF3sgcbS92" \
  -H "Authorization: Bearer <token>" 
```

> The above command returns JSON structured like this:

```json
{
   "customer": {
      "entity_id": "6",
      "website_id": "1",
      "email": "life4dieth2@gmail.com",
      "group_id": "1",
      "increment_id": null,
      "store_id": "1",
      "created_at": "2019-04-02 04:35:17",
      "updated_at": "2019-04-02 04:35:17",
      "is_active": "1",
      "disable_auto_group_change": "0",
      "created_in": "Default Store View",
      "prefix": null,
      "firstname": "Hai Nguyen",
      "middlename": null,
      "lastname": "Hai Nguyen",
      "suffix": null,
      "dob": null,
      "password_hash": "3605332a87f069006a5effb6af51a610b32779b030b9fde3ab4d54b54962b6be:oqmOXwB1EHuVo8XMU5r0Lmxsg9jMp5hj:1",
      "rp_token": null,
      "rp_token_created_at": null,
      "default_billing": null,
      "default_shipping": null,
      "taxvat": null,
      "confirmation": null,
      "gender": null,
      "failures_num": "0",
      "first_failure": null,
      "lock_expires": null,
      "news_letter": "0",
      "simi_hash": "tk_9ee6152f2eb4c7c14556c38b4133454a80340f42969d34c89d1f2dae698f9fad"
   }
}
```

This API is to Login and Register Customer By Email get From Social Platforms

Required params:

uid - string - User Id of the social network account

providerId - social network provider - string - eg. google, google.com, facebook, ...

Optional params:

email - Customer email

firstname - Customer First name

lastname - Customer Last name

hash - Customer password