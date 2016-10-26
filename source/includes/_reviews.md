# Reviews in App

## Reviews in product's list Properties

Attributes| Type| Description
--------- | ------- | -----------
app_reviews.rate | float | is the rating in product
app_reviews.number | float | is numbers of message that review in product

```shell
curl "https://abc.com/simiconnector/rest/v2/products" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",

		"app_reviews": {
            "rate": 3.25,
            "number": 4
        }
	}
}
```
This endpoint retrieves a list of products.

### HTTP Request

`GET /rest/products/`

## Reviews in product's detail Properties
Attributes| Type| Description
--------- | ------- | -----------
app_reviews.rate | float | is the rating in product
app_reviews.number | float | is number of message that review in product
app_reviews.5_star_number | float | is number of 5 star that rating
app_reviews.4_star_number | float | is number of 4 star that rating
app_reviews.3_star_number | float | is number of 3 star that rating
app_reviews.2_star_number | float | is number of 2 star that rating
app_reviews.1_star_number | float | is number of 1 star that rating
app_reviews.form_add_reviews | JsonArrayObject | is the form to add review.

```shell
curl "https://abc.com/simiconnector/rest/v2/products/83" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",

		"app_reviews": {
            "rate": 3,
            "number": 1,
            "5_star_number": 0,
            "4_star_number": 0,
            "3_star_number": 1,
            "2_star_number": 0,
            "1_star_number": 0,
            "form_add_reviews": [{
                "rates": [{
                    "rate_code": "Quality",
                    "rate_options": [{
                        "key": "1",
                        "value": "1"
                    }, {
                        "key": "1",
                        "value": "2"
                    }, {
                        "key": "1",
                        "value": "3"
                    }, {
                        "key": "1",
                        "value": "4"
                    }, {
                        "key": "1",
                        "value": "5"
                    }]
                }, {
                    "rate_code": "Price",
                    "rate_options": [{
                        "key": "3",
                        "value": "11"
                    }, {
                        "key": "3",
                        "value": "12"
                    }, {
                        "key": "3",
                        "value": "13"
                    }, {
                        "key": "3",
                        "value": "14"
                    }, {
                        "key": "3",
                        "value": "15"
                    }]
                }, {
                    "rate_code": "Value",
                    "rate_options": [{
                        "key": "2",
                        "value": "6"
                    }, {
                        "key": "2",
                        "value": "7"
                    }, {
                        "key": "2",
                        "value": "8"
                    }, {
                        "key": "2",
                        "value": "9"
                    }, {
                        "key": "2",
                        "value": "10"
                    }]
                }],
                "form_review": {
                    "key_1": "nickname",
                    "key_2": "title",
                    "key_3": "detail",
                    "form_key": [
                        {
                            "key": "nickname",
                            "value": "Nickname"
                        },
                        {
                            "key": "title",
                            "value": "Title"
                        },
                        {
                            "key": "detail",
                            "value": "Detail"
                        }]
                    }
                }
            }]
        }
	}
}
```
This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/83`

## List of reviews with product Id
Attributes| Type| Description
--------- | ------- | -----------
review_id | int | is the review's ID
created_at | String | is the date that reviewed the review
entity_id | int | nothing
entity_pk_value | int | nothing
status_id | int | status's review
detail_id | int | nothing
title | String | is the title's review
detail | Stirng | is the detail's review
nickname | String | is the nickname's review
customer_id | int | nothing
entity_code | String | nothing
rating_votes | JsonObject | nothing
rate_points | float | is the points that rating in this product

```shell
curl "https://abc.com/simiconnector/rest/v2/reviews?filter[product_id]=83" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"reviews": [{
    	"review_id": "112",
    	"created_at": "2008-04-18 11:12:13",
    	"entity_id": "1",
    	"entity_pk_value": "83",
    	"status_id": "1",
    	"detail_id": "112",
    	"title": "perfect and cool",
    	"detail": "nice shoes, i recommend to y'all.\r\n\r\n",
    	"nickname": "turgen",
    	"customer_id": null,
    	"entity_code": "product",
    	"rating_votes": {},
    	"rate_points": 3
    }]
    ....
}
```
This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/reviews?filter[product_id]=83`

## Add review to product's detail Properties

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/reviews" \
  -H "Authorization: Bearer <token>"
-d '{
    	"product_id": 16,
    	"ratings": {
    		"1": 4,
    		"3": 14,
    		"2": 9
    	},
    	"nickname": "max",
    	"title": "Magento mobile App",
    	"detail": "sjkdfhajksdhfjasdf"
    }'
```
> The above command returns JSON structured like this:

```json
{
    "review": {
        "product_id": 16,
        "ratings": {
            "1": 4,
            "2": 9,
            "3": 14
        },
        "nickname": "max",
        "title": "Magento mobile App",
        "detail": "sjkdfhajksdhfjasdf",
        "entity_id": "1",
        "entity_pk_value": "16",
        "status_id": 2,
        "customer_id": null,
        "store_id": "3",
        "stores": [
            "3",
            0
        ],
        "created_at": "2016-08-18 07:55:42",
        "review_id": "122"
    },
    "message": "Your review has been accepted for moderation."
}
```
This endpoint add a review in product.

### HTTP Request

`POST /rest/reviews`