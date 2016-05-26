# Configurable Product in App

## Prices & Options Properties

Attributes| Type| Description
--------- | ------- | -----------
app_prices.has_special_price | int | is special price in product
app_prices.show_ex_in_price | int | show exclude tax and include tax in product
app_prices.price_excluding_tax | json object | label and price
app_prices.price_including_tax | json object | label and price

app_options.configurable_options | json object |  configurable options in product
app_options.configurable_options.attributes | json object | list attributes options in product

app_options.custom_options | json array object | list custom options in product
app_options.custom_options.id | string | custom option id
app_options.custom_options.title | string | custom option title
app_options.custom_options.type | string | custom option type
app_options.custom_options.position | string | custom option position
app_options.custom_options.isRequired | string | custom option is required
app_options.custom_options.values | json object | list values (label and price) in custom option

## Both Exclude Tax and Include Tax

```shell
curl "https://abc.com/simiconnector/rest/v2/products/83" \
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
				"price": 15.99
			},
			"price_including_tax": {
				"label": "Incl. Tax:",
				"price": 15.99
			}
		},
		"app_options": {
			"configurable_options": {
				"attributes": {
					"501": {
						"id": "501",
						"code": "gender",
						"label": "Gender",
						"options": [{
							"id": "36",
							"label": "Mens",
							"price": "0",
							"oldPrice": "0",
							"products": ["88", "89", "90", "91", "92"]
						}, {
							"id": "35",
							"label": "Womens",
							"price": "0",
							"oldPrice": "0",
							"products": ["29", "84", "85", "86", "87"]
						}]
					},
					"502": {
						"id": "502",
						"code": "shoe_size",
						"label": "Shoe Size",
						"options": [{
							"id": "46",
							"label": "3",
							"price": "0",
							"oldPrice": "0",
							"products": ["29"]
						}, {
							"id": "45",
							"label": "4",
							"price": "0",
							"oldPrice": "0",
							"products": ["84"]
						}, {
							"id": "44",
							"label": "5",
							"price": "0",
							"oldPrice": "0",
							"products": ["85"]
						}, {
							"id": "43",
							"label": "6",
							"price": "0",
							"oldPrice": "0",
							"products": ["86"]
						}, {
							"id": "42",
							"label": "7",
							"price": "0",
							"oldPrice": "0",
							"products": ["87"]
						}, {
							"id": "41",
							"label": "8",
							"price": "0",
							"oldPrice": "0",
							"products": ["88"]
						}, {
							"id": "40",
							"label": "9",
							"price": "0",
							"oldPrice": "0",
							"products": ["89"]
						}, {
							"id": "39",
							"label": "10",
							"price": "1",
							"oldPrice": "1",
							"products": ["90"]
						}, {
							"id": "38",
							"label": "11",
							"price": "2",
							"oldPrice": "2",
							"products": ["91"]
						}, {
							"id": "37",
							"label": "12",
							"price": "3",
							"oldPrice": "3",
							"products": ["92"]
						}]
					}
				},
				"template": "$#{price}",
				"basePrice": "15.99",
				"oldPrice": "15.99",
				"productId": "83",
				"chooseText": "Choose an Option...",
				"taxConfig": {
					"includeTax": false,
					"showIncludeTax": false,
					"showBothPrices": true,
					"defaultTax": 8.25,
					"currentTax": 0,
					"inclTaxTitle": "Incl. Tax"
				}
			},
			"custom_options": {
				"custom_options": [{
					"id": "7",
					"title": "Test",
					"type": "field",
					"position": "0",
					"isRequired": "1",
					"values": [{
						"price_excluding_tax": {
							"label": "Excl. Tax:",
							"price": 12
						},
						"price_including_tax": {
							"label": "Incl. Tax:",
							"price": 12
						}
					}]
				}]
			}
		}
	}
}
```

This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


## Exclude Tax or Include Tax

```shell
curl "https://abc.com/simiconnector/rest/v2/products/83" \
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
			"price": 15.99
		},
		"app_options": {
			"configurable_options": {
				"attributes": {
					"501": {
						"id": "501",
						"code": "gender",
						"label": "Gender",
						"options": [{
							"id": "36",
							"label": "Mens",
							"price": "0",
							"oldPrice": "0",
							"products": ["88", "89", "90", "91", "92"]
						}, {
							"id": "35",
							"label": "Womens",
							"price": "0",
							"oldPrice": "0",
							"products": ["29", "84", "85", "86", "87"]
						}]
					},
					"502": {
						"id": "502",
						"code": "shoe_size",
						"label": "Shoe Size",
						"options": [{
							"id": "46",
							"label": "3",
							"price": "0",
							"oldPrice": "0",
							"products": ["29"]
						}, {
							"id": "45",
							"label": "4",
							"price": "0",
							"oldPrice": "0",
							"products": ["84"]
						}, {
							"id": "44",
							"label": "5",
							"price": "0",
							"oldPrice": "0",
							"products": ["85"]
						}, {
							"id": "43",
							"label": "6",
							"price": "0",
							"oldPrice": "0",
							"products": ["86"]
						}, {
							"id": "42",
							"label": "7",
							"price": "0",
							"oldPrice": "0",
							"products": ["87"]
						}, {
							"id": "41",
							"label": "8",
							"price": "0",
							"oldPrice": "0",
							"products": ["88"]
						}, {
							"id": "40",
							"label": "9",
							"price": "0",
							"oldPrice": "0",
							"products": ["89"]
						}, {
							"id": "39",
							"label": "10",
							"price": "1",
							"oldPrice": "1",
							"products": ["90"]
						}, {
							"id": "38",
							"label": "11",
							"price": "2",
							"oldPrice": "2",
							"products": ["91"]
						}, {
							"id": "37",
							"label": "12",
							"price": "3",
							"oldPrice": "3",
							"products": ["92"]
						}]
					}
				},
				"template": "$#{price}",
				"basePrice": "15.99",
				"oldPrice": "15.99",
				"productId": "83",
				"chooseText": "Choose an Option...",
				"taxConfig": {
					"includeTax": false,
					"showIncludeTax": true,
					"showBothPrices": false,
					"defaultTax": 8.25,
					"currentTax": 0,
					"inclTaxTitle": "Incl. Tax"
				}
			},
			"custom_options": [{
				"id": "7",
				"title": "Test",
				"type": "field",
				"position": "0",
				"isRequired": "1",
				"values": [{
					"price": 12
				}]
			}]
		}
	}
}
```
This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


