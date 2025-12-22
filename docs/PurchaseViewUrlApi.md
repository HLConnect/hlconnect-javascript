# HlConnector.PurchaseViewUrlApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseViewUrl**](PurchaseViewUrlApi.md#connectorPurchaseViewUrl) | **GET** /purchase/view-url | Get asset view URL



## connectorPurchaseViewUrl

> ViewUrl connectorPurchaseViewUrl(orderId, orderLineId)

Get asset view URL

Generates and returns a secure, time-limited view URL for a purchased digital asset. The URL can be used to view the asset online (e.g., sheet music viewer).

### Example

```javascript
import HlConnector from 'hl_connector';
let defaultClient = HlConnector.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnector.PurchaseViewUrlApi();
let orderId = 12345; // Number | Vendor order ID that contains the asset to view
let orderLineId = 1; // Number | Specific line item within the order that identifies the asset to view
apiInstance.connectorPurchaseViewUrl(orderId, orderLineId, (error, data, response) => {
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
 **orderId** | **Number**| Vendor order ID that contains the asset to view | 
 **orderLineId** | **Number**| Specific line item within the order that identifies the asset to view | 

### Return type

[**ViewUrl**](ViewUrl.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

