# CCAvenue

## CCAvenue Properties


## After Order Placed

```shell
curl POST "https://abc.com/simiconnector/rest/v2/orders/onepage" \
  -H "Authorization: Bearer <token>"
```

> The above command returns JSON structured like this:

```json
{
    "order": {
        "invoice_number": "100000013",
        "payment_method": "simiavenue",
        "url_action": "https://test.ccavenue.com/transaction/transaction.do?command=initiateTransaction&encRequest=16de9c21bd000967e029a91afd38ad2f5e6d9962bec0a86220716edba563f2609faf4ba7d18283059ed0632cec347421abdb9a089627e4aac40e1d08d2bfb2dd351426488a20b6cd3ca7cc5d504d04f89a8c3cb72d12e145e4768cf27ccc3b65da7dff04b4052a17c81b723a863d418fac4f456dd5fe534b1c962159451d295e0bd00319d93afbdbab1e4846e88de9c4a256284e5c00c0e2142c88291cf8c84349e032f61aa573813ec2cbab0e8183cdec2eb92593c6bb966ffcf7f33a6c3973a25045af4d342682c8f97cc35027a3a4b9b2ede5b6255af276c325506305cf2ce2a12830d8896c308301eaec30e4b1b93b0d269e751adac59c7adb673c73c58682e431734093d6435adb7ec302ff21c0a201e9382c1c8ab120a0aab19b787cad319e68061989898cddec8420d5d13eff0fadfc4382ef6dd050356e99afe23e861607cf4097a0858f2bcc895bb62c6ceb0d645c20ba7caf4535f2c6a658ab5eb0f241f1002d0fef5e6f16a6c9d59e461eb9492509f77b1a50b8555f7c25b9aad930841b6065c3ea7ce6429060801caeda1ce5929f3e63719689280ad0183a16c3d676bbf5343c06d46f19af9ce587c065703ba614ff9be67eaaaf35453865af8f44f020ba451ba6bba5509c11136bd2fe928b5f88839a6043a422b469fa7b68e3b7ae89bcd6c5ad990b7f218dbeb8992c947689cf5727d5356da8dec64e79e64a528f4aa63033ae3f960606a0c2e7c7b6718e1b07acf4a63c5159e8536584f6625be53ab2849c1d12c53624f8b44764b4f47c2defae614d0fbaa28fc46b684088a5d3dba110e472fbc1782013ac9ae87a1ecafdf7b88c91019ee5d95377add132&access_code="
    }
}
```

Open the url on url_action

Check the url opened on webview:

“onepage/success” -> Show Thank you pop up. Back to home screen.

“onepage/review” -> Show Thank you and let customer know that rewiew would be required pop up. Back to home screen.

“onepage/failure” -> Show error pop up. Back to home screen.

“simiavenue/api/index” -> Show error pop up. Back to home screen.


### HTTP Request


