# Grouped Product in App

## Prices & Options Properties

Attributes| Type| Description
--------- | ------- | -----------
app_prices.price_label | string | label price in product
app_prices.show_ex_in_price | int | show exclude tax and include tax in product
app_prices.price_excluding_tax | json object | label and price
app_prices.price_including_tax | json object | label and price
app_options.grouped_options | json object | list grouped options in product
app_options.grouped_options.id | string |  option id
app_options.grouped_options.name | string | custom option title
app_options.grouped_options.is_salable | string | is salable (1 or 0)
app_options.grouped_options.has_special_price | int | is special price (1 or 0)
app_options.grouped_options.special_price_label | string | special label
app_options.grouped_options.price_excluding_tax | json object | object (label and price)
app_options.grouped_options.price_including_tax | json object | object (label and price)

## Both Exclude Tax and Include Tax

```shell
curl "https://abc.com/simiconnector/rest/v2/products/54" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",
		"app_prices": {
			"price_label": "Starting at:",
			"show_ex_in_price": 1,
			"price_excluding_tax": {
				"label": "Excl. Tax:",
				"price": 699.99
			},
			"price_including_tax": {
				"label": "Incl. Tax:",
				"price": 699.99
			}
		},
		"app_options": {
			"grouped_options": [{
				"id": "51",
				"name": "Ottoman",
				"is_salable": "1",
				"regular_price_label": "Regular Price",
				"regular_price": "299.9900",
				"has_special_price": 1,
				"special_price_label": "Special Price",
				"price_excluding_tax": {
					"label": "Excl. Tax:",
					"price": 100
				},
				"price_including_tax": {
					"label": "Incl. Tax:",
					"price": 100
				}
			}, {
				"id": "52",
				"name": "Chair",
				"is_salable": "1",
				"has_special_price": 0,
				"price_excluding_tax": {
					"label": "Excl. Tax:",
					"price": 129.99
				},
				"price_including_tax": {
					"label": "Incl. Tax:",
					"price": 129.99
				}
			}, {
				"id": "53",
				"name": "Couch",
				"is_salable": "1",
				"has_special_price": 0,
				"price_excluding_tax": {
					"label": "Excl. Tax:",
					"price": 599.99
				},
				"price_including_tax": {
					"label": "Incl. Tax:",
					"price": 599.99
				}
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
curl "https://abc.com/simiconnector/rest/v2/products/54" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",
		"app_prices": {
			"price_label": "Starting at:",
			"show_ex_in_price": 0,
			"price": 699.99
		},
		"app_options": {
			"grouped_options": [{
				"id": "51",
				"name": "Ottoman",
				"is_salable": "1",
				"regular_price_label": "Regular Price",
				"regular_price": "299.9900",
				"has_special_price": 1,
				"special_price_label": "Special Price",
				"price": 100
			}, {
				"id": "52",
				"name": "Chair",
				"is_salable": "1",
				"has_special_price": 0,
				"price": 129.99
			}, {
				"id": "53",
				"name": "Couch",
				"is_salable": "1",
				"has_special_price": 0,
				"price": 599.99
			}]
		}
	}
}
```
This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


