# Daily Deal

## Daily Deal Properties

Attributes| Type| Description
--------- | ------- | -----------
id | int | Deal Id
title | string | Deal Title
product_id | int | Deal Product Id
product_name | string | Deal Product Name
save | int | Deal Discount (%)
deal_price | int | Deal Price
quantity | int | Deal Quantity
sold | int | Deal Product Sold
start_time | datetime | Deal Start Time
close_time | datetime | Deal Close Time
deal_time | int | Deal Timestamp 
time_left | int | Deal Time Left
status | int | Deal Status
store_id | int | Store Id
is_random | int | Is Ramdom


## View List Of Products

```shell
curl "https://abc.com/simiconnector/rest/v2/simidailydeals" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "all_ids": [
    "549",
    "916"
  ],
  "products": [
    {
      "entity_id": "549",
      "entity_type_id": "4",
      "attribute_set_id": "17",
      "type_id": "simple",
      "sku": "acj0006s",
      "has_options": "0",
      "comment" : ".....",
      "dailydeal": {
        "id": "3",
        "title": "Blue Horizons Bracelets sale off 50%",
        "product_id": "549",
        "product_name": "Blue Horizons Bracelets",
        "thumbnail_image": null,
        "save": "50",
        "deal_price": 27.5,
        "quantity": "2",
        "sold": "0",
        "start_time": "2017-08-14 08:49:00",
        "deal_time": 1382400,
        "time_left": 1033345,
        "close_time": "2017-08-30 08:49:00",
        "status": "3",
        "store_id": "0",
        "process": "0",
        "is_random": "0",
        "currency": "$"
      }
    },
    {
      "entity_id": "916",
      "entity_type_id": "4",
      "attribute_set_id": "4",
      "type_id": "virtual",
      "sku": "axevituralproduct",
      "has_options": "1",
      "comment" : "......",
      "dailydeal": {
        "id": "2",
        "title": "Axe virtual product sale off 30%",
        "product_id": "916",
        "product_name": "Axe virtual product",
        "thumbnail_image": null,
        "save": "30",
        "deal_price": 70,
        "quantity": "5",
        "sold": "0",
        "start_time": "2017-08-14 08:49:00",
        "deal_time": 1468800,
        "time_left": 1119745,
        "close_time": "2017-08-31 08:49:00",
        "status": "3",
        "store_id": "0",
        "process": "0",
        "is_random": "0",
        "currency": "$"
      }
    }
  ],
  "total": 2,
  "page_size": 15,
  "from": 0
}
```

This endpoint retrieves a list of products.

