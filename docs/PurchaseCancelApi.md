# HlConnect.PurchaseCancelApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseCancel**](PurchaseCancelApi.md#connectorPurchaseCancel) | **DELETE** /purchase/cancel | Cancel purchase order line item



## connectorPurchaseCancel

> connectorPurchaseCancel(orderId, orderLineId)

Cancel purchase order line item

Cancels a specific line item within a purchase order. The order must be in a cancellable status. Both order ID and order line ID must be specified.

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.PurchaseCancelApi();
let orderId = 12345; // Number | Vendor order ID containing the line item to cancel
let orderLineId = 1; // Number | Specific line item within the order to cancel
apiInstance.connectorPurchaseCancel(orderId, orderLineId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **Number**| Vendor order ID containing the line item to cancel | 
 **orderLineId** | **Number**| Specific line item within the order to cancel | 

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

