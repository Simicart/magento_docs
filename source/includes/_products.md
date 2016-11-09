# Products

## Product Properties

Attributes| Type| Description
--------- | ------- | -----------
entity_id | string | product id <code>read only</code>
entity_type_id | int | type id of product
attribute_set_id | string | product attribute set
type_id | int | type of product ( simple, grouped, bundle, downloadable)
sku | string | stock keeping unit
name | string | product name
created_at | datetime | created time
updated_at | datetime | updated time
has_options | string | "0" or "1" has options?
required_options| string | "0" or "1" is required options when do add cart
cat_index_position| string | position of session cart
price | string | original price of product
tax_class_id | string | tax_id of product
final_price | string | sale price of product
description | string | product description
short_description | string | product short description
images | JSON Array | list images of product
is_salable | string | product is salable

## View A Product

```shell
curl "https://abc.com/simiconnector/rest/v2/products/166" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "product":{
		"entity_id":"16",
		"entity_type_id":"10",
		"attribute_set_id":"38",
		"type_id":"simple",
		"sku":"n2610",
		"created_at":"2007-08-23T06:03:05-07:00",
		"updated_at":"2008-08-08 14:50:04",
		"has_options":"0",
		"required_options":"0",
		"name":"Nokia 2610 Phone",
		"manufacturer":"20",
		"meta_title":"Nokia 2610",
		"meta_description":"Offering advanced media and calling features without breaking the bank, The Nokia 2610 is an easy to use",
		"image":"\/n\/o\/nokia-2610-phone-2.jpg",
		"small_image":"\/n\/o\/nokia-2610-phone-2.jpg",
		"url_key":"nokia-2610-phone",
		"thumbnail":"\/n\/o\/nokia-2610-phone-2.jpg",
		"gift_message_available":"",
		"url_path":"nokia-2610-phone.html",
		"custom_design":"",
		"options_container":"container2",
		"price":"149.9900",
		"cost":"20.0000",
		"weight":"3.2000",
		"minimal_price":"149.9900",
		"description":"The Nokia 2610 is an easy to use device that combines multiple messaging options including email, instant messaging, and more. You can even download MP3 ringtones, graphics, and games straight to the phone, or surf the Internet with Cingular's MEdia Net service. It's the perfect complement to Cingular service for those even remotely interested in mobile Web capabilities in an affordable handset.<br><br>\r\n\r\n<b>Design<\/b><br>\r\nCompact and stylish, the 2610 features a candybar design sporting a bright 128 x 128 pixel display capable of displaying over 65,000 colors. Most of the phone's features and on-screen menus are controlled by a center toggle on the control pad. A standard hands-free headphone jack is provided, as are volume control keys, and there's even a \"Go-To\" button that can be assigned by the user for quick access to favorite applications. Lastly, the included speakerphone allows you to talk handsfree, and because the phone sports an internal antenna, there's nothing to snag or break off.\r\n\r\n",
		"meta_keyword":"Nokia 2610, cell, phone, ",
		"in_depth":"<ul>\r\n<ul class\"disc\">\r\n<li>Integrated camera with video recorder to capture those special moments<br><\/li>\r\n<li>Enriched data connections for complete mobile access via Email, MMS, and MEdia Net<br><\/li>\r\n<li> Personalize with downloadable MP3 and polyphonic Ring tones, Games, and Graphics<br><\/li>\r\n<li>Use AIM, Yahoo! and MSN Messenger to stay in touch on the go<br><\/li>\r\n<li>Mobile Internet browser and email<\/li>\r\n<\/ul>",
		"dimension":"4.1 x 1.7 x 0.7 inches ",
		"model":"2610",
		"activation_information":"Conditional $250 Equipment Discount Included: Your price paid includes an equipment discount of $250 that has been provided to you in exchange for either activating a new, non-substitute line of service or renewing an existing line of service with AT&T and your agreement that for the 181-day period following such activation or renewal you will: (1) pay your balance due to AT&T each month and otherwise maintain your account in good standing; (2) not disconnect this AT&T line of service; (3) not transfer this equipment to another AT&T line of service; (4) not change your AT&T service rate plan to a lower monthly service rate--this includes canceling or removing required PDA, BlackBerry, or smartphone features after your product has shipped; (5) not use this line of service to replace an existing account with AT&T. If these conditions are not met, you hereby authorize Magento to charge your credit card $250 as reimbursement of this equipment discount without need for further approval.",
		"short_description":"The words \"entry level\" no longer mean \"low-end,\" especially when it comes to the Nokia 2610. Offering advanced media and calling features without breaking the bank",
		"custom_layout_update":"",
		"color":"24",
		"status":"1",
		"tax_class_id":"2",
		"visibility":"4",
		"group_price":[
		],
		"group_price_changed":0,
		"tier_price":[
			{
            "price_id": "11",
            "website_id": "0",
            "all_groups": "1",
            "cust_group": 32000,
            "price": "12.0000",
            "price_qty": "12.0000",
            "website_price": "12.0000"
            },
		],
		"tier_price_changed":0,
		"media_gallery":{
		"images":[
			{
			"value_id":"189",
			"file":"\/n\/o\/nokia-2610-phone-2.jpg",
			"label":"",
			"position":"0",
			"disabled":"1",
			"label_default":"",
			"position_default":"0",
			"disabled_default":"1"
			},
			{
			"value_id":"127",
			"file":"\/n\/o\/nokia-2610-phone-1.jpg",
			"label":"",
			"position":"1",
			"disabled":"0",
			"label_default":"",
			"position_default":"1",
			"disabled_default":"0"
			},
			{
			"value_id":"126",
			"file":"\/n\/o\/nokia-2610-phone.jpg",
			"label":"",
			"position":"2",
			"disabled":"0",
			"label_default":"",
			"position_default":"2",
			"disabled_default":"0"
			}
		],
		"values":[
		]
		},
		"stock_item":{
			"item_id":"1",
			"product_id":"16",
			"stock_id":"1",
			"qty":"996.0000",
			"min_qty":"0.0000",
			"use_config_min_qty":"1",
			"is_qty_decimal":"0",
			"backorders":"0",
			"use_config_backorders":"1",
			"min_sale_qty":"1.0000",
			"use_config_min_sale_qty":"1",
			"max_sale_qty":"100.0000",
			"use_config_max_sale_qty":"1",
			"is_in_stock":"1",
			"low_stock_date":"0000-00-00 00:00:00",
			"notify_stock_qty":null,
			"use_config_notify_stock_qty":"1",
			"manage_stock":"0",
			"use_config_manage_stock":"1",
			"stock_status_changed_auto":"0",
			"use_config_qty_increments":"1",
			"qty_increments":"0.0000",
			"use_config_enable_qty_inc":"1",
			"enable_qty_increments":"0",
			"is_decimal_divided":"0",
			"type_id":"simple",
			"stock_status_changed_automatically":"0",
			"use_config_enable_qty_increments":"1",
			"product_name":"Nokia 2610 Phone",
			"store_id":"1",
			"product_type_id":"simple",
			"product_status_changed":true,
			"product_changed_websites":null
		},
		"is_in_stock":"1",
		"is_salable":"1",
		"images":[
			{
				"url":"https://abc.com/thumbnail.jpg",
				"position":"1"			     
			},
			{
				"url":"https://abc.com/thumbnail.jpg",
				"position":"1"																															       
			}
		],
		"app_tier_prices": [
			"Buy 1 for €92.38 (€92.38 incl. tax) each and save 94% ",
			"Buy 4 for €73.90 (€73.90 incl. tax) each and save 95% "
		]
	}
}
```

This endpoint retrieves a specific product.

### HTTP Request

`GET /rest/products/<id>`


## View List Of Products

```shell
curl "https://abc.com/simiconnector/rest/v2/products" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
	"all_ids": ["16"],
	"products": [{
		"entity_id": "16",
		"entity_type_id": "10",
		"attribute_set_id": "38",
		"type_id": "simple",
		"sku": "n2610",
		"created_at": "2007-08-23 13:03:05",
		"updated_at": "2008-08-08 14:50:04",
		"has_options": "0",
		"required_options": "0",
		"cat_index_position": "90027",
		"price": "149.9900",
		"tax_class_id": "2",
		"final_price": "149.9900",
		"minimal_price": "149.9900",
		"min_price": "149.9900",
		"max_price": "149.9900",
		"tier_price": null,
		"name": "Nokia 2610 Phone",
		"small_image": "\/n\/o\/nokia-2610-phone-2.jpg",
		"url_key": "nokia-2610-phone",
		"thumbnail": "\/n\/o\/nokia-2610-phone-2.jpg",
		"status": "1",
		"short_description": "The words \"entry level\" no longer mean \"low-end,\" especially when it comes to the Nokia 2610. Offering advanced media and calling features without breaking the bank",
		"do_not_use_category_id": true,
		"request_path": "nokia-2610-phone.html",
		"is_salable": "1",
		"stock_item": {
			"is_in_stock": "1"
		},
		"tax_percent": 0,
		"images": [{
			"url": "http:\/\/localhost.com:90\/magento\/media\/catalog\/product\/cache\/1\/small_image\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/small_image.jpg",
			"position": 1
		}]
	}],
	"total": 61,
	"page_size": "1",
	"from": 0,
	"layers": {
		"layer_filter": [{
			"attribute": "cat",
			"title": "Category",
			"filter": [{
				"value": "10",
				"label": "Furniture"
			}, {
				"value": "13",
				"label": "Electronics"
			}, {
				"value": "18",
				"label": "Apparel"
			}]
		}, {
			"attribute": "contrast_ratio",
			"title": "Contrast Ratio",
			"filter": [{
				"value": "106",
				"label": "10000:1"
			}, {
				"value": "107",
				"label": "1500:1"
			}, {
				"value": "110",
				"label": "3000:1"
			}]
		}, {
			"attribute": "price",
			"title": "Price",
			"filter": [{
				"value": "-1000",
				"label": "$0.00 - $999.99"
			}, {
				"value": "1000-2000",
				"label": "$1,000.00 - $1,999.99"
			}, {
				"value": "2000-3000",
				"label": "$2,000.00 - $2,999.99"
			}, {
				"value": "4000-",
				"label": "$4,000.00 and above"
			}]
		}, {
			"attribute": "color",
			"title": "Color",
			"filter": [{
				"value": "24",
				"label": "Black"
			}, {
				"value": "25",
				"label": "Blue"
			}, {
				"value": "59",
				"label": "Brown"
			}, {
				"value": "61",
				"label": "Gray"
			}, {
				"value": "22",
				"label": "Green"
			}, {
				"value": "26",
				"label": "Red"
			}, {
				"value": "23",
				"label": "Silver"
			}, {
				"value": "60",
				"label": "White"
			}]
		}, {
			"attribute": "computer_manufacturers",
			"title": "Brand",
			"filter": [{
				"value": "79",
				"label": "Acer"
			}, {
				"value": "77",
				"label": "Apple"
			}, {
				"value": "73",
				"label": "Dell"
			}, {
				"value": "75",
				"label": "Gateway"
			}, {
				"value": "78",
				"label": "IBM"
			}, {
				"value": "76",
				"label": "Sony"
			}, {
				"value": "74",
				"label": "Toshiba"
			}]
		}, {
			"attribute": "manufacturer",
			"title": "Manufacturer",
			"filter": [{
				"value": "117",
				"label": "AMD"
			}, {
				"value": "29",
				"label": "Apple"
			}, {
				"value": "111",
				"label": "Crucial"
			}, {
				"value": "116",
				"label": "Intel"
			}, {
				"value": "121",
				"label": "Logitech"
			}, {
				"value": "120",
				"label": "Microsoft"
			}, {
				"value": "119",
				"label": "Seagate"
			}, {
				"value": "118",
				"label": "Western Digital"
			}, {
				"value": "1",
				"label": "LG"
			}, {
				"value": "3",
				"label": "Samsung"
			}]
		}, {
			"attribute": "megapixels",
			"title": "Megapixels",
			"filter": [{
				"value": "93",
				"label": "5"
			}, {
				"value": "91",
				"label": "7"
			}, {
				"value": "90",
				"label": "8"
			}]
		}, {
			"attribute": "shoe_type",
			"title": "Shoe Type",
			"filter": [{
				"value": "52",
				"label": "Dress"
			}, {
				"value": "47",
				"label": "Golf Shoes"
			}, {
				"value": "51",
				"label": "High Heels"
			}, {
				"value": "49",
				"label": "Running"
			}, {
				"value": "97",
				"label": "Sandal"
			}, {
				"value": "53",
				"label": "Tennis"
			}]
		}]
	},
	"orders": [{
    		"key": "position",
    		"value": "Position",
    		"direction": "desc",
    		"default": "1"
    	}, {
    		"key": "name",
    		"value": "Name",
    		"direction": "asc",
    		"default": "0"
    	}, {
    		"key": "name",
    		"value": "Name",
    		"direction": "desc",
    		"default": "0"
    	}, {
    		"key": "price",
    		"value": "Price",
    		"direction": "asc",
    		"default": "0"
    	}, {
    		"key": "price",
    		"value": "Price",
    		"direction": "desc",
    		"default": "0"
    	}]
}
```

This endpoint retrieves a list of products.

### HTTP Request

`GET /rest/products`

Params with and height for images (image_width, image_height)

Search products

`GET /rest/products?filter[q]=nokia&image_height=100&image_width=100`

Get products that related to a product by Id

`GET /rest/products?filter[related_to_id]=392`

Get products via category

`GET /rest/products?filter[cat_id]=10`

Get products with layers

`GET /rest/products?filter[layer][{attribute}]={value}&filter[layer][{attribute}]={value}`

{attribute} = layers.layer_filter[index].attribute

{value} = layers.layer_filter[0].filter[index].10

Ex

`GET /rest/products?filter[layer][cat]=10&filter[layer][contrast_ratio]=106`

Get products with sort by order

`GET /rest/products?dir={direction}&order={key}`

Note that if default = "1", please up them with this API

`GET /rest/v2/products?filter[q]=no&dir=asc&order=price`