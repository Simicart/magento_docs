# Catalog Category Tree

## Category tree Properties

Attributes| Type| Description
--------- | ------- | -----------
entity_id | id | Category Id
parent_id | id | Parent Category Id
level | int | Category Level
name | string | Category Name
image_url | string | Image URL path
thumbnail_url | string | Thumbnail URL path
child_cats | array | Child cats


## View Category Tree for the Root Category

```shell
curl "https://abc.com/simiconnector/rest/v2/categorytrees" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "categorytrees": [
    {
      "entity_id": "4",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "2",
      "created_at": "2013-01-25 17:43:31",
      "updated_at": "2018-04-05 02:35:48",
      "path": "1/2/4",
      "position": "2",
      "level": "2",
      "children_count": "5",
      "image_url": "http://codymamp.com/magento19/media/catalog/category/cat_2.png",
      "thumbnail_url": "http://codymamp.com/magento19/media/catalog/category/cat_1.png",
      "name": "Women",
      "child_cats": [
        {
          "entity_id": "10",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "4",
          "created_at": "2013-01-25 17:56:08",
          "updated_at": "2014-03-07 22:01:55",
          "path": "1/2/4/10",
          "position": "1",
          "level": "3",
          "children_count": "0",
          "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-w-newarrivals_1.jpg",
          "name": "New Arrivals",
          "child_cats": null
        },
        {
          "entity_id": "11",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "4",
          "created_at": "2013-01-25 17:57:32",
          "updated_at": "2014-11-23 06:50:26",
          "path": "1/2/4/11",
          "position": "2",
          "level": "3",
          "children_count": "0",
          "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-w-blouses.jpg",
          "name": "Tops & Blouses",
          "child_cats": null
        },
        {
          "entity_id": "12",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "4",
          "created_at": "2013-01-25 17:58:32",
          "updated_at": "2013-05-06 11:11:20",
          "path": "1/2/4/12",
          "position": "3",
          "level": "3",
          "children_count": "0",
          "name": "Pants & Denim",
          "child_cats": null
        },
        {
          "entity_id": "13",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "4",
          "created_at": "2013-01-25 17:59:21",
          "updated_at": "2013-03-05 11:45:24",
          "path": "1/2/4/13",
          "position": "4",
          "level": "3",
          "children_count": "1",
          "name": "Dresses & Skirts",
          "child_cats": [
            {
              "entity_id": "41",
              "entity_type_id": "3",
              "attribute_set_id": "3",
              "parent_id": "13",
              "created_at": "2018-04-05 02:12:32",
              "updated_at": "2018-04-05 02:12:32",
              "path": "1/2/4/13/41",
              "position": "1",
              "level": "4",
              "children_count": "0",
              "name": "Dress",
              "child_cats": null
            }
          ]
        }
      ]
    },
    {
      "entity_id": "5",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "2",
      "created_at": "2013-01-25 17:44:47",
      "updated_at": "2013-05-08 12:20:07",
      "path": "1/2/5",
      "position": "3",
      "level": "2",
      "children_count": "5",
      "name": "Men",
      "child_cats": [
        {
          "entity_id": "14",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "5",
          "created_at": "2013-01-25 18:01:03",
          "updated_at": "2013-05-06 11:12:42",
          "path": "1/2/5/14",
          "position": "1",
          "level": "3",
          "children_count": "0",
          "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-m-newarrivals.jpg",
          "name": "New Arrivals",
          "child_cats": null
        },
        {
          "entity_id": "15",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "5",
          "created_at": "2013-01-25 18:01:28",
          "updated_at": "2014-11-23 07:08:20",
          "path": "1/2/5/15",
          "position": "2",
          "level": "3",
          "children_count": "0",
          "name": "Shirts",
          "child_cats": null
        },
        {
          "entity_id": "16",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "5",
          "created_at": "2013-01-25 18:03:19",
          "updated_at": "2013-04-16 15:52:47",
          "path": "1/2/5/16",
          "position": "3",
          "level": "3",
          "children_count": "0",
          "name": "Tees, Knits and Polos",
          "child_cats": null
        },
        {
          "entity_id": "17",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "5",
          "created_at": "2013-01-25 18:03:48",
          "updated_at": "2013-03-05 14:15:31",
          "path": "1/2/5/17",
          "position": "4",
          "level": "3",
          "children_count": "0",
          "name": "Pants & Denim",
          "child_cats": null
        },
        {
          "entity_id": "40",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "5",
          "created_at": "2013-11-04 10:18:58",
          "updated_at": "2014-11-21 09:27:50",
          "path": "1/2/5/40",
          "position": "5",
          "level": "3",
          "children_count": "0",
          "name": "Blazers",
          "child_cats": null
        }
      ]
    },
    {
      "entity_id": "6",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "2",
      "created_at": "2013-01-25 17:47:41",
      "updated_at": "2013-12-25 19:28:34",
      "path": "1/2/6",
      "position": "4",
      "level": "2",
      "children_count": "4",
      "name": "Accessories",
      "child_cats": [
        {
          "entity_id": "18",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "6",
          "created_at": "2013-01-25 18:04:27",
          "updated_at": "2013-03-05 14:16:27",
          "path": "1/2/6/18",
          "position": "1",
          "level": "3",
          "children_count": "0",
          "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-eye.jpg",
          "name": "Eyewear",
          "child_cats": null
        },
        {
          "entity_id": "19",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "6",
          "created_at": "2013-01-25 18:05:03",
          "updated_at": "2013-03-05 14:16:42",
          "path": "1/2/6/19",
          "position": "2",
          "level": "3",
          "children_count": "0",
          "name": "Jewelry",
          "child_cats": null
        },
        {
          "entity_id": "20",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "6",
          "created_at": "2013-01-25 18:06:05",
          "updated_at": "2013-05-08 12:21:45",
          "path": "1/2/6/20",
          "position": "3",
          "level": "3",
          "children_count": "0",
          "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-shoes.jpg",
          "name": "Shoes",
          "child_cats": null
        },
        {
          "entity_id": "21",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "6",
          "created_at": "2013-01-25 18:07:12",
          "updated_at": "2013-03-05 14:17:10",
          "path": "1/2/6/21",
          "position": "4",
          "level": "3",
          "children_count": "0",
          "name": "Bags & Luggage",
          "child_cats": null
        }
      ]
    },
    {
      "entity_id": "7",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "2",
      "created_at": "2013-01-25 17:49:05",
      "updated_at": "2013-05-08 12:26:34",
      "path": "1/2/7",
      "position": "5",
      "level": "2",
      "children_count": "4",
      "name": "Home & Decor",
      "child_cats": [
        {
          "entity_id": "22",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "7",
          "created_at": "2013-01-25 18:07:52",
          "updated_at": "2013-05-17 03:06:14",
          "path": "1/2/7/22",
          "position": "1",
          "level": "3",
          "children_count": "0",
          "name": "Books & Music",
          "child_cats": null
        },
        {
          "entity_id": "23",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "7",
          "created_at": "2013-01-25 18:08:31",
          "updated_at": "2013-03-05 14:17:38",
          "path": "1/2/7/23",
          "position": "2",
          "level": "3",
          "children_count": "0",
          "name": "Bed & Bath",
          "child_cats": null
        },
        {
          "entity_id": "24",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "7",
          "created_at": "2013-01-25 18:08:54",
          "updated_at": "2013-03-09 02:27:16",
          "path": "1/2/7/24",
          "position": "3",
          "level": "3",
          "children_count": "0",
          "name": "Electronics",
          "child_cats": null
        },
        {
          "entity_id": "25",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "7",
          "created_at": "2013-01-25 18:10:06",
          "updated_at": "2013-03-30 05:54:12",
          "path": "1/2/7/25",
          "position": "4",
          "level": "3",
          "children_count": "0",
          "name": "Decorative Accents",
          "child_cats": null
        }
      ]
    },
    {
      "entity_id": "8",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "2",
      "created_at": "2013-01-25 17:49:50",
      "updated_at": "2013-05-16 05:49:33",
      "path": "1/2/8",
      "position": "6",
      "level": "2",
      "children_count": "4",
      "name": "Sale",
      "child_cats": [
        {
          "entity_id": "26",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "8",
          "created_at": "2013-01-25 18:10:39",
          "updated_at": "2013-05-06 11:17:00",
          "path": "1/2/8/26",
          "position": "1",
          "level": "3",
          "children_count": "0",
          "name": "Women",
          "child_cats": null
        },
        {
          "entity_id": "27",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "8",
          "created_at": "2013-01-25 18:11:07",
          "updated_at": "2013-05-06 11:17:12",
          "path": "1/2/8/27",
          "position": "2",
          "level": "3",
          "children_count": "0",
          "name": "Men",
          "child_cats": null
        },
        {
          "entity_id": "28",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "8",
          "created_at": "2013-01-25 18:11:31",
          "updated_at": "2013-05-06 11:17:24",
          "path": "1/2/8/28",
          "position": "3",
          "level": "3",
          "children_count": "0",
          "name": "Accessories",
          "child_cats": null
        },
        {
          "entity_id": "29",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "8",
          "created_at": "2013-01-25 18:12:07",
          "updated_at": "2013-05-06 11:17:34",
          "path": "1/2/8/29",
          "position": "4",
          "level": "3",
          "children_count": "0",
          "name": "Home & Decor",
          "child_cats": null
        }
      ]
    },
    {
      "entity_id": "9",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "2",
      "created_at": "2013-01-25 17:50:47",
      "updated_at": "2013-05-11 00:17:59",
      "path": "1/2/9",
      "position": "7",
      "level": "2",
      "children_count": "0",
      "name": "VIP",
      "child_cats": null
    }
  ]
}
```

This request return the Root category's tree



## View Category Tree of A Category

```shell
curl "https://abc.com/simiconnector/rest/v2/categorytrees/4" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
  "categorytrees": [
    {
      "entity_id": "10",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "4",
      "created_at": "2013-01-25 17:56:08",
      "updated_at": "2014-03-07 22:01:55",
      "path": "1/2/4/10",
      "position": "1",
      "level": "3",
      "children_count": "0",
      "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-w-newarrivals_1.jpg",
      "name": "New Arrivals",
      "child_cats": null
    },
    {
      "entity_id": "11",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "4",
      "created_at": "2013-01-25 17:57:32",
      "updated_at": "2014-11-23 06:50:26",
      "path": "1/2/4/11",
      "position": "2",
      "level": "3",
      "children_count": "0",
      "image_url": "http://codymamp.com/magento19/media/catalog/category/plp-w-blouses.jpg",
      "name": "Tops & Blouses",
      "child_cats": null
    },
    {
      "entity_id": "12",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "4",
      "created_at": "2013-01-25 17:58:32",
      "updated_at": "2013-05-06 11:11:20",
      "path": "1/2/4/12",
      "position": "3",
      "level": "3",
      "children_count": "0",
      "name": "Pants & Denim",
      "child_cats": null
    },
    {
      "entity_id": "13",
      "entity_type_id": "3",
      "attribute_set_id": "3",
      "parent_id": "4",
      "created_at": "2013-01-25 17:59:21",
      "updated_at": "2013-03-05 11:45:24",
      "path": "1/2/4/13",
      "position": "4",
      "level": "3",
      "children_count": "1",
      "name": "Dresses & Skirts",
      "child_cats": [
        {
          "entity_id": "41",
          "entity_type_id": "3",
          "attribute_set_id": "3",
          "parent_id": "13",
          "created_at": "2018-04-05 02:12:32",
          "updated_at": "2018-04-05 02:12:32",
          "path": "1/2/4/13/41",
          "position": "1",
          "level": "4",
          "children_count": "0",
          "name": "Dress",
          "child_cats": null
        }
      ]
    }
  ]
}
```

This one return Category tree of A Category.
