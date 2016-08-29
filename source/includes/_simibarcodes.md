# QR Code/Barcode Scan

## QR Code/Barcode Properties

Attributes| Type| Description
--------- | ------- | -----------
barcode_id | id | QR/BarCode Id
barcode | string | Barcode
qrcode | string | QR Code
barcode_status | int | Barcode enabled
product_entity_id | id | Product Entity Id
product_name | string | Product Name
product_sku | string | Product SKU


## Get Information of a QR Code/Barcode

```shell
curl "https://abc.com/simiconnector/rest/v2/simibarcodes/QRBNSLD40CDY?type=1" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{  
   "simibarcode":{  
      "barcode_id":"4",
      "barcode":"BARJKASN2F8TAHAI",
      "qrcode":"QRBNSLD40CDY",
      "barcode_status":"1",
      "product_entity_id":"873",
      "product_name":"Annie Pump",
      "product_sku":"shw003",
      "created_date":"2016-06-21 08:41:59"
   }
}
```

This request is to get Information From QR/Bar Code