# HlConnect.HealthApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**health**](HealthApi.md#health) | **GET** /health | Perform system health check



## health

> [HealthItem] health()

Perform system health check

Checks the status of critical system components such as database connections and external services. Returns an array of health check results indicating whether each component is functioning properly. This endpoint is publicly accessible and can be used for monitoring system uptime.

### Example

```javascript
import HlConnect from 'hl_connect';

let apiInstance = new HlConnect.HealthApi();
apiInstance.health((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**[HealthItem]**](HealthItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

