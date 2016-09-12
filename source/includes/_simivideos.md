# Product Videos

## Product Videos Properties

Attributes| Type| Description
--------- | ------- | -----------
video_id | id | Video Id
video_url | string | Video URL
video_key | string | Video Key (for Youtube SDK)
video_title | string | Video Title
status | int | Video Enabled or Not


## Videos of a Product on Product Detail

```shell
curl "https://abc.com/simiconnector/rest/v2/simiconnector/rest/v2/products/16" \
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
      "additional":{  
         "model":{  
            "label":"Model",
            "value":"2610",
            "code":"model"
         },
         "in_depth":{  
            "label":"In Depth",
            "value":"<ul>\r\n<ul class\"disc\">\r\n<li>Integrated camera with video recorder to capture those special moments<br><\/li>\r\n<li>Enriched data connections for complete mobile access via Email, MMS, and MEdia Net<br><\/li>\r\n<li> Personalize with downloadable MP3 and polyphonic Ring tones, Games, and Graphics<br><\/li>\r\n<li>Use AIM, Yahoo! and MSN Messenger to stay in touch on the go<br><\/li>\r\n<li>Mobile Internet browser and email<\/li>\r\n<\/ul>",
            "code":"in_depth"
         },
         "dimension":{  
            "label":"Dimensions",
            "value":"4.1 x 1.7 x 0.7 inches ",
            "code":"dimension"
         },
         "activation_information":{  
            "label":"Activation Information",
            "value":"Conditional $250 Equipment Discount Included: Your price paid includes an equipment discount of $250 that has been provided to you in exchange for either activating a new, non-substitute line of service or renewing an existing line of service with AT&T and your agreement that for the 181-day period following such activation or renewal you will: (1) pay your balance due to AT&T each month and otherwise maintain your account in good standing; (2) not disconnect this AT&T line of service; (3) not transfer this equipment to another AT&T line of service; (4) not change your AT&T service rate plan to a lower monthly service rate--this includes canceling or removing required PDA, BlackBerry, or smartphone features after your product has shipped; (5) not use this line of service to replace an existing account with AT&T. If these conditions are not met, you hereby authorize Magento to charge your credit card $250 as reimbursement of this equipment discount without need for further approval.",
            "code":"activation_information"
         }
      },
      "images":[  
         {  
            "url":"http:\/\/localhost.com\/magento18\/media\/catalog\/product\/cache\/1\/thumbnail\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/thumbnail.jpg",
            "position":"1"
         },
         {  
            "url":"http:\/\/localhost.com\/magento18\/media\/catalog\/product\/cache\/1\/thumbnail\/600x600\/040ec09b1e35df139433887a97daa66f\/images\/catalog\/product\/placeholder\/thumbnail.jpg",
            "position":"2"
         }
      ],
      "app_prices":{  
         "has_special_price":0,
         "show_ex_in_price":0,
         "price":149.99
      },
      "app_reviews":{  
         "rate":2,
         "number":2,
         "5_star_number":0,
         "4_star_number":0,
         "3_star_number":1,
         "2_star_number":0,
         "1_star_number":1,
         "form_add_reviews":[  
            {  
               "rates":[  
                  {  
                     "rate_code":"Quality",
                     "rate_options":[  
                        {  
                           "key":"1",
                           "value":"1"
                        },
                        {  
                           "key":"1",
                           "value":"2"
                        },
                        {  
                           "key":"1",
                           "value":"3"
                        },
                        {  
                           "key":"1",
                           "value":"4"
                        },
                        {  
                           "key":"1",
                           "value":"5"
                        }
                     ]
                  },
                  {  
                     "rate_code":"Price",
                     "rate_options":[  
                        {  
                           "key":"3",
                           "value":"11"
                        },
                        {  
                           "key":"3",
                           "value":"12"
                        },
                        {  
                           "key":"3",
                           "value":"13"
                        },
                        {  
                           "key":"3",
                           "value":"14"
                        },
                        {  
                           "key":"3",
                           "value":"15"
                        }
                     ]
                  },
                  {  
                     "rate_code":"Value",
                     "rate_options":[  
                        {  
                           "key":"2",
                           "value":"6"
                        },
                        {  
                           "key":"2",
                           "value":"7"
                        },
                        {  
                           "key":"2",
                           "value":"8"
                        },
                        {  
                           "key":"2",
                           "value":"9"
                        },
                        {  
                           "key":"2",
                           "value":"10"
                        }
                     ]
                  }
               ],
               "form_review":{  
                  "key_1":"nickname",
                  "key_2":"title",
                  "key_3":"detail"
               }
            }
         ]
      },
      "app_options":{  
         "custom_options":[  

         ]
      },
      "wishlist_item_id":null,
      "product_label":{  
         "name":"132123",
         "label_id":"1",
         "description":"1212",
         "text":"abc",
         "image":"http:\/\/localhost.com\/magento18\/media\/simi\/simiconnector\/productlabel\/1473429806_1_eid--3-ar.jpg",
         "position":"1"
      },
      "product_video":[  
         {  
            "video_id":"1",
            "video_url":"https:\/\/www.youtube.com\/watch?v=AfgX7GB_Rkc",
            "video_key":"AfgX7GB_Rkc",
            "video_title":"121212",
            "product_ids":"16, 17, 18, 19, 20, 25",
            "storeview_id":"0",
            "status":"1"
         }
      ]
   }
}
```

On product detail there will be a list of Videos defined with key "product_video" 

## Get Videos of a Product

```shell
curl "https://abc.com/simiconnector/rest/v2/simivideos?product_id=397" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1",
      "2",
      "3"
   ],
   "simivideos":[  
      {  
         "video_id":"1",
         "video_url":"https:\/\/www.youtube.com\/watch?v=AfgX7GB_Rkc",
         "video_key":"AfgX7GB_Rkc",
         "video_title":"Test 1",
         "product_ids":"338, 372, 374, 378, 339, 397",
         "status":"1"
      },
      {  
         "video_id":"2",
         "video_url":"https:\/\/www.youtube.com\/watch?v=6SXYovVYvOQ&t=1474s",
         "video_key":"6SXYovVYvOQ",
         "video_title":"Test 2",
         "product_ids":"378, 339, 397",
         "status":"1"
      },
      {  
         "video_id":"3",
         "video_url":"http:\/\/www.sample-videos.com\/video\/mp4\/720\/big_buck_bunny_720p_1mb.mp4",
         "video_key":null,
         "video_title":"Test 3",
         "product_ids":"337, 397",
         "status":"1"
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

This request is to get Videos of Product.
If the Video key is NULL, then it's not a Valid Youtube URL, Use Webview to Open Video URL instead.