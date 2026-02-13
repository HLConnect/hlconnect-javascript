# HlConnect.PurchaseValidationApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connectorPurchaseValidatePurchaseBeforePayment**](PurchaseValidationApi.md#connectorPurchaseValidatePurchaseBeforePayment) | **POST** /purchase/validate-purchase-before-payment | Validate purchase before payment



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

let apiInstance = new HlConnect.PurchaseValidationApi();
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

