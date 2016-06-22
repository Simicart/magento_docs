# Catalog Categories

## Category Properties

Attributes| Type| Description
--------- | ------- | -----------
entity_id | id | Category Id
parent_id | id | Parent Category Id
level | int | Category Level
name | string | Category Name
url_path | string | Category URL path
has_children | boolean | Has Chidren Or Not


## View Children Categoríe of Root Category

```shell
curl "https://abc.com/simiconnector/rest/v2/categories" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "4",
      "5",
      "7",
      "8",
      "9"
   ],
   "categories":[  
      {  
         "entity_id":"4",
         "entity_type_id":"3",
         "attribute_set_id":"3",
         "parent_id":"2",
         "created_at":"2013-01-25 17:43:31",
         "updated_at":"2013-05-16 05:50:23",
         "path":"1\/2\/4",
         "position":"2",
         "level":"2",
         "children_count":"4",
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":"<reference>\r\n<remove name=\"right.poll\"\/>\r\n<\/reference>",
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":"27",
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"Women",
         "url_key":"women",
         "image":null,
         "meta_title":null,
         "display_mode":"PAGE",
         "url_path":"women.html",
         "custom_design":null,
         "page_layout":"one_column",
         "custom_design_from":null,
         "custom_design_to":null,
         "filter_price_range":null,
         "has_children":true
      },
      {  
         "entity_id":"5",
         "entity_type_id":"3",
         "attribute_set_id":"3",
         "parent_id":"2",
         "created_at":"2013-01-25 17:44:47",
         "updated_at":"2013-05-08 12:20:07",
         "path":"1\/2\/5",
         "position":"3",
         "level":"2",
         "children_count":"5",
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":null,
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":"24",
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"Men",
         "url_key":"men",
         "image":null,
         "meta_title":null,
         "display_mode":"PAGE",
         "url_path":"men.html",
         "custom_design":null,
         "page_layout":"one_column",
         "custom_design_from":null,
         "custom_design_to":null,
         "filter_price_range":null,
         "has_children":true
      },
      {  
         "entity_id":"7",
         "entity_type_id":"3",
         "attribute_set_id":"3",
         "parent_id":"2",
         "created_at":"2013-01-25 17:49:05",
         "updated_at":"2013-05-08 12:26:34",
         "path":"1\/2\/7",
         "position":"5",
         "level":"2",
         "children_count":"4",
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":null,
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":"21",
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"Home & Decor",
         "url_key":"home-decor",
         "meta_title":null,
         "display_mode":"PAGE",
         "url_path":"home-decor.html",
         "custom_design":null,
         "page_layout":"one_column",
         "custom_design_from":null,
         "custom_design_to":null,
         "filter_price_range":null,
         "has_children":true
      },
      {  
         "entity_id":"8",
         "entity_type_id":"3",
         "attribute_set_id":"3",
         "parent_id":"2",
         "created_at":"2013-01-25 17:49:50",
         "updated_at":"2013-05-16 05:49:33",
         "path":"1\/2\/8",
         "position":"6",
         "level":"2",
         "children_count":"4",
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":"<reference>\r\n<remove name=\"right.poll\"\/>\r\n<\/reference>",
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":null,
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"Sale",
         "url_key":"sale",
         "image":null,
         "meta_title":null,
         "display_mode":"PRODUCTS",
         "url_path":"sale.html",
         "custom_design":null,
         "page_layout":"three_columns",
         "custom_design_from":null,
         "custom_design_to":null,
         "filter_price_range":null,
         "has_children":true
      },
      {  
         "entity_id":"9",
         "entity_type_id":"3",
         "attribute_set_id":"3",
         "parent_id":"2",
         "created_at":"2013-01-25 17:50:47",
         "updated_at":"2013-05-11 00:17:59",
         "path":"1\/2\/9",
         "position":"7",
         "level":"2",
         "children_count":"0",
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":null,
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":"31",
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"VIP",
         "url_key":"vip",
         "image":null,
         "meta_title":null,
         "display_mode":"PRODUCTS_AND_PAGE",
         "url_path":"vip.html",
         "custom_design":null,
         "page_layout":"three_columns",
         "custom_design_from":null,
         "custom_design_to":null,
         "filter_price_range":null,
         "has_children":false
      }
   ],
   "total":5,
   "page_size":15,
   "from":0
}

```

This request return the Root category's children



## View Children Categoríe of A Category

```shell
curl "https://abc.com/simiconnector/rest/v2/categories/4" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "all_ids":[  
      "10",
      "11",
      "13"
   ],
   "categories":[  
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
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":null,
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":null,
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"New Arrivals German",
         "url_key":"new-arrivals",
         "image":"plp-w-newarrivals_1.jpg",
         "meta_title":null,
         "display_mode":"PRODUCTS",
         "url_path":"women\/new-arrivals.html",
         "custom_design":null,
         "page_layout":"three_columns",
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
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":null,
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":null,
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"Tops & Blouses",
         "url_key":"tops-blouses",
         "image":"plp-w-blouses.jpg",
         "meta_title":null,
         "display_mode":"PRODUCTS",
         "url_path":"women\/tops-blouses.html",
         "custom_design":null,
         "page_layout":"three_columns",
         "thumbnail":null,
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
         "description":null,
         "meta_keywords":null,
         "meta_description":null,
         "custom_layout_update":null,
         "available_sort_by":null,
         "is_active":"1",
         "landing_page":null,
         "is_anchor":"1",
         "include_in_menu":"1",
         "custom_use_parent_settings":"0",
         "custom_apply_to_products":"0",
         "name":"Dresses & Skirts",
         "url_key":"dresses-skirts",
         "image":null,
         "meta_title":null,
         "display_mode":"PRODUCTS",
         "url_path":"women\/dresses-skirts.html",
         "custom_design":null,
         "page_layout":"three_columns",
         "thumbnail":null,
         "custom_design_from":null,
         "custom_design_to":null,
         "filter_price_range":null,
         "has_children":false
      }
   ],
   "total":3,
   "page_size":15,
   "from":0
}
```

This one return Category list of A Category.