# HlConnect.PurchaseRegisterRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **String** | Validation token | 
**orderNumber** | **Number** | Vendor-generated order number that uniquely identifies this purchase order. | 
**orderLineId** | **Number** | Line number within the order that identifies this specific item. Used to distinguish multiple items in the same order. | 
**lineItemPrice** | **Number** | Price for this specific line item as a real number. Represents the total price for the quantity specified. | 
**unitPrice** | **Number** | Unit price for a single item as a real number | 
**customer** | **String** | Customer name for asset personalization. May be printed on the asset if personalization is supported. | 
**parts** | [**[AssetPartForm]**](AssetPartForm.md) | Optional parts specification for ensemble assets. Allows customers to select specific parts of an ensemble for individual purchase rather than buying the complete set. | [optional] 


