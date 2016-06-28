# Home Categories

## Home Categories Properties

Attributes| Type| Description
--------- | ------- | -----------
simicategory_id | id | Home Category Id
simicategory_name | string | Home Category Name
simicategory_filename | string | Home Category Image URL
category_id | int | Home Category ID
status | int | Home Category Status
width | int | Category Image Width
height | int | Category Image Height
width_tablet | int | Category Image Width Tablet
height_tablet | int | Category Image Height Tablet
cat_name | string | Category Name
has_children | boolean | Category Has Child Or Not

## View Home Scren Categories

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homecategories" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1"
   ],
   "homecategories":[  
      {  
         "simicategory_id":"1",
         "simicategory_name":"Women",
         "simicategory_filename":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/cat6.jpg",
		 "simicategory_filename_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/3784554_CV-Grimsel.jpg",
         "category_id":"4",
         "status":"1",
         "website_id":"0",
         "storeview_id":"Array",
         "sort_order":"123",
         "entity_id":"54",
         "content_type":"3",
         "item_id":"1",
         "store_view_id":"1",
		 "width":2048,
         "height":893,
         "width_tablet":960,
         "height_tablet":358,
         "has_children":true,
         "cat_name":"Women"
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

Return Home Categories

## View Home Scren Categories With Children

```shell
curl GET "https://abc.com/simiconnector/rest/v2/homecategories?get_child_cat=1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "1"
   ],
   "homecategories":[  
      {  
         "simicategory_id":"1",
         "simicategory_name":"Women",
         "simicategory_filename":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/cat6.jpg",
		 "simicategory_filename_tablet":"http:\/\/localhost.com\/magento19\/media\/simi\/simicart\/simicategory\/3784554_CV-Grimsel.jpg",
         "category_id":"4",
         "status":"1",
         "website_id":"0",
         "storeview_id":"Array",
         "sort_order":"123",
         "entity_id":"54",
         "content_type":"3",
         "item_id":"1",
         "store_view_id":"1",
		 "width":2048,
         "height":893,
         "width_tablet":960,
         "height_tablet":358,
         "cat_name":"Women",
         "has_children":true,
         "children":[  
            {  
               "entity_id":"10",
               "entity_type_id":"3",
               "attribute_set_id":"3",
               "parent_id":"4",
               "created_at":"2013-01-25 17:56:08",
               "updated_at":"2016-06-15 06:22:39",
               "path":"1\/2\/4\/10",
               "position":"1",
               "level":"3",
               "children_count":"0",
               "name":"New Arrivals",
               "url_key":"new-arrivals",
               "image":"plp-w-newarrivals_1.jpg",
               "meta_title":null,
               "display_mode":"PRODUCTS",
               "url_path":"women\/new-arrivals.html",
               "custom_design":null,
               "page_layout":"three_columns",
               "is_active":"1",
               "landing_page":null,
               "is_anchor":"1",
               "include_in_menu":"1",
               "custom_use_parent_settings":"0",
               "custom_apply_to_products":"0",
               "description":null,
               "meta_keywords":null,
               "meta_description":null,
               "custom_layout_update":null,
               "available_sort_by":null,
               "custom_design_from":null,
               "custom_design_to":null,
               "filter_price_range":null,
               "has_children":false
            },
            {  
               "entity_id":"11",
               "entity_type_id":"3",
               "attribute_set_id":"3",
               "parent_id":"4",
               "created_at":"2013-01-25 17:57:32",
               "updated_at":"2013-05-16 05:51:02",
               "path":"1\/2\/4\/11",
               "position":"2",
               "level":"3",
               "children_count":"0",
               "name":"Tops & Blouses",
               "url_key":"tops-blouses",
               "image":"plp-w-blouses.jpg",
               "meta_title":null,
               "display_mode":"PRODUCTS",
               "url_path":"women\/tops-blouses.html",
               "custom_design":null,
               "page_layout":"three_columns",
               "thumbnail":null,
               "is_active":"1",
               "landing_page":null,
               "is_anchor":"1",
               "include_in_menu":"1",
               "custom_use_parent_settings":"0",
               "custom_apply_to_products":"0",
               "description":null,
               "meta_keywords":null,
               "meta_description":null,
               "custom_layout_update":null,
               "available_sort_by":null,
               "custom_design_from":null,
               "custom_design_to":null,
               "filter_price_range":null,
               "has_children":false
            },
            {  
               "entity_id":"12",
               "entity_type_id":"3",
               "attribute_set_id":"3",
               "parent_id":"4",
               "created_at":"2013-01-25 17:58:32",
               "updated_at":"2013-05-06 11:11:20",
               "path":"1\/2\/4\/12",
               "position":"3",
               "level":"3",
               "children_count":"0",
               "name":"Pants & Denim",
               "url_key":"pants-denim",
               "image":null,
               "meta_title":null,
               "display_mode":"PRODUCTS",
               "url_path":"women\/pants-denim.html",
               "custom_design":null,
               "page_layout":"three_columns",
               "thumbnail":null,
               "is_active":"1",
               "landing_page":null,
               "is_anchor":"1",
               "include_in_menu":"1",
               "custom_use_parent_settings":"0",
               "custom_apply_to_products":"0",
               "description":null,
               "meta_keywords":null,
               "meta_description":null,
               "custom_layout_update":null,
               "available_sort_by":null,
               "custom_design_from":null,
               "custom_design_to":null,
               "filter_price_range":null,
               "has_children":false
            },
            {  
               "entity_id":"13",
               "entity_type_id":"3",
               "attribute_set_id":"3",
               "parent_id":"4",
               "created_at":"2013-01-25 17:59:21",
               "updated_at":"2013-03-05 11:45:24",
               "path":"1\/2\/4\/13",
               "position":"4",
               "level":"3",
               "children_count":"0",
               "name":"Dresses & Skirts",
               "url_key":"dresses-skirts",
               "image":null,
               "meta_title":null,
               "display_mode":"PRODUCTS",
               "url_path":"women\/dresses-skirts.html",
               "custom_design":null,
               "page_layout":"three_columns",
               "thumbnail":null,
               "is_active":"1",
               "landing_page":null,
               "is_anchor":"1",
               "include_in_menu":"1",
               "custom_use_parent_settings":"0",
               "custom_apply_to_products":"0",
               "description":null,
               "meta_keywords":null,
               "meta_description":null,
               "custom_layout_update":null,
               "available_sort_by":null,
               "custom_design_from":null,
               "custom_design_to":null,
               "filter_price_range":null,
               "has_children":false
            }
         ]
      }
   ],
   "total":1,
   "page_size":15,
   "from":0
}
```

Return Home Categories With Children Categories.

Use the same input parameter on home screen request to get the same result.
