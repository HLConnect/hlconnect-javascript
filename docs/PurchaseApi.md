# HlConnect.PurchaseApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseCancel**](PurchaseApi.md#connectorPurchaseCancel) | **DELETE** /purchase/cancel | Cancel purchase order line item
[**connectorPurchaseDownloadUrl**](PurchaseApi.md#connectorPurchaseDownloadUrl) | **GET** /purchase/download-url | Get asset download URL
[**connectorPurchaseInfo**](PurchaseApi.md#connectorPurchaseInfo) | **GET** /purchase/info | Retrieve purchase order information
[**connectorPurchaseRegister**](PurchaseApi.md#connectorPurchaseRegister) | **POST** /purchase/register | Register a new purchase transaction
[**connectorPurchaseValidatePurchaseBeforePayment**](PurchaseApi.md#connectorPurchaseValidatePurchaseBeforePayment) | **POST** /purchase/validate-purchase-before-payment | Validate purchase before payment
[**connectorPurchaseViewUrl**](PurchaseApi.md#connectorPurchaseViewUrl) | **GET** /purchase/view-url | Get asset view URL



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

let apiInstance = new HlConnect.PurchaseApi();
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

let apiInstance = new HlConnect.PurchaseApi();
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


## connectorPurchaseInfo

> [OrderItem] connectorPurchaseInfo(orderId)

Retrieve purchase order information

Returns detailed information about a purchase order including status, asset details, pricing, and fulfillment status. Response varies based on processing status (complete, processing, failed).

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.PurchaseApi();
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


## connectorPurchaseRegister

> connectorPurchaseRegister(purchaseRegisterRequest)

Register a new purchase transaction

Initiates the purchase process for a digital asset. Validates request parameters, creates a new order, and begins fulfillment. This is an asynchronous operation - use /purchase/info to check order status.

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.PurchaseApi();
let purchaseRegisterRequest = new HlConnect.PurchaseRegisterRequest(); // PurchaseRegisterRequest | Purchase registration request with asset and order details
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


## connectorPurchaseValidatePurchaseBeforePayment

> ValidationToken connectorPurchaseValidatePurchaseBeforePayment(purchaseValidateBeforePaymentRequest)

Validate purchase before payment

Validates purchase parameters before payment is initiated. Checks asset availability, regional restrictions (based on buyer IP), and minimum quantity requirements. 

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.PurchaseApi();
let purchaseValidateBeforePaymentRequest = new HlConnect.PurchaseValidateBeforePaymentRequest(); // PurchaseValidateBeforePaymentRequest | Purchase validation request with asset, buyer IP and quantity
apiInstance.connectorPurchaseValidatePurchaseBeforePayment(purchaseValidateBeforePaymentRequest, (error, data, response) => {
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
 **purchaseValidateBeforePaymentRequest** | [**PurchaseValidateBeforePaymentRequest**](PurchaseValidateBeforePaymentRequest.md)| Purchase validation request with asset, buyer IP and quantity | 

### Return type

[**ValidationToken**](ValidationToken.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## connectorPurchaseViewUrl

> ViewUrl connectorPurchaseViewUrl(orderId, orderLineId)

Get asset view URL

Generates and returns a secure, time-limited view URL for a purchased digital asset. The URL can be used to view the asset online (e.g., sheet music viewer).

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.PurchaseApi();
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

