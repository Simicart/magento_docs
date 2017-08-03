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
    "giftvoucher_id": "2",
    "gift_code": "0711-3CHQF-CTYA",
    "balance": "0.0000",
    "currency": "USD",
    "status": "4",
    "expired_at": "2018-07-19 00:00:00",
    "customer_id": "150",
    "customer_name": "Peter",
    "customer_email": "peter@simicart.com",
    "recipient_name": "Cody",
    "recipient_email": "cody@simicart.com",
    "recipient_address": "mr Test Simi\r\nsimicart\r\nha noi\r\n\r\n\r\n\r\n\r\nla thanh,  Arkansas, Giojhh\r\nUnited States\r\nT: 56668556\r\n\r\n",
    "message": "Test Message",
    "store_id": "1",
    "conditions_serialized": {
      "type": "salesrule/rule_condition_combine",
      "attribute": null,
      "operator": null,
      "value": "1",
      "is_value_processed": null,
      "aggregator": "all",
      "conditions": [
        {
          "type": "salesrule/rule_condition_address",
          "attribute": "base_subtotal",
          "operator": ">=",
          "value": "100",
          "is_value_processed": false
        }
      ]
    },
    "day_to_send": "2017-07-20",
    "is_sent": "2",
    "shipped_to_customer": "0",
    "created_form": null,
    "template_id": null,
    "description": "Describe conditions applied to shopping cart when using this gift code",
    "giftvoucher_comments": "Test Comment",
    "email_sender": "0",
    "notify_success": "1",
    "giftcard_custom_image": "0",
    "giftcard_template_id": "1",
    "giftcard_template_image": "default.png",
    "actions_serialized": {
      "type": "salesrule/rule_condition_product_combine",
      "attribute": null,
      "operator": null,
      "value": "1",
      "is_value_processed": null,
      "aggregator": "all",
      "conditions": [
        {
          "type": "salesrule/rule_condition_product",
          "attribute": "quote_item_price",
          "operator": ">=",
          "value": "100",
          "is_value_processed": false
        }
      ]
    },
    "timezone_to_send": "America/Los_Angeles",
    "day_store": "2017-07-20 00:00:00",
    "set_id": null,
    "used": null,
    "is_deleted": false,
    "history": [
      {
        "history_id": "2",
        "giftvoucher_id": "2",
        "action": "1",
        "created_at": "2017-07-19 08:22:05",
        "amount": "100.0000",
        "currency": "USD",
        "status": "1",
        "comments": "Created for order 145000428",
        "order_increment_id": "145000428",
        "order_item_id": "1284",
        "order_amount": "90.0000",
        "extra_content": "Created by customer frank simi",
        "balance": "100.0000",
        "customer_id": "150",
        "customer_email": "test@simicart.com"
      },
      {
        "history_id": "7",
        "giftvoucher_id": "2",
        "action": "2",
        "created_at": "2017-07-19 08:23:03",
        "amount": "100.0000",
        "currency": "USD",
        "status": "2",
        "comments": "Active when order is complete",
        "order_increment_id": "",
        "order_item_id": "1284",
        "order_amount": "0.0000",
        "extra_content": null,
        "balance": "100.0000",
        "customer_id": null,
        "customer_email": null
      },
      {
        "history_id": "14",
        "giftvoucher_id": "2",
        "action": "2",
        "created_at": "2017-07-19 08:47:44",
        "amount": "100.0000",
        "currency": "USD",
        "status": "2",
        "comments": null,
        "order_increment_id": "",
        "order_item_id": null,
        "order_amount": "0.0000",
        "extra_content": "Updated by admin",
        "balance": "100.0000",
        "customer_id": null,
        "customer_email": null
      },
      {
        "history_id": "25",
        "giftvoucher_id": "2",
        "action": "2",
        "created_at": "2017-07-24 08:14:32",
        "amount": "100.0000",
        "currency": "USD",
        "status": "2",
        "comments": "Test Comment",
        "order_increment_id": "",
        "order_item_id": null,
        "order_amount": "0.0000",
        "extra_content": "Updated by admin",
        "balance": "100.0000",
        "customer_id": null,
        "customer_email": null
      },
      {
        "history_id": "26",
        "giftvoucher_id": "2",
        "action": "7",
        "created_at": "2017-07-25 09:36:41",
        "amount": "100.0000",
        "currency": "USD",
        "status": "2",
        "comments": "Redeem to Gift Card credit balance",
        "order_increment_id": null,
        "order_item_id": null,
        "order_amount": "0.0000",
        "extra_content": "Redeemed by Mr frank simi",
        "balance": "0.0000",
        "customer_id": "150",
        "customer_email": "test@simicart.com"
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
  "giftcode" : "0711-3CHQF-CTYA"
  }"
```

> The above command returns JSON structured like this:

```json
{
    "giftvoucher_id": "2",
    "gift_code": "0711-3CHQF-CTYA",
    "balance": "0.0000",
    "currency": "USD",
    "status": "4",
    "expired_at": "2018-07-19 00:00:00",
    "customer_id": "150",
    "customer_name": "Peter",
    "customer_email": "peter@simicart.com",
    "recipient_name": "Cody",
    "recipient_email": "cody@simicart.com",
    "recipient_address": "mr Test Simi\r\nsimicart\r\nha noi\r\n\r\n\r\n\r\n\r\nla thanh,  Arkansas, Giojhh\r\nUnited States\r\nT: 56668556\r\n\r\n",
    "message": "Test Message",
    "store_id": "1",
    "conditions_serialized": {
        "type": "salesrule/rule_condition_combine",
        "attribute": null,
        "operator": null,
        "value": true,
        "is_value_processed": null,
        "aggregator": "all"
    },
    "day_to_send": "2017-07-20",
    "is_sent": "2",
    "shipped_to_customer": "1",
    "created_form": null,
    "template_id": null,
    "description": "Describe conditions applied to shopping cart when using this gift code",
    "giftvoucher_comments": "Test Comment",
    "email_sender": "0",
    "notify_success": "1",
    "giftcard_custom_image": "0",
    "giftcard_template_id": "1",
    "giftcard_template_image": "default.png",
    "actions_serialized": {
        "type": "salesrule/rule_condition_product_combine",
        "attribute": null,
        "operator": null,
        "value": true,
        "is_value_processed": null,
        "aggregator": "all"
    },
    "timezone_to_send": "America/Los_Angeles",
    "day_store": "2017-07-20 00:00:00",
    "set_id": null,
    "used": null
}
```