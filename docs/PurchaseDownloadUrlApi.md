# HlConnect.PurchaseDownloadUrlApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseDownloadUrl**](PurchaseDownloadUrlApi.md#connectorPurchaseDownloadUrl) | **GET** /purchase/download-url | Get asset download URL



## connectorPurchaseDownloadUrl

> DownloadUrl connectorPurchaseDownloadUrl(orderId, orderLineId)

Get asset download URL

Generates and returns a secure download URL for a purchased digital asset. The URL can be used to download the asset file.

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.PurchaseDownloadUrlApi();
let orderId = 12345; // Number | Vendor order ID that contains the asset to download
let orderLineId = 1; // Number | Specific line item within the order that identifies the asset to download
apiInstance.connectorPurchaseDownloadUrl(orderId, orderLineId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **Number**| Vendor order ID that contains the asset to download | 
 **orderLineId** | **Number**| Specific line item within the order that identifies the asset to download | 

### Return type

[**DownloadUrl**](DownloadUrl.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

