# HlConnect.AssetsApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**assetsList**](AssetsApi.md#assetsList) | **GET** /assets/list | Retrieve a paginated list of digital assets



## assetsList

> AssetsListResponse assetsList(opts)

Retrieve a paginated list of digital assets

Returns a list of digital assets with their complete metadata. Assets include information about formats, pricing, contributors, categories, instruments, and related media.

### Example

```javascript
import HlConnect from 'hl_connect';
let defaultClient = HlConnect.ApiClient.instance;
// Configure Bearer access token for authorization: access_token
let access_token = defaultClient.authentications['access_token'];
access_token.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new HlConnect.AssetsApi();
let opts = {
  'pageSize': 20, // Number | Number of assets to return per page
  'lastId': 56 // Number | The ID of the last asset from the previous page. Used for pagination to retrieve the next page of results.
};
apiInstance.assetsList(opts, (error, data, response) => {
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
 **pageSize** | **Number**| Number of assets to return per page | [optional] [default to 20]
 **lastId** | **Number**| The ID of the last asset from the previous page. Used for pagination to retrieve the next page of results. | [optional] 

### Return type

[**AssetsListResponse**](AssetsListResponse.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

