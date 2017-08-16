# Giftvoucher (Gift Code)

## View A Gift Code

### HTTP Request

`GET /rest/simigiftcsode/<id>`

```shell
curl "http://dev-magento19.jajahub.com/simiconnector/rest/v2/simigiftcodes/2" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "simigiftcode": {
        "giftvoucher_id": "30",
        "gift_code": "1193-8UDMY-BJQK",
        "balance": "30.0000",
        "currency": "USD",
        "status": "1",
        "expired_at": "Aug 14, 2018",
        "customer_id": "150",
        "customer_name": "frank simi",
        "customer_email": "test@simicart.com",
        "recipient_name": "",
        "recipient_email": "",
        "recipient_address": null,
        "message": null,
        "store_id": "1",
        "conditions_serialized": "a:6:{s:4:\"type\";s:32:\"salesrule/rule_condition_combine\";s:9:\"attribute\";N;s:8:\"operator\";N;s:5:\"value\";s:1:\"1\";s:18:\"is_value_processed\";N;s:10:\"aggregator\";s:3:\"all\";}",
        "day_to_send": null,
        "is_sent": "0",
        "shipped_to_customer": "0",
        "created_form": null,
        "template_id": null,
        "description": null,
        "giftvoucher_comments": null,
        "email_sender": "0",
        "notify_success": "0",
        "giftcard_custom_image": "0",
        "giftcard_template_id": "1",
        "giftcard_template_image": "default.png",
        "actions_serialized": "a:6:{s:4:\"type\";s:40:\"salesrule/rule_condition_product_combine\";s:9:\"attribute\";N;s:8:\"operator\";N;s:5:\"value\";s:1:\"1\";s:18:\"is_value_processed\";N;s:10:\"aggregator\";s:3:\"all\";}",
        "timezone_to_send": null,
        "day_store": null,
        "set_id": null,
        "used": null,
        "is_deleted": false,
        "added_date": "Aug 14, 2017",
        "currency_symbol": "$",
        "actions": [
            "Remove"
        ],
        "history": [
            {
                "history_id": "66",
                "giftvoucher_id": "30",
                "action": "1",
                "created_at": "Aug 16, 2017",
                "amount": "30.0000",
                "currency": "USD",
                "status": "1",
                "comments": "Created for order 145000444",
                "order_increment_id": "145000444",
                "order_item_id": "1308",
                "order_amount": "30.0000",
                "extra_content": "Created by customer frank simi",
                "balance": "30.0000",
                "customer_id": "150",
                "customer_email": "test@simicart.com",
                "currency_symbol": "$"
            }
        ]
    }
}
```

This endpoint retrieves a gift code

### Gift Code Properties

Attributes| Type| Description
--------- | ------- | -----------
giftvoucher_id | int | Gift Code Id
gift_code | string | Gift Code
balance | int | Gift Code Balance
currency | string | Gift Code Currency
status | int | Gift Code Status
expired_at | datetime | Expired At
customer_name | string | Customer Name
customer_email | string | Customer Email
recipient_name | string | Recipicent Name
recipient_email | string | Recipicent Email
recipient_address | string | Recipient Address
message | string | Message Content
conditions_serialized | array | Gift Code Conditions
day_to_send | date | Day to Send
is_sent | int  | Send to Customer
shipped_to_customer | int | Shipment Tracking
description | string | Gift Code Description Condition
giftvoucher_comments | string | Gift Code Comment
giftcard_custom_image | string | Gift Card Custom Image
timezone_to_send | string | Timezone to Send
history | array | Gift Code History
history.history_id | int | History Id
history.action | int | History Action
history.created_at | date | Create At
history.status | int | Gift Code Status
history.order_increment_id | int | Order Increment Id
history.extra_content | string | Action Created by
history.balance | int | Gift Code History Balance

Gift Code Status

- 1 : Pending
- 2 : Active
- 3 : Disable
- 4 : Used
- 5 : Expired
- 6 : Delete

History Action

- 1 : Create
- 2 : Update
- 3 : Mass Update
- 4 : Email
- 5 : Spen Order
- 6 : Refund
- 7 : Redeem

## Check Information Gift Code

### HTTP Request

`POST /rest/checkgiftcodes`

```shell
curl POST "http://dev-magento19.jajahub.com/simiconnector/rest/v2/checkgiftcodes" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "1193-8UDMY-BJQK"
  }"
```

> The above command returns JSON structured like this:

```json
{
    "giftvoucher_id": "30",
    "gift_code": "1193-8UDMY-BJQK",
    "balance": "30.0000",
    "currency": "USD",
    "status": "1",
    "expired_at": "Aug 14, 2018",
    "customer_id": "150",
    "customer_name": "frank simi",
    "customer_email": "test@simicart.com",
    "recipient_name": "",
    "recipient_email": "",
    "recipient_address": null,
    "message": null,
    "store_id": "1",
    "conditions_serialized": "a:6:{s:4:\"type\";s:32:\"salesrule/rule_condition_combine\";s:9:\"attribute\";N;s:8:\"operator\";N;s:5:\"value\";s:1:\"1\";s:18:\"is_value_processed\";N;s:10:\"aggregator\";s:3:\"all\";}",
    "day_to_send": "Aug 16, 2017",
    "is_sent": "0",
    "shipped_to_customer": "0",
    "created_form": null,
    "template_id": null,
    "description": null,
    "giftvoucher_comments": null,
    "email_sender": "0",
    "notify_success": "0",
    "giftcard_custom_image": "0",
    "giftcard_template_id": "1",
    "giftcard_template_image": "default.png",
    "actions_serialized": "a:6:{s:4:\"type\";s:40:\"salesrule/rule_condition_product_combine\";s:9:\"attribute\";N;s:8:\"operator\";N;s:5:\"value\";s:1:\"1\";s:18:\"is_value_processed\";N;s:10:\"aggregator\";s:3:\"all\";}",
    "timezone_to_send": null,
    "day_store": "Aug 16, 2017",
    "set_id": null,
    "used": null
}
```