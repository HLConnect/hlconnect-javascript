# HlConnector.PurchaseRegisterRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assetId** | **Number** | Unique identifier for the digital asset to be purchased. This is Hal Leonard&#39;s internal asset ID. | 
**orderNumber** | **Number** | Vendor-generated order number that uniquely identifies this purchase order. | 
**orderLineId** | **Number** | Line number within the order that identifies this specific item. Used to distinguish multiple items in the same order. | 
**countryCode** | **String** | ISO 3166-1 alpha-2 country code identifying the country of sale for the customer. | 
**lineItemPrice** | **Number** | Price for this specific line item as a real number. Represents the total price for the quantity specified. | 
**unitPrice** | **Number** | Unit price for a single item as a real number | 
**quantity** | **Number** | Quantity of items being purchased in this line item. | 
**customer** | **String** | Customer name for asset personalization. May be printed on the asset if personalization is supported. | 
**parts** | [**[AssetPartForm]**](AssetPartForm.md) | Optional parts specification for ensemble assets. Allows customers to select specific parts of an ensemble for individual purchase rather than buying the complete set. | [optional] 


