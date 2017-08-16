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

Gift Code Status :
- 1 - Pending
- 2 - Active
- 3 - Disable
- 4 - Used
- 5 - Expired
- 6 - Deleted


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
    "currency_symbol": "$",
    "listcode": [
      {
        "customer_voucher_id": "9",
        "customer_id": "150",
        "voucher_id": "14",
        "added_date": "Aug 11, 2017",
        "recipient_name": "",
        "gift_code": "6961-D66DA-NXZU",
        "balance": "500.0000",
        "currency": "USD",
        "status": "2",
        "expired_at": "Aug 31, 2017",
        "customer_check_id": "150",
        "recipient_email": "",
        "customer_email": "test@simicart.com",
        "currency_symbol": "$",
        "action": [
            "Remove"
        ],
        "giftvoucher_id": "14"
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
            "created_date": "Jul 19, 2017",
            "currency_symbol": "$"
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
            "created_date": "Jul 19, 2017",
            "currency_symbol": "$"
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
  "giftcode" : "GIFT-WMEW-LGR06F"
  }"
```

> The above command returns JSON structured like this:

```json
{
    "message": {
        "success": "Gift card \"GIFT-WMEW-LGR06F\" was successfully redeemed"
    }
}
```

## Add Giftcode to My List

```shell
curl PUT: "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits/addlist" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "GIFT-WMEW-LGR06F"
  }"
```

> The above command returns JSON structured like this:

```json
{
    "message": {
        "success": "The gift code has been added to your list successfully."
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
curl DELETE : "http://dev-magento19.jajahub.com/default/simiconnector/rest/v2/simicustomercredits"/self/{giftvoucher_id} 
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "simicustomercredit": {
        "credit_id": "1",
        "customer_id": "150",
        "balance": 1240,
        "currency": "USD",
        "currency_symbol": "$",
        "listcode": [
            {
                "customer_voucher_id": "30",
                "customer_id": "150",
                "voucher_id": "30",
                "added_date": "Aug 14, 2017",
                "recipient_name": "",
                "gift_code": "1193-8UDMY-BJQK",
                "balance": "30.0000",
                "currency": "USD",
                "status": "1",
                "expired_at": "Aug 14, 2018",
                "customer_check_id": "150",
                "recipient_email": "",
                "customer_email": "test@simicart.com",
                "currency_symbol": "$",
                "action": [
                    "Remove"
                ],
                "giftvoucher_id": "30"
            }
        ],
        "history": [
            {
                "history_id": "1",
                "customer_id": "150",
                "action": "Admin Update",
                "currency_balance": "100.0000",
                "giftcard_code": "",
                "order_id": null,
                "order_number": "",
                "balance_change": "100.0000",
                "currency": "USD",
                "base_amount": "0.0000",
                "amount": "0.0000",
                "created_date": "Jul 19, 2017",
                "currency_symbol": "$"
            }
        ],
        "message": "Gift Code was removed successfully !"
    }
}
```