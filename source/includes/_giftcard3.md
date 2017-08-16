# Giftvoucher Checkout

## Giftvoucher Checkout Properties

Attributes| Type| Description
--------- | ------- | -----------
use_giftcard | int | Do Use Gift Card ( 1 or 0 )
customer.credit_id | int | Credit Id of Customer
customer.balance | int | Balance Credit of Customer
customer.currency | string | Credit Currency
customer.list_code | array | List Existed Gift Code of Customer
credit.use_credit | int | Do Use Balance Credit ( 1 or 0 )
credit.use_credit_amount | int | Amount Credit Used
giftcode.use_giftcode | int | Do Use Gift Code ( 1 or 0 )
giftcode.giftcode | string | Gift Code Used
giftcode.amount | int | Amount Gift Code Used
message.success | string | Success Message
message.notice | string | Notice Message

## Use balance credit to Cart page

### HTTP Request

`PUT /rest/giftvouchercheckouts/usecredit`

```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/usecredit" \
  -H "Authorization: Bearer <token>"
  -d "{
  "usecredit" : "1",
  "credit_amount" : 150
  }"
```

> The above command returns JSON structured like this:

```json
{  
    "gift_card": {
        "use_giftcard": true,
        "customer": {
            "credit_id": "1",
            "customer_id": "150",
            "balance": "$100.00",
            "currency": "USD",
            "list_code": [
                {
                    "store_id": "1",
                    "gift_code": "3711-A2SGS-JTUB",
                    "hidden_code": "3711-XXXXX-XXXX",
                    "balance": "$500.00"
                },
                {
                    "store_id": "1",
                    "gift_code": "6961-D66DA-NXZU",
                    "hidden_code": "6961-XXXXX-XXXX",
                    "balance": "$500.00"
                },
                {
                    "store_id": "0",
                    "gift_code": "xmas-TZA-8PJXEI",
                    "hidden_code": "xmas-XXX-XXXXXX",
                    "balance": "$200.00"
                },
                {
                    "store_id": "0",
                    "gift_code": "xmas-XOU-BEY99G",
                    "hidden_code": "xmas-XXX-XXXXXX",
                    "balance": "$100.00"
                }
            ]
        },
        "credit": {
            "use_credit": 1,
            "use_credit_amount": 150
        },
        "giftcode": {
            "use_giftcode": 0
        },
        "message": {
            "success": "Your Credit has been used successfully."
        }
    }
}
```

## Use Gift Code from Cart page

### HTTP Request

`PUT /rest/giftvouchercheckouts/usecode`

```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/usecode" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftvoucher" : "1",
  "giftcode" : "3711-A2SGS-JTUB",
  "existed_giftcode" : "xmas-XOU-BEY99G"
  }"
```

> The above command returns JSON structured like this:

```json
{
"gift_card": {
        "use_giftcard": true,
        "customer": {
            "credit_id": "1",
            "customer_id": "150",
            "balance": "$250.00",
            "currency": "USD",
            "list_code": [
                {
                    "store_id": "1",
                    "gift_code": "6961-D66DA-NXZU",
                    "hidden_code": "6961-XXXXX-XXXX",
                    "balance": "$500.00"
                },
                {
                    "store_id": "0",
                    "gift_code": "xmas-TZA-8PJXEI",
                    "hidden_code": "xmas-XXX-XXXXXX",
                    "balance": "$200.00"
                }
            ]
        },
        "credit": {
            "use_credit": 0
        },
        "giftcode": {
            "0": {
                "giftcode": "xmas-XOU-BEY99G",
                "giftcode_hidden": "xmas-XXX-XXXXXX",
                "amount": "100"
            },
            "1": {
                "giftcode": "3711-A2SGS-JTUB",
                "giftcode_hidden": "3711-XXXXX-XXXX",
                "amount": "500"
            },
            "use_giftcode": 1
        },
        "message": {
            "success": "Gift code \"3711-XXXXX-XXXX\" has been applied successfully."
        }
    }
}
```

## Remove Gift Code from Cart page

### HTTP Request

`PUT /rest/giftvouchercheckouts/remove`

```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/remove" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "3711-A2SGS-JTUB"
  }"
```

> The above command returns JSON structured like this:

```json
{
"gift_card": {
        "use_giftcard": true,
        "customer": {
            "credit_id": "1",
            "customer_id": "150",
            "balance": "$250.00",
            "currency": "USD",
            "list_code": [
                {
                    "store_id": "1",
                    "gift_code": "3711-A2SGS-JTUB",
                    "hidden_code": "3711-XXXXX-XXXX",
                    "balance": "$500.00"
                },
                {
                    "store_id": "1",
                    "gift_code": "6961-D66DA-NXZU",
                    "hidden_code": "6961-XXXXX-XXXX",
                    "balance": "$500.00"
                },
                {
                    "store_id": "0",
                    "gift_code": "xmas-TZA-8PJXEI",
                    "hidden_code": "xmas-XXX-XXXXXX",
                    "balance": "$200.00"
                }
            ]
        },
        "credit": {
            "use_credit": 0
        },
        "giftcode": {
            "0": {
                "giftcode": "xmas-XOU-BEY99G",
                "giftcode_hidden": "xmas-XXX-XXXXXX",
                "amount": "100"
            },
            "use_giftcode": 1
        },
        "message": {
            "success": "Gift Card \"3711-XXXXX-XXXX\" has been removed successfully!"
        }
    }
}
```

## Change amount Gift Code from Cart page

### HTTP Request

`PUT : /rest/giftvouchercheckouts/updatecode`

```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/updatecode" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "xmas-XOU-BEY99G",
  "amount" : "50"
  }"
```

> The above command returns JSON structured like this:

```json
{
      "gift_card": {
            "use_giftcard": true,
            "customer": {
                "credit_id": "1",
                "customer_id": "150",
                "balance": "$250.00",
                "currency": "USD",
                "list_code": [
                    {
                        "store_id": "1",
                        "gift_code": "3711-A2SGS-JTUB",
                        "hidden_code": "3711-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "1",
                        "gift_code": "6961-D66DA-NXZU",
                        "hidden_code": "6961-XXXXX-XXXX",
                        "balance": "$500.00"
                    }
                ]
            },
            "credit": {
                "use_credit": 0
            },
            "giftcode": {
                "0": {
                    "giftcode": "xmas-TZA-8PJXEI",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "200"
                },
                "1": {
                    "giftcode": "xmas-XOU-BEY99G",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "50"
                },
                "use_giftcode": 1
            },
            "message": {
                "success": "Amount gift code \"xmas-XOU-BEY99G\" changed successfully!."
            }
        }
}
```

## Use Balance Credit from Checkout

### HTTP Request

`PUT /rest/giftvouchercheckouts/usecreditcheckout`


```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/usecreditcheckout" \
  -H "Authorization: Bearer <token>"
  -d "{
    "usecredit" : "1",
    "credit_amount" : 150
    }"
  ```
  
  > The above command returns JSON structured like this:
  
  ```json
  {  
      "gift_card": {
          "use_giftcard": true,
          "customer": {
              "credit_id": "1",
              "customer_id": "150",
              "balance": "$100.00",
              "currency": "USD",
              "list_code": [
                  {
                      "store_id": "1",
                      "gift_code": "3711-A2SGS-JTUB",
                      "hidden_code": "3711-XXXXX-XXXX",
                      "balance": "$500.00"
                  },
                  {
                      "store_id": "1",
                      "gift_code": "6961-D66DA-NXZU",
                      "hidden_code": "6961-XXXXX-XXXX",
                      "balance": "$500.00"
                  },
                  {
                      "store_id": "0",
                      "gift_code": "xmas-TZA-8PJXEI",
                      "hidden_code": "xmas-XXX-XXXXXX",
                      "balance": "$200.00"
                  },
                  {
                      "store_id": "0",
                      "gift_code": "xmas-XOU-BEY99G",
                      "hidden_code": "xmas-XXX-XXXXXX",
                      "balance": "$100.00"
                  }
              ]
          },
          "credit": {
              "use_credit": 1,
              "use_credit_amount": 150
          },
          "giftcode": {
              "use_giftcode": 0
          },
          "message": {
              "success": "Your Credit has been used successfully."
          }
      }
  }
  ```

## Change Amount Credit from Checkout

### HTTP Request

`PUT /rest/giftvouchercheckouts/updatecredit`


```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/updatecredit" \
  -H "Authorization: Bearer <token>"
  -d "{
  "credit_amount" : "100"
  }"
```

> The above command returns JSON structured like this:

```json
{
      "gift_card": {
            "use_giftcard": true,
            "customer": {
                "credit_id": "1",
                "customer_id": "150",
                "balance": "$150.00",
                "currency": "USD",
                "list_code": [
                    {
                        "store_id": "1",
                        "gift_code": "3711-A2SGS-JTUB",
                        "hidden_code": "3711-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "1",
                        "gift_code": "6961-D66DA-NXZU",
                        "hidden_code": "6961-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "0",
                        "gift_code": "xmas-TZA-8PJXEI",
                        "hidden_code": "xmas-XXX-XXXXXX",
                        "balance": "$200.00"
                    }
                ]
            },
            "credit": {
                "use_credit": 1,
                "credit_amount" : 100
            },
             "message": {
                 "success": "Amount Your credit has been updated successfully."
             }
       }
}
```

## Use Gift Code from Checkout

### HTTP Request

`PUT /rest/giftvouchercheckouts/addcodecheckout`


```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/addcodecheckout" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftvoucher" : 1,
  "existed_giftcode" : "xmas-TZA-8PJXEI",
  "giftcode" : "6961-D66DA-NXZU"
  }"
```

> The above command returns JSON structured like this:

```json
{
      "gift_card": {
            "use_giftcard": true,
            "customer": {
                "credit_id": "1",
                "customer_id": "150",
                "balance": "$250.00",
                "currency": "USD",
                "list_code": [
                    {
                        "store_id": "1",
                        "gift_code": "3711-A2SGS-JTUB",
                        "hidden_code": "3711-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "1",
                        "gift_code": "6961-D66DA-NXZU",
                        "hidden_code": "6961-XXXXX-XXXX",
                        "balance": "$500.00"
                    }
                ]
            },
            "credit": {
                "use_credit": 0
            },
            "giftcode": {
                "0": {
                    "giftcode": "xmas-TZA-8PJXEI",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "200"
                },
                "1": {
                    "giftcode": "xmas-XOU-BEY99G",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "100"
                },
                "use_giftcode": 1
            },
            "message": {
                "succcess": "Gift code \"xmas-XXX-XXXXXX\" has been applied successfully."
            }
        }
}
```

## Change Amount Gift Code from Checkout

### HTTP Request

`PUT /rest/giftvouchercheckouts/updategiftcode`

```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/updategiftcode" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "xmas-TZA-8PJXEI",
  "amount" : "50"
  }"
```

> The above command returns JSON structured like this:

```json
{
      "gift_card": {
            "use_giftcard": true,
            "customer": {
                "credit_id": "1",
                "customer_id": "150",
                "balance": "$250.00",
                "currency": "USD",
                "list_code": [
                    {
                        "store_id": "1",
                        "gift_code": "3711-A2SGS-JTUB",
                        "hidden_code": "3711-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "1",
                        "gift_code": "6961-D66DA-NXZU",
                        "hidden_code": "6961-XXXXX-XXXX",
                        "balance": "$500.00"
                    }
                ]
            },
            "credit": {
                "use_credit": 0
            },
            "giftcode": {
                "0": {
                    "giftcode": "xmas-TZA-8PJXEI",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "200"
                },
                "1": {
                    "giftcode": "xmas-XOU-BEY99G",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "50"
                },
                "use_giftcode": 1
            },
            "message": {
                "success": "Amount gift code \"xmas-XOU-BEY99G\" changed successfully!."
            }
        }
}
```

## Remove Gift Code from Checkout

### HTTP Request

`PUT /rest/giftvouchercheckouts/removegiftcode`

```shell
curl PUT "http://dev-magento19.jajahub.com/simiconnector/rest/v2/giftvouchercheckouts/removegiftcode" \
  -H "Authorization: Bearer <token>"
  -d "{
  "giftcode" : "xmas-TZA-8PJXEI"
  }"
```

> The above command returns JSON structured like this:

```json
{
    "gift_card": {
            "use_giftcard": true,
            "customer": {
                "credit_id": "1",
                "customer_id": "150",
                "balance": "$250.00",
                "currency": "USD",
                "list_code": [
                    {
                        "store_id": "1",
                        "gift_code": "3711-A2SGS-JTUB",
                        "hidden_code": "3711-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "1",
                        "gift_code": "6961-D66DA-NXZU",
                        "hidden_code": "6961-XXXXX-XXXX",
                        "balance": "$500.00"
                    },
                    {
                        "store_id": "0",
                        "gift_code": "xmas-XOU-BEY99G",
                        "hidden_code": "xmas-XXX-XXXXXX",
                        "balance": "$100.00"
                    }
                ]
            },
            "credit": {
                "use_credit": 0
            },
            "giftcode": {
                "0": {
                    "giftcode": "xmas-TZA-8PJXEI",
                    "giftcode_hidden": "xmas-XXX-XXXXXX",
                    "amount": "200"
                },
                "use_giftcode": 1
            },
            "message": {
                "success": "Gift card \"xmas-XOU-BEY99G\" is removed successfully."
            }
        }
}
```

