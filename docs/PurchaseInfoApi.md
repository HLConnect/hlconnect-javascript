# HlConnector.PurchaseInfoApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseInfo**](PurchaseInfoApi.md#connectorPurchaseInfo) | **GET** /purchase/info | Retrieve purchase order information



## connectorPurchaseInfo

> [OrderItem] connectorPurchaseInfo(orderId)

Retrieve purchase order information

Returns detailed information about a purchase order including status, asset details, pricing, and fulfillment status. Response varies based on processing status (complete, processing, failed).

### Example

```javascript
import HlConnector from 'hl_connector';
let defaultClient = HlConnector.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnector.PurchaseInfoApi();
let orderId = 12345; // Number | Vendor order ID to retrieve purchase details for. This is the unique identifier assigned by the vendor when placing the order.
apiInstance.connectorPurchaseInfo(orderId, (error, data, response) => {
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
 **orderId** | **Number**| Vendor order ID to retrieve purchase details for. This is the unique identifier assigned by the vendor when placing the order. | 

### Return type

[**[OrderItem]**](OrderItem.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

