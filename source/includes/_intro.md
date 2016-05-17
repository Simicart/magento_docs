# Introduction Testing

Welcome to the MAGENTO API from SIMICART TEAM! You can use our API to access MAGENTO API endpoints, which can get information on various products, customers, sales, and so on.

## Resource's URI
<code>http(s)://{your_base_url}/simiconnector/rest/version/**resources/{id}*/nested_resources/{nested_id}*?refines**</code>

- version is v2
- **resources** is the name of document that you want to work with. For example: products, customers, orders...
- **nested_resources** is the name of document that related with the main resource (above). For example nested resources of products: images, categories, stock_item ...

## Authentication

> To authorize, use this code:

```shell
curl -X POST "api_endpoint_here" \
  -H "Content-Type:application/json" \
  -H "Authorization: Bearer <token>" \
  -d '{}'
```

> Make sure to replace `token` with your OAuth2.0 API token.

LavaHub uses [OAuth2.0](https://tools.ietf.org/html/rfc6749) to allow access to the API. You can register your developer account and your applications at our [developer portal](http://developer.jajahub.com/)

LavaHub expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer <token>`

<aside class="notice">
You must replace <code>token</code> with your OAuth2.0 API token.
</aside>

## HTTP Verbs
We use HTTP Verbs to determine the action with API resource. There are the table of HTTP Verbs are using for REST API:

Verb | Action | Example
---- | ------ | -------
<code>POST</code> | **C**reate | **<code>POST</code> /products** <br> Create new product <br><br> **<code>POST</code> /products/123** <br> Create new product with data similar as product 123
<code>GET</code> | **R**ead | **<code>GET</code> /products** <br> Receive the list of products <br><br> **<code>GET</code> /products/123** <br> Receive the detail of product 123
<code>PUT</code> | **U**pdate | **<code>PUT</code> /products** <br> Mass update products <br><br> **<code>PUT</code> /products/123** <br> Update product 123
<code>DELETE</code> | **D**elete | **<code>DELETE</code> /products** <br> Mass delete warehouses with ids from query param <br><br> **<code>DELETE</code> /products/123** <br> Delete product 123


## Request
All requests to MAGENTO API Gateway need an Authorization.

### Query params
- To filter the result when listing the resource document, we use <code>filter</code> param. For example:
<code>products?filter[name][like]=John&filter[created_at]=2015-03-20T13:59:00Z&filter[status]=1</code>

- To get only some fields of document in the result, we use <code>fields</code> param. For example:
<code>products/123?fields=name,status</code>

### Payload Body

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/customers" \
  -H "Content-Type:application/json" \
  -H "Authorization: Bearer <token>" \
  -d '{
  "name": "John Doe",
  "email": "user@sample.com"
}'
```
The data posted to MAGENTO API Gateway must be presented as JSON string.
<br><br><br><br><br><br><br><br>

### Encode Binary Data

```shell
curl -X POST "https://abc.com/simiconnector/rest/v2/products/123/images" \
  -H "Content-Type:application/json" \
  -H "Authorization: Bearer <token>" \
  -d '{
  "product_id": "123",
  "file_name": "sanvado_base.png"
  "content-type": "image/png",
  "content-length": "1024000",
  "file_data": "R0lGODlhbgCMAPf\/APbr48VySrxTO7IgKt2qmKQdJeK8lsFjROG5p\/nz7Zg3\nMNmnd7Q1MLNVS9GId71hSJMZIuzTu4UtKbeEeakhKMl8U8WYjfr18YQaIbAf\nKKwhKdKzqpQtLebFortOOejKrOjZ1Mt7aMNpVbAqLLV7bsNqR+3WwMqEWenN\nsZYxL\/Ddy\/Pm2e7ZxLlUQrIjNPXp3bU5MbhENbEtLtqhj5ZQTfHh0bMxL7Ip\nNsNyUYkZIrZJPcqGdYIUHb5aPKkeJnoUHd2yiJkiLKYiKLRFOsyJXKVDO8up\nosFaS+TBnK4kKti5sNaYg\/z49aqYl5kqLrljUtORfMOlo\/36+H4ZH8yDYq0f\nKKFYTaU9MrY8MrZBNXwXHpgaIdGVYu\/byLZNP9SaZLIyOuXCtHkpJst+Wpcm",
  "title": "Sanvado shoes",
  "type": "1"
}'
```
We use BASE64 Coding to encode binary data and transfer as a field of Payload JSON string.

## Pagination and sort order
### Pagination
Request that presents multiple items will be paginated to 10 items by default. To control the pagination, we use three query params:

Param | Description | Example
--- | ----- | ----------- | -------
limit | Limit the number of items per page. Default value is 10. | <code>/products?limit=20</code> <br>Limit 20 products on result
offset | The number of items the be skipped on result. Default value is 0. | <code>/products?offset=20</code> <br> Get 10 products from 21th product
page | The page number of result. Default value is 1. If this param is presented, we ignore the offset param. | <code>/products?page=2</code> <br> Get 10 product of page 2 (that mean we skip 10 items)
ids | List id object want get in one query | <code>/products?ids=16,17</code> <br> Get 2 products has id = 16 and 17

### Sort order
By the default, we will sort the result by <code>_id</code> field with <code>desc</code> direction. To control the sort order, we use two query params:

Param | Description | Example
----- | ----------- | -------
order | The attribute (field) that will be use for sorting. Default is <code>_id</code> | <code>/products?order=name</code> <br> We sort the result by name
dir | The sort direction. We accept two types <code>asc</code> and <code>desc</code>. Default is <code>desc</code>. | <code>/products?dir=asc</code> <br> We sort the result by increment <code>_id</code>

## Response
```json
{
  "all_ids": [
    "16",
    "17"
  ],
  "products": [
    {
      "entity_id":"16",
      "entity_type_id":"10",
      "attribute_set_id":"38",
      "type_id":"simple",
      "sku":"n2610",
      "created_at":"2007-08-23 13:03:05",
      "updated_at":"2008-08-08 14:50:04",
      "has_options":"0",
      "required_options":"0",
      "price":"149.9900",
      "tax_class_id":"2",
      "final_price":"149.9900",
      "minimal_price":"149.9900",
      "min_price":"149.9900",
      "max_price":"149.9900",
      "tier_price":null,
      "cat_index_position":"90027",
      "name":"Nokia 2610 Phone",
      "url_key":"nokia-2610-phone",
      "small_image":"\/n\/o\/nokia-2610-phone-2.jpg",
      "thumbnail":"\/n\/o\/nokia-2610-phone-2.jpg",
      "status":"1",
      "short_description":"The words \"entry level\" no longer mean \"low-end,\" especially when it comes to the Nokia 2610. Offering advanced media and calling features without breaking the bank",
      "do_not_use_category_id":true,
      "request_path":"nokia-2610-phone.html",
      "is_salable":"1",
      "stock_item":{
        "is_in_stock":"1"
      }
    },
    {
        "entity_id":"17",
        "entity_type_id":"10",
        "attribute_set_id":"38",
        "type_id":"simple",
        "sku":"bb8100",
        "created_at":"2007-08-23 15:40:26",
        "updated_at":"2008-08-08 14:50:23",
        "has_options":"0",
        "required_options":"0",
        "price":"349.9900",
        "tax_class_id":"2",
        "final_price":"349.9900",
        "minimal_price":"349.9900",
        "min_price":"349.9900",
        "max_price":"349.9900",
        "tier_price":null,
        "cat_index_position":"90027",
        "name":"BlackBerry 8100 Pearl",
        "url_key":"blackberry-8100-pearl",
        "thumbnail":"\/b\/l\/blackberry-8100-pearl-2.jpg",
        "small_image":"\/b\/l\/blackberry-8100-pearl-2.jpg",
        "status":"1",
        "short_description":"The BlackBerry 8100 Pearl is a departure from the form factor of previous BlackBerry devices. This BlackBerry handset is far more phone-like, and RIM's engineers have managed to fit a QWERTY keyboard onto the handset's slim frame.",
        "do_not_use_category_id":true,
        "request_path":"blackberry-8100-pearl.html",
        "is_salable":"1",
        "stock_item":{
          "is_in_stock":"1"
        }
    }
  ],
  "total": 2,
  "page_size": 10,
  "from": 0
}
```

Our REST API response with success HTTP statuses:

Status Code | Description
----------- | -----------
200 | Request successfully
201 | Created resource successfully

### Collection meta data
With reponses that present the collection of data, we will have these meta data:

Param | Description | Example
----- | ----------- | -------
total | The number of all results that match the critical | 100
page_size | The number of items per page | 10
from | The start index of item in the result | 1
all_ids | An ids array of all results that match the critical, not only the response items | [1,2,3,4,5,6,7...]
cur_page | Current page of result | 2
total_pages | The number of pages of result | 7
order | The attribute (field) that will be use for sorting. Default is <code>_id</code> | <code>name</code>
dir | The sort direction. We accept two types <code>asc</code> and <code>desc</code>. Default is <code>desc</code>. | <code>asc</code>


## Errors

> The error returns with JSON body like this:

```json
{
  "errors": [
    {
      "code": "1",
      "message": "Unsupported request method"
    }
  ]
}
```

The LavaHub API uses the following HTTP error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request sucks
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- The resource requested is hidden from your permission
404 | Not Found -- The specified resource could not be found
405 | Method Not Allowed -- You tried to access a resource with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The resource requested has been removed from our servers
418 | I'm a teapot
429 | Too Many Requests -- You're requesting too many resources! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
