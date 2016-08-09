# Store Views

## Store View Properties

Attributes| Type| Description
--------- | ------- | -----------
store_id | string | Store View id <code>read only</code>
code | string | Store View code
base_url | string | Store View Base URL
website_id | int | id of the Website that Store View belongs to
group_id | int | id of the Store (Group) that Store View belongs to
name | string | Store View name
base_url | string | Store View Base URL
sort_order | int | display sort order
is_active | int | "1" for active, "0" for inactive
base | array | Store View base information
sales | array | Store View sales configuration
checkout | array | Store View checkout configuration
tax | array | Store View tax configuration
google_analytics | array | Google API configuration values
customer | array | Customer Address and Account configuration
wishlist | array | Website Wishlist configuration
catalog | array | Catalog frontend display and review configuration values
cms | array | CMS pages


## View Default Store View

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews/default" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "storeview":{  
      "base":{  
         "country_code":"US",
         "country_name":"\u00c9tats-Unis",
         "locale_identifier":"fr_FR",
         "store_id":"2",
         "store_name":"French",
         "store_code":"french",
         "use_store":"0",
		 "group_id":"1",
		 "base_url":"http:\/\/dev-vn.magestore.com\/simicart\/new\/magento\/en",
         "is_rtl":"0",
         "is_show_sample_data":"1",
         "android_sender":"518903118242",
         "currency_symbol":"$US",
         "currency_code":"USD",
         "currency_position":"after",
         "thousand_separator":",",
         "decimal_separator":".",
         "min_number_of_decimals":"0",
         "max_number_of_decimals":"2",
         "currencies":[  
            {  
               "value":"ALL",
               "title":"lek albanais"
            },
            {  
               "value":"COP",
               "title":"peso colombien"
            },
            {  
               "value":"KMF",
               "title":"franc comorien"
            },
            {  
               "value":"CDF",
               "title":"franc congolais"
            },
            {  
               "value":"HRK",
               "title":"kuna croate"
            },
            {  
               "value":"CZK",
               "title":"couronne tch\u00e8que"
            },
            {  
               "value":"QAR",
               "title":"rial qatari"
            },
            {  
               "value":"RHD",
               "title":"dollar rhod\u00e9sien"
            },
            {  
               "value":"SKK",
               "title":"couronne slovaque"
            },
            {  
               "value":"SOS",
               "title":"shilling somalien"
            },
            {  
               "value":"USD",
               "title":"dollar des \u00c9tats-Unis"
            }
         ]
      },
      "sales":{  
         "sales_reorder_allow":"1",
         "sales_totals_sort_subtotal":"10",
         "sales_totals_sort_discount":"20",
         "sales_totals_sort_shipping":"30",
         "sales_totals_sort_weee":"50",
         "sales_totals_sort_tax":"40",
         "sales_totals_sort_grand_total":"100"
      },
      "checkout":{  
         "enable_guest_checkout":"1",
         "is_reload_payment_method":"0",
         "enable_agreements":"0"
      },
      "tax":{  
         "tax_display_type":"1",
         "tax_display_shipping":"1",
         "tax_cart_display_price":"1",
         "tax_cart_display_subtotal":"2",
         "tax_cart_display_shipping":"3",
         "tax_cart_display_grandtotal":"0",
         "tax_cart_display_full_summary":"0",
         "tax_cart_display_zero_tax":"0"
      },
      "google_analytics":{  
         "google_analytics_active":"0",
         "google_analytics_type":"universal",
         "google_analytics_account":"",
         "google_analytics_anonymization":"0"
      },
      "customer":{  
         "address_option":{  
            "prefix_show":"",
            "suffix_show":"",
            "dob_show":"",
            "taxvat_show":"opt",
            "gender_show":"",
            "gender_value":[  
               {  
                  "label":"Male",
                  "value":"1"
               },
               {  
                  "label":"Female",
                  "value":"2"
               }
            ]
         },
         "account_option":{  
            "taxvat_show":"0"
         }
      },
      "wishlist":{  
         "wishlist_general_active":"1",
         "wishlist_wishlist_link_use_qty":"0"
      },
      "catalog":{  
         "frontend":{  
            "view_products_default":"0",
            "is_show_zero_price":"1",
            "is_show_link_all_product":"1",
            "catalog_frontend_list_mode":"grid-list",
            "catalog_frontend_grid_per_page_values":"12,24,36",
            "catalog_frontend_list_per_page":"10",
            "catalog_frontend_list_allow_all":"0",
            "catalog_frontend_default_sort_by":"position",
            "catalog_frontend_flat_catalog_category":"0",
            "catalog_frontend_flat_catalog_product":"0",
            "catalog_frontend_parse_url_directives":"1"
         },
         "review":{  
            "catalog_review_allow_guest":"1"
         }
      },
      "cms":{  
         "all_ids":[  
            "1",
            "2"
         ],
         "cmspages":[  
            {  
               "cms_id":"1",
               "cms_title":"Title 1",
               "cms_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/cms\/photo1464572154470@2x.png",
               "cms_content":"Content 1",
               "cms_status":"0",
               "website_id":"0",
               "sort_order":"1",
               "entity_id":"51",
               "content_type":"1",
               "item_id":"1",
               "store_view_id":"2"
            },
            {  
               "cms_id":"2",
               "cms_title":"Title 2",
               "cms_image":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/cms\/photo1464572154555@2x.png",
               "cms_content":"Content 2",
               "cms_status":"1",
               "website_id":"0",
               "sort_order":"2",
               "entity_id":"53",
               "content_type":"1",
               "item_id":"2",
               "store_view_id":"2"
            }
         ],
         "total":2,
         "page_size":15,
         "from":0
      },
      "allowed_countries":[  
         {  
            "country_code":"US",
            "country_name":"\u00c9tats-Unis",
            "states":[  
               {  
                  "state_id":"1",
                  "state_name":"Alabama",
                  "state_code":"AL"
               },
               {  
                  "state_id":"2",
                  "state_name":"Alaska",
                  "state_code":"AK"
               },
               {  
                  "state_id":"3",
                  "state_name":"American Samoa",
                  "state_code":"AS"
               },
               {  
                  "state_id":"4",
                  "state_name":"Arizona",
                  "state_code":"AZ"
               },
               {  
                  "state_id":"5",
                  "state_name":"Arkansas",
                  "state_code":"AR"
               },
               {  
                  "state_id":"6",
                  "state_name":"Armed Forces Africa",
                  "state_code":"AE"
               },
               {  
                  "state_id":"7",
                  "state_name":"Armed Forces Americas",
                  "state_code":"AA"
               },
               {  
                  "state_id":"8",
                  "state_name":"Armed Forces Canada",
                  "state_code":"AE"
               },
               {  
                  "state_id":"9",
                  "state_name":"Armed Forces Europe",
                  "state_code":"AE"
               },
               {  
                  "state_id":"10",
                  "state_name":"Armed Forces Middle East",
                  "state_code":"AE"
               },
               {  
                  "state_id":"11",
                  "state_name":"Armed Forces Pacific",
                  "state_code":"AP"
               },
               {  
                  "state_id":"12",
                  "state_name":"California",
                  "state_code":"CA"
               },
               {  
                  "state_id":"13",
                  "state_name":"Colorado",
                  "state_code":"CO"
               },
               {  
                  "state_id":"14",
                  "state_name":"Connecticut",
                  "state_code":"CT"
               },
               {  
                  "state_id":"15",
                  "state_name":"Delaware",
                  "state_code":"DE"
               },
               {  
                  "state_id":"16",
                  "state_name":"District of Columbia",
                  "state_code":"DC"
               },
               {  
                  "state_id":"17",
                  "state_name":"Federated States Of Micronesia",
                  "state_code":"FM"
               },
               {  
                  "state_id":"18",
                  "state_name":"Florida",
                  "state_code":"FL"
               },
               {  
                  "state_id":"19",
                  "state_name":"Georgia",
                  "state_code":"GA"
               },
               {  
                  "state_id":"20",
                  "state_name":"Guam",
                  "state_code":"GU"
               },
               {  
                  "state_id":"21",
                  "state_name":"Hawaii",
                  "state_code":"HI"
               },
               {  
                  "state_id":"22",
                  "state_name":"Idaho",
                  "state_code":"ID"
               },
               {  
                  "state_id":"23",
                  "state_name":"Illinois",
                  "state_code":"IL"
               },
               {  
                  "state_id":"24",
                  "state_name":"Indiana",
                  "state_code":"IN"
               },
               {  
                  "state_id":"25",
                  "state_name":"Iowa",
                  "state_code":"IA"
               },
               {  
                  "state_id":"26",
                  "state_name":"Kansas",
                  "state_code":"KS"
               },
               {  
                  "state_id":"27",
                  "state_name":"Kentucky",
                  "state_code":"KY"
               },
               {  
                  "state_id":"28",
                  "state_name":"Louisiana",
                  "state_code":"LA"
               },
               {  
                  "state_id":"29",
                  "state_name":"Maine",
                  "state_code":"ME"
               },
               {  
                  "state_id":"30",
                  "state_name":"Marshall Islands",
                  "state_code":"MH"
               },
               {  
                  "state_id":"31",
                  "state_name":"Maryland",
                  "state_code":"MD"
               },
               {  
                  "state_id":"32",
                  "state_name":"Massachusetts",
                  "state_code":"MA"
               },
               {  
                  "state_id":"33",
                  "state_name":"Michigan",
                  "state_code":"MI"
               },
               {  
                  "state_id":"34",
                  "state_name":"Minnesota",
                  "state_code":"MN"
               },
               {  
                  "state_id":"35",
                  "state_name":"Mississippi",
                  "state_code":"MS"
               },
               {  
                  "state_id":"36",
                  "state_name":"Missouri",
                  "state_code":"MO"
               },
               {  
                  "state_id":"37",
                  "state_name":"Montana",
                  "state_code":"MT"
               },
               {  
                  "state_id":"38",
                  "state_name":"Nebraska",
                  "state_code":"NE"
               },
               {  
                  "state_id":"39",
                  "state_name":"Nevada",
                  "state_code":"NV"
               },
               {  
                  "state_id":"40",
                  "state_name":"New Hampshire",
                  "state_code":"NH"
               },
               {  
                  "state_id":"41",
                  "state_name":"New Jersey",
                  "state_code":"NJ"
               },
               {  
                  "state_id":"42",
                  "state_name":"New Mexico",
                  "state_code":"NM"
               },
               {  
                  "state_id":"43",
                  "state_name":"New York",
                  "state_code":"NY"
               },
               {  
                  "state_id":"44",
                  "state_name":"North Carolina",
                  "state_code":"NC"
               },
               {  
                  "state_id":"45",
                  "state_name":"North Dakota",
                  "state_code":"ND"
               },
               {  
                  "state_id":"46",
                  "state_name":"Northern Mariana Islands",
                  "state_code":"MP"
               },
               {  
                  "state_id":"47",
                  "state_name":"Ohio",
                  "state_code":"OH"
               },
               {  
                  "state_id":"48",
                  "state_name":"Oklahoma",
                  "state_code":"OK"
               },
               {  
                  "state_id":"49",
                  "state_name":"Oregon",
                  "state_code":"OR"
               },
               {  
                  "state_id":"50",
                  "state_name":"Palau",
                  "state_code":"PW"
               },
               {  
                  "state_id":"51",
                  "state_name":"Pennsylvania",
                  "state_code":"PA"
               },
               {  
                  "state_id":"52",
                  "state_name":"Puerto Rico",
                  "state_code":"PR"
               },
               {  
                  "state_id":"53",
                  "state_name":"Rhode Island",
                  "state_code":"RI"
               },
               {  
                  "state_id":"54",
                  "state_name":"South Carolina",
                  "state_code":"SC"
               },
               {  
                  "state_id":"55",
                  "state_name":"South Dakota",
                  "state_code":"SD"
               },
               {  
                  "state_id":"56",
                  "state_name":"Tennessee",
                  "state_code":"TN"
               },
               {  
                  "state_id":"57",
                  "state_name":"Texas",
                  "state_code":"TX"
               },
               {  
                  "state_id":"58",
                  "state_name":"Utah",
                  "state_code":"UT"
               },
               {  
                  "state_id":"59",
                  "state_name":"Vermont",
                  "state_code":"VT"
               },
               {  
                  "state_id":"60",
                  "state_name":"Virgin Islands",
                  "state_code":"VI"
               },
               {  
                  "state_id":"61",
                  "state_name":"Virginia",
                  "state_code":"VA"
               },
               {  
                  "state_id":"62",
                  "state_name":"Washington",
                  "state_code":"WA"
               },
               {  
                  "state_id":"63",
                  "state_name":"West Virginia",
                  "state_code":"WV"
               },
               {  
                  "state_id":"64",
                  "state_name":"Wisconsin",
                  "state_code":"WI"
               },
               {  
                  "state_id":"65",
                  "state_name":"Wyoming",
                  "state_code":"WY"
               }
            ]
         },
         {  
            "country_code":"AD",
            "country_name":"Andorre",
            "states":[  

            ]
         },
         {  
            "country_code":"AE",
            "country_name":"\u00c9mirats arabes unis",
            "states":[  

            ]
         },
         {  
            "country_code":"AF",
            "country_name":"Afghanistan",
            "states":[  

            ]
         },
         {  
            "country_code":"AG",
            "country_name":"Antigua-et-Barbuda",
            "states":[  

            ]
         },
         {  
            "country_code":"AI",
            "country_name":"Anguilla",
            "states":[  

            ]
         },
         {  
            "country_code":"AL",
            "country_name":"Albanie",
            "states":[  

            ]
         },
         {  
            "country_code":"AM",
            "country_name":"Arm\u00e9nie",
            "states":[  

            ]
         },
         {  
            "country_code":"AN",
            "country_name":"Antilles n\u00e9erlandaises",
            "states":[  

            ]
         },
         {  
            "country_code":"AO",
            "country_name":"Angola",
            "states":[  

            ]
         },
         {  
            "country_code":"AQ",
            "country_name":"Antarctique",
            "states":[  

            ]
         },
         {  
            "country_code":"AR",
            "country_name":"Argentine",
            "states":[  

            ]
         },
         {  
            "country_code":"AS",
            "country_name":"Samoa am\u00e9ricaines",
            "states":[  

            ]
         },
         {  
            "country_code":"AT",
            "country_name":"Autriche",
            "states":[  
               {  
                  "state_id":"102",
                  "state_name":"Burgenland",
                  "state_code":"BL"
               },
               {  
                  "state_id":"99",
                  "state_name":"K\u00e4rnten",
                  "state_code":"KN"
               },
               {  
                  "state_id":"96",
                  "state_name":"Nieder\u00f6sterreich",
                  "state_code":"NO"
               },
               {  
                  "state_id":"97",
                  "state_name":"Ober\u00f6sterreich",
                  "state_code":"OO"
               },
               {  
                  "state_id":"98",
                  "state_name":"Salzburg",
                  "state_code":"SB"
               },
               {  
                  "state_id":"100",
                  "state_name":"Steiermark",
                  "state_code":"ST"
               },
               {  
                  "state_id":"101",
                  "state_name":"Tirol",
                  "state_code":"TI"
               },
               {  
                  "state_id":"103",
                  "state_name":"Vorarlberg",
                  "state_code":"VB"
               },
               {  
                  "state_id":"95",
                  "state_name":"Wien",
                  "state_code":"WI"
               }
            ]
         },
         {  
            "country_code":"AU",
            "country_name":"Australie",
            "states":[  

            ]
         },
         {  
            "country_code":"AW",
            "country_name":"Aruba",
            "states":[  

            ]
         },
         {  
            "country_code":"AX",
            "country_name":"\u00celes \u00c5land",
            "states":[  

            ]
         },
         {  
            "country_code":"AZ",
            "country_name":"Azerba\u00efdjan",
            "states":[  

            ]
         },
         {  
            "country_code":"BA",
            "country_name":"Bosnie-Herz\u00e9govine",
            "states":[  

            ]
         },
         {  
            "country_code":"BB",
            "country_name":"Barbade",
            "states":[  

            ]
         },
         {  
            "country_code":"BD",
            "country_name":"Bangladesh",
            "states":[  

            ]
         },
         {  
            "country_code":"BE",
            "country_name":"Belgique",
            "states":[  

            ]
         },
         {  
            "country_code":"BF",
            "country_name":"Burkina Faso",
            "states":[  

            ]
         },
         {  
            "country_code":"BG",
            "country_name":"Bulgarie",
            "states":[  

            ]
         },
         {  
            "country_code":"BH",
            "country_name":"Bahre\u00efn",
            "states":[  

            ]
         },
         {  
            "country_code":"BI",
            "country_name":"Burundi",
            "states":[  

            ]
         },
         {  
            "country_code":"BJ",
            "country_name":"B\u00e9nin",
            "states":[  

            ]
         },
         {  
            "country_code":"BL",
            "country_name":"Saint-Barth\u00e9lemy",
            "states":[  

            ]
         },
         {  
            "country_code":"BM",
            "country_name":"Bermudes",
            "states":[  

            ]
         },
         {  
            "country_code":"BN",
            "country_name":"Brun\u00e9i Darussalam",
            "states":[  

            ]
         },
         {  
            "country_code":"BO",
            "country_name":"Bolivie",
            "states":[  

            ]
         },
         {  
            "country_code":"BR",
            "country_name":"Br\u00e9sil",
            "states":[  

            ]
         },
         {  
            "country_code":"BS",
            "country_name":"Bahamas",
            "states":[  

            ]
         },
         {  
            "country_code":"BT",
            "country_name":"Bhoutan",
            "states":[  

            ]
         },
         {  
            "country_code":"BV",
            "country_name":"\u00cele Bouvet",
            "states":[  

            ]
         },
         {  
            "country_code":"BW",
            "country_name":"Botswana",
            "states":[  

            ]
         },
         {  
            "country_code":"BY",
            "country_name":"Bi\u00e9lorussie",
            "states":[  

            ]
         },
         {  
            "country_code":"BZ",
            "country_name":"Belize",
            "states":[  

            ]
         },
         {  
            "country_code":"CA",
            "country_name":"Canada",
            "states":[  
               {  
                  "state_id":"66",
                  "state_name":"Alberta",
                  "state_code":"AB"
               },
               {  
                  "state_id":"67",
                  "state_name":"British Columbia",
                  "state_code":"BC"
               },
               {  
                  "state_id":"68",
                  "state_name":"Manitoba",
                  "state_code":"MB"
               },
               {  
                  "state_id":"70",
                  "state_name":"New Brunswick",
                  "state_code":"NB"
               },
               {  
                  "state_id":"69",
                  "state_name":"Newfoundland and Labrador",
                  "state_code":"NL"
               },
               {  
                  "state_id":"72",
                  "state_name":"Northwest Territories",
                  "state_code":"NT"
               },
               {  
                  "state_id":"71",
                  "state_name":"Nova Scotia",
                  "state_code":"NS"
               },
               {  
                  "state_id":"73",
                  "state_name":"Nunavut",
                  "state_code":"NU"
               },
               {  
                  "state_id":"74",
                  "state_name":"Ontario",
                  "state_code":"ON"
               },
               {  
                  "state_id":"75",
                  "state_name":"Prince Edward Island",
                  "state_code":"PE"
               },
               {  
                  "state_id":"76",
                  "state_name":"Quebec",
                  "state_code":"QC"
               },
               {  
                  "state_id":"77",
                  "state_name":"Saskatchewan",
                  "state_code":"SK"
               },
               {  
                  "state_id":"78",
                  "state_name":"Yukon Territory",
                  "state_code":"YT"
               }
            ]
         },
         {  
            "country_code":"CC",
            "country_name":"\u00celes Cocos (Keeling)",
            "states":[  

            ]
         },
         {  
            "country_code":"CD",
            "country_name":"Congo-Kinshasa",
            "states":[  

            ]
         },
         {  
            "country_code":"CF",
            "country_name":"R\u00e9publique centrafricaine",
            "states":[  

            ]
         },
         {  
            "country_code":"CG",
            "country_name":"Congo-Brazzaville",
            "states":[  

            ]
         },
         {  
            "country_code":"CH",
            "country_name":"Suisse",
            "states":[  
               {  
                  "state_id":"104",
                  "state_name":"Aargau",
                  "state_code":"AG"
               },
               {  
                  "state_id":"106",
                  "state_name":"Appenzell Ausserrhoden",
                  "state_code":"AR"
               },
               {  
                  "state_id":"105",
                  "state_name":"Appenzell Innerrhoden",
                  "state_code":"AI"
               },
               {  
                  "state_id":"108",
                  "state_name":"Basel-Landschaft",
                  "state_code":"BL"
               },
               {  
                  "state_id":"109",
                  "state_name":"Basel-Stadt",
                  "state_code":"BS"
               },
               {  
                  "state_id":"107",
                  "state_name":"Bern",
                  "state_code":"BE"
               },
               {  
                  "state_id":"110",
                  "state_name":"Freiburg",
                  "state_code":"FR"
               },
               {  
                  "state_id":"111",
                  "state_name":"Genf",
                  "state_code":"GE"
               },
               {  
                  "state_id":"112",
                  "state_name":"Glarus",
                  "state_code":"GL"
               },
               {  
                  "state_id":"113",
                  "state_name":"Graub\u00fcnden",
                  "state_code":"GR"
               },
               {  
                  "state_id":"114",
                  "state_name":"Jura",
                  "state_code":"JU"
               },
               {  
                  "state_id":"115",
                  "state_name":"Luzern",
                  "state_code":"LU"
               },
               {  
                  "state_id":"116",
                  "state_name":"Neuenburg",
                  "state_code":"NE"
               },
               {  
                  "state_id":"117",
                  "state_name":"Nidwalden",
                  "state_code":"NW"
               },
               {  
                  "state_id":"118",
                  "state_name":"Obwalden",
                  "state_code":"OW"
               },
               {  
                  "state_id":"120",
                  "state_name":"Schaffhausen",
                  "state_code":"SH"
               },
               {  
                  "state_id":"122",
                  "state_name":"Schwyz",
                  "state_code":"SZ"
               },
               {  
                  "state_id":"121",
                  "state_name":"Solothurn",
                  "state_code":"SO"
               },
               {  
                  "state_id":"119",
                  "state_name":"St. Gallen",
                  "state_code":"SG"
               },
               {  
                  "state_id":"124",
                  "state_name":"Tessin",
                  "state_code":"TI"
               },
               {  
                  "state_id":"123",
                  "state_name":"Thurgau",
                  "state_code":"TG"
               },
               {  
                  "state_id":"125",
                  "state_name":"Uri",
                  "state_code":"UR"
               },
               {  
                  "state_id":"126",
                  "state_name":"Waadt",
                  "state_code":"VD"
               },
               {  
                  "state_id":"127",
                  "state_name":"Wallis",
                  "state_code":"VS"
               },
               {  
                  "state_id":"128",
                  "state_name":"Zug",
                  "state_code":"ZG"
               },
               {  
                  "state_id":"129",
                  "state_name":"Z\u00fcrich",
                  "state_code":"ZH"
               }
            ]
         },
         {  
            "country_code":"CI",
            "country_name":"C\u00f4te d\u2019Ivoire",
            "states":[  

            ]
         },
         {  
            "country_code":"CK",
            "country_name":"\u00celes Cook",
            "states":[  

            ]
         },
         {  
            "country_code":"CL",
            "country_name":"Chili",
            "states":[  

            ]
         },
         {  
            "country_code":"CM",
            "country_name":"Cameroun",
            "states":[  

            ]
         },
         {  
            "country_code":"CN",
            "country_name":"Chine",
            "states":[  

            ]
         },
         {  
            "country_code":"CO",
            "country_name":"Colombie",
            "states":[  

            ]
         },
         {  
            "country_code":"CR",
            "country_name":"Costa Rica",
            "states":[  

            ]
         },
         {  
            "country_code":"CU",
            "country_name":"Cuba",
            "states":[  

            ]
         },
         {  
            "country_code":"CV",
            "country_name":"Cap-Vert",
            "states":[  

            ]
         },
         {  
            "country_code":"CX",
            "country_name":"\u00cele Christmas",
            "states":[  

            ]
         },
         {  
            "country_code":"CY",
            "country_name":"Chypre",
            "states":[  

            ]
         },
         {  
            "country_code":"CZ",
            "country_name":"R\u00e9publique tch\u00e8que",
            "states":[  

            ]
         },
         {  
            "country_code":"DE",
            "country_name":"Allemagne",
            "states":[  
               {  
                  "state_id":"80",
                  "state_name":"Baden-W\u00fcrttemberg",
                  "state_code":"BAW"
               },
               {  
                  "state_id":"81",
                  "state_name":"Bayern",
                  "state_code":"BAY"
               },
               {  
                  "state_id":"82",
                  "state_name":"Berlin",
                  "state_code":"BER"
               },
               {  
                  "state_id":"83",
                  "state_name":"Brandenburg",
                  "state_code":"BRG"
               },
               {  
                  "state_id":"84",
                  "state_name":"Bremen",
                  "state_code":"BRE"
               },
               {  
                  "state_id":"85",
                  "state_name":"Hamburg",
                  "state_code":"HAM"
               },
               {  
                  "state_id":"86",
                  "state_name":"Hessen",
                  "state_code":"HES"
               },
               {  
                  "state_id":"87",
                  "state_name":"Mecklenburg-Vorpommern",
                  "state_code":"MEC"
               },
               {  
                  "state_id":"79",
                  "state_name":"Niedersachsen",
                  "state_code":"NDS"
               },
               {  
                  "state_id":"88",
                  "state_name":"Nordrhein-Westfalen",
                  "state_code":"NRW"
               },
               {  
                  "state_id":"89",
                  "state_name":"Rheinland-Pfalz",
                  "state_code":"RHE"
               },
               {  
                  "state_id":"90",
                  "state_name":"Saarland",
                  "state_code":"SAR"
               },
               {  
                  "state_id":"91",
                  "state_name":"Sachsen",
                  "state_code":"SAS"
               },
               {  
                  "state_id":"92",
                  "state_name":"Sachsen-Anhalt",
                  "state_code":"SAC"
               },
               {  
                  "state_id":"93",
                  "state_name":"Schleswig-Holstein",
                  "state_code":"SCN"
               },
               {  
                  "state_id":"94",
                  "state_name":"Th\u00fcringen",
                  "state_code":"THE"
               }
            ]
         },
         {  
            "country_code":"DJ",
            "country_name":"Djibouti",
            "states":[  

            ]
         },
         {  
            "country_code":"DK",
            "country_name":"Danemark",
            "states":[  

            ]
         },
         {  
            "country_code":"DM",
            "country_name":"Dominique",
            "states":[  

            ]
         },
         {  
            "country_code":"DO",
            "country_name":"R\u00e9publique dominicaine",
            "states":[  

            ]
         },
         {  
            "country_code":"DZ",
            "country_name":"Alg\u00e9rie",
            "states":[  

            ]
         },
         {  
            "country_code":"EC",
            "country_name":"\u00c9quateur",
            "states":[  

            ]
         },
         {  
            "country_code":"EE",
            "country_name":"Estonie",
            "states":[  
               {  
                  "state_id":"340",
                  "state_name":"Harjumaa",
                  "state_code":"EE-37"
               },
               {  
                  "state_id":"341",
                  "state_name":"Hiiumaa",
                  "state_code":"EE-39"
               },
               {  
                  "state_id":"342",
                  "state_name":"Ida-Virumaa",
                  "state_code":"EE-44"
               },
               {  
                  "state_id":"344",
                  "state_name":"J\u00e4rvamaa",
                  "state_code":"EE-51"
               },
               {  
                  "state_id":"343",
                  "state_name":"J\u00f5gevamaa",
                  "state_code":"EE-49"
               },
               {  
                  "state_id":"346",
                  "state_name":"L\u00e4\u00e4ne-Virumaa",
                  "state_code":"EE-59"
               },
               {  
                  "state_id":"345",
                  "state_name":"L\u00e4\u00e4nemaa",
                  "state_code":"EE-57"
               },
               {  
                  "state_id":"348",
                  "state_name":"P\u00e4rnumaa",
                  "state_code":"EE-67"
               },
               {  
                  "state_id":"347",
                  "state_name":"P\u00f5lvamaa",
                  "state_code":"EE-65"
               },
               {  
                  "state_id":"349",
                  "state_name":"Raplamaa",
                  "state_code":"EE-70"
               },
               {  
                  "state_id":"350",
                  "state_name":"Saaremaa",
                  "state_code":"EE-74"
               },
               {  
                  "state_id":"351",
                  "state_name":"Tartumaa",
                  "state_code":"EE-78"
               },
               {  
                  "state_id":"352",
                  "state_name":"Valgamaa",
                  "state_code":"EE-82"
               },
               {  
                  "state_id":"353",
                  "state_name":"Viljandimaa",
                  "state_code":"EE-84"
               },
               {  
                  "state_id":"354",
                  "state_name":"V\u00f5rumaa",
                  "state_code":"EE-86"
               }
            ]
         },
         {  
            "country_code":"EG",
            "country_name":"\u00c9gypte",
            "states":[  

            ]
         },
         {  
            "country_code":"EH",
            "country_name":"Sahara occidental",
            "states":[  

            ]
         },
         {  
            "country_code":"ER",
            "country_name":"\u00c9rythr\u00e9e",
            "states":[  

            ]
         },
         {  
            "country_code":"ES",
            "country_name":"Espagne",
            "states":[  
               {  
                  "state_id":"130",
                  "state_name":"A Coru\u00f1a",
                  "state_code":"A Coru\u0441a"
               },
               {  
                  "state_id":"131",
                  "state_name":"Alava",
                  "state_code":"Alava"
               },
               {  
                  "state_id":"132",
                  "state_name":"Albacete",
                  "state_code":"Albacete"
               },
               {  
                  "state_id":"133",
                  "state_name":"Alicante",
                  "state_code":"Alicante"
               },
               {  
                  "state_id":"134",
                  "state_name":"Almeria",
                  "state_code":"Almeria"
               },
               {  
                  "state_id":"135",
                  "state_name":"Asturias",
                  "state_code":"Asturias"
               },
               {  
                  "state_id":"136",
                  "state_name":"Avila",
                  "state_code":"Avila"
               },
               {  
                  "state_id":"137",
                  "state_name":"Badajoz",
                  "state_code":"Badajoz"
               },
               {  
                  "state_id":"138",
                  "state_name":"Baleares",
                  "state_code":"Baleares"
               },
               {  
                  "state_id":"139",
                  "state_name":"Barcelona",
                  "state_code":"Barcelona"
               },
               {  
                  "state_id":"140",
                  "state_name":"Burgos",
                  "state_code":"Burgos"
               },
               {  
                  "state_id":"141",
                  "state_name":"Caceres",
                  "state_code":"Caceres"
               },
               {  
                  "state_id":"142",
                  "state_name":"Cadiz",
                  "state_code":"Cadiz"
               },
               {  
                  "state_id":"143",
                  "state_name":"Cantabria",
                  "state_code":"Cantabria"
               },
               {  
                  "state_id":"144",
                  "state_name":"Castellon",
                  "state_code":"Castellon"
               },
               {  
                  "state_id":"145",
                  "state_name":"Ceuta",
                  "state_code":"Ceuta"
               },
               {  
                  "state_id":"146",
                  "state_name":"Ciudad Real",
                  "state_code":"Ciudad Real"
               },
               {  
                  "state_id":"147",
                  "state_name":"Cordoba",
                  "state_code":"Cordoba"
               },
               {  
                  "state_id":"148",
                  "state_name":"Cuenca",
                  "state_code":"Cuenca"
               },
               {  
                  "state_id":"149",
                  "state_name":"Girona",
                  "state_code":"Girona"
               },
               {  
                  "state_id":"150",
                  "state_name":"Granada",
                  "state_code":"Granada"
               },
               {  
                  "state_id":"151",
                  "state_name":"Guadalajara",
                  "state_code":"Guadalajara"
               },
               {  
                  "state_id":"152",
                  "state_name":"Guipuzcoa",
                  "state_code":"Guipuzcoa"
               },
               {  
                  "state_id":"153",
                  "state_name":"Huelva",
                  "state_code":"Huelva"
               },
               {  
                  "state_id":"154",
                  "state_name":"Huesca",
                  "state_code":"Huesca"
               },
               {  
                  "state_id":"155",
                  "state_name":"Jaen",
                  "state_code":"Jaen"
               },
               {  
                  "state_id":"156",
                  "state_name":"La Rioja",
                  "state_code":"La Rioja"
               },
               {  
                  "state_id":"157",
                  "state_name":"Las Palmas",
                  "state_code":"Las Palmas"
               },
               {  
                  "state_id":"158",
                  "state_name":"Leon",
                  "state_code":"Leon"
               },
               {  
                  "state_id":"159",
                  "state_name":"Lleida",
                  "state_code":"Lleida"
               },
               {  
                  "state_id":"160",
                  "state_name":"Lugo",
                  "state_code":"Lugo"
               },
               {  
                  "state_id":"161",
                  "state_name":"Madrid",
                  "state_code":"Madrid"
               },
               {  
                  "state_id":"162",
                  "state_name":"Malaga",
                  "state_code":"Malaga"
               },
               {  
                  "state_id":"163",
                  "state_name":"Melilla",
                  "state_code":"Melilla"
               },
               {  
                  "state_id":"164",
                  "state_name":"Murcia",
                  "state_code":"Murcia"
               },
               {  
                  "state_id":"165",
                  "state_name":"Navarra",
                  "state_code":"Navarra"
               },
               {  
                  "state_id":"166",
                  "state_name":"Ourense",
                  "state_code":"Ourense"
               },
               {  
                  "state_id":"167",
                  "state_name":"Palencia",
                  "state_code":"Palencia"
               },
               {  
                  "state_id":"168",
                  "state_name":"Pontevedra",
                  "state_code":"Pontevedra"
               },
               {  
                  "state_id":"169",
                  "state_name":"Salamanca",
                  "state_code":"Salamanca"
               },
               {  
                  "state_id":"170",
                  "state_name":"Santa Cruz de Tenerife",
                  "state_code":"Santa Cruz de Tenerife"
               },
               {  
                  "state_id":"171",
                  "state_name":"Segovia",
                  "state_code":"Segovia"
               },
               {  
                  "state_id":"172",
                  "state_name":"Sevilla",
                  "state_code":"Sevilla"
               },
               {  
                  "state_id":"173",
                  "state_name":"Soria",
                  "state_code":"Soria"
               },
               {  
                  "state_id":"174",
                  "state_name":"Tarragona",
                  "state_code":"Tarragona"
               },
               {  
                  "state_id":"175",
                  "state_name":"Teruel",
                  "state_code":"Teruel"
               },
               {  
                  "state_id":"176",
                  "state_name":"Toledo",
                  "state_code":"Toledo"
               },
               {  
                  "state_id":"177",
                  "state_name":"Valencia",
                  "state_code":"Valencia"
               },
               {  
                  "state_id":"178",
                  "state_name":"Valladolid",
                  "state_code":"Valladolid"
               },
               {  
                  "state_id":"179",
                  "state_name":"Vizcaya",
                  "state_code":"Vizcaya"
               },
               {  
                  "state_id":"180",
                  "state_name":"Zamora",
                  "state_code":"Zamora"
               },
               {  
                  "state_id":"181",
                  "state_name":"Zaragoza",
                  "state_code":"Zaragoza"
               }
            ]
         },
         {  
            "country_code":"ET",
            "country_name":"\u00c9thiopie",
            "states":[  

            ]
         },
         {  
            "country_code":"FI",
            "country_name":"Finlande",
            "states":[  
               {  
                  "state_id":"339",
                  "state_name":"Ahvenanmaa",
                  "state_code":"Ahvenanmaa"
               },
               {  
                  "state_id":"333",
                  "state_name":"Etel\u00e4-Karjala",
                  "state_code":"Etel\u00e4-Karjala"
               },
               {  
                  "state_id":"326",
                  "state_name":"Etel\u00e4-Pohjanmaa",
                  "state_code":"Etel\u00e4-Pohjanmaa"
               },
               {  
                  "state_id":"325",
                  "state_name":"Etel\u00e4-Savo",
                  "state_code":"Etel\u00e4-Savo"
               },
               {  
                  "state_id":"337",
                  "state_name":"It\u00e4-Uusimaa",
                  "state_code":"It\u00e4-Uusimaa"
               },
               {  
                  "state_id":"322",
                  "state_name":"Kainuu",
                  "state_code":"Kainuu"
               },
               {  
                  "state_id":"335",
                  "state_name":"Kanta-H\u00e4me",
                  "state_code":"Kanta-H\u00e4me"
               },
               {  
                  "state_id":"330",
                  "state_name":"Keski-Pohjanmaa",
                  "state_code":"Keski-Pohjanmaa"
               },
               {  
                  "state_id":"331",
                  "state_name":"Keski-Suomi",
                  "state_code":"Keski-Suomi"
               },
               {  
                  "state_id":"338",
                  "state_name":"Kymenlaakso",
                  "state_code":"Kymenlaakso"
               },
               {  
                  "state_id":"320",
                  "state_name":"Lappi",
                  "state_code":"Lappi"
               },
               {  
                  "state_id":"334",
                  "state_name":"P\u00e4ij\u00e4t-H\u00e4me",
                  "state_code":"P\u00e4ij\u00e4t-H\u00e4me"
               },
               {  
                  "state_id":"328",
                  "state_name":"Pirkanmaa",
                  "state_code":"Pirkanmaa"
               },
               {  
                  "state_id":"327",
                  "state_name":"Pohjanmaa",
                  "state_code":"Pohjanmaa"
               },
               {  
                  "state_id":"323",
                  "state_name":"Pohjois-Karjala",
                  "state_code":"Pohjois-Karjala"
               },
               {  
                  "state_id":"321",
                  "state_name":"Pohjois-Pohjanmaa",
                  "state_code":"Pohjois-Pohjanmaa"
               },
               {  
                  "state_id":"324",
                  "state_name":"Pohjois-Savo",
                  "state_code":"Pohjois-Savo"
               },
               {  
                  "state_id":"329",
                  "state_name":"Satakunta",
                  "state_code":"Satakunta"
               },
               {  
                  "state_id":"336",
                  "state_name":"Uusimaa",
                  "state_code":"Uusimaa"
               },
               {  
                  "state_id":"332",
                  "state_name":"Varsinais-Suomi",
                  "state_code":"Varsinais-Suomi"
               }
            ]
         },
         {  
            "country_code":"FJ",
            "country_name":"Fidji",
            "states":[  

            ]
         },
         {  
            "country_code":"FK",
            "country_name":"\u00celes Malouines",
            "states":[  

            ]
         },
         {  
            "country_code":"FM",
            "country_name":"\u00c9tats f\u00e9d\u00e9r\u00e9s de Micron\u00e9sie",
            "states":[  

            ]
         },
         {  
            "country_code":"FO",
            "country_name":"\u00celes F\u00e9ro\u00e9",
            "states":[  

            ]
         },
         {  
            "country_code":"FR",
            "country_name":"France",
            "states":[  
               {  
                  "state_id":"182",
                  "state_name":"Ain",
                  "state_code":"1"
               },
               {  
                  "state_id":"183",
                  "state_name":"Aisne",
                  "state_code":"2"
               },
               {  
                  "state_id":"184",
                  "state_name":"Allier",
                  "state_code":"3"
               },
               {  
                  "state_id":"185",
                  "state_name":"Alpes-de-Haute-Provence",
                  "state_code":"4"
               },
               {  
                  "state_id":"187",
                  "state_name":"Alpes-Maritimes",
                  "state_code":"6"
               },
               {  
                  "state_id":"188",
                  "state_name":"Ard\u00e8che",
                  "state_code":"7"
               },
               {  
                  "state_id":"189",
                  "state_name":"Ardennes",
                  "state_code":"8"
               },
               {  
                  "state_id":"190",
                  "state_name":"Ari\u00e8ge",
                  "state_code":"9"
               },
               {  
                  "state_id":"191",
                  "state_name":"Aube",
                  "state_code":"10"
               },
               {  
                  "state_id":"192",
                  "state_name":"Aude",
                  "state_code":"11"
               },
               {  
                  "state_id":"193",
                  "state_name":"Aveyron",
                  "state_code":"12"
               },
               {  
                  "state_id":"249",
                  "state_name":"Bas-Rhin",
                  "state_code":"67"
               },
               {  
                  "state_id":"194",
                  "state_name":"Bouches-du-Rh\u00f4ne",
                  "state_code":"13"
               },
               {  
                  "state_id":"195",
                  "state_name":"Calvados",
                  "state_code":"14"
               },
               {  
                  "state_id":"196",
                  "state_name":"Cantal",
                  "state_code":"15"
               },
               {  
                  "state_id":"197",
                  "state_name":"Charente",
                  "state_code":"16"
               },
               {  
                  "state_id":"198",
                  "state_name":"Charente-Maritime",
                  "state_code":"17"
               },
               {  
                  "state_id":"199",
                  "state_name":"Cher",
                  "state_code":"18"
               },
               {  
                  "state_id":"200",
                  "state_name":"Corr\u00e8ze",
                  "state_code":"19"
               },
               {  
                  "state_id":"201",
                  "state_name":"Corse-du-Sud",
                  "state_code":"2A"
               },
               {  
                  "state_id":"203",
                  "state_name":"C\u00f4te-d'Or",
                  "state_code":"21"
               },
               {  
                  "state_id":"204",
                  "state_name":"C\u00f4tes-d'Armor",
                  "state_code":"22"
               },
               {  
                  "state_id":"205",
                  "state_name":"Creuse",
                  "state_code":"23"
               },
               {  
                  "state_id":"261",
                  "state_name":"Deux-S\u00e8vres",
                  "state_code":"79"
               },
               {  
                  "state_id":"206",
                  "state_name":"Dordogne",
                  "state_code":"24"
               },
               {  
                  "state_id":"207",
                  "state_name":"Doubs",
                  "state_code":"25"
               },
               {  
                  "state_id":"208",
                  "state_name":"Dr\u00f4me",
                  "state_code":"26"
               },
               {  
                  "state_id":"273",
                  "state_name":"Essonne",
                  "state_code":"91"
               },
               {  
                  "state_id":"209",
                  "state_name":"Eure",
                  "state_code":"27"
               },
               {  
                  "state_id":"210",
                  "state_name":"Eure-et-Loir",
                  "state_code":"28"
               },
               {  
                  "state_id":"211",
                  "state_name":"Finist\u00e8re",
                  "state_code":"29"
               },
               {  
                  "state_id":"212",
                  "state_name":"Gard",
                  "state_code":"30"
               },
               {  
                  "state_id":"214",
                  "state_name":"Gers",
                  "state_code":"32"
               },
               {  
                  "state_id":"215",
                  "state_name":"Gironde",
                  "state_code":"33"
               },
               {  
                  "state_id":"250",
                  "state_name":"Haut-Rhin",
                  "state_code":"68"
               },
               {  
                  "state_id":"202",
                  "state_name":"Haute-Corse",
                  "state_code":"2B"
               },
               {  
                  "state_id":"213",
                  "state_name":"Haute-Garonne",
                  "state_code":"31"
               },
               {  
                  "state_id":"225",
                  "state_name":"Haute-Loire",
                  "state_code":"43"
               },
               {  
                  "state_id":"234",
                  "state_name":"Haute-Marne",
                  "state_code":"52"
               },
               {  
                  "state_id":"252",
                  "state_name":"Haute-Sa\u00f4ne",
                  "state_code":"70"
               },
               {  
                  "state_id":"256",
                  "state_name":"Haute-Savoie",
                  "state_code":"74"
               },
               {  
                  "state_id":"269",
                  "state_name":"Haute-Vienne",
                  "state_code":"87"
               },
               {  
                  "state_id":"186",
                  "state_name":"Hautes-Alpes",
                  "state_code":"5"
               },
               {  
                  "state_id":"247",
                  "state_name":"Hautes-Pyr\u00e9n\u00e9es",
                  "state_code":"65"
               },
               {  
                  "state_id":"274",
                  "state_name":"Hauts-de-Seine",
                  "state_code":"92"
               },
               {  
                  "state_id":"216",
                  "state_name":"H\u00e9rault",
                  "state_code":"34"
               },
               {  
                  "state_id":"217",
                  "state_name":"Ille-et-Vilaine",
                  "state_code":"35"
               },
               {  
                  "state_id":"218",
                  "state_name":"Indre",
                  "state_code":"36"
               },
               {  
                  "state_id":"219",
                  "state_name":"Indre-et-Loire",
                  "state_code":"37"
               },
               {  
                  "state_id":"220",
                  "state_name":"Is\u00e8re",
                  "state_code":"38"
               },
               {  
                  "state_id":"221",
                  "state_name":"Jura",
                  "state_code":"39"
               },
               {  
                  "state_id":"222",
                  "state_name":"Landes",
                  "state_code":"40"
               },
               {  
                  "state_id":"223",
                  "state_name":"Loir-et-Cher",
                  "state_code":"41"
               },
               {  
                  "state_id":"224",
                  "state_name":"Loire",
                  "state_code":"42"
               },
               {  
                  "state_id":"226",
                  "state_name":"Loire-Atlantique",
                  "state_code":"44"
               },
               {  
                  "state_id":"227",
                  "state_name":"Loiret",
                  "state_code":"45"
               },
               {  
                  "state_id":"228",
                  "state_name":"Lot",
                  "state_code":"46"
               },
               {  
                  "state_id":"229",
                  "state_name":"Lot-et-Garonne",
                  "state_code":"47"
               },
               {  
                  "state_id":"230",
                  "state_name":"Loz\u00e8re",
                  "state_code":"48"
               },
               {  
                  "state_id":"231",
                  "state_name":"Maine-et-Loire",
                  "state_code":"49"
               },
               {  
                  "state_id":"232",
                  "state_name":"Manche",
                  "state_code":"50"
               },
               {  
                  "state_id":"233",
                  "state_name":"Marne",
                  "state_code":"51"
               },
               {  
                  "state_id":"235",
                  "state_name":"Mayenne",
                  "state_code":"53"
               },
               {  
                  "state_id":"236",
                  "state_name":"Meurthe-et-Moselle",
                  "state_code":"54"
               },
               {  
                  "state_id":"237",
                  "state_name":"Meuse",
                  "state_code":"55"
               },
               {  
                  "state_id":"238",
                  "state_name":"Morbihan",
                  "state_code":"56"
               },
               {  
                  "state_id":"239",
                  "state_name":"Moselle",
                  "state_code":"57"
               },
               {  
                  "state_id":"240",
                  "state_name":"Ni\u00e8vre",
                  "state_code":"58"
               },
               {  
                  "state_id":"241",
                  "state_name":"Nord",
                  "state_code":"59"
               },
               {  
                  "state_id":"242",
                  "state_name":"Oise",
                  "state_code":"60"
               },
               {  
                  "state_id":"243",
                  "state_name":"Orne",
                  "state_code":"61"
               },
               {  
                  "state_id":"257",
                  "state_name":"Paris",
                  "state_code":"75"
               },
               {  
                  "state_id":"244",
                  "state_name":"Pas-de-Calais",
                  "state_code":"62"
               },
               {  
                  "state_id":"245",
                  "state_name":"Puy-de-D\u00f4me",
                  "state_code":"63"
               },
               {  
                  "state_id":"246",
                  "state_name":"Pyr\u00e9n\u00e9es-Atlantiques",
                  "state_code":"64"
               },
               {  
                  "state_id":"248",
                  "state_name":"Pyr\u00e9n\u00e9es-Orientales",
                  "state_code":"66"
               },
               {  
                  "state_id":"251",
                  "state_name":"Rh\u00f4ne",
                  "state_code":"69"
               },
               {  
                  "state_id":"253",
                  "state_name":"Sa\u00f4ne-et-Loire",
                  "state_code":"71"
               },
               {  
                  "state_id":"254",
                  "state_name":"Sarthe",
                  "state_code":"72"
               },
               {  
                  "state_id":"255",
                  "state_name":"Savoie",
                  "state_code":"73"
               },
               {  
                  "state_id":"259",
                  "state_name":"Seine-et-Marne",
                  "state_code":"77"
               },
               {  
                  "state_id":"258",
                  "state_name":"Seine-Maritime",
                  "state_code":"76"
               },
               {  
                  "state_id":"275",
                  "state_name":"Seine-Saint-Denis",
                  "state_code":"93"
               },
               {  
                  "state_id":"262",
                  "state_name":"Somme",
                  "state_code":"80"
               },
               {  
                  "state_id":"263",
                  "state_name":"Tarn",
                  "state_code":"81"
               },
               {  
                  "state_id":"264",
                  "state_name":"Tarn-et-Garonne",
                  "state_code":"82"
               },
               {  
                  "state_id":"272",
                  "state_name":"Territoire-de-Belfort",
                  "state_code":"90"
               },
               {  
                  "state_id":"277",
                  "state_name":"Val-d'Oise",
                  "state_code":"95"
               },
               {  
                  "state_id":"276",
                  "state_name":"Val-de-Marne",
                  "state_code":"94"
               },
               {  
                  "state_id":"265",
                  "state_name":"Var",
                  "state_code":"83"
               },
               {  
                  "state_id":"266",
                  "state_name":"Vaucluse",
                  "state_code":"84"
               },
               {  
                  "state_id":"267",
                  "state_name":"Vend\u00e9e",
                  "state_code":"85"
               },
               {  
                  "state_id":"268",
                  "state_name":"Vienne",
                  "state_code":"86"
               },
               {  
                  "state_id":"270",
                  "state_name":"Vosges",
                  "state_code":"88"
               },
               {  
                  "state_id":"271",
                  "state_name":"Yonne",
                  "state_code":"89"
               },
               {  
                  "state_id":"260",
                  "state_name":"Yvelines",
                  "state_code":"78"
               }
            ]
         },
         {  
            "country_code":"GA",
            "country_name":"Gabon",
            "states":[  

            ]
         },
         {  
            "country_code":"GB",
            "country_name":"Royaume-Uni",
            "states":[  

            ]
         },
         {  
            "country_code":"GD",
            "country_name":"Grenade",
            "states":[  

            ]
         },
         {  
            "country_code":"GE",
            "country_name":"G\u00e9orgie",
            "states":[  

            ]
         },
         {  
            "country_code":"GF",
            "country_name":"Guyane fran\u00e7aise",
            "states":[  

            ]
         },
         {  
            "country_code":"GG",
            "country_name":"Guernesey",
            "states":[  

            ]
         },
         {  
            "country_code":"GH",
            "country_name":"Ghana",
            "states":[  

            ]
         },
         {  
            "country_code":"GI",
            "country_name":"Gibraltar",
            "states":[  

            ]
         },
         {  
            "country_code":"GL",
            "country_name":"Groenland",
            "states":[  

            ]
         },
         {  
            "country_code":"GM",
            "country_name":"Gambie",
            "states":[  

            ]
         },
         {  
            "country_code":"GN",
            "country_name":"Guin\u00e9e",
            "states":[  

            ]
         },
         {  
            "country_code":"GP",
            "country_name":"Guadeloupe",
            "states":[  

            ]
         },
         {  
            "country_code":"GQ",
            "country_name":"Guin\u00e9e \u00e9quatoriale",
            "states":[  

            ]
         },
         {  
            "country_code":"GR",
            "country_name":"Gr\u00e8ce",
            "states":[  

            ]
         },
         {  
            "country_code":"GS",
            "country_name":"G\u00e9orgie du Sud et les \u00celes Sandwich du Sud",
            "states":[  

            ]
         },
         {  
            "country_code":"GT",
            "country_name":"Guatemala",
            "states":[  

            ]
         },
         {  
            "country_code":"GU",
            "country_name":"Guam",
            "states":[  

            ]
         },
         {  
            "country_code":"GW",
            "country_name":"Guin\u00e9e-Bissau",
            "states":[  

            ]
         },
         {  
            "country_code":"GY",
            "country_name":"Guyana",
            "states":[  

            ]
         },
         {  
            "country_code":"HK",
            "country_name":"R.A.S. chinoise de Hong Kong",
            "states":[  

            ]
         },
         {  
            "country_code":"HM",
            "country_name":"\u00celes Heard et MacDonald",
            "states":[  

            ]
         },
         {  
            "country_code":"HN",
            "country_name":"Honduras",
            "states":[  

            ]
         },
         {  
            "country_code":"HR",
            "country_name":"Croatie",
            "states":[  

            ]
         },
         {  
            "country_code":"HT",
            "country_name":"Ha\u00efti",
            "states":[  

            ]
         },
         {  
            "country_code":"HU",
            "country_name":"Hongrie",
            "states":[  

            ]
         },
         {  
            "country_code":"ID",
            "country_name":"Indon\u00e9sie",
            "states":[  

            ]
         },
         {  
            "country_code":"IE",
            "country_name":"Irlande",
            "states":[  

            ]
         },
         {  
            "country_code":"IL",
            "country_name":"Isra\u00ebl",
            "states":[  

            ]
         },
         {  
            "country_code":"IM",
            "country_name":"\u00cele de Man",
            "states":[  

            ]
         },
         {  
            "country_code":"IN",
            "country_name":"Inde",
            "states":[  

            ]
         },
         {  
            "country_code":"IO",
            "country_name":"Territoire britannique de l\u2019oc\u00e9an Indien",
            "states":[  

            ]
         },
         {  
            "country_code":"IQ",
            "country_name":"Irak",
            "states":[  

            ]
         },
         {  
            "country_code":"IR",
            "country_name":"Iran",
            "states":[  

            ]
         },
         {  
            "country_code":"IS",
            "country_name":"Islande",
            "states":[  

            ]
         },
         {  
            "country_code":"IT",
            "country_name":"Italie",
            "states":[  

            ]
         },
         {  
            "country_code":"JE",
            "country_name":"Jersey",
            "states":[  

            ]
         },
         {  
            "country_code":"JM",
            "country_name":"Jama\u00efque",
            "states":[  

            ]
         },
         {  
            "country_code":"JO",
            "country_name":"Jordanie",
            "states":[  

            ]
         },
         {  
            "country_code":"JP",
            "country_name":"Japon",
            "states":[  

            ]
         },
         {  
            "country_code":"KE",
            "country_name":"Kenya",
            "states":[  

            ]
         },
         {  
            "country_code":"KG",
            "country_name":"Kirghizistan",
            "states":[  

            ]
         },
         {  
            "country_code":"KH",
            "country_name":"Cambodge",
            "states":[  

            ]
         },
         {  
            "country_code":"KI",
            "country_name":"Kiribati",
            "states":[  

            ]
         },
         {  
            "country_code":"KM",
            "country_name":"Comores",
            "states":[  

            ]
         },
         {  
            "country_code":"KN",
            "country_name":"Saint-Kitts-et-Nevis",
            "states":[  

            ]
         },
         {  
            "country_code":"KP",
            "country_name":"Cor\u00e9e du Nord",
            "states":[  

            ]
         },
         {  
            "country_code":"KR",
            "country_name":"Cor\u00e9e du Sud",
            "states":[  

            ]
         },
         {  
            "country_code":"KW",
            "country_name":"Kowe\u00eft",
            "states":[  

            ]
         },
         {  
            "country_code":"KY",
            "country_name":"\u00celes Ca\u00efmans",
            "states":[  

            ]
         },
         {  
            "country_code":"KZ",
            "country_name":"Kazakhstan",
            "states":[  

            ]
         },
         {  
            "country_code":"LA",
            "country_name":"Laos",
            "states":[  

            ]
         },
         {  
            "country_code":"LB",
            "country_name":"Liban",
            "states":[  

            ]
         },
         {  
            "country_code":"LC",
            "country_name":"Sainte-Lucie",
            "states":[  

            ]
         },
         {  
            "country_code":"LI",
            "country_name":"Liechtenstein",
            "states":[  

            ]
         },
         {  
            "country_code":"LK",
            "country_name":"Sri Lanka",
            "states":[  

            ]
         },
         {  
            "country_code":"LR",
            "country_name":"Lib\u00e9ria",
            "states":[  

            ]
         },
         {  
            "country_code":"LS",
            "country_name":"Lesotho",
            "states":[  

            ]
         },
         {  
            "country_code":"LT",
            "country_name":"Lituanie",
            "states":[  
               {  
                  "state_id":"475",
                  "state_name":"Alytaus Apskritis",
                  "state_code":"LT-AL"
               },
               {  
                  "state_id":"476",
                  "state_name":"Kauno Apskritis",
                  "state_code":"LT-KU"
               },
               {  
                  "state_id":"477",
                  "state_name":"Klaip\u0117dos Apskritis",
                  "state_code":"LT-KL"
               },
               {  
                  "state_id":"478",
                  "state_name":"Marijampol\u0117s Apskritis",
                  "state_code":"LT-MR"
               },
               {  
                  "state_id":"479",
                  "state_name":"Panev\u0117\u017eio Apskritis",
                  "state_code":"LT-PN"
               },
               {  
                  "state_id":"480",
                  "state_name":"\u0160iauli\u0173 Apskritis",
                  "state_code":"LT-SA"
               },
               {  
                  "state_id":"481",
                  "state_name":"Taurag\u0117s Apskritis",
                  "state_code":"LT-TA"
               },
               {  
                  "state_id":"482",
                  "state_name":"Tel\u0161i\u0173 Apskritis",
                  "state_code":"LT-TE"
               },
               {  
                  "state_id":"483",
                  "state_name":"Utenos Apskritis",
                  "state_code":"LT-UT"
               },
               {  
                  "state_id":"484",
                  "state_name":"Vilniaus Apskritis",
                  "state_code":"LT-VL"
               }
            ]
         },
         {  
            "country_code":"LU",
            "country_name":"Luxembourg",
            "states":[  

            ]
         },
         {  
            "country_code":"LV",
            "country_name":"Lettonie",
            "states":[  
               {  
                  "state_id":"471",
                  "state_name":"\u0100da\u017eu novads",
                  "state_code":"\u0100da\u017eu novads"
               },
               {  
                  "state_id":"366",
                  "state_name":"Aglonas novads",
                  "state_code":"Aglonas novads"
               },
               {  
                  "state_id":"367",
                  "state_name":"Aizkraukles novads",
                  "state_code":"LV-AI"
               },
               {  
                  "state_id":"368",
                  "state_name":"Aizputes novads",
                  "state_code":"Aizputes novads"
               },
               {  
                  "state_id":"369",
                  "state_name":"Akn\u012bstes novads",
                  "state_code":"Akn\u012bstes novads"
               },
               {  
                  "state_id":"370",
                  "state_name":"Alojas novads",
                  "state_code":"Alojas novads"
               },
               {  
                  "state_id":"371",
                  "state_name":"Alsungas novads",
                  "state_code":"Alsungas novads"
               },
               {  
                  "state_id":"372",
                  "state_name":"Al\u016bksnes novads",
                  "state_code":"LV-AL"
               },
               {  
                  "state_id":"373",
                  "state_name":"Amatas novads",
                  "state_code":"Amatas novads"
               },
               {  
                  "state_id":"374",
                  "state_name":"Apes novads",
                  "state_code":"Apes novads"
               },
               {  
                  "state_id":"375",
                  "state_name":"Auces novads",
                  "state_code":"Auces novads"
               },
               {  
                  "state_id":"376",
                  "state_name":"Bab\u012btes novads",
                  "state_code":"Bab\u012btes novads"
               },
               {  
                  "state_id":"377",
                  "state_name":"Baldones novads",
                  "state_code":"Baldones novads"
               },
               {  
                  "state_id":"378",
                  "state_name":"Baltinavas novads",
                  "state_code":"Baltinavas novads"
               },
               {  
                  "state_id":"379",
                  "state_name":"Balvu novads",
                  "state_code":"LV-BL"
               },
               {  
                  "state_id":"380",
                  "state_name":"Bauskas novads",
                  "state_code":"LV-BU"
               },
               {  
                  "state_id":"381",
                  "state_name":"Bever\u012bnas novads",
                  "state_code":"Bever\u012bnas novads"
               },
               {  
                  "state_id":"382",
                  "state_name":"Broc\u0113nu novads",
                  "state_code":"Broc\u0113nu novads"
               },
               {  
                  "state_id":"383",
                  "state_name":"Burtnieku novads",
                  "state_code":"Burtnieku novads"
               },
               {  
                  "state_id":"384",
                  "state_name":"Carnikavas novads",
                  "state_code":"Carnikavas novads"
               },
               {  
                  "state_id":"387",
                  "state_name":"C\u0113su novads",
                  "state_code":"LV-CE"
               },
               {  
                  "state_id":"385",
                  "state_name":"Cesvaines novads",
                  "state_code":"Cesvaines novads"
               },
               {  
                  "state_id":"386",
                  "state_name":"Ciblas novads",
                  "state_code":"Ciblas novads"
               },
               {  
                  "state_id":"388",
                  "state_name":"Dagdas novads",
                  "state_code":"Dagdas novads"
               },
               {  
                  "state_id":"355",
                  "state_name":"Daugavpils",
                  "state_code":"LV-DGV"
               },
               {  
                  "state_id":"389",
                  "state_name":"Daugavpils novads",
                  "state_code":"LV-DA"
               },
               {  
                  "state_id":"390",
                  "state_name":"Dobeles novads",
                  "state_code":"LV-DO"
               },
               {  
                  "state_id":"391",
                  "state_name":"Dundagas novads",
                  "state_code":"Dundagas novads"
               },
               {  
                  "state_id":"392",
                  "state_name":"Durbes novads",
                  "state_code":"Durbes novads"
               },
               {  
                  "state_id":"393",
                  "state_name":"Engures novads",
                  "state_code":"Engures novads"
               },
               {  
                  "state_id":"472",
                  "state_name":"\u0112rg\u013cu novads",
                  "state_code":"\u0112rg\u013cu novads"
               },
               {  
                  "state_id":"394",
                  "state_name":"Garkalnes novads",
                  "state_code":"Garkalnes novads"
               },
               {  
                  "state_id":"395",
                  "state_name":"Grobi\u0146as novads",
                  "state_code":"Grobi\u0146as novads"
               },
               {  
                  "state_id":"396",
                  "state_name":"Gulbenes novads",
                  "state_code":"LV-GU"
               },
               {  
                  "state_id":"397",
                  "state_name":"Iecavas novads",
                  "state_code":"Iecavas novads"
               },
               {  
                  "state_id":"398",
                  "state_name":"Ik\u0161\u0137iles novads",
                  "state_code":"Ik\u0161\u0137iles novads"
               },
               {  
                  "state_id":"399",
                  "state_name":"Il\u016bkstes novads",
                  "state_code":"Il\u016bkstes novads"
               },
               {  
                  "state_id":"400",
                  "state_name":"In\u010dukalna novads",
                  "state_code":"In\u010dukalna novads"
               },
               {  
                  "state_id":"401",
                  "state_name":"Jaunjelgavas novads",
                  "state_code":"Jaunjelgavas novads"
               },
               {  
                  "state_id":"402",
                  "state_name":"Jaunpiebalgas novads",
                  "state_code":"Jaunpiebalgas novads"
               },
               {  
                  "state_id":"403",
                  "state_name":"Jaunpils novads",
                  "state_code":"Jaunpils novads"
               },
               {  
                  "state_id":"357",
                  "state_name":"J\u0113kabpils",
                  "state_code":"J\u0113kabpils"
               },
               {  
                  "state_id":"405",
                  "state_name":"J\u0113kabpils novads",
                  "state_code":"LV-JK"
               },
               {  
                  "state_id":"356",
                  "state_name":"Jelgava",
                  "state_code":"LV-JEL"
               },
               {  
                  "state_id":"404",
                  "state_name":"Jelgavas novads",
                  "state_code":"LV-JL"
               },
               {  
                  "state_id":"358",
                  "state_name":"J\u016brmala",
                  "state_code":"LV-JUR"
               },
               {  
                  "state_id":"406",
                  "state_name":"Kandavas novads",
                  "state_code":"Kandavas novads"
               },
               {  
                  "state_id":"412",
                  "state_name":"K\u0101rsavas novads",
                  "state_code":"K\u0101rsavas novads"
               },
               {  
                  "state_id":"473",
                  "state_name":"\u0136eguma novads",
                  "state_code":"\u0136eguma novads"
               },
               {  
                  "state_id":"474",
                  "state_name":"\u0136ekavas novads",
                  "state_code":"\u0136ekavas novads"
               },
               {  
                  "state_id":"407",
                  "state_name":"Kokneses novads",
                  "state_code":"Kokneses novads"
               },
               {  
                  "state_id":"410",
                  "state_name":"Kr\u0101slavas novads",
                  "state_code":"LV-KR"
               },
               {  
                  "state_id":"408",
                  "state_name":"Krimuldas novads",
                  "state_code":"Krimuldas novads"
               },
               {  
                  "state_id":"409",
                  "state_name":"Krustpils novads",
                  "state_code":"Krustpils novads"
               },
               {  
                  "state_id":"411",
                  "state_name":"Kuld\u012bgas novads",
                  "state_code":"LV-KU"
               },
               {  
                  "state_id":"413",
                  "state_name":"Lielv\u0101rdes novads",
                  "state_code":"Lielv\u0101rdes novads"
               },
               {  
                  "state_id":"359",
                  "state_name":"Liep\u0101ja",
                  "state_code":"LV-LPX"
               },
               {  
                  "state_id":"360",
                  "state_name":"Liep\u0101jas novads",
                  "state_code":"LV-LE"
               },
               {  
                  "state_id":"417",
                  "state_name":"L\u012bgatnes novads",
                  "state_code":"L\u012bgatnes novads"
               },
               {  
                  "state_id":"414",
                  "state_name":"Limba\u017eu novads",
                  "state_code":"LV-LM"
               },
               {  
                  "state_id":"418",
                  "state_name":"L\u012bv\u0101nu novads",
                  "state_code":"L\u012bv\u0101nu novads"
               },
               {  
                  "state_id":"415",
                  "state_name":"Lub\u0101nas novads",
                  "state_code":"Lub\u0101nas novads"
               },
               {  
                  "state_id":"416",
                  "state_name":"Ludzas novads",
                  "state_code":"LV-LU"
               },
               {  
                  "state_id":"419",
                  "state_name":"Madonas novads",
                  "state_code":"LV-MA"
               },
               {  
                  "state_id":"421",
                  "state_name":"M\u0101lpils novads",
                  "state_code":"M\u0101lpils novads"
               },
               {  
                  "state_id":"422",
                  "state_name":"M\u0101rupes novads",
                  "state_code":"M\u0101rupes novads"
               },
               {  
                  "state_id":"420",
                  "state_name":"Mazsalacas novads",
                  "state_code":"Mazsalacas novads"
               },
               {  
                  "state_id":"423",
                  "state_name":"Nauk\u0161\u0113nu novads",
                  "state_code":"Nauk\u0161\u0113nu novads"
               },
               {  
                  "state_id":"424",
                  "state_name":"Neretas novads",
                  "state_code":"Neretas novads"
               },
               {  
                  "state_id":"425",
                  "state_name":"N\u012bcas novads",
                  "state_code":"N\u012bcas novads"
               },
               {  
                  "state_id":"426",
                  "state_name":"Ogres novads",
                  "state_code":"LV-OG"
               },
               {  
                  "state_id":"427",
                  "state_name":"Olaines novads",
                  "state_code":"Olaines novads"
               },
               {  
                  "state_id":"428",
                  "state_name":"Ozolnieku novads",
                  "state_code":"Ozolnieku novads"
               },
               {  
                  "state_id":"432",
                  "state_name":"P\u0101rgaujas novads",
                  "state_code":"P\u0101rgaujas novads"
               },
               {  
                  "state_id":"433",
                  "state_name":"P\u0101vilostas novads",
                  "state_code":"P\u0101vilostas novads"
               },
               {  
                  "state_id":"434",
                  "state_name":"P\u013cavi\u0146u novads",
                  "state_code":"P\u013cavi\u0146u novads"
               },
               {  
                  "state_id":"429",
                  "state_name":"Prei\u013cu novads",
                  "state_code":"LV-PR"
               },
               {  
                  "state_id":"430",
                  "state_name":"Priekules novads",
                  "state_code":"Priekules novads"
               },
               {  
                  "state_id":"431",
                  "state_name":"Prieku\u013cu novads",
                  "state_code":"Prieku\u013cu novads"
               },
               {  
                  "state_id":"435",
                  "state_name":"Raunas novads",
                  "state_code":"Raunas novads"
               },
               {  
                  "state_id":"361",
                  "state_name":"R\u0113zekne",
                  "state_code":"LV-REZ"
               },
               {  
                  "state_id":"442",
                  "state_name":"R\u0113zeknes novads",
                  "state_code":"LV-RE"
               },
               {  
                  "state_id":"436",
                  "state_name":"Riebi\u0146u novads",
                  "state_code":"Riebi\u0146u novads"
               },
               {  
                  "state_id":"362",
                  "state_name":"R\u012bga",
                  "state_code":"LV-RIX"
               },
               {  
                  "state_id":"363",
                  "state_name":"R\u012bgas novads",
                  "state_code":"LV-RI"
               },
               {  
                  "state_id":"437",
                  "state_name":"Rojas novads",
                  "state_code":"Rojas novads"
               },
               {  
                  "state_id":"438",
                  "state_name":"Ropa\u017eu novads",
                  "state_code":"Ropa\u017eu novads"
               },
               {  
                  "state_id":"439",
                  "state_name":"Rucavas novads",
                  "state_code":"Rucavas novads"
               },
               {  
                  "state_id":"440",
                  "state_name":"Rug\u0101ju novads",
                  "state_code":"Rug\u0101ju novads"
               },
               {  
                  "state_id":"443",
                  "state_name":"R\u016bjienas novads",
                  "state_code":"R\u016bjienas novads"
               },
               {  
                  "state_id":"441",
                  "state_name":"Rund\u0101les novads",
                  "state_code":"Rund\u0101les novads"
               },
               {  
                  "state_id":"444",
                  "state_name":"Salacgr\u012bvas novads",
                  "state_code":"Salacgr\u012bvas novads"
               },
               {  
                  "state_id":"445",
                  "state_name":"Salas novads",
                  "state_code":"Salas novads"
               },
               {  
                  "state_id":"446",
                  "state_name":"Salaspils novads",
                  "state_code":"Salaspils novads"
               },
               {  
                  "state_id":"447",
                  "state_name":"Saldus novads",
                  "state_code":"LV-SA"
               },
               {  
                  "state_id":"448",
                  "state_name":"Saulkrastu novads",
                  "state_code":"Saulkrastu novads"
               },
               {  
                  "state_id":"455",
                  "state_name":"S\u0113jas novads",
                  "state_code":"S\u0113jas novads"
               },
               {  
                  "state_id":"449",
                  "state_name":"Siguldas novads",
                  "state_code":"Siguldas novads"
               },
               {  
                  "state_id":"451",
                  "state_name":"Skr\u012bveru novads",
                  "state_code":"Skr\u012bveru novads"
               },
               {  
                  "state_id":"450",
                  "state_name":"Skrundas novads",
                  "state_code":"Skrundas novads"
               },
               {  
                  "state_id":"452",
                  "state_name":"Smiltenes novads",
                  "state_code":"Smiltenes novads"
               },
               {  
                  "state_id":"453",
                  "state_name":"Stopi\u0146u novads",
                  "state_code":"Stopi\u0146u novads"
               },
               {  
                  "state_id":"454",
                  "state_name":"Stren\u010du novads",
                  "state_code":"Stren\u010du novads"
               },
               {  
                  "state_id":"456",
                  "state_name":"Talsu novads",
                  "state_code":"LV-TA"
               },
               {  
                  "state_id":"458",
                  "state_name":"T\u0113rvetes novads",
                  "state_code":"T\u0113rvetes novads"
               },
               {  
                  "state_id":"457",
                  "state_name":"Tukuma novads",
                  "state_code":"LV-TU"
               },
               {  
                  "state_id":"459",
                  "state_name":"Vai\u0146odes novads",
                  "state_code":"Vai\u0146odes novads"
               },
               {  
                  "state_id":"460",
                  "state_name":"Valkas novads",
                  "state_code":"LV-VK"
               },
               {  
                  "state_id":"364",
                  "state_name":"Valmiera",
                  "state_code":"Valmiera"
               },
               {  
                  "state_id":"461",
                  "state_name":"Valmieras novads",
                  "state_code":"LV-VM"
               },
               {  
                  "state_id":"462",
                  "state_name":"Varak\u013c\u0101nu novads",
                  "state_code":"Varak\u013c\u0101nu novads"
               },
               {  
                  "state_id":"469",
                  "state_name":"V\u0101rkavas novads",
                  "state_code":"V\u0101rkavas novads"
               },
               {  
                  "state_id":"463",
                  "state_name":"Vecpiebalgas novads",
                  "state_code":"Vecpiebalgas novads"
               },
               {  
                  "state_id":"464",
                  "state_name":"Vecumnieku novads",
                  "state_code":"Vecumnieku novads"
               },
               {  
                  "state_id":"365",
                  "state_name":"Ventspils",
                  "state_code":"LV-VEN"
               },
               {  
                  "state_id":"465",
                  "state_name":"Ventspils novads",
                  "state_code":"LV-VE"
               },
               {  
                  "state_id":"466",
                  "state_name":"Vies\u012btes novads",
                  "state_code":"Vies\u012btes novads"
               },
               {  
                  "state_id":"467",
                  "state_name":"Vi\u013cakas novads",
                  "state_code":"Vi\u013cakas novads"
               },
               {  
                  "state_id":"468",
                  "state_name":"Vi\u013c\u0101nu novads",
                  "state_code":"Vi\u013c\u0101nu novads"
               },
               {  
                  "state_id":"470",
                  "state_name":"Zilupes novads",
                  "state_code":"Zilupes novads"
               }
            ]
         },
         {  
            "country_code":"LY",
            "country_name":"Libye",
            "states":[  

            ]
         },
         {  
            "country_code":"MA",
            "country_name":"Maroc",
            "states":[  

            ]
         },
         {  
            "country_code":"MC",
            "country_name":"Monaco",
            "states":[  

            ]
         },
         {  
            "country_code":"MD",
            "country_name":"Moldavie",
            "states":[  

            ]
         },
         {  
            "country_code":"ME",
            "country_name":"Mont\u00e9n\u00e9gro",
            "states":[  

            ]
         },
         {  
            "country_code":"MF",
            "country_name":"Saint-Martin (partie fran\u00e7aise)",
            "states":[  

            ]
         },
         {  
            "country_code":"MG",
            "country_name":"Madagascar",
            "states":[  

            ]
         },
         {  
            "country_code":"MH",
            "country_name":"\u00celes Marshall",
            "states":[  

            ]
         },
         {  
            "country_code":"MK",
            "country_name":"Mac\u00e9doine",
            "states":[  

            ]
         },
         {  
            "country_code":"ML",
            "country_name":"Mali",
            "states":[  

            ]
         },
         {  
            "country_code":"MM",
            "country_name":"Myanmar",
            "states":[  

            ]
         },
         {  
            "country_code":"MN",
            "country_name":"Mongolie",
            "states":[  

            ]
         },
         {  
            "country_code":"MO",
            "country_name":"R.A.S. chinoise de Macao",
            "states":[  

            ]
         },
         {  
            "country_code":"MP",
            "country_name":"\u00celes Mariannes du Nord",
            "states":[  

            ]
         },
         {  
            "country_code":"MQ",
            "country_name":"Martinique",
            "states":[  

            ]
         },
         {  
            "country_code":"MR",
            "country_name":"Mauritanie",
            "states":[  

            ]
         },
         {  
            "country_code":"MS",
            "country_name":"Montserrat",
            "states":[  

            ]
         },
         {  
            "country_code":"MT",
            "country_name":"Malte",
            "states":[  

            ]
         },
         {  
            "country_code":"MU",
            "country_name":"Maurice",
            "states":[  

            ]
         },
         {  
            "country_code":"MV",
            "country_name":"Maldives",
            "states":[  

            ]
         },
         {  
            "country_code":"MW",
            "country_name":"Malawi",
            "states":[  

            ]
         },
         {  
            "country_code":"MX",
            "country_name":"Mexique",
            "states":[  

            ]
         },
         {  
            "country_code":"MY",
            "country_name":"Malaisie",
            "states":[  

            ]
         },
         {  
            "country_code":"MZ",
            "country_name":"Mozambique",
            "states":[  

            ]
         },
         {  
            "country_code":"NA",
            "country_name":"Namibie",
            "states":[  

            ]
         },
         {  
            "country_code":"NC",
            "country_name":"Nouvelle-Cal\u00e9donie",
            "states":[  

            ]
         },
         {  
            "country_code":"NE",
            "country_name":"Niger",
            "states":[  

            ]
         },
         {  
            "country_code":"NF",
            "country_name":"\u00cele Norfolk",
            "states":[  

            ]
         },
         {  
            "country_code":"NG",
            "country_name":"Nig\u00e9ria",
            "states":[  

            ]
         },
         {  
            "country_code":"NI",
            "country_name":"Nicaragua",
            "states":[  

            ]
         },
         {  
            "country_code":"NL",
            "country_name":"Pays-Bas",
            "states":[  

            ]
         },
         {  
            "country_code":"NO",
            "country_name":"Norv\u00e8ge",
            "states":[  

            ]
         },
         {  
            "country_code":"NP",
            "country_name":"N\u00e9pal",
            "states":[  

            ]
         },
         {  
            "country_code":"NR",
            "country_name":"Nauru",
            "states":[  

            ]
         },
         {  
            "country_code":"NU",
            "country_name":"Niue",
            "states":[  

            ]
         },
         {  
            "country_code":"NZ",
            "country_name":"Nouvelle-Z\u00e9lande",
            "states":[  

            ]
         },
         {  
            "country_code":"OM",
            "country_name":"Oman",
            "states":[  

            ]
         },
         {  
            "country_code":"PA",
            "country_name":"Panama",
            "states":[  

            ]
         },
         {  
            "country_code":"PE",
            "country_name":"P\u00e9rou",
            "states":[  

            ]
         },
         {  
            "country_code":"PF",
            "country_name":"Polyn\u00e9sie fran\u00e7aise",
            "states":[  

            ]
         },
         {  
            "country_code":"PG",
            "country_name":"Papouasie-Nouvelle-Guin\u00e9e",
            "states":[  

            ]
         },
         {  
            "country_code":"PH",
            "country_name":"Philippines",
            "states":[  

            ]
         },
         {  
            "country_code":"PK",
            "country_name":"Pakistan",
            "states":[  

            ]
         },
         {  
            "country_code":"PL",
            "country_name":"Pologne",
            "states":[  

            ]
         },
         {  
            "country_code":"PM",
            "country_name":"Saint-Pierre-et-Miquelon",
            "states":[  

            ]
         },
         {  
            "country_code":"PN",
            "country_name":"Pitcairn",
            "states":[  

            ]
         },
         {  
            "country_code":"PR",
            "country_name":"Porto Rico",
            "states":[  

            ]
         },
         {  
            "country_code":"PS",
            "country_name":"Territoires palestiniens",
            "states":[  

            ]
         },
         {  
            "country_code":"PT",
            "country_name":"Portugal",
            "states":[  

            ]
         },
         {  
            "country_code":"PW",
            "country_name":"Palaos",
            "states":[  

            ]
         },
         {  
            "country_code":"PY",
            "country_name":"Paraguay",
            "states":[  

            ]
         },
         {  
            "country_code":"QA",
            "country_name":"Qatar",
            "states":[  

            ]
         },
         {  
            "country_code":"RE",
            "country_name":"La R\u00e9union",
            "states":[  

            ]
         },
         {  
            "country_code":"RO",
            "country_name":"Roumanie",
            "states":[  
               {  
                  "state_id":"278",
                  "state_name":"Alba",
                  "state_code":"AB"
               },
               {  
                  "state_id":"279",
                  "state_name":"Arad",
                  "state_code":"AR"
               },
               {  
                  "state_id":"280",
                  "state_name":"Arge\u015f",
                  "state_code":"AG"
               },
               {  
                  "state_id":"281",
                  "state_name":"Bac\u0103u",
                  "state_code":"BC"
               },
               {  
                  "state_id":"282",
                  "state_name":"Bihor",
                  "state_code":"BH"
               },
               {  
                  "state_id":"283",
                  "state_name":"Bistri\u0163a-N\u0103s\u0103ud",
                  "state_code":"BN"
               },
               {  
                  "state_id":"284",
                  "state_name":"Boto\u015fani",
                  "state_code":"BT"
               },
               {  
                  "state_id":"286",
                  "state_name":"Br\u0103ila",
                  "state_code":"BR"
               },
               {  
                  "state_id":"285",
                  "state_name":"Bra\u015fov",
                  "state_code":"BV"
               },
               {  
                  "state_id":"287",
                  "state_name":"Bucure\u015fti",
                  "state_code":"B"
               },
               {  
                  "state_id":"288",
                  "state_name":"Buz\u0103u",
                  "state_code":"BZ"
               },
               {  
                  "state_id":"290",
                  "state_name":"C\u0103l\u0103ra\u015fi",
                  "state_code":"CL"
               },
               {  
                  "state_id":"289",
                  "state_name":"Cara\u015f-Severin",
                  "state_code":"CS"
               },
               {  
                  "state_id":"291",
                  "state_name":"Cluj",
                  "state_code":"CJ"
               },
               {  
                  "state_id":"292",
                  "state_name":"Constan\u0163a",
                  "state_code":"CT"
               },
               {  
                  "state_id":"293",
                  "state_name":"Covasna",
                  "state_code":"CV"
               },
               {  
                  "state_id":"294",
                  "state_name":"D\u00e2mbovi\u0163a",
                  "state_code":"DB"
               },
               {  
                  "state_id":"295",
                  "state_name":"Dolj",
                  "state_code":"DJ"
               },
               {  
                  "state_id":"296",
                  "state_name":"Gala\u0163i",
                  "state_code":"GL"
               },
               {  
                  "state_id":"297",
                  "state_name":"Giurgiu",
                  "state_code":"GR"
               },
               {  
                  "state_id":"298",
                  "state_name":"Gorj",
                  "state_code":"GJ"
               },
               {  
                  "state_id":"299",
                  "state_name":"Harghita",
                  "state_code":"HR"
               },
               {  
                  "state_id":"300",
                  "state_name":"Hunedoara",
                  "state_code":"HD"
               },
               {  
                  "state_id":"301",
                  "state_name":"Ialomi\u0163a",
                  "state_code":"IL"
               },
               {  
                  "state_id":"302",
                  "state_name":"Ia\u015fi",
                  "state_code":"IS"
               },
               {  
                  "state_id":"303",
                  "state_name":"Ilfov",
                  "state_code":"IF"
               },
               {  
                  "state_id":"304",
                  "state_name":"Maramure\u015f",
                  "state_code":"MM"
               },
               {  
                  "state_id":"305",
                  "state_name":"Mehedin\u0163i",
                  "state_code":"MH"
               },
               {  
                  "state_id":"306",
                  "state_name":"Mure\u015f",
                  "state_code":"MS"
               },
               {  
                  "state_id":"307",
                  "state_name":"Neam\u0163",
                  "state_code":"NT"
               },
               {  
                  "state_id":"308",
                  "state_name":"Olt",
                  "state_code":"OT"
               },
               {  
                  "state_id":"309",
                  "state_name":"Prahova",
                  "state_code":"PH"
               },
               {  
                  "state_id":"311",
                  "state_name":"S\u0103laj",
                  "state_code":"SJ"
               },
               {  
                  "state_id":"310",
                  "state_name":"Satu-Mare",
                  "state_code":"SM"
               },
               {  
                  "state_id":"312",
                  "state_name":"Sibiu",
                  "state_code":"SB"
               },
               {  
                  "state_id":"313",
                  "state_name":"Suceava",
                  "state_code":"SV"
               },
               {  
                  "state_id":"314",
                  "state_name":"Teleorman",
                  "state_code":"TR"
               },
               {  
                  "state_id":"315",
                  "state_name":"Timi\u015f",
                  "state_code":"TM"
               },
               {  
                  "state_id":"316",
                  "state_name":"Tulcea",
                  "state_code":"TL"
               },
               {  
                  "state_id":"318",
                  "state_name":"V\u00e2lcea",
                  "state_code":"VL"
               },
               {  
                  "state_id":"317",
                  "state_name":"Vaslui",
                  "state_code":"VS"
               },
               {  
                  "state_id":"319",
                  "state_name":"Vrancea",
                  "state_code":"VN"
               }
            ]
         },
         {  
            "country_code":"RS",
            "country_name":"Serbie",
            "states":[  

            ]
         },
         {  
            "country_code":"RU",
            "country_name":"Russie",
            "states":[  

            ]
         },
         {  
            "country_code":"RW",
            "country_name":"Rwanda",
            "states":[  

            ]
         },
         {  
            "country_code":"SA",
            "country_name":"Arabie saoudite",
            "states":[  

            ]
         },
         {  
            "country_code":"SB",
            "country_name":"\u00celes Salomon",
            "states":[  

            ]
         },
         {  
            "country_code":"SC",
            "country_name":"Seychelles",
            "states":[  

            ]
         },
         {  
            "country_code":"SD",
            "country_name":"Soudan",
            "states":[  

            ]
         },
         {  
            "country_code":"SE",
            "country_name":"Su\u00e8de",
            "states":[  

            ]
         },
         {  
            "country_code":"SG",
            "country_name":"Singapour",
            "states":[  

            ]
         },
         {  
            "country_code":"SH",
            "country_name":"Sainte-H\u00e9l\u00e8ne",
            "states":[  

            ]
         },
         {  
            "country_code":"SI",
            "country_name":"Slov\u00e9nie",
            "states":[  

            ]
         },
         {  
            "country_code":"SJ",
            "country_name":"Svalbard et Jan Mayen",
            "states":[  

            ]
         },
         {  
            "country_code":"SK",
            "country_name":"Slovaquie",
            "states":[  

            ]
         },
         {  
            "country_code":"SL",
            "country_name":"Sierra Leone",
            "states":[  

            ]
         },
         {  
            "country_code":"SM",
            "country_name":"Saint-Marin",
            "states":[  

            ]
         },
         {  
            "country_code":"SN",
            "country_name":"S\u00e9n\u00e9gal",
            "states":[  

            ]
         },
         {  
            "country_code":"SO",
            "country_name":"Somalie",
            "states":[  

            ]
         },
         {  
            "country_code":"SR",
            "country_name":"Suriname",
            "states":[  

            ]
         },
         {  
            "country_code":"ST",
            "country_name":"Sao Tom\u00e9-et-Principe",
            "states":[  

            ]
         },
         {  
            "country_code":"SV",
            "country_name":"El Salvador",
            "states":[  

            ]
         },
         {  
            "country_code":"SY",
            "country_name":"Syrie",
            "states":[  

            ]
         },
         {  
            "country_code":"SZ",
            "country_name":"Swaziland",
            "states":[  

            ]
         },
         {  
            "country_code":"TC",
            "country_name":"\u00celes Turques-et-Ca\u00efques",
            "states":[  

            ]
         },
         {  
            "country_code":"TD",
            "country_name":"Tchad",
            "states":[  

            ]
         },
         {  
            "country_code":"TF",
            "country_name":"Terres australes fran\u00e7aises",
            "states":[  

            ]
         },
         {  
            "country_code":"TG",
            "country_name":"Togo",
            "states":[  

            ]
         },
         {  
            "country_code":"TH",
            "country_name":"Tha\u00eflande",
            "states":[  

            ]
         },
         {  
            "country_code":"TJ",
            "country_name":"Tadjikistan",
            "states":[  

            ]
         },
         {  
            "country_code":"TK",
            "country_name":"Tokelau",
            "states":[  

            ]
         },
         {  
            "country_code":"TL",
            "country_name":"Timor oriental",
            "states":[  

            ]
         },
         {  
            "country_code":"TM",
            "country_name":"Turkm\u00e9nistan",
            "states":[  

            ]
         },
         {  
            "country_code":"TN",
            "country_name":"Tunisie",
            "states":[  

            ]
         },
         {  
            "country_code":"TO",
            "country_name":"Tonga",
            "states":[  

            ]
         },
         {  
            "country_code":"TR",
            "country_name":"Turquie",
            "states":[  

            ]
         },
         {  
            "country_code":"TT",
            "country_name":"Trinit\u00e9-et-Tobago",
            "states":[  

            ]
         },
         {  
            "country_code":"TV",
            "country_name":"Tuvalu",
            "states":[  

            ]
         },
         {  
            "country_code":"TW",
            "country_name":"Ta\u00efwan",
            "states":[  

            ]
         },
         {  
            "country_code":"TZ",
            "country_name":"Tanzanie",
            "states":[  

            ]
         },
         {  
            "country_code":"UA",
            "country_name":"Ukraine",
            "states":[  

            ]
         },
         {  
            "country_code":"UG",
            "country_name":"Ouganda",
            "states":[  

            ]
         },
         {  
            "country_code":"UM",
            "country_name":"\u00celes mineures \u00e9loign\u00e9es des \u00c9tats-Unis",
            "states":[  

            ]
         },
         {  
            "country_code":"UY",
            "country_name":"Uruguay",
            "states":[  

            ]
         },
         {  
            "country_code":"UZ",
            "country_name":"Ouzb\u00e9kistan",
            "states":[  

            ]
         },
         {  
            "country_code":"VA",
            "country_name":"\u00c9tat de la Cit\u00e9 du Vatican",
            "states":[  

            ]
         },
         {  
            "country_code":"VC",
            "country_name":"Saint-Vincent-et-les Grenadines",
            "states":[  

            ]
         },
         {  
            "country_code":"VE",
            "country_name":"Venezuela",
            "states":[  

            ]
         },
         {  
            "country_code":"VG",
            "country_name":"\u00celes Vierges britanniques",
            "states":[  

            ]
         },
         {  
            "country_code":"VI",
            "country_name":"\u00celes Vierges des \u00c9tats-Unis",
            "states":[  

            ]
         },
         {  
            "country_code":"VN",
            "country_name":"Vietnam",
            "states":[  

            ]
         },
         {  
            "country_code":"VU",
            "country_name":"Vanuatu",
            "states":[  

            ]
         },
         {  
            "country_code":"WF",
            "country_name":"Wallis-et-Futuna",
            "states":[  

            ]
         },
         {  
            "country_code":"WS",
            "country_name":"Samoa",
            "states":[  

            ]
         },
         {  
            "country_code":"YE",
            "country_name":"Y\u00e9men",
            "states":[  

            ]
         },
         {  
            "country_code":"YT",
            "country_name":"Mayotte",
            "states":[  

            ]
         },
         {  
            "country_code":"ZA",
            "country_name":"Afrique du Sud",
            "states":[  

            ]
         },
         {  
            "country_code":"ZM",
            "country_name":"Zambie",
            "states":[  

            ]
         },
         {  
            "country_code":"ZW",
            "country_name":"Zimbabwe",
            "states":[  

            ]
         }
      ],
      "stores":{  
         "all_ids":[  
            "1",
            "2"
         ],
         "stores":[  
            {  
               "group_id":"1",
               "website_id":"1",
               "name":"Madison Island",
               "root_category_id":"2",
               "default_store_id":"1",
               "storeview":{  
                  "all_ids":[  
                     "1",
                     "2",
                     "3"
                  ],
                  "storeviews":[  
                     {  
                        "store_id":"1",
                        "code":"default",
                        "website_id":"1",
                        "group_id":"1",
                        "name":"English",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":"http:\/\/default.com\/magento19"
                     },
                     {  
                        "store_id":"2",
                        "code":"french",
                        "website_id":"1",
                        "group_id":"1",
                        "name":"French",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":"http:\/\/localhost.com\/magento19\/index.php"
                     },
                     {  
                        "store_id":"3",
                        "code":"german",
                        "website_id":"1",
                        "group_id":"1",
                        "name":"German",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":""
                     }
                  ],
                  "total":3,
                  "page_size":15,
                  "from":0
               }
            },
            {  
               "group_id":"2",
               "website_id":"1",
               "name":"Store 2",
               "root_category_id":"2",
               "default_store_id":"4",
               "storeview":{  
                  "all_ids":[  
                     "4"
                  ],
                  "storeviews":[  
                     {  
                        "store_id":"4",
                        "code":"storeview2",
                        "website_id":"1",
                        "group_id":"2",
                        "name":"Storeview 2",
                        "sort_order":"0",
                        "is_active":"1",
                        "base_url":""
                     }
                  ],
                  "total":1,
                  "page_size":15,
                  "from":0
               }
            }
         ],
         "total":2,
         "page_size":15,
         "from":0
      }
   }
}

```

Get default Store View



## View A Store View

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews/3" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON the Same structure with "View Default Store View" API

```json
{
   "_comment": "The above command returns JSON the Same structure with View Default Store View API"
}
```

This endpoint retrieves a specific Store View.

### HTTP Request

`GET /rest/storeviews/<id>`


## View List Of Store Views

```shell
curl "https://abc.com/simiconnector/rest/v2/storeviews" \
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
   "storeviews":[  
      {  
         "store_id":"1",
         "code":"default",
         "website_id":"1",
         "group_id":"1",
         "name":"English",
         "sort_order":"0",
         "is_active":"1",
         "base_url":"http:\/\/default.com\/magento19"
      },
      {  
         "store_id":"2",
         "code":"french",
         "website_id":"1",
         "group_id":"1",
         "name":"French",
         "sort_order":"0",
         "is_active":"1",
         "base_url":"http:\/\/localhost.com\/magento19\/index.php"
      },
      {  
         "store_id":"3",
         "code":"german",
         "website_id":"1",
         "group_id":"1",
         "name":"German",
         "sort_order":"0",
         "is_active":"1",
         "base_url":""
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

This endpoint retrieves a list of Store Views.



## Change Currency

```shell
curl GET "https://abc.com/simiconnector/rest/v2/storeviews/default?currency=KMF" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON the Same structure with "View Default Store View" API

```json
{
   "_comment": "The above command returns JSON the Same structure with View Default Store View API"
}
```

This request is to Change customer Currency.