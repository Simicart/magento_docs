# Simple & Virtual Product in App

## Prices & Options Properties

Attributes| Type| Description
--------- | ------- | -----------
app_prices.has_special_price | int | is special price in product
app_prices.show_ex_in_price | int | show exclude tax and include tax in product
app_prices.price_excluding_tax | json object | label and price
app_prices.price_including_tax | json object | label and price

app_options.custom_options | json array object | list custom options in product
app_options.custom_options.id | string | custom option id
app_options.custom_options.title | string | custom option title
app_options.custom_options.type | string | custom option type
app_options.custom_options.position | string | custom option position
app_options.custom_options.isRequired | string | custom option is required
app_options.custom_options.values | json object | list values (label and price) in custom option

## Both Exclude Tax and Include Tax

```shell
curl "https://abc.com/simiconnector/rest/v2/products/166" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",
		"app_prices": {
			"has_special_price": 0,
			"show_ex_in_price": 1,
			"price_excluding_tax": {
				"label": "Excl. Tax:",
				"price": 750
			},
			"price_including_tax": {
				"label": "Incl. Tax:",
				"price": 750
			}
		},
		"app_options": {
			"custom_options": [{
				"id": "6",
				"title": "Test",
				"type": "field",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"price_excluding_tax": {
						"label": "Excl. Tax:",
						"price": 90
					},
					"price_including_tax": {
						"label": "Incl. Tax:",
						"price": 90
					}
				}]
			}, {
				"id": "5",
				"title": "Test1",
				"type": "drop_down",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"id": "7",
					"title": "1234",
					"price_excluding_tax": {
						"label": "Excl. Tax:",
						"price": 12
					},
					"price_including_tax": {
						"label": "Incl. Tax:",
						"price": 12
					}
				}]
			}, {
				"id": "4",
				"title": "Test2",
				"type": "file",
				"position": "0",
				"isRequired": "1",
				"file_extension": "png",
				"values": [{
					"price_excluding_tax": {
						"label": "Excl. Tax:",
						"price": 134
					},
					"price_including_tax": {
						"label": "Incl. Tax:",
						"price": 134
					}
				}]
			}, {
				"id": "3",
				"title": "Test3",
				"type": "date_time",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"price_excluding_tax": {
						"label": "Excl. Tax:",
						"price": 1234
					},
					"price_including_tax": {
						"label": "Incl. Tax:",
						"price": 1234
					}
				}]
			}]
		}
	}
}
```

This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


## Exclude Tax or Include Tax

```shell
curl "https://abc.com/simiconnector/rest/v2/products/166" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",
		"app_prices": {
			"has_special_price": 0,
			"show_ex_in_price": 0,
			"price": 750
		},
		"app_options": {
			"custom_options": [{
				"id": "6",
				"title": "Test",
				"type": "field",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"price": 90
				}]
			}, {
				"id": "5",
				"title": "Test1",
				"type": "drop_down",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"id": "7",
					"title": "1234",
					"price": 12
				}]
			}, {
				"id": "4",
				"title": "Test2",
				"type": "file",
				"position": "0",
				"isRequired": "1",
				"file_extension": "png",
				"values": [{
					"price": 134
				}]
			}, {
				"id": "3",
				"title": "Test3",
				"type": "date_time",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"price": 1234
				}]
			}]
		}
	}
}
```
This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


