# HlConnector.PurchaseRegisterApi

All URIs are relative to *https://hlconnect-api-sandbox.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseRegister**](PurchaseRegisterApi.md#connectorPurchaseRegister) | **POST** /purchase/register | Register a new purchase transaction



## connectorPurchaseRegister

> connectorPurchaseRegister(purchaseRegisterRequest)

Register a new purchase transaction

Initiates the purchase process for a digital asset. Validates request parameters, creates a new order, and begins fulfillment. This is an asynchronous operation - use /purchase/info to check order status.

### Example

```javascript
import HlConnector from 'hl_connector';
let defaultClient = HlConnector.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnector.PurchaseRegisterApi();
let purchaseRegisterRequest = new HlConnector.PurchaseRegisterRequest(); // PurchaseRegisterRequest | Purchase registration request with asset and order details
apiInstance.connectorPurchaseRegister(purchaseRegisterRequest, (error, data, response) => {
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
 **purchaseRegisterRequest** | [**PurchaseRegisterRequest**](PurchaseRegisterRequest.md)| Purchase registration request with asset and order details | 

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

