# Giftvoucher (Gift Card)

## View List of Gift Card Product

### HTTP Request

`GET /rest/simigiftcards`

```shell
curl "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simigiftcards" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "all_ids": [
    "919",
    "925"
  ],
  "simigiftcards": [
    {
      "entity_id" : "919",    
      "_comment" : ".....",
      "app_prices": {
        "minimal_price": 0,
        "product_from_label": "From",
        "product_to_label": "To",
        "show_from_to_tax_price": 0,
        "show_ex_in_price": 1,
        "from_price_excluding_tax": {
          "label": "Excl. Tax",
          "price": 100
        },
        "from_price_including_tax": {
          "label": "Incl. Tax",
          "price": 108.25
        },
        "to_price_excluding_tax": {
          "label": "Excl. Tax",
          "price": 500
        },
        "to_price_including_tax": {
          "label": "Incl. Tax",
          "price": 541.25
        },
        "from_price": 108.25,
        "to_price": 541.25
      },
      "_comment" : "....."
    },
    {
      "entity_id" : "925",
      "_comment" : ".....",
      "app_prices": {
        "minimal_price": 1,
        "show_ex_in_price": 1,
        "price_excluding_tax": {
          "price_label": "Excl. Tax",
          "price": 40.00
        },
        "price_including_tax": {
          "price_label": "Incl. Tax",
          "price": 43.30
        }
      },
      "_comment" : "....."
    }    
  ],
  "total": 2,
  "page_size": 15,
  "from": 0,
  "layers": [],
  "orders": []
}
```
This endpoint retrieves a list gift card product

### Both Exclude Tax and Include Tax Properties

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


## View A Gift Card Product

### HTTP Request

`GET /rest/simigiftcards/<id>`

```shell
curl "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simigiftcards/919" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "simigiftcard": {
    "entity_id": "923",
    "entity_type_id": "4",
    "attribute_set_id": "4",
    "type_id": "simigiftvoucher",
    "sku": "dsdsadsa",
    "has_options": "0",
    "required_options": "0",
    "created_at": "2017-07-28T20:22:32-07:00",
    "updated_at": "2017-07-29 03:22:32",
    "weight": "123.0000",
    "name": "Gift Card Dropdown Percent",
    "meta_title": null,
    "meta_description": null,
    "url_key": null,
    "custom_design": null,
    "page_layout": null,
    "options_container": "container2",
    "gift_message_available": null,
    "gift_wrapping_available": "0",
    "simigift_template_ids": [
      {
        "giftcard_template_id": "1",
        "template_name": "Amazon Gift Card Style",
        "style_color": "#DC8C71",
        "text_color": "#949392",
        "caption": "Gift Card",
        "notes": null,
        "images": [
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/default.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_01.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_02.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_03.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_04.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_05.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_06.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_07.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_08.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_09.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_10.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_11.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_12.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_13.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_14.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_15.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_16.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_17.png"
          },
          {
            "url": "http://dev-magento19.jajahub.com/media/simigiftvoucher/template/images/giftcard_amazon_18.png"
          }
        ],
        "design_pattern": "5",
        "background_img": null,
        "status": "1"
      }
    ],
    "simigift_code_sets": null,
    "status": "1",
    "visibility": "4",
    "tax_class_id": "0",
    "simigift_type": "3",
    "description": "dsa",
    "short_description": "gfdggd",
    "meta_keyword": null,
    "custom_layout_update": null,
    "simigift_price": "50,60,70,80,90",
    "simigift_dropdown": "10,20,30,40,50",
    "simigift_price_type": "3",
    "news_from_date": null,
    "news_to_date": null,
    "custom_design_from": null,
    "custom_design_to": null,
    "media_gallery": {},
    "stock_item": {},
    "is_in_stock": true,
    "is_salable": null,
    "conditions": {
      "0": {
        "giftcard_product_id": "5",
        "product_id": "923",
        "conditions_serialized": {
          "type": "salesrule/rule_condition_combine",
          "attribute": null,
          "operator": null,
          "value": "1",
          "is_value_processed": null,
          "aggregator": "all"
        },
        "simigiftcard_description": "Customers can\r\nonly use their Gift Card for orders which have Subtotal equals or is greater than\r\n$200",
        "actions_serialized": {
          "type": "salesrule/rule_condition_product_combine",
          "attribute": null,
          "operator": null,
          "value": "1",
          "is_value_processed": null,
          "aggregator": "all"
        }
      },
      "conditions_serialized": false,
      "actions_serialized": false
    },
    "additional": [],
    "images": [],
    "app_prices": {},
    "giftcard_prices": {
      "type_value": "dropdown",
      "options": [
        10,
        20,
        30,
        40,
        50
      ],
      "type_price": "percent",
      "prices_dropdown": {
        "10": 5,
        "20": 12,
        "30": 21,
        "40": 32,
        "50": 45
      }
    },
    "app_reviews": {
      "rate": 0,
      "number": 0,
      "5_star_number": 0,
      "4_star_number": 0,
      "3_star_number": 0,
      "2_star_number": 0,
      "1_star_number": 0,
      "form_add_reviews": [
        "Only registered users can write reviews"
      ]
    },
    "app_options": null,
    "wishlist_item_id": null,
    "product_label": null,
    "product_video": [
      
    ]
  }
}
```

This endpoint retrieves a gift card product

### Gift Card Properties

Attributes| Type| Description
--------- | ------- | -----------
simigift_template_ids.giftcard_template_id | int | Giftcard Template Image Id
simigift_template_ids.template_name | string | Template name
simigift_template_ids.style_color | string | Template style color
simigift_template_ids.text_color | tring | Text color
simigift_template_ids.caption | string | Template caption
simigift_template_ids.notes | string | Template Comment
simigift_template_ids.images | array | List url image
conditions | array | Gift card conditions
conditions.simigiftcard_description | string | Description Gift card condition
giftcard_prices | object | Gift Card prices
giftcard_prices.type_value | string | Type of Gift Card value (fixed or range or dropdown)
giftcard_prices.type_price | string | Type price of Gift Card (fixed or default or percent)
giftcard_prices.value | int | Gift Card value (type_value = fixed )
giftcard_prices.price | int | Gift Card price (type_value = fixed )
giftcard_prices.percent_value | int | Pecent Price of Gift Card value 
giftcard_prices.from | int | Minimum Gift Card value (type_value = range)
giftcard_prices.to | int | Maximum Gift Card value (type_value = range)
giftcard_prices.options | array | Gift Card value options (type_value = dropdown)
giftcard_prices.prices_dropdown | array | Gift Card price options (type_value = dropdown)


Type Price of Gift Card

- fixed : Fixed price

- default : Same as Gift Card value

- percent : Percent of Gift Card value

## Upload Custom Image Gift Card

### HTTP Request

`POST /rest/v2/simigiftcards/uploadimage`

Use form-data to upload image

```shell
curl POST : "http://dev-magento19.jajahub.com/simiconnector/rest/v2/simigiftcards/uploadimage" \
  -H "Authorization: Bearer <token>"
  -d form-data {
  "key" => "image",
  "value" => "a.png"
  }
```

> The above command returns JSON structured like this:

```json
{
  "images": {
        "name": "a.png",
        "type": "image/png",
        "tmp_name": "/tmp/phpVVZ8to",
        "error": 0,
        "size": 30343,
        "path": "/data/www/dev/magento1/dev/19/media/tmp/simigiftvoucher/images/",
        "file": "a.png",
        "url": "http://dev-magento19.jajahub.com/media/tmp/simigiftvoucher/images/a.png",
        "sucess": true
    }
}
```

## Add to Card

### HTTP Request

`POST /rest/quoteitems`

```shell
curl "http://dev-magento19.jajahub.com/simiconnector/rest/v2/quoteitems" \
  -H "Authorization: Bearer <token>"
  -d {    
    "product":"906",
    "related_product":"",
    "price_amount":"100",
    "amount":"100","giftcard_template_id":"1",
    "giftcard_template_image":"1.jpg",
    "giftcard_use_custom_image":"1",
    "recipient_ship":"Yes","recipient_address":"",
    "send_friend":"1","customer_name":"Peter",
    "recipient_name":"Cody",
    "recipient_email":"cody@simicart.com",
    "message":"Cody Message",
    "notify_success":"1",
    "day_to_send":"07\/31\/2017",
    "timezone_to_send":"Asia\/Hong_Kong",
    "qty":"1"  
  }
```

> The above command returns JSON structured like this:

```json

```

### Params Properties

Attributes| Type| Description
--------- | ------- | -----------
product | int | Gift Card Product Id ( required )
qty | int | Qty Product ( required )
amount | int | Gift Card Value ( required )
price_amount | int | Gift Card Price ( required )
giftcard_template_id | int | Gift Card Template Id ( required )
giftcard_template_image | string | Gift Card Template Image Name ( required )
giftcard_use_custom_image | int | Is Use Custom Image ( 1 or 0 )
recipient_ship | int | Send through post office ( 1 or 0 )
recipient_address | string | Recipient Address
send_friend | int | Send Gift Card to friend ( 1 or 0 )
customer_name | string | Sender Name
recipient_name | string | Recipient Name
recipient_email | string | Recipient Email
message | string | Custom Message
notify_success | int | Get notification email when your friend receives Gift Card ( 1 or 0 )
day_to_send | date | Day to send
timezone_to_send | string | Timezone to send
