# Giftvoucher (Customer Credit)

## Customer Giftvoucher Credit Properties

Attributes| Type| Description
--------- | ------- | -----------
credit_id | int | Credit Id
balance   | int | Credit Balance
currency  | string | Credit Balance Currency
listcode  | array | List Code of Customer
listcode.customer_voucher_id | int | Customer Voucher Id
listcode.voucher_id | int | Giftcode Id
listcode.added_date | date | Added Datetime
listcode.recipient_name | string | Recipient Name
listcode.gift_code | string | Gift Code
listcode.balance | int | Giftcode Balance
listcode.status | int | Giftcode Status
listcode.expired_at | date | Expired At
listcode.customer_check_id | int | Customer Id Owned Giftcode
listcode.recipient_email | string | Recipient Email
listcode.action | array | Actions of Giftcode
history   | array | History Change Credit Balance
history.history_id | int | History Id
history.action | string | Action History
history.currency_balance | int | Currency Balance
history.giftcard_code | string | Giftcard Code Used
history.order_id | int | Order Id
history.order_number | int | Order Number
history.balance_change | int | Amount Balance Change
history.created_date | date | Created Date


## View Customer Giftvoucher Credit Information

```shell
curl "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits/self" \
  -H "Authorization: Bearer <token>"
```
> The above command returns JSON structured like this:

```json
{
  "simicustomercredit": {
    "credit_id": "1",
    "customer_id": "150",
    "balance": "150.0000",
    "currency": "USD",
    "listcode": [
      {
        "customer_voucher_id": "9",
        "customer_id": "150",
        "voucher_id": "14",
        "added_date": "2017-07-20 04:05:42",
        "recipient_name": "",
        "gift_code": "6961-D66DA-NXZU",
        "balance": "500.0000",
        "currency": "USD",
        "status": "2",
        "expired_at": "2018-07-20 04:05:42",
        "customer_check_id": "150",
        "recipient_email": "",
        "customer_email": "test@simicart.com"
      }
    ],
    "history": [
       {
            "history_id": "1",
            "customer_id": "150",
            "action": "Adminupdate",
            "currency_balance": "100.0000",
            "giftcard_code": "",
            "order_id": null,
            "order_number": "",
            "balance_change": "100.0000",
            "currency": "USD",
            "base_amount": "0.0000",
            "amount": "0.0000",
            "created_date": "2017-07-19 07:35:00"
          },
          {
            "history_id": "2",
            "customer_id": "150",
            "action": "Redeem",
            "currency_balance": "150.0000",
            "giftcard_code": "GIFT-QFYC-8G9YGG",
            "order_id": null,
            "order_number": "",
            "balance_change": "50.0000",
            "currency": "USD",
            "base_amount": "0.0000",
            "amount": "0.0000",
            "created_date": "2017-07-20 02:14:17"
          }
    ] 
  }
}
```

This endpoint retrieves Customer Giftvoucher Credit Information

## Add Redeem Giftcode to Change Balance Credit

```sell
curl PUT: "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits/addredeem" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "0711-3CHQF-CTYA"
  }"
```

> The above command returns JSON structured like this:

```json
{
  "simicustomercredit": {
      "credit_id": "1",
      "customer_id": "150",
      "balance": "150.0000",
      "currency": "USD",
      "listcode": [
          {
              "customer_voucher_id": "2",
              "customer_id": "150",
              "voucher_id": "2",
              "added_date": "2017-07-19 08:22:05",
              "recipient_name": "Cody",
              "gift_code": "0711-3CHQF-CTYA",
              "balance": "0.0000",
              "currency": "USD",
              "status": "4",
              "expired_at": "2018-07-19 07:00:00",
              "customer_check_id": "150",
              "recipient_email": "cody@simicart.com",
              "customer_email": "peter@simicart.com"
          },
          {
              "customer_voucher_id": "1",
              "customer_id": "150",
              "voucher_id": "1",
              "added_date": "2017-07-19 14:51:46",
              "recipient_name": "cody@simicart.com",
              "gift_code": "GIFT-QFYC-8G9YGG",
              "balance": "0.0000",
              "currency": "USD",
              "status": "4",
              "expired_at": "2017-07-20 07:00:00",
              "customer_check_id": "0",
              "recipient_email": "Cody",
              "customer_email": "Frank"
          }
      ],
      "history": [
          {
              "history_id": "1",
              "customer_id": "150",
              "action": "Adminupdate",
              "currency_balance": "100.0000",
              "giftcard_code": "",
              "order_id": null,
              "order_number": "",
              "balance_change": "100.0000",
              "currency": "USD",
              "base_amount": "0.0000",
              "amount": "0.0000",
              "created_date": "2017-07-19 07:35:00"
          },
          {
              "history_id": "2",
              "customer_id": "150",
              "action": "Redeem",
              "currency_balance": "150.0000",
              "giftcard_code": "GIFT-QFYC-8G9YGG",
              "order_id": null,
              "order_number": "",
              "balance_change": "50.0000",
              "currency": "USD",
              "base_amount": "0.0000",
              "amount": "0.0000",
              "created_date": "2017-07-20 02:14:17"
          },
          {
              "history_id": "3",
              "customer_id": "150",
              "action": "Redeem",
              "currency_balance": "250.0000",
              "giftcard_code": "0711-3CHQF-CTYA",
              "order_id": null,
              "order_number": "",
              "balance_change": "100.0000",
              "currency": "USD",
              "base_amount": "0.0000",
              "amount": "0.0000",
              "created_date": "2017-07-25 09:36:41"
          }
      ],
      "message": "Gift card 0711-3CHQF-CTYA was successfully redeemed"
  }  
}
```

## Add Giftcode to My List

```shell
curl PUT: "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits/addlist" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "xmas-TZA-8PJXEI"
  }"
```

> The above command returns JSON structured like this:

```json
{
  "simicustomercredit": {
      "credit_id": "1",
      "customer_id": "150",
      "balance": "250.0000",
      "currency": "USD",
      "listcode": [
          {
              "customer_voucher_id": "10",
              "customer_id": "150",
              "voucher_id": "15",
              "added_date": "2017-07-25 16:51:52",
              "recipient_name": "",
              "gift_code": "xmas-TZA-8PJXEI",
              "balance": "200.0000",
              "currency": "USD",
              "status": "2",
              "expired_at": "2017-07-26 07:00:00",
              "customer_check_id": "0",
              "recipient_email": "",
              "customer_email": ""
          }
      ],
      "history": [],
      "message": "The gift code has been added to your list successfully."
  }
}
```

## Send Email Giftcode to Friend

```shell
curl PUT: "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits/sendemail" \
  -H "Authorization: Bearer <token>"
  -d "{
  "voucher_id" : "2"
  }"
```

> The above command returns JSON structured like this:

```json
{
    "message": {
        "success": "The Gift Card email has been sent successfully."
    }
}
```

## Remove Giftcodes from customer's account

```shell
curl DELETE : "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits" \
  -H "Authorization: Bearer <token>"
  -d "{
  "customer_voucher_id" : "2"
  }"
```

```json
{
    "message": {
        "success": "Gift Code was successfully removed !"
    }
}
```