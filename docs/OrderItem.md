# HlConnector.OrderItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orderId** | **Number** | Vendor order ID that uniquely identifies this purchase order. | [optional] 
**orderLineId** | **Number** | Line number within the order that identifies this specific item. | [optional] 
**assetId** | **Number** | Unique identifier for the digital asset associated with this order item. | [optional] 
**customer** | **String** | Customer name associated with the order for personalization purposes. | [optional] 
**unitPrice** | **Number** | Unit price for a single item in the vendor&#39;s currency. | [optional] 
**lineItemPrice** | **Number** | Total price for this line item (unit price × quantity) in the vendor&#39;s currency. | [optional] 
**quantity** | **Number** | Quantity of items ordered in this line item. | [optional] 
**countryCode** | **String** | ISO 3166-1 alpha-2 country code for the country of sale. | [optional] 
**downloadUrl** | **String** | Secure download URL for the purchased asset. Available when the order is completed. Null if not yet fulfilled or if not applicable. | [optional] 
**viewUrl** | **String** | Secure view URL for the purchased asset. Available when the order is completed. Null if not yet fulfilled or if not applicable. | [optional] 
**status** | **String** | Current status of the order item (e.g., COMPLETED, PROCESSING, FAILED). | [optional] 


