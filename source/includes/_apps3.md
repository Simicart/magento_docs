# Bundle Product in App

## Prices & Options Properties

Attributes| Type| Description
--------- | ------- | -----------
app_prices.minimal_price | int | show as low as price (1 or 0)
app_prices.show_ex_in_price | int | show exclude tax and include tax in product
app_prices.product_from_label | string | label from
app_prices.product_to_label | string | label to
app_prices.from_price_excluding_tax | json object | label and price
app_prices.from_price_including_tax | json object | label and price
app_prices.to_price_excluding_tax | json object | label and price
app_prices.to_price_including_tax | json object | label and price
app_prices.configure | json object | object to set price when choosing options

app_options.bundle_options | json object |  bundle options in product
app_options.configurable_options.options | json object | list options in product
app_options.configurable_options.selected | json object | list options are the default


## Both Exclude Tax and Include Tax

```shell
curl "https://abc.com/simiconnector/rest/v2/products/165" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",
		"app_prices": {
			"minimal_price": 0,
			"product_from_label": "From",
			"product_to_label": "To",
			"show_from_to_tax_price": 1,
			"show_ex_in_price": 1,
			"from_price_excluding_tax": {
				"label": "Excl. Tax:",
				"price": 4999.95
			},
			"from_price_including_tax": {
				"label": "Incl. Tax:",
				"price": 4999.95
			},
			"to_price_excluding_tax": {
				"label": "Excl. Tax:",
				"price": 6348.95
			},
			"to_price_including_tax": {
				"label": "Incl. Tax:",
				"price": 6348.95
			},
			"configure": {
				"product_label": "Price as configured",
				"show_ex_in_price": 1,
				"price_excluding_tax": {
					"label": "Excl. Tax:",
					"price": 4999.95
				},
				"price_including_tax": {
					"label": "Incl. Tax:",
					"price": 4999.95
				}
			}
		},
		"app_options": {
			"bundle_options": {
				"options": {
					"21": {
						"selections": {
							"58": {
								"qty": 1,
								"customQty": "0",
								"price": 199.99,
								"priceInclTax": 0,
								"priceExclTax": 0,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "NZXT Lexa Silver Aluminum ATX Mid-Tower Case (Default)",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Case",
						"isMulti": false,
						"position": 0,
						"isRequired": "1"
					},
					"20": {
						"selections": {
							"54": {
								"qty": 1,
								"customQty": "0",
								"price": 2049.99,
								"priceInclTax": 700,
								"priceExclTax": 700,
								"priceValue": 700,
								"priceType": "0",
								"tierPrice": [],
								"name": "Intel Core 2 Extreme QX9775 3.20GHz Retail",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"55": {
								"qty": 1,
								"customQty": "0",
								"price": 98.99,
								"priceInclTax": 200,
								"priceExclTax": 200,
								"priceValue": 200,
								"priceType": "0",
								"tierPrice": [],
								"name": "Intel C2D E8400 3.0GHz Retail",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"56": {
								"qty": 1,
								"customQty": "0",
								"price": 98.99,
								"priceInclTax": 100,
								"priceExclTax": 100,
								"priceValue": 100,
								"priceType": "0",
								"tierPrice": [],
								"name": "AMD A64 X2 3800+ 2.0GHz OEM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"57": {
								"qty": 1,
								"customQty": "0",
								"price": 335.99,
								"priceInclTax": 0,
								"priceExclTax": 0,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "AMD Phenom X4 9850 Black Ed. 2.50GHz Retail",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "CPU",
						"isMulti": false,
						"position": 1,
						"isRequired": "1"
					},
					"11": {
						"selections": {
							"27": {
								"qty": 1,
								"customQty": "0",
								"price": 99.99,
								"priceInclTax": 0,
								"priceExclTax": 0,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Crucial 512MB PC4200 DDR2 533MHz Memory",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"28": {
								"qty": 1,
								"customQty": "0",
								"price": 150.99,
								"priceInclTax": 75,
								"priceExclTax": 75,
								"priceValue": 75,
								"priceType": "0",
								"tierPrice": [],
								"name": "Crucial 1GB PC4200 DDR2 533MHz Memory",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"29": {
								"qty": 1,
								"customQty": "0",
								"price": 199.99,
								"priceInclTax": 150,
								"priceExclTax": 150,
								"priceValue": 150,
								"priceType": "0",
								"tierPrice": [],
								"name": "Crucial 2GB PC4200 DDR2 533MHz Memory",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "RAM",
						"isMulti": false,
						"position": 2,
						"isRequired": "1"
					},
					"12": {
						"selections": {
							"30": {
								"qty": 1,
								"customQty": "1",
								"price": 399,
								"priceInclTax": 250,
								"priceExclTax": 250,
								"priceValue": 250,
								"priceType": "0",
								"tierPrice": [],
								"name": "Western Digital - 1TB HD - 7200RPM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"31": {
								"qty": 1,
								"customQty": "1",
								"price": 299,
								"priceInclTax": 0,
								"priceExclTax": 0,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Seagate 500GB HD - 5400RPM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Hard Drive",
						"isMulti": true,
						"position": 3,
						"isRequired": "1"
					},
					"13": {
						"selections": {
							"32": {
								"qty": 1,
								"customQty": "1",
								"price": 239.99,
								"priceInclTax": 199,
								"priceExclTax": 199,
								"priceValue": 199,
								"priceType": "0",
								"tierPrice": [],
								"name": "Logitech diNovo Edge Keyboard",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"33": {
								"qty": 1,
								"customQty": "1",
								"price": 79.99,
								"priceInclTax": 50,
								"priceExclTax": 50,
								"priceValue": 50,
								"priceType": "0",
								"tierPrice": [],
								"name": "Logitech Cordless Optical Trackman",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"34": {
								"qty": 1,
								"customQty": "1",
								"price": 59.99,
								"priceInclTax": 0,
								"priceExclTax": 0,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Microsoft Wireless Optical Mouse 5000",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"35": {
								"qty": 1,
								"customQty": "1",
								"price": 99.99,
								"priceInclTax": 0,
								"priceExclTax": 0,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Microsoft Natural Ergonomic Keyboard 4000",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Peripherals",
						"isMulti": true,
						"position": 4,
						"isRequired": "0"
					}
				},
				"selected": {
					"21": ["58"]
				},
				"bundleId": "164",
				"priceFormat": {
					"pattern": "$%s",
					"precision": 2,
					"requiredPrecision": 2,
					"decimalSymbol": ".",
					"groupSymbol": ",",
					"groupLength": 3,
					"integerRequired": 1
				},
				"basePrice": 4999.95,
				"priceType": "1",
				"specialPrice": null,
				"includeTax": false,
				"showIncludeTax": false,
				"showBothPrices": true,
				"isFixedPrice": true,
				"isMAPAppliedDirectly": false
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
curl "https://abc.com/simiconnector/rest/v2/products/165" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"product": {
		"_comment": "......",
		"app_prices": {
			"price_label": "As low as",
			"minimal_price": 1,
			"show_ex_in_price": 0,
			"price": 635.979,
			"configure": {
				"product_label": "Price as configured",
				"price": 0
			}
		},
		"app_options": {
			"bundle_options": {
				"options": {
					"17": {
						"selections": {
							"47": {
								"qty": 1,
								"customQty": "0",
								"price": 150,
								"priceInclTax": 112.5,
								"priceExclTax": 112.5,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Apevia Black X-Cruiser Case ATX Mid-Tower Case (Default)",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"48": {
								"qty": 1,
								"customQty": "0",
								"price": 199.99,
								"priceInclTax": 149.993,
								"priceExclTax": 149.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "NZXT Lexa Silver Aluminum ATX Mid-Tower Case (Default)",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Case",
						"isMulti": false,
						"position": 0,
						"isRequired": "1"
					},
					"22": {
						"selections": {
							"59": {
								"qty": 1,
								"customQty": "0",
								"price": 335.99,
								"priceInclTax": 251.993,
								"priceExclTax": 251.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "AMD Phenom X4 9850 Black Ed. 2.50GHz Retail",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"60": {
								"qty": 1,
								"customQty": "0",
								"price": 98.99,
								"priceInclTax": 74.243,
								"priceExclTax": 74.243,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Intel C2D E8400 3.0GHz Retail",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"61": {
								"qty": 1,
								"customQty": "0",
								"price": 98.99,
								"priceInclTax": 74.243,
								"priceExclTax": 74.243,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "AMD A64 X2 3800+ 2.0GHz OEM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"62": {
								"qty": 1,
								"customQty": "0",
								"price": 2049.99,
								"priceInclTax": 1537.493,
								"priceExclTax": 1537.493,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Intel Core 2 Extreme QX9775 3.20GHz Retail",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "CPU",
						"isMulti": false,
						"position": 1,
						"isRequired": "1"
					},
					"16": {
						"selections": {
							"43": {
								"qty": 1,
								"customQty": "1",
								"price": 399,
								"priceInclTax": 299.25,
								"priceExclTax": 299.25,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Western Digital - 1TB HD - 7200RPM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"44": {
								"qty": 1,
								"customQty": "1",
								"price": 299,
								"priceInclTax": 224.25,
								"priceExclTax": 224.25,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Western Digital 500GB HD - 7200RPM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"45": {
								"qty": 1,
								"customQty": "1",
								"price": 299,
								"priceInclTax": 224.25,
								"priceExclTax": 224.25,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Seagate 500GB HD - 5400RPM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"46": {
								"qty": 1,
								"customQty": "1",
								"price": 99,
								"priceInclTax": 74.25,
								"priceExclTax": 74.25,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Seagate 250GB HD - 5400RPM",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Hard Drive",
						"isMulti": false,
						"position": 2,
						"isRequired": "1"
					},
					"15": {
						"selections": {
							"40": {
								"qty": 1,
								"customQty": "0",
								"price": 99.99,
								"priceInclTax": 74.993,
								"priceExclTax": 74.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Crucial 512MB PC4200 DDR2 533MHz Memory",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"41": {
								"qty": 1,
								"customQty": "0",
								"price": 150.99,
								"priceInclTax": 113.243,
								"priceExclTax": 113.243,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Crucial 1GB PC4200 DDR2 533MHz Memory",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"42": {
								"qty": 1,
								"customQty": "0",
								"price": 199.99,
								"priceInclTax": 149.993,
								"priceExclTax": 149.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "Crucial 2GB PC4200 DDR2 533MHz Memory",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Ram",
						"isMulti": false,
						"position": 3,
						"isRequired": "1"
					},
					"14": {
						"selections": {
							"36": {
								"qty": 1,
								"customQty": "1",
								"price": 699.99,
								"priceInclTax": 524.993,
								"priceExclTax": 524.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "30\" Flat-Panel TFT-LCD Cinema HD Monitor",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"37": {
								"qty": 1,
								"customQty": "1",
								"price": 399.99,
								"priceInclTax": 299.993,
								"priceExclTax": 299.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "19\" Widescreen Flat-Panel LCD Monitor",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"38": {
								"qty": 1,
								"customQty": "1",
								"price": 699.99,
								"priceInclTax": 524.993,
								"priceExclTax": 524.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "24\" Widescreen Flat-Panel LCD Monitor",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							},
							"39": {
								"qty": 1,
								"customQty": "1",
								"price": 399.99,
								"priceInclTax": 299.993,
								"priceExclTax": 299.993,
								"priceValue": 0,
								"priceType": "0",
								"tierPrice": [],
								"name": "22\" Syncmaster LCD Monitor",
								"plusDisposition": 0,
								"minusDisposition": 0,
								"canApplyMAP": false,
								"tierPriceHtml": "\n"
							}
						},
						"title": "Monitor",
						"isMulti": true,
						"position": 4,
						"isRequired": "1"
					}
				},
				"selected": [],
				"bundleId": "165",
				"priceFormat": {
					"pattern": "$%s",
					"precision": 2,
					"requiredPrecision": 2,
					"decimalSymbol": ".",
					"groupSymbol": ",",
					"groupLength": 3,
					"integerRequired": 1
				},
				"basePrice": 0,
				"priceType": "0",
				"specialPrice": "75.0000",
				"includeTax": false,
				"showIncludeTax": true,
				"showBothPrices": false,
				"isFixedPrice": false,
				"isMAPAppliedDirectly": false
			}
		}
	}
}
```
This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


