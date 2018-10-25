# URL Dictionary

## Dictionary result Properties

Attributes| Type| Description
--------- | ------- | -----------
url_rewrite_id | id | Url Rewrite Id
request_path | string | Request path
target_path | string | Target path
category_id | string | Category Id, if not null, it's category Url
product_id | string | Product Id, if not null, it's product Url (If has both category_id and product_id, it's category)
simi_category_products | array | Products of category
simi_category_child | array | Child categories of that category (if contains get_child_cat=1 in param)
simi_product_data | array | Product detail data

## Get Category from url

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/urldicts/detail?url=home-decor.html&image_width=120&image_height=120&get_child_cat=1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "urldict": {
  "url_rewrite_id": "21",
  "store_id": "1",
  "id_path": "category/7",
  "request_path": "home-decor.html",
  "target_path": "catalog/category/view/id/7",
  "is_system": "1",
  "options": null,
  "description": null,
  "category_id": "7",
  "product_id": null,
  "simi_catetory_name": "Home & Decor",
  "simi_category_child": {
    "all_ids": [],
    "categories": [],
    "total": 4,
    "page_size": 15,
    "from": 0
  },
  "simi_category_products": {
    "all_ids": [],
    "products": [],
    "total": 36,
    "page_size": 12,
    "from": 0,
    "layers": {},
    "orders": []
    }
  }
}
```

This api return category when the url sent points to a category.

If get_child_cat !== 1, there won't be simi_category_child included.

Paging, offset, image width, height, ... can be included too.



## Get Product from url

```shell
curl -X GET "https://abc.com/simiconnector/rest/v2/urldicts/detail?url=linen-blazer-693.html" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "urldict": {
    "url_rewrite_id": "9886",
    "store_id": "1",
    "id_path": "product/406",
    "request_path": "linen-blazer-693.html",
    "target_path": "catalog/product/view/id/406",
    "is_system": "1",
    "options": null,
    "description": null,
    "category_id": null,
    "product_id": "406",
    "simi_product_data": {
    "product": {
      "entity_id": "406",
      "entity_type_id": "4",
      "attribute_set_id": "13",
      "type_id": "configurable",
      "sku": "msj012c",
      "has_options": "1",
      "required_options": "1",
      "created_at": "2013-03-04T22:25:10-08:00",
      "updated_at": "2018-05-22 07:53:52",
      "name": "Linen Blazer",
      "meta_title": null,
      "meta_description": null,
      "image": "/m/s/msj012t_2.jpg",
      "small_image": "/m/s/msj012t_2.jpg",
      "thumbnail": "/m/s/msj012t_2.jpg",
      "media_gallery": {},
      "gallery": null,
      "url_key": "linen-blazer",
      "url_path": "linen-blazer-693.html",
      "custom_design": null,
      "page_layout": "one_column",
      "options_container": "container1",
      "image_label": null,
      "small_image_label": null,
      "thumbnail_label": null,
      "country_of_manufacture": null,
      "msrp_enabled": "2",
      "msrp_display_actual_price_type": "4",
      "gift_message_available": null,
      "gift_wrapping_available": "0",
      "color": null,
      "status": "1",
      "visibility": "4",
      "tax_class_id": "0",
      "occasion": "31",
      "apparel_type": "211",
      "sleeve_length": "47",
      "fit": "49",
      "size": null,
      "gender": "93",
      "description": "Single vented, notched lapels. Flap pockets. Tonal stitching. Fully lined. Linen. Dry clean.",
      "short_description": "In airy lightweight linen, this blazer is classic tailoring with a warm weather twist.",
      "meta_keyword": null,
      "custom_layout_update": null,
      "special_from_date": null,
      "special_to_date": null,
      "news_from_date": "2013-03-01 00:00:00",
      "news_to_date": null,
      "custom_design_from": null,
      "custom_design_to": null,
      "price": "455.0000",
      "special_price": null,
      "msrp": null,
      "gift_wrapping_price": null,
      "_cache_instance_products": [],
      "_cache_instance_configurable_attributes": {},
      "children_products": [],
      "group_price": [],
      "group_price_changed": 0,
      "tier_price": [],
      "tier_price_changed": 0,
      "stock_item": {},
      "is_in_stock": "1",
      "is_salable": "1",
      "child_attribute_label_mapping": {},
      "list_swatch_attr_values": {},
      "list_swatch_attr_stock_values": {},
      "additional": {},
      "images": [],
      "app_prices": {},
      "app_tier_prices": [],
      "app_reviews": {},
      "app_options": {},
      "wishlist_item_id": null,
      "product_labels": [],
      "product_video": null,
      "loyalty_image": "https://d373zvlpznfl2h.cloudfront.net/media/simirewardpoints/default/dr-icons-01.png",
      "loyalty_label": "You could receive some Points for purchasing this product"
      }
    }
  }
}
```

This one return Product from url.
