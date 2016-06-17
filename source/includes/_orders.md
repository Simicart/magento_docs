# Orders

## Order Properties

Attributes| Type| Description
--------- | ------- | -----------
entity_id | id | Order Id <code>read only</code>
increment_id | string | Order Encrement Id
status | string | Order Status
store_id | id | Store Id
customer_id | id | Customer Id
shipping_address | array | Shipping Address
billing_address | array | Billing Address
total | array | Total Values (Same with QuoteItems)
order_items | array | Ordered Items
payment_method | string | Payment Method
shipping_method | string | Shipping Method
order_currency_code | string | Currency Code
customer_email | string | Customer Email
shipping | array | Shipping Methods (Onepage)
billing | array | Billing Methods (Onepage)


## View Order History

```shell
curl "https://abc.com/simiconnector/rest/v2/orders" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "195",
      "196"
   ],
   "orders":[  
      {  
         "entity_id":"195",
         "state":"new",
         "status":"pending",
         "coupon_code":null,
         "protect_code":"43646e",
         "shipping_description":"Flat Rate - Fixed",
         "is_virtual":"0",
         "store_id":"1",
         "customer_id":"137",
         "base_discount_amount":"0.0000",
         "base_discount_canceled":null,
         "base_discount_invoiced":null,
         "base_discount_refunded":null,
         "base_grand_total":"350.0000",
         "base_shipping_amount":"10.0000",
         "base_shipping_canceled":null,
         "base_shipping_invoiced":null,
         "base_shipping_refunded":null,
         "base_shipping_tax_amount":"0.0000",
         "base_shipping_tax_refunded":null,
         "base_subtotal":"340.0000",
         "base_subtotal_canceled":null,
         "base_subtotal_invoiced":null,
         "base_subtotal_refunded":null,
         "base_tax_amount":"0.0000",
         "base_tax_canceled":null,
         "base_tax_invoiced":null,
         "base_tax_refunded":null,
         "base_to_global_rate":"1.0000",
         "base_to_order_rate":"1.0000",
         "base_total_canceled":null,
         "base_total_invoiced":null,
         "base_total_invoiced_cost":null,
         "base_total_offline_refunded":null,
         "base_total_online_refunded":null,
         "base_total_paid":null,
         "base_total_qty_ordered":null,
         "base_total_refunded":null,
         "discount_amount":"0.0000",
         "discount_canceled":null,
         "discount_invoiced":null,
         "discount_refunded":null,
         "grand_total":"350.0000",
         "shipping_amount":"10.0000",
         "shipping_canceled":null,
         "shipping_invoiced":null,
         "shipping_refunded":null,
         "shipping_tax_amount":"0.0000",
         "shipping_tax_refunded":null,
         "store_to_base_rate":"1.0000",
         "store_to_order_rate":"1.0000",
         "subtotal":"340.0000",
         "subtotal_canceled":null,
         "subtotal_invoiced":null,
         "subtotal_refunded":null,
         "tax_amount":"0.0000",
         "tax_canceled":null,
         "tax_invoiced":null,
         "tax_refunded":null,
         "total_canceled":null,
         "total_invoiced":null,
         "total_offline_refunded":null,
         "total_online_refunded":null,
         "total_paid":null,
         "total_qty_ordered":"1.0000",
         "total_refunded":null,
         "can_ship_partially":null,
         "can_ship_partially_item":null,
         "customer_is_guest":"0",
         "customer_note_notify":"1",
         "billing_address_id":"382",
         "customer_group_id":"1",
         "edit_increment":null,
         "email_sent":"1",
         "forced_shipment_with_invoice":null,
         "forced_do_shipment_with_invoice":null,
         "payment_auth_expiration":null,
         "payment_authorization_expiration":null,
         "quote_address_id":null,
         "quote_id":"681",
         "shipping_address_id":"383",
         "adjustment_negative":null,
         "adjustment_positive":null,
         "base_adjustment_negative":null,
         "base_adjustment_positive":null,
         "base_shipping_discount_amount":"0.0000",
         "base_subtotal_incl_tax":"340.0000",
         "base_total_due":null,
         "payment_authorization_amount":null,
         "shipping_discount_amount":"0.0000",
         "subtotal_incl_tax":"340.0000",
         "total_due":null,
         "weight":"1.0000",
         "customer_dob":"2016-05-18 00:00:00",
         "increment_id":"145000006",
         "applied_rule_ids":null,
         "base_currency_code":"USD",
         "customer_email":"test@simicart.com",
         "customer_firstname":"Cody",
         "customer_lastname":"Nguyen",
         "customer_middlename":null,
         "customer_prefix":null,
         "customer_suffix":null,
         "customer_taxvat":null,
         "discount_description":null,
         "ext_customer_id":null,
         "ext_order_id":null,
         "global_currency_code":"USD",
         "hold_before_state":null,
         "hold_before_status":null,
         "order_currency_code":"USD",
         "original_increment_id":null,
         "relation_child_id":null,
         "relation_child_real_id":null,
         "relation_parent_id":null,
         "relation_parent_real_id":null,
         "remote_ip":"127.0.0.1",
         "shipping_method":"Flat Rate - Fixed",
         "store_currency_code":"USD",
         "store_name":"Main Website\nMadison Island\nEnglish",
         "x_forwarded_for":null,
         "customer_note":null,
         "created_at":"2016-06-08 07:21:37",
         "updated_at":"2016-06-08 07:21:39",
         "total_item_count":"1",
         "customer_gender":"2",
         "hidden_tax_amount":"0.0000",
         "base_hidden_tax_amount":"0.0000",
         "shipping_hidden_tax_amount":"0.0000",
         "base_shipping_hidden_tax_amnt":"0.0000",
         "base_shipping_hidden_tax_amount":"0.0000",
         "hidden_tax_invoiced":null,
         "base_hidden_tax_invoiced":null,
         "hidden_tax_refunded":null,
         "base_hidden_tax_refunded":null,
         "shipping_incl_tax":"10.0000",
         "base_shipping_incl_tax":"10.0000",
         "coupon_rule_name":null,
         "paypal_ipn_customer_notified":"0",
         "gift_message_id":null,
         "base_customer_balance_amount":null,
         "customer_balance_amount":null,
         "base_customer_balance_invoiced":null,
         "customer_balance_invoiced":null,
         "base_customer_balance_refunded":null,
         "customer_balance_refunded":null,
         "bs_customer_bal_total_refunded":null,
         "customer_bal_total_refunded":null,
         "gift_cards":null,
         "base_gift_cards_amount":null,
         "gift_cards_amount":null,
         "base_gift_cards_invoiced":null,
         "gift_cards_invoiced":null,
         "base_gift_cards_refunded":null,
         "gift_cards_refunded":null,
         "gw_id":null,
         "gw_allow_gift_receipt":null,
         "gw_add_card":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_items_base_price":null,
         "gw_items_price":null,
         "gw_card_base_price":null,
         "gw_card_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "gw_items_base_tax_amount":null,
         "gw_items_tax_amount":null,
         "gw_card_base_tax_amount":null,
         "gw_card_tax_amount":null,
         "gw_base_price_invoiced":null,
         "gw_price_invoiced":null,
         "gw_items_base_price_invoiced":null,
         "gw_items_price_invoiced":null,
         "gw_card_base_price_invoiced":null,
         "gw_card_price_invoiced":null,
         "gw_base_tax_amount_invoiced":null,
         "gw_tax_amount_invoiced":null,
         "gw_items_base_tax_invoiced":null,
         "gw_items_tax_invoiced":null,
         "gw_card_base_tax_invoiced":null,
         "gw_card_tax_invoiced":null,
         "gw_base_price_refunded":null,
         "gw_price_refunded":null,
         "gw_items_base_price_refunded":null,
         "gw_items_price_refunded":null,
         "gw_card_base_price_refunded":null,
         "gw_card_price_refunded":null,
         "gw_base_tax_amount_refunded":null,
         "gw_tax_amount_refunded":null,
         "gw_items_base_tax_refunded":null,
         "gw_items_tax_refunded":null,
         "gw_card_base_tax_refunded":null,
         "gw_card_tax_refunded":null,
         "reward_points_balance":null,
         "base_reward_currency_amount":null,
         "reward_currency_amount":null,
         "base_rwrd_crrncy_amt_invoiced":null,
         "rwrd_currency_amount_invoiced":null,
         "base_rwrd_crrncy_amnt_refnded":null,
         "rwrd_crrncy_amnt_refunded":null,
         "reward_points_balance_refund":null,
         "reward_points_balance_refunded":null,
         "reward_salesrule_points":null,
         "cod_fee":null,
         "base_cod_fee":null,
         "cod_fee_invoiced":null,
         "base_cod_fee_invoiced":null,
         "cod_tax_amount":null,
         "base_cod_tax_amount":null,
         "cod_tax_amount_invoiced":null,
         "base_cod_tax_amount_invoiced":null,
         "cod_fee_refunded":null,
         "base_cod_fee_refunded":null,
         "cod_tax_amount_refunded":null,
         "base_cod_tax_amount_refunded":null,
         "cod_fee_canceled":null,
         "base_cod_fee_canceled":null,
         "cod_tax_amount_canceled":null,
         "base_cod_tax_amount_canceled":null,
         "payment_method":"Cash On Delivery",
         "shipping_address":{  
            "firstname":"Cody",
            "lastname":"Nguyen",
            "prefix":null,
            "suffix":null,
            "vat_id":"vat num",
            "street":"street",
            "city":"city",
            "region":"Alabama",
            "region_id":"1",
            "region_code":"AL",
            "postcode":"10000",
            "country_name":"United States",
            "country_id":"US",
            "telephone":"098765412321",
            "email":"test@simicart.com",
            "company":"company",
            "latlng":""
         },
         "billing_address":{  
            "firstname":"Cody",
            "lastname":"Nguyen",
            "prefix":null,
            "suffix":null,
            "vat_id":"vat num",
            "street":"street",
            "city":"city",
            "region":"Alabama",
            "region_id":"1",
            "region_code":"AL",
            "postcode":"10000",
            "country_name":"United States",
            "country_id":"US",
            "telephone":"098765412321",
            "email":"test@simicart.com",
            "company":"company",
            "latlng":""
         },
         "order_items":[  
            {  
               "item_id":"596",
               "order_id":"195",
               "parent_item_id":null,
               "quote_item_id":"2555",
               "store_id":"2",
               "created_at":"2016-06-08 07:21:37",
               "updated_at":"2016-06-08 07:21:37",
               "product_id":"425",
               "product_type":"configurable",
               "product_options":"a:6:{s:15:\"info_buyRequest\";a:6:{s:4:\"uenc\";s:84:\"aHR0cDovL2xvY2FsaG9zdC5jb20vbWFnZW50bzE5L2xhZmF5ZXR0ZS1jb252ZXJ0aWJsZS1kcmVzcy5odG1s\";s:7:\"product\";s:3:\"425\";s:8:\"form_key\";s:16:\"fr1AHQFca9gAFkhg\";s:15:\"related_product\";s:0:\"\";s:15:\"super_attribute\";a:2:{i:92;s:2:\"27\";i:180;s:2:\"74\";}s:3:\"qty\";s:1:\"1\";}s:15:\"attributes_info\";a:2:{i:0;a:2:{s:5:\"label\";s:5:\"Color\";s:5:\"value\";s:4:\"Blue\";}i:1;a:2:{s:5:\"label\";s:4:\"Size\";s:5:\"value\";s:1:\"6\";}}s:11:\"simple_name\";s:17:\"Convertible Dress\";s:10:\"simple_sku\";s:6:\"wsd015\";s:20:\"product_calculations\";i:1;s:13:\"shipment_type\";i:0;}",
               "weight":"1.0000",
               "is_virtual":"0",
               "sku":"wsd015",
               "name":"Lafayette Convertible Dress",
               "description":null,
               "applied_rule_ids":null,
               "additional_data":null,
               "free_shipping":"0",
               "is_qty_decimal":"0",
               "no_discount":"0",
               "qty_backordered":null,
               "qty_canceled":"0.0000",
               "qty_invoiced":"0.0000",
               "qty_ordered":"1.0000",
               "qty_refunded":"0.0000",
               "qty_shipped":"0.0000",
               "base_cost":null,
               "price":"340.0000",
               "base_price":"340.0000",
               "original_price":"340.0000",
               "base_original_price":"340.0000",
               "tax_percent":"0.0000",
               "tax_amount":"0.0000",
               "base_tax_amount":"0.0000",
               "tax_invoiced":"0.0000",
               "base_tax_invoiced":"0.0000",
               "discount_percent":"0.0000",
               "discount_amount":"0.0000",
               "base_discount_amount":"0.0000",
               "discount_invoiced":"0.0000",
               "base_discount_invoiced":"0.0000",
               "amount_refunded":"0.0000",
               "base_amount_refunded":"0.0000",
               "row_total":"340.0000",
               "base_row_total":"340.0000",
               "row_invoiced":"0.0000",
               "base_row_invoiced":"0.0000",
               "row_weight":"1.0000",
               "base_tax_before_discount":null,
               "tax_before_discount":null,
               "ext_order_item_id":null,
               "locked_do_invoice":null,
               "locked_do_ship":null,
               "price_incl_tax":"340.0000",
               "base_price_incl_tax":"340.0000",
               "row_total_incl_tax":"340.0000",
               "base_row_total_incl_tax":"340.0000",
               "hidden_tax_amount":"0.0000",
               "base_hidden_tax_amount":"0.0000",
               "hidden_tax_invoiced":null,
               "base_hidden_tax_invoiced":null,
               "hidden_tax_refunded":null,
               "base_hidden_tax_refunded":null,
               "is_nominal":"0",
               "tax_canceled":null,
               "hidden_tax_canceled":null,
               "tax_refunded":null,
               "base_tax_refunded":null,
               "discount_refunded":null,
               "base_discount_refunded":null,
               "gift_message_id":null,
               "gift_message_available":"1",
               "base_weee_tax_applied_amount":"0.0000",
               "base_weee_tax_applied_row_amnt":"0.0000",
               "base_weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied_amount":"0.0000",
               "weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied":"a:0:{}",
               "weee_tax_disposition":"0.0000",
               "weee_tax_row_disposition":"0.0000",
               "base_weee_tax_disposition":"0.0000",
               "base_weee_tax_row_disposition":"0.0000",
               "event_id":null,
               "giftregistry_item_id":null,
               "gw_id":null,
               "gw_base_price":null,
               "gw_price":null,
               "gw_base_tax_amount":null,
               "gw_tax_amount":null,
               "gw_base_price_invoiced":null,
               "gw_price_invoiced":null,
               "gw_base_tax_amount_invoiced":null,
               "gw_tax_amount_invoiced":null,
               "gw_base_price_refunded":null,
               "gw_price_refunded":null,
               "gw_base_tax_amount_refunded":null,
               "gw_tax_amount_refunded":null,
               "qty_returned":"0.0000",
               "has_children":true
            }
         ],
         "total":{  
            "subtotal_excl_tax":"340.0000",
            "subtotal_incl_tax":"340.0000",
            "shipping_hand_excl_tax":"10.0000",
            "shipping_hand_incl_tax":"10.0000",
            "tax":"0.0000",
            "discount":0,
            "grand_total_excl_tax":350,
            "grand_total_incl_tax":"350.0000",
            "currency_symbol":"$"
         }
      },
      {  
         "entity_id":"196",
         "state":"new",
         "status":"pending",
         "coupon_code":"MYCOUPON",
         "protect_code":"778683",
         "shipping_description":"Free Shipping - Free",
         "is_virtual":"0",
         "store_id":"1",
         "customer_id":"137",
         "base_discount_amount":"-5.0000",
         "base_discount_canceled":null,
         "base_discount_invoiced":null,
         "base_discount_refunded":null,
         "base_grand_total":"272.0000",
         "base_shipping_amount":"0.0000",
         "base_shipping_canceled":null,
         "base_shipping_invoiced":null,
         "base_shipping_refunded":null,
         "base_shipping_tax_amount":"0.0000",
         "base_shipping_tax_refunded":null,
         "base_subtotal":"277.0000",
         "base_subtotal_canceled":null,
         "base_subtotal_invoiced":null,
         "base_subtotal_refunded":null,
         "base_tax_amount":"0.0000",
         "base_tax_canceled":null,
         "base_tax_invoiced":null,
         "base_tax_refunded":null,
         "base_to_global_rate":"1.0000",
         "base_to_order_rate":"1.0000",
         "base_total_canceled":null,
         "base_total_invoiced":null,
         "base_total_invoiced_cost":null,
         "base_total_offline_refunded":null,
         "base_total_online_refunded":null,
         "base_total_paid":null,
         "base_total_qty_ordered":null,
         "base_total_refunded":null,
         "discount_amount":"-5.0000",
         "discount_canceled":null,
         "discount_invoiced":null,
         "discount_refunded":null,
         "grand_total":"272.0000",
         "shipping_amount":"0.0000",
         "shipping_canceled":null,
         "shipping_invoiced":null,
         "shipping_refunded":null,
         "shipping_tax_amount":"0.0000",
         "shipping_tax_refunded":null,
         "store_to_base_rate":"1.0000",
         "store_to_order_rate":"1.0000",
         "subtotal":"277.0000",
         "subtotal_canceled":null,
         "subtotal_invoiced":null,
         "subtotal_refunded":null,
         "tax_amount":"0.0000",
         "tax_canceled":null,
         "tax_invoiced":null,
         "tax_refunded":null,
         "total_canceled":null,
         "total_invoiced":null,
         "total_offline_refunded":null,
         "total_online_refunded":null,
         "total_paid":null,
         "total_qty_ordered":"6.0000",
         "total_refunded":null,
         "can_ship_partially":null,
         "can_ship_partially_item":null,
         "customer_is_guest":"0",
         "customer_note_notify":"1",
         "billing_address_id":"384",
         "customer_group_id":"1",
         "edit_increment":null,
         "email_sent":"1",
         "forced_shipment_with_invoice":null,
         "forced_do_shipment_with_invoice":null,
         "payment_auth_expiration":null,
         "payment_authorization_expiration":null,
         "quote_address_id":null,
         "quote_id":"690",
         "shipping_address_id":"385",
         "adjustment_negative":null,
         "adjustment_positive":null,
         "base_adjustment_negative":null,
         "base_adjustment_positive":null,
         "base_shipping_discount_amount":"0.0000",
         "base_subtotal_incl_tax":"277.0000",
         "base_total_due":null,
         "payment_authorization_amount":null,
         "shipping_discount_amount":"0.0000",
         "subtotal_incl_tax":"277.0000",
         "total_due":null,
         "weight":"6.0000",
         "customer_dob":"2016-05-18 00:00:00",
         "increment_id":"145000007",
         "applied_rule_ids":"6",
         "base_currency_code":"USD",
         "customer_email":"test@simicart.com",
         "customer_firstname":"Cody",
         "customer_lastname":"Nguyen",
         "customer_middlename":null,
         "customer_prefix":null,
         "customer_suffix":null,
         "customer_taxvat":null,
         "discount_description":"MYCOUPON",
         "ext_customer_id":null,
         "ext_order_id":null,
         "global_currency_code":"USD",
         "hold_before_state":null,
         "hold_before_status":null,
         "order_currency_code":"USD",
         "original_increment_id":null,
         "relation_child_id":null,
         "relation_child_real_id":null,
         "relation_parent_id":null,
         "relation_parent_real_id":null,
         "remote_ip":"127.0.0.1",
         "shipping_method":"Free Shipping - Free",
         "store_currency_code":"USD",
         "store_name":"Main Website\nMadison Island\nEnglish",
         "x_forwarded_for":null,
         "customer_note":null,
         "created_at":"2016-06-13 10:04:47",
         "updated_at":"2016-06-13 10:04:50",
         "total_item_count":"3",
         "customer_gender":"2",
         "hidden_tax_amount":"0.0000",
         "base_hidden_tax_amount":"0.0000",
         "shipping_hidden_tax_amount":"0.0000",
         "base_shipping_hidden_tax_amnt":"0.0000",
         "base_shipping_hidden_tax_amount":"0.0000",
         "hidden_tax_invoiced":null,
         "base_hidden_tax_invoiced":null,
         "hidden_tax_refunded":null,
         "base_hidden_tax_refunded":null,
         "shipping_incl_tax":"0.0000",
         "base_shipping_incl_tax":"0.0000",
         "coupon_rule_name":" $5 off when you choose UPS(NextDay Air) shipping",
         "paypal_ipn_customer_notified":"0",
         "gift_message_id":null,
         "base_customer_balance_amount":null,
         "customer_balance_amount":null,
         "base_customer_balance_invoiced":null,
         "customer_balance_invoiced":null,
         "base_customer_balance_refunded":null,
         "customer_balance_refunded":null,
         "bs_customer_bal_total_refunded":null,
         "customer_bal_total_refunded":null,
         "gift_cards":null,
         "base_gift_cards_amount":null,
         "gift_cards_amount":null,
         "base_gift_cards_invoiced":null,
         "gift_cards_invoiced":null,
         "base_gift_cards_refunded":null,
         "gift_cards_refunded":null,
         "gw_id":null,
         "gw_allow_gift_receipt":null,
         "gw_add_card":null,
         "gw_base_price":null,
         "gw_price":null,
         "gw_items_base_price":null,
         "gw_items_price":null,
         "gw_card_base_price":null,
         "gw_card_price":null,
         "gw_base_tax_amount":null,
         "gw_tax_amount":null,
         "gw_items_base_tax_amount":null,
         "gw_items_tax_amount":null,
         "gw_card_base_tax_amount":null,
         "gw_card_tax_amount":null,
         "gw_base_price_invoiced":null,
         "gw_price_invoiced":null,
         "gw_items_base_price_invoiced":null,
         "gw_items_price_invoiced":null,
         "gw_card_base_price_invoiced":null,
         "gw_card_price_invoiced":null,
         "gw_base_tax_amount_invoiced":null,
         "gw_tax_amount_invoiced":null,
         "gw_items_base_tax_invoiced":null,
         "gw_items_tax_invoiced":null,
         "gw_card_base_tax_invoiced":null,
         "gw_card_tax_invoiced":null,
         "gw_base_price_refunded":null,
         "gw_price_refunded":null,
         "gw_items_base_price_refunded":null,
         "gw_items_price_refunded":null,
         "gw_card_base_price_refunded":null,
         "gw_card_price_refunded":null,
         "gw_base_tax_amount_refunded":null,
         "gw_tax_amount_refunded":null,
         "gw_items_base_tax_refunded":null,
         "gw_items_tax_refunded":null,
         "gw_card_base_tax_refunded":null,
         "gw_card_tax_refunded":null,
         "reward_points_balance":null,
         "base_reward_currency_amount":null,
         "reward_currency_amount":null,
         "base_rwrd_crrncy_amt_invoiced":null,
         "rwrd_currency_amount_invoiced":null,
         "base_rwrd_crrncy_amnt_refnded":null,
         "rwrd_crrncy_amnt_refunded":null,
         "reward_points_balance_refund":null,
         "reward_points_balance_refunded":null,
         "reward_salesrule_points":null,
         "cod_fee":"0.0000",
         "base_cod_fee":"0.0000",
         "cod_fee_invoiced":null,
         "base_cod_fee_invoiced":null,
         "cod_tax_amount":"0.0000",
         "base_cod_tax_amount":"0.0000",
         "cod_tax_amount_invoiced":null,
         "base_cod_tax_amount_invoiced":null,
         "cod_fee_refunded":null,
         "base_cod_fee_refunded":null,
         "cod_tax_amount_refunded":null,
         "base_cod_tax_amount_refunded":null,
         "cod_fee_canceled":null,
         "base_cod_fee_canceled":null,
         "cod_tax_amount_canceled":null,
         "base_cod_tax_amount_canceled":null,
         "payment_method":"Cash on Delivery",
         "shipping_address":{  
            "firstname":"Cody",
            "lastname":"Nguyen",
            "prefix":null,
            "suffix":null,
            "vat_id":"vat num",
            "street":"street",
            "city":"city",
            "region":"Alabama",
            "region_id":"1",
            "region_code":"AL",
            "postcode":"10000",
            "country_name":"United States",
            "country_id":"US",
            "telephone":"098765412321",
            "email":"test@simicart.com",
            "company":"company",
            "latlng":""
         },
         "billing_address":{  
            "firstname":"Cody",
            "lastname":"Nguyen",
            "prefix":null,
            "suffix":null,
            "vat_id":"vat num",
            "street":"street",
            "city":"city",
            "region":"Alabama",
            "region_id":"1",
            "region_code":"AL",
            "postcode":"10000",
            "country_name":"United States",
            "country_id":"US",
            "telephone":"098765412321",
            "email":"test@simicart.com",
            "company":"company",
            "latlng":""
         },
         "order_items":[  
            {  
               "item_id":"598",
               "order_id":"196",
               "parent_item_id":null,
               "quote_item_id":"2557",
               "store_id":"1",
               "created_at":"2016-06-13 10:04:47",
               "updated_at":"2016-06-13 10:04:47",
               "product_id":"888",
               "product_type":"simple",
               "product_options":"a:2:{s:15:\"info_buyRequest\";a:3:{s:7:\"product\";s:3:\"888\";s:3:\"qty\";s:1:\"1\";s:7:\"options\";a:1:{i:7;s:1:\"3\";}}s:7:\"options\";a:1:{i:0;a:7:{s:5:\"label\";s:16:\"mydropdownoption\";s:5:\"value\";s:13:\"option1 title\";s:11:\"print_value\";s:13:\"option1 title\";s:9:\"option_id\";s:1:\"7\";s:11:\"option_type\";s:9:\"drop_down\";s:12:\"option_value\";s:1:\"3\";s:11:\"custom_view\";b:0;}}}",
               "weight":"1.0000",
               "is_virtual":"0",
               "sku":"testcustom-option1",
               "name":"Test Custom Option Simple Product",
               "description":null,
               "applied_rule_ids":"6",
               "additional_data":null,
               "free_shipping":"0",
               "is_qty_decimal":"0",
               "no_discount":"0",
               "qty_backordered":null,
               "qty_canceled":"0.0000",
               "qty_invoiced":"0.0000",
               "qty_ordered":"4.0000",
               "qty_refunded":"0.0000",
               "qty_shipped":"0.0000",
               "base_cost":null,
               "price":"2.0000",
               "base_price":"2.0000",
               "original_price":"2.0000",
               "base_original_price":"2.0000",
               "tax_percent":"0.0000",
               "tax_amount":"0.0000",
               "base_tax_amount":"0.0000",
               "tax_invoiced":"0.0000",
               "base_tax_invoiced":"0.0000",
               "discount_percent":"0.0000",
               "discount_amount":"0.1400",
               "base_discount_amount":"0.1400",
               "discount_invoiced":"0.0000",
               "base_discount_invoiced":"0.0000",
               "amount_refunded":"0.0000",
               "base_amount_refunded":"0.0000",
               "row_total":"8.0000",
               "base_row_total":"8.0000",
               "row_invoiced":"0.0000",
               "base_row_invoiced":"0.0000",
               "row_weight":"4.0000",
               "base_tax_before_discount":null,
               "tax_before_discount":null,
               "ext_order_item_id":null,
               "locked_do_invoice":null,
               "locked_do_ship":null,
               "price_incl_tax":"2.0000",
               "base_price_incl_tax":"2.0000",
               "row_total_incl_tax":"8.0000",
               "base_row_total_incl_tax":"8.0000",
               "hidden_tax_amount":"0.0000",
               "base_hidden_tax_amount":"0.0000",
               "hidden_tax_invoiced":null,
               "base_hidden_tax_invoiced":null,
               "hidden_tax_refunded":null,
               "base_hidden_tax_refunded":null,
               "is_nominal":"0",
               "tax_canceled":null,
               "hidden_tax_canceled":null,
               "tax_refunded":null,
               "base_tax_refunded":null,
               "discount_refunded":null,
               "base_discount_refunded":null,
               "gift_message_id":null,
               "gift_message_available":"1",
               "base_weee_tax_applied_amount":"0.0000",
               "base_weee_tax_applied_row_amnt":"0.0000",
               "base_weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied_amount":"0.0000",
               "weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied":"a:0:{}",
               "weee_tax_disposition":"0.0000",
               "weee_tax_row_disposition":"0.0000",
               "base_weee_tax_disposition":"0.0000",
               "base_weee_tax_row_disposition":"0.0000",
               "event_id":null,
               "giftregistry_item_id":null,
               "gw_id":null,
               "gw_base_price":null,
               "gw_price":null,
               "gw_base_tax_amount":null,
               "gw_tax_amount":null,
               "gw_base_price_invoiced":null,
               "gw_price_invoiced":null,
               "gw_base_tax_amount_invoiced":null,
               "gw_tax_amount_invoiced":null,
               "gw_base_price_refunded":null,
               "gw_price_refunded":null,
               "gw_base_tax_amount_refunded":null,
               "gw_tax_amount_refunded":null,
               "qty_returned":"0.0000"
            },
            {  
               "item_id":"599",
               "order_id":"196",
               "parent_item_id":null,
               "quote_item_id":"2562",
               "store_id":"1",
               "created_at":"2016-06-13 10:04:47",
               "updated_at":"2016-06-13 10:04:47",
               "product_id":"410",
               "product_type":"configurable",
               "product_options":"a:7:{s:15:\"info_buyRequest\";a:7:{s:4:\"uenc\";s:88:\"aHR0cDovL2xvY2FsaG9zdC5jb20vbWFnZW50bzE5L21lbi9uZXctYXJyaXZhbHMvY2hlbHNlYS10ZWUuaHRtbA,,\";s:7:\"product\";s:3:\"410\";s:8:\"form_key\";s:16:\"mzi5hPyv2qmToSv9\";s:15:\"related_product\";s:0:\"\";s:15:\"super_attribute\";a:2:{i:92;s:2:\"20\";i:180;s:2:\"81\";}s:7:\"options\";a:2:{i:3;s:0:\"\";i:2;s:1:\"2\";}s:3:\"qty\";s:1:\"1\";}s:7:\"options\";a:1:{i:0;a:7:{s:5:\"label\";s:19:\"Test Custom Options\";s:5:\"value\";s:7:\"model 2\";s:11:\"print_value\";s:7:\"model 2\";s:9:\"option_id\";s:1:\"2\";s:11:\"option_type\";s:9:\"drop_down\";s:12:\"option_value\";s:1:\"2\";s:11:\"custom_view\";b:0;}}s:15:\"attributes_info\";a:2:{i:0;a:2:{s:5:\"label\";s:5:\"Color\";s:5:\"value\";s:5:\"Black\";}i:1;a:2:{s:5:\"label\";s:4:\"Size\";s:5:\"value\";s:2:\"XS\";}}s:11:\"simple_name\";s:11:\"Chelsea Tee\";s:10:\"simple_sku\";s:8:\"mtk004xs\";s:20:\"product_calculations\";i:1;s:13:\"shipment_type\";i:0;}",
               "weight":"1.0000",
               "is_virtual":"0",
               "sku":"mtk004xs",
               "name":"Chelsea Tee",
               "description":null,
               "applied_rule_ids":"6",
               "additional_data":null,
               "free_shipping":"0",
               "is_qty_decimal":"0",
               "no_discount":"0",
               "qty_backordered":null,
               "qty_canceled":"0.0000",
               "qty_invoiced":"0.0000",
               "qty_ordered":"1.0000",
               "qty_refunded":"0.0000",
               "qty_shipped":"0.0000",
               "base_cost":null,
               "price":"135.0000",
               "base_price":"135.0000",
               "original_price":"135.0000",
               "base_original_price":"135.0000",
               "tax_percent":"0.0000",
               "tax_amount":"0.0000",
               "base_tax_amount":"0.0000",
               "tax_invoiced":"0.0000",
               "base_tax_invoiced":"0.0000",
               "discount_percent":"0.0000",
               "discount_amount":"2.4400",
               "base_discount_amount":"2.4400",
               "discount_invoiced":"0.0000",
               "base_discount_invoiced":"0.0000",
               "amount_refunded":"0.0000",
               "base_amount_refunded":"0.0000",
               "row_total":"135.0000",
               "base_row_total":"135.0000",
               "row_invoiced":"0.0000",
               "base_row_invoiced":"0.0000",
               "row_weight":"1.0000",
               "base_tax_before_discount":null,
               "tax_before_discount":null,
               "ext_order_item_id":null,
               "locked_do_invoice":null,
               "locked_do_ship":null,
               "price_incl_tax":"135.0000",
               "base_price_incl_tax":"135.0000",
               "row_total_incl_tax":"135.0000",
               "base_row_total_incl_tax":"135.0000",
               "hidden_tax_amount":"0.0000",
               "base_hidden_tax_amount":"0.0000",
               "hidden_tax_invoiced":null,
               "base_hidden_tax_invoiced":null,
               "hidden_tax_refunded":null,
               "base_hidden_tax_refunded":null,
               "is_nominal":"0",
               "tax_canceled":null,
               "hidden_tax_canceled":null,
               "tax_refunded":null,
               "base_tax_refunded":null,
               "discount_refunded":null,
               "base_discount_refunded":null,
               "gift_message_id":null,
               "gift_message_available":"1",
               "base_weee_tax_applied_amount":"0.0000",
               "base_weee_tax_applied_row_amnt":"0.0000",
               "base_weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied_amount":"0.0000",
               "weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied":"a:0:{}",
               "weee_tax_disposition":"0.0000",
               "weee_tax_row_disposition":"0.0000",
               "base_weee_tax_disposition":"0.0000",
               "base_weee_tax_row_disposition":"0.0000",
               "event_id":null,
               "giftregistry_item_id":null,
               "gw_id":null,
               "gw_base_price":null,
               "gw_price":null,
               "gw_base_tax_amount":null,
               "gw_tax_amount":null,
               "gw_base_price_invoiced":null,
               "gw_price_invoiced":null,
               "gw_base_tax_amount_invoiced":null,
               "gw_tax_amount_invoiced":null,
               "gw_base_price_refunded":null,
               "gw_price_refunded":null,
               "gw_base_tax_amount_refunded":null,
               "gw_tax_amount_refunded":null,
               "qty_returned":"0.0000",
               "has_children":true
            },
            {  
               "item_id":"601",
               "order_id":"196",
               "parent_item_id":null,
               "quote_item_id":"2569",
               "store_id":"1",
               "created_at":"2016-06-13 10:04:47",
               "updated_at":"2016-06-13 10:04:47",
               "product_id":"410",
               "product_type":"configurable",
               "product_options":"a:7:{s:15:\"info_buyRequest\";a:7:{s:4:\"uenc\";s:68:\"aHR0cDovL2xvY2FsaG9zdC5jb20vbWFnZW50bzE5L2NoZWxzZWEtdGVlLTcwMy5odG1s\";s:7:\"product\";s:3:\"410\";s:8:\"form_key\";s:16:\"KStwREIgL1HJdjXu\";s:15:\"related_product\";s:0:\"\";s:15:\"super_attribute\";a:2:{i:92;s:2:\"20\";i:180;s:2:\"79\";}s:7:\"options\";a:2:{i:3;s:0:\"\";i:2;s:1:\"1\";}s:3:\"qty\";s:1:\"1\";}s:7:\"options\";a:1:{i:0;a:7:{s:5:\"label\";s:19:\"Test Custom Options\";s:5:\"value\";s:7:\"model 1\";s:11:\"print_value\";s:7:\"model 1\";s:9:\"option_id\";s:1:\"2\";s:11:\"option_type\";s:9:\"drop_down\";s:12:\"option_value\";s:1:\"1\";s:11:\"custom_view\";b:0;}}s:15:\"attributes_info\";a:2:{i:0;a:2:{s:5:\"label\";s:5:\"Color\";s:5:\"value\";s:5:\"Black\";}i:1;a:2:{s:5:\"label\";s:4:\"Size\";s:5:\"value\";s:1:\"M\";}}s:11:\"simple_name\";s:11:\"Chelsea Tee\";s:10:\"simple_sku\";s:7:\"mtk004m\";s:20:\"product_calculations\";i:1;s:13:\"shipment_type\";i:0;}",
               "weight":"1.0000",
               "is_virtual":"0",
               "sku":"mtk004m",
               "name":"Chelsea Tee",
               "description":null,
               "applied_rule_ids":"6",
               "additional_data":null,
               "free_shipping":"0",
               "is_qty_decimal":"0",
               "no_discount":"0",
               "qty_backordered":null,
               "qty_canceled":"0.0000",
               "qty_invoiced":"0.0000",
               "qty_ordered":"1.0000",
               "qty_refunded":"0.0000",
               "qty_shipped":"0.0000",
               "base_cost":null,
               "price":"134.0000",
               "base_price":"134.0000",
               "original_price":"134.0000",
               "base_original_price":"134.0000",
               "tax_percent":"0.0000",
               "tax_amount":"0.0000",
               "base_tax_amount":"0.0000",
               "tax_invoiced":"0.0000",
               "base_tax_invoiced":"0.0000",
               "discount_percent":"0.0000",
               "discount_amount":"2.4200",
               "base_discount_amount":"2.4200",
               "discount_invoiced":"0.0000",
               "base_discount_invoiced":"0.0000",
               "amount_refunded":"0.0000",
               "base_amount_refunded":"0.0000",
               "row_total":"134.0000",
               "base_row_total":"134.0000",
               "row_invoiced":"0.0000",
               "base_row_invoiced":"0.0000",
               "row_weight":"1.0000",
               "base_tax_before_discount":null,
               "tax_before_discount":null,
               "ext_order_item_id":null,
               "locked_do_invoice":null,
               "locked_do_ship":null,
               "price_incl_tax":"134.0000",
               "base_price_incl_tax":"134.0000",
               "row_total_incl_tax":"134.0000",
               "base_row_total_incl_tax":"134.0000",
               "hidden_tax_amount":"0.0000",
               "base_hidden_tax_amount":"0.0000",
               "hidden_tax_invoiced":null,
               "base_hidden_tax_invoiced":null,
               "hidden_tax_refunded":null,
               "base_hidden_tax_refunded":null,
               "is_nominal":"0",
               "tax_canceled":null,
               "hidden_tax_canceled":null,
               "tax_refunded":null,
               "base_tax_refunded":null,
               "discount_refunded":null,
               "base_discount_refunded":null,
               "gift_message_id":null,
               "gift_message_available":"1",
               "base_weee_tax_applied_amount":"0.0000",
               "base_weee_tax_applied_row_amnt":"0.0000",
               "base_weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied_amount":"0.0000",
               "weee_tax_applied_row_amount":"0.0000",
               "weee_tax_applied":"a:0:{}",
               "weee_tax_disposition":"0.0000",
               "weee_tax_row_disposition":"0.0000",
               "base_weee_tax_disposition":"0.0000",
               "base_weee_tax_row_disposition":"0.0000",
               "event_id":null,
               "giftregistry_item_id":null,
               "gw_id":null,
               "gw_base_price":null,
               "gw_price":null,
               "gw_base_tax_amount":null,
               "gw_tax_amount":null,
               "gw_base_price_invoiced":null,
               "gw_price_invoiced":null,
               "gw_base_tax_amount_invoiced":null,
               "gw_tax_amount_invoiced":null,
               "gw_base_price_refunded":null,
               "gw_price_refunded":null,
               "gw_base_tax_amount_refunded":null,
               "gw_tax_amount_refunded":null,
               "qty_returned":"0.0000",
               "has_children":true
            }
         ],
         "total":{  
            "subtotal_excl_tax":"277.0000",
            "subtotal_incl_tax":"277.0000",
            "shipping_hand_excl_tax":"0.0000",
            "shipping_hand_incl_tax":"0.0000",
            "tax":"0.0000",
            "discount":5,
            "grand_total_excl_tax":272,
            "grand_total_incl_tax":"272.0000",
            "currency_symbol":"$"
         }
      }
   ],
   "total":2,
   "page_size":15,
   "from":0
}
```

This request return Order history

### HTTP Request

`GET /rest/orders/<id>`


## View An Order from history

```shell
curl "https://abc.com/simiconnector/rest/v2/orders/195" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "entity_id":"195",
      "state":"new",
      "status":"pending",
      "coupon_code":null,
      "protect_code":"43646e",
      "shipping_description":"Flat Rate - Fixed",
      "is_virtual":"0",
      "store_id":"1",
      "customer_id":"137",
      "base_discount_amount":"0.0000",
      "base_discount_canceled":null,
      "base_discount_invoiced":null,
      "base_discount_refunded":null,
      "base_grand_total":"350.0000",
      "base_shipping_amount":"10.0000",
      "base_shipping_canceled":null,
      "base_shipping_invoiced":null,
      "base_shipping_refunded":null,
      "base_shipping_tax_amount":"0.0000",
      "base_shipping_tax_refunded":null,
      "base_subtotal":"340.0000",
      "base_subtotal_canceled":null,
      "base_subtotal_invoiced":null,
      "base_subtotal_refunded":null,
      "base_tax_amount":"0.0000",
      "base_tax_canceled":null,
      "base_tax_invoiced":null,
      "base_tax_refunded":null,
      "base_to_global_rate":"1.0000",
      "base_to_order_rate":"1.0000",
      "base_total_canceled":null,
      "base_total_invoiced":null,
      "base_total_invoiced_cost":null,
      "base_total_offline_refunded":null,
      "base_total_online_refunded":null,
      "base_total_paid":null,
      "base_total_qty_ordered":null,
      "base_total_refunded":null,
      "discount_amount":"0.0000",
      "discount_canceled":null,
      "discount_invoiced":null,
      "discount_refunded":null,
      "grand_total":"350.0000",
      "shipping_amount":"10.0000",
      "shipping_canceled":null,
      "shipping_invoiced":null,
      "shipping_refunded":null,
      "shipping_tax_amount":"0.0000",
      "shipping_tax_refunded":null,
      "store_to_base_rate":"1.0000",
      "store_to_order_rate":"1.0000",
      "subtotal":"340.0000",
      "subtotal_canceled":null,
      "subtotal_invoiced":null,
      "subtotal_refunded":null,
      "tax_amount":"0.0000",
      "tax_canceled":null,
      "tax_invoiced":null,
      "tax_refunded":null,
      "total_canceled":null,
      "total_invoiced":null,
      "total_offline_refunded":null,
      "total_online_refunded":null,
      "total_paid":null,
      "total_qty_ordered":"1.0000",
      "total_refunded":null,
      "can_ship_partially":null,
      "can_ship_partially_item":null,
      "customer_is_guest":"0",
      "customer_note_notify":"1",
      "billing_address_id":"382",
      "customer_group_id":"1",
      "edit_increment":null,
      "email_sent":"1",
      "forced_shipment_with_invoice":null,
      "payment_auth_expiration":null,
      "quote_address_id":null,
      "quote_id":"681",
      "shipping_address_id":"383",
      "adjustment_negative":null,
      "adjustment_positive":null,
      "base_adjustment_negative":null,
      "base_adjustment_positive":null,
      "base_shipping_discount_amount":"0.0000",
      "base_subtotal_incl_tax":"340.0000",
      "base_total_due":null,
      "payment_authorization_amount":null,
      "shipping_discount_amount":"0.0000",
      "subtotal_incl_tax":"340.0000",
      "total_due":null,
      "weight":"1.0000",
      "customer_dob":"2016-05-18 00:00:00",
      "increment_id":"145000006",
      "applied_rule_ids":null,
      "base_currency_code":"USD",
      "customer_email":"test@simicart.com",
      "customer_firstname":"Cody",
      "customer_lastname":"Nguyen",
      "customer_middlename":null,
      "customer_prefix":null,
      "customer_suffix":null,
      "customer_taxvat":null,
      "discount_description":null,
      "ext_customer_id":null,
      "ext_order_id":null,
      "global_currency_code":"USD",
      "hold_before_state":null,
      "hold_before_status":null,
      "order_currency_code":"USD",
      "original_increment_id":null,
      "relation_child_id":null,
      "relation_child_real_id":null,
      "relation_parent_id":null,
      "relation_parent_real_id":null,
      "remote_ip":"127.0.0.1",
      "shipping_method":"Flat Rate - Fixed",
      "store_currency_code":"USD",
      "store_name":"Main Website\nMadison Island\nEnglish",
      "x_forwarded_for":null,
      "customer_note":null,
      "created_at":"2016-06-08 07:21:37",
      "updated_at":"2016-06-08 07:21:39",
      "total_item_count":"1",
      "customer_gender":"2",
      "hidden_tax_amount":"0.0000",
      "base_hidden_tax_amount":"0.0000",
      "shipping_hidden_tax_amount":"0.0000",
      "base_shipping_hidden_tax_amnt":"0.0000",
      "hidden_tax_invoiced":null,
      "base_hidden_tax_invoiced":null,
      "hidden_tax_refunded":null,
      "base_hidden_tax_refunded":null,
      "shipping_incl_tax":"10.0000",
      "base_shipping_incl_tax":"10.0000",
      "coupon_rule_name":null,
      "paypal_ipn_customer_notified":"0",
      "gift_message_id":null,
      "base_customer_balance_amount":null,
      "customer_balance_amount":null,
      "base_customer_balance_invoiced":null,
      "customer_balance_invoiced":null,
      "base_customer_balance_refunded":null,
      "customer_balance_refunded":null,
      "bs_customer_bal_total_refunded":null,
      "customer_bal_total_refunded":null,
      "gift_cards":null,
      "base_gift_cards_amount":null,
      "gift_cards_amount":null,
      "base_gift_cards_invoiced":null,
      "gift_cards_invoiced":null,
      "base_gift_cards_refunded":null,
      "gift_cards_refunded":null,
      "gw_id":null,
      "gw_allow_gift_receipt":null,
      "gw_add_card":null,
      "gw_base_price":null,
      "gw_price":null,
      "gw_items_base_price":null,
      "gw_items_price":null,
      "gw_card_base_price":null,
      "gw_card_price":null,
      "gw_base_tax_amount":null,
      "gw_tax_amount":null,
      "gw_items_base_tax_amount":null,
      "gw_items_tax_amount":null,
      "gw_card_base_tax_amount":null,
      "gw_card_tax_amount":null,
      "gw_base_price_invoiced":null,
      "gw_price_invoiced":null,
      "gw_items_base_price_invoiced":null,
      "gw_items_price_invoiced":null,
      "gw_card_base_price_invoiced":null,
      "gw_card_price_invoiced":null,
      "gw_base_tax_amount_invoiced":null,
      "gw_tax_amount_invoiced":null,
      "gw_items_base_tax_invoiced":null,
      "gw_items_tax_invoiced":null,
      "gw_card_base_tax_invoiced":null,
      "gw_card_tax_invoiced":null,
      "gw_base_price_refunded":null,
      "gw_price_refunded":null,
      "gw_items_base_price_refunded":null,
      "gw_items_price_refunded":null,
      "gw_card_base_price_refunded":null,
      "gw_card_price_refunded":null,
      "gw_base_tax_amount_refunded":null,
      "gw_tax_amount_refunded":null,
      "gw_items_base_tax_refunded":null,
      "gw_items_tax_refunded":null,
      "gw_card_base_tax_refunded":null,
      "gw_card_tax_refunded":null,
      "reward_points_balance":null,
      "base_reward_currency_amount":null,
      "reward_currency_amount":null,
      "base_rwrd_crrncy_amt_invoiced":null,
      "rwrd_currency_amount_invoiced":null,
      "base_rwrd_crrncy_amnt_refnded":null,
      "rwrd_crrncy_amnt_refunded":null,
      "reward_points_balance_refund":null,
      "reward_points_balance_refunded":null,
      "reward_salesrule_points":null,
      "cod_fee":null,
      "base_cod_fee":null,
      "cod_fee_invoiced":null,
      "base_cod_fee_invoiced":null,
      "cod_tax_amount":null,
      "base_cod_tax_amount":null,
      "cod_tax_amount_invoiced":null,
      "base_cod_tax_amount_invoiced":null,
      "cod_fee_refunded":null,
      "base_cod_fee_refunded":null,
      "cod_tax_amount_refunded":null,
      "base_cod_tax_amount_refunded":null,
      "cod_fee_canceled":null,
      "base_cod_fee_canceled":null,
      "cod_tax_amount_canceled":null,
      "base_cod_tax_amount_canceled":null,
      "payment_authorization_expiration":null,
      "forced_do_shipment_with_invoice":null,
      "base_shipping_hidden_tax_amount":"0.0000",
      "payment_method":"Cash On Delivery",
      "shipping_address":{  
         "firstname":"Cody",
         "lastname":"Nguyen",
         "prefix":null,
         "suffix":null,
         "vat_id":"vat num",
         "street":"street",
         "city":"city",
         "region":"Alabama",
         "region_id":"1",
         "region_code":"AL",
         "postcode":"10000",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"098765412321",
         "email":"test@simicart.com",
         "company":"company",
         "latlng":""
      },
      "billing_address":{  
         "firstname":"Cody",
         "lastname":"Nguyen",
         "prefix":null,
         "suffix":null,
         "vat_id":"vat num",
         "street":"street",
         "city":"city",
         "region":"Alabama",
         "region_id":"1",
         "region_code":"AL",
         "postcode":"10000",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"098765412321",
         "email":"test@simicart.com",
         "company":"company",
         "latlng":""
      },
      "order_items":[  
         {  
            "item_id":"596",
            "order_id":"195",
            "parent_item_id":null,
            "quote_item_id":"2555",
            "store_id":"2",
            "created_at":"2016-06-08 07:21:37",
            "updated_at":"2016-06-08 07:21:37",
            "product_id":"425",
            "product_type":"configurable",
            "product_options":"a:6:{s:15:\"info_buyRequest\";a:6:{s:4:\"uenc\";s:84:\"aHR0cDovL2xvY2FsaG9zdC5jb20vbWFnZW50bzE5L2xhZmF5ZXR0ZS1jb252ZXJ0aWJsZS1kcmVzcy5odG1s\";s:7:\"product\";s:3:\"425\";s:8:\"form_key\";s:16:\"fr1AHQFca9gAFkhg\";s:15:\"related_product\";s:0:\"\";s:15:\"super_attribute\";a:2:{i:92;s:2:\"27\";i:180;s:2:\"74\";}s:3:\"qty\";s:1:\"1\";}s:15:\"attributes_info\";a:2:{i:0;a:2:{s:5:\"label\";s:5:\"Color\";s:5:\"value\";s:4:\"Blue\";}i:1;a:2:{s:5:\"label\";s:4:\"Size\";s:5:\"value\";s:1:\"6\";}}s:11:\"simple_name\";s:17:\"Convertible Dress\";s:10:\"simple_sku\";s:6:\"wsd015\";s:20:\"product_calculations\";i:1;s:13:\"shipment_type\";i:0;}",
            "weight":"1.0000",
            "is_virtual":"0",
            "sku":"wsd015",
            "name":"Lafayette Convertible Dress",
            "description":null,
            "applied_rule_ids":null,
            "additional_data":null,
            "free_shipping":"0",
            "is_qty_decimal":"0",
            "no_discount":"0",
            "qty_backordered":null,
            "qty_canceled":"0.0000",
            "qty_invoiced":"0.0000",
            "qty_ordered":"1.0000",
            "qty_refunded":"0.0000",
            "qty_shipped":"0.0000",
            "base_cost":null,
            "price":"340.0000",
            "base_price":"340.0000",
            "original_price":"340.0000",
            "base_original_price":"340.0000",
            "tax_percent":"0.0000",
            "tax_amount":"0.0000",
            "base_tax_amount":"0.0000",
            "tax_invoiced":"0.0000",
            "base_tax_invoiced":"0.0000",
            "discount_percent":"0.0000",
            "discount_amount":"0.0000",
            "base_discount_amount":"0.0000",
            "discount_invoiced":"0.0000",
            "base_discount_invoiced":"0.0000",
            "amount_refunded":"0.0000",
            "base_amount_refunded":"0.0000",
            "row_total":"340.0000",
            "base_row_total":"340.0000",
            "row_invoiced":"0.0000",
            "base_row_invoiced":"0.0000",
            "row_weight":"1.0000",
            "base_tax_before_discount":null,
            "tax_before_discount":null,
            "ext_order_item_id":null,
            "locked_do_invoice":null,
            "locked_do_ship":null,
            "price_incl_tax":"340.0000",
            "base_price_incl_tax":"340.0000",
            "row_total_incl_tax":"340.0000",
            "base_row_total_incl_tax":"340.0000",
            "hidden_tax_amount":"0.0000",
            "base_hidden_tax_amount":"0.0000",
            "hidden_tax_invoiced":null,
            "base_hidden_tax_invoiced":null,
            "hidden_tax_refunded":null,
            "base_hidden_tax_refunded":null,
            "is_nominal":"0",
            "tax_canceled":null,
            "hidden_tax_canceled":null,
            "tax_refunded":null,
            "base_tax_refunded":null,
            "discount_refunded":null,
            "base_discount_refunded":null,
            "gift_message_id":null,
            "gift_message_available":"1",
            "base_weee_tax_applied_amount":"0.0000",
            "base_weee_tax_applied_row_amnt":"0.0000",
            "base_weee_tax_applied_row_amount":"0.0000",
            "weee_tax_applied_amount":"0.0000",
            "weee_tax_applied_row_amount":"0.0000",
            "weee_tax_applied":"a:0:{}",
            "weee_tax_disposition":"0.0000",
            "weee_tax_row_disposition":"0.0000",
            "base_weee_tax_disposition":"0.0000",
            "base_weee_tax_row_disposition":"0.0000",
            "event_id":null,
            "giftregistry_item_id":null,
            "gw_id":null,
            "gw_base_price":null,
            "gw_price":null,
            "gw_base_tax_amount":null,
            "gw_tax_amount":null,
            "gw_base_price_invoiced":null,
            "gw_price_invoiced":null,
            "gw_base_tax_amount_invoiced":null,
            "gw_tax_amount_invoiced":null,
            "gw_base_price_refunded":null,
            "gw_price_refunded":null,
            "gw_base_tax_amount_refunded":null,
            "gw_tax_amount_refunded":null,
            "qty_returned":"0.0000",
            "has_children":true
         }
      ],
      "total":{  
         "subtotal_excl_tax":"340.0000",
         "subtotal_incl_tax":"340.0000",
         "shipping_hand_excl_tax":"10.0000",
         "shipping_hand_incl_tax":"10.0000",
         "tax":"0.0000",
         "discount":0,
         "grand_total_excl_tax":350,
         "grand_total_incl_tax":"350.0000",
         "currency_symbol":"$"
      }
   }
}
```

This endpoint retrieves an Order from history.

### HTTP Request

`GET /rest/orders/<id>`


## View Order Onpage (Checkout) Detail

```shell
curl "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16902",
            "s_method_code":"ups_GND",
            "s_method_title":"United Parcel Service",
            "s_method_fee":13.6,
            "s_method_name":"Ground",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16903",
            "s_method_code":"ups_3DS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":25.27,
            "s_method_name":"3 Day Select",
            "s_method_selected":true
         },
         {  
            "s_method_id":"16904",
            "s_method_code":"ups_1DA",
            "s_method_title":"United Parcel Service",
            "s_method_fee":70.57,
            "s_method_name":"Next Day Air",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16901",
            "s_method_code":"freeshipping_freeshipping",
            "s_method_title":"Free Shipping",
            "s_method_fee":0,
            "s_method_name":"Free",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16900",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":true
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":295,
         "subtotal_incl_tax":295,
         "shipping_hand_incl_tax":25.27,
         "shipping_hand_excl_tax":25.27,
         "tax":0,
         "grand_total_excl_tax":320.27,
         "grand_total_incl_tax":320.27
      }
   }
}
```

This endpoint Return Order Onepage (Checkout) information.


## Checkout Terms and Conditions

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews/1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "storeview":{  
      "checkout":{  
         "enable_guest_checkout":"1",
         "is_reload_payment_method":"0",
         "enable_agreements":"0",
         "checkout_terms_and_conditions":{  
            "title":"Title",
            "content":"Content"
         }
      }
   }
}
```

If there's Terms and condition for Checking Out, there'd be one more value at key storeview.checkout.checkout_terms_and_conditions while getting storeview configuration. 

- title: Term and condition Title (show on Order screen)

- content: Term and condition Detailed (show on Webview HTML)



## Checkout as New Customer


```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
  -d '{"b_address":
{
        "firstname":"My First Name",
        "lastname":"My Last Name2",
        "prefix":"My Prefix",
        "suffix":"My Suffix",
        "vat_id":"My Vat ID1",
        "street":"Street",
        "city":"City",
        "region_id":"5",
        "postcode":"123456",
        "country_name":"USA",
        "country_id":"US",
        "company":"Company",
        "telephone":"0987123456",
        "fax":"123456",
        "vat_id":"123",
		"email":"mail12@mail.com",
        "customer_password":"123456",
        "confirm_password":"123456"
    }
}'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16902",
            "s_method_code":"ups_GND",
            "s_method_title":"United Parcel Service",
            "s_method_fee":13.6,
            "s_method_name":"Ground",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16903",
            "s_method_code":"ups_3DS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":25.27,
            "s_method_name":"3 Day Select",
            "s_method_selected":true
         },
         {  
            "s_method_id":"16904",
            "s_method_code":"ups_1DA",
            "s_method_title":"United Parcel Service",
            "s_method_fee":70.57,
            "s_method_name":"Next Day Air",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16901",
            "s_method_code":"freeshipping_freeshipping",
            "s_method_title":"Free Shipping",
            "s_method_fee":0,
            "s_method_name":"Free",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16900",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":true
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":295,
         "subtotal_incl_tax":295,
         "shipping_hand_incl_tax":25.27,
         "shipping_hand_excl_tax":25.27,
         "tax":0,
         "grand_total_excl_tax":320.27,
         "grand_total_incl_tax":320.27
      }
   }
}
```

Start Checkout as new Customer (If shipping address is not added, the billing address will be used for shipping).
Shipping address is the same with Billing address, key is "b_address".
Address Data is the same (key/value) with Address editing.
If Password and Email added, the order would be "checkout as new customer", if not, it's "Checkout as Guest".


## Checkout as Guest


```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
  -d '{"b_address":
{
        "firstname":"My First Name",
        "lastname":"My Last Name2",
        "prefix":"My Prefix",
        "suffix":"My Suffix",
        "vat_id":"My Vat ID1",
        "street":"Street",
        "city":"City",
        "region_id":"5",
        "postcode":"123456",
        "country_name":"USA",
        "country_id":"US",
        "company":"Company",
        "telephone":"0987123456",
        "fax":"123456",
        "vat_id":"123"
    }
}
'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16836",
            "s_method_code":"ups_GND",
            "s_method_title":"United Parcel Service",
            "s_method_fee":13.6,
            "s_method_name":"Ground",
            "s_method_selected":true
         },
         {  
            "s_method_id":"16837",
            "s_method_code":"ups_3DS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":25.27,
            "s_method_name":"3 Day Select",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16838",
            "s_method_code":"ups_1DA",
            "s_method_title":"United Parcel Service",
            "s_method_fee":70.57,
            "s_method_name":"Next Day Air",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16835",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":true
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":134,
         "subtotal_incl_tax":145.06,
         "shipping_hand_incl_tax":13.6,
         "shipping_hand_excl_tax":13.6,
         "tax":11.06,
         "grand_total_excl_tax":147.6,
         "grand_total_incl_tax":158.66
      }
   }
}
```

## Checkout as Logged in Customer


```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
  -d '{"b_address":
{
        "entity_id":"102"
    }
"s_address":
{
        "entity_id":"103"
    }
}
'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"Cody",
         "lastname":"Nguyen",
         "prefix":null,
         "suffix":null,
         "vat_id":"vat num",
         "street":"street",
         "city":"city",
         "region":"Alabama",
         "region_id":"1",
         "region_code":"AL",
         "postcode":"10000",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"098765412321",
         "email":"test@simicart.com",
         "company":"company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name2",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"56",
         "region_id":"56",
         "region_code":null,
         "postcode":"123456",
         "country_name":"Albania",
         "country_id":"AL",
         "telephone":"0987123456",
         "email":"test@simicart.com",
         "company":"Company2",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16859",
            "s_method_code":"ups_XPD",
            "s_method_title":"United Parcel Service",
            "s_method_fee":242.53,
            "s_method_name":"Worldwide Expedited",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16860",
            "s_method_code":"ups_WXS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":285.9,
            "s_method_name":"Worldwide Express Saver",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16858",
            "s_method_code":"freeshipping_freeshipping",
            "s_method_title":"Free Shipping",
            "s_method_fee":0,
            "s_method_name":"Free",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16857",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":true
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":277,
         "subtotal_incl_tax":277,
         "tax":0,
         "discount":5,
         "grand_total_excl_tax":272,
         "grand_total_incl_tax":272,
         "coupon_code":"MYCOUPON"
      }
   }
}
```

If customer logged in and has Address on address Book, Shipping and Billing address can be added via entity Id beside the Detail Address like Guest checking out.


## Save Shipping Method


```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
  -d '{  
"s_method":{
   "method":"ups_GND"
   }   
}'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16832",
            "s_method_code":"ups_GND",
            "s_method_title":"United Parcel Service",
            "s_method_fee":13.6,
            "s_method_name":"Ground",
            "s_method_selected":true
         },
         {  
            "s_method_id":"16833",
            "s_method_code":"ups_3DS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":25.27,
            "s_method_name":"3 Day Select",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16834",
            "s_method_code":"ups_1DA",
            "s_method_title":"United Parcel Service",
            "s_method_fee":70.57,
            "s_method_name":"Next Day Air",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16831",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":true
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":134,
         "subtotal_incl_tax":145.06,
         "shipping_hand_incl_tax":13.6,
         "shipping_hand_excl_tax":13.6,
         "tax":11.06,
         "grand_total_excl_tax":147.6,
         "grand_total_incl_tax":158.66
      }
   }
}
```

This request is to save Shipping Method

## Save Payment Method


```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
  -d '{  
"p_method":{
   "method":"PHOENIX_CASHONDELIVERY"
   }
}'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16840",
            "s_method_code":"ups_GND",
            "s_method_title":"United Parcel Service",
            "s_method_fee":13.6,
            "s_method_name":"Ground",
            "s_method_selected":true
         },
         {  
            "s_method_id":"16841",
            "s_method_code":"ups_3DS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":25.27,
            "s_method_name":"3 Day Select",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16842",
            "s_method_code":"ups_1DA",
            "s_method_title":"United Parcel Service",
            "s_method_fee":70.57,
            "s_method_name":"Next Day Air",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16839",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":true
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":134,
         "subtotal_incl_tax":145.06,
         "shipping_hand_incl_tax":13.6,
         "shipping_hand_excl_tax":13.6,
         "tax":11.06,
         "grand_total_excl_tax":147.6,
         "grand_total_incl_tax":158.66
      }
   }
}
```

This request is to save Payment Method

## Save Payment Method with Card Details


```shell
curl -X PUT "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
  -d '{  
"p_method":{
   "method":"AUTHORIZENET",
   "cc_type":"VI",
   "cc_cid":"123",
   "cc_exp_month":"01",
   "cc_number":"4111111111111111",
   "cc_exp_year":"2019"
   }
}'
  "

```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "billing_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping_address":{  
         "firstname":"My First Name",
         "lastname":"My Last Name2",
         "prefix":null,
         "suffix":null,
         "vat_id":"123",
         "street":"Street",
         "city":"City",
         "region":"Arkansas",
         "region_id":"5",
         "region_code":"AR",
         "postcode":"123456",
         "country_name":"United States",
         "country_id":"US",
         "telephone":"0987123456",
         "email":null,
         "company":"Company",
         "latlng":""
      },
      "shipping":[  
         {  
            "s_method_id":"16832",
            "s_method_code":"ups_GND",
            "s_method_title":"United Parcel Service",
            "s_method_fee":13.6,
            "s_method_name":"Ground",
            "s_method_selected":true
         },
         {  
            "s_method_id":"16833",
            "s_method_code":"ups_3DS",
            "s_method_title":"United Parcel Service",
            "s_method_fee":25.27,
            "s_method_name":"3 Day Select",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16834",
            "s_method_code":"ups_1DA",
            "s_method_title":"United Parcel Service",
            "s_method_fee":70.57,
            "s_method_name":"Next Day Air",
            "s_method_selected":false
         },
         {  
            "s_method_id":"16831",
            "s_method_code":"flatrate_flatrate",
            "s_method_title":"Flat Rate",
            "s_method_fee":10,
            "s_method_name":"Fixed",
            "s_method_selected":false
         }
      ],
      "payment":[  
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"AUTHORIZENET",
            "title":"Credit Card (Authorize.net)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":true
         },
         {  
            "content":null,
            "payment_method":"PHOENIX_CASHONDELIVERY",
            "title":"Cash on Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "content":"",
            "payment_method":"CASHONDELIVERY",
            "title":"Cash On Delivery",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "payment_method":"CHECKMO",
            "title":"Check \/ Money order",
            "content":"Make Check Payable to: Send Check to: ",
            "show_type":0,
            "p_method_selected":false
         },
         {  
            "cc_types":[  
               {  
                  "cc_code":"AE",
                  "cc_name":"American Express"
               },
               {  
                  "cc_code":"VI",
                  "cc_name":"Visa"
               },
               {  
                  "cc_code":"MC",
                  "cc_name":"MasterCard"
               },
               {  
                  "cc_code":"DI",
                  "cc_name":"Discover"
               }
            ],
            "payment_method":"CCSAVE",
            "title":"Credit Card (saved)",
            "useccv":"0",
            "show_type":1,
            "p_method_selected":false
         }
      ],
      "total":{  
         "subtotal_excl_tax":134,
         "subtotal_incl_tax":145.06,
         "shipping_hand_incl_tax":13.6,
         "shipping_hand_excl_tax":13.6,
         "tax":11.06,
         "grand_total_excl_tax":147.6,
         "grand_total_incl_tax":158.66
      }
   }
}
```

This request is to save Payment Method with Card Detail

## Place order


```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "invoice_number":"145000009",
      "payment_method":"phoenix_cashondelivery"
   }
}
```

This request is to place Order


## Place order and Show notification


```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>" \
```

> The above command returns JSON structured like this:

```json
{  
   "order":{  
      "invoice_number":"302000002",
      "payment_method":"checkmo",
      "notification":{  
         "show_popup":"1",
         "title":"title",
         "url":null,
         "message":"order message",
         "notice_sanbox":0,
         "type":"2",
         "productID":"1",
         "categoryID":"6",
         "categoryName":"Accessories",
         "has_children":1,
         "created_time":"2016-06-16 04:47:33",
         "notice_type":3
      }
   }
}
```

If there's notification to be shown, the result of order placing request would contain 'notification' value as array.