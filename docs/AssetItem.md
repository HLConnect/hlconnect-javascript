# HlConnector.AssetItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assetId** | **Number** | Unique identifier for the asset. This is Hal Leonard&#39;s internal identifier for the digital product. | [optional] 
**formatShortName** | **String** | Short name of the asset format (e.g., PVG for Piano/Vocal/Guitar, SSA for Soprano/Soprano/Alto). | [optional] 
**format** | **String** | Full name of the asset format (e.g., Piano/Vocal/Guitar, Soprano/Soprano/Alto). | [optional] 
**pageCount** | **Number** | The number of pages in the sheet music or document. | [optional] 
**title** | **String** | Title of the asset (song or composition name). | [optional] 
**description** | **String** | Detailed description of the asset, including background information, arrangement details, and other relevant content. | [optional] 
**songNumber** | **Number** | Hal Leonard&#39;s internal song identifier. This is a unique number assigned to each musical composition. | [optional] 
**publicDomain** | **Boolean** | Indicates whether the song represented by this asset exists in the public domain. | [optional] 
**externalRef** | **String** | Identifier of the company providing the asset. This field identifies the external source or provider of the asset. | [optional] 
**externalRefId** | **Number** | Numeric identifier of the company providing the asset. | [optional] 
**voicing** | **String** | Voicing configuration for choral format assets (e.g., SATB for Soprano/Alto/Tenor/Bass, SSA for Soprano/Soprano/Alto). | [optional] 
**performanceTime** | **Number** | Performance duration of the asset in seconds. | [optional] 
**difficultyLevelLow** | **Number** | Lower bound of difficulty level on a scale (typically 1-5 or 1-10). | [optional] 
**difficultyLevelHigh** | **Number** | Upper bound of difficulty level on a scale (typically 1-5 or 1-10). | [optional] 
**minQty** | **Number** | Minimum allowed purchase quantity, typically enforced on choral format assets to ensure complete sets are purchased. | [optional] 
**tempo** | **Number** | Tempo of the musical piece in beats per minute (BPM). | [optional] 
**world** | **Boolean** | Indicates if the asset can be sold in all countries (true) or has geographic restrictions (false). | [optional] 
**retailPrice** | **Number** | Hal Leonard&#39;s suggested retail price for the asset in the vendor&#39;s currency. | [optional] 
**smdId** | **String** | SMD (Sheet Music Direct) identifier for the asset. | [optional] 
**assetType** | **String** | Type classification of the asset (e.g., FOLIO for folio editions, CHMBK for chord books, PCK for packs). | [optional] 
**explicit** | **Boolean** | Indicator that denotes whether an asset contains graphic material such as profanity in lyrics. | [optional] 
**partable** | **Boolean** | Indicator that denotes whether an ensemble&#39;s parts may be sold individually. | [optional] 
**countries** | **[String]** | List of ISO 3166-1 alpha-2 country codes where the asset is available for sale. | [optional] 
**instruments** | [**[InstrumentItem]**](InstrumentItem.md) | List of instruments associated with the asset. | [optional] 
**categories** | **[String]** | List of categories that classify the asset (e.g., Pop, Rock, Jazz). | [optional] 
**images** | [**[ImageItem]**](ImageItem.md) | List of images associated with the asset (cover art, sample pages, etc.). | [optional] 
**contributors** | [**[ContributorItem]**](ContributorItem.md) | List of contributors (composers, arrangers, editors, etc.) associated with the asset. | [optional] 
**keywords** | **[String]** | List of keywords associated with the asset for search and discovery. | [optional] 
**relatedGoods** | [**[RelatedGoodItem]**](RelatedGoodItem.md) | List of related goods (physical products, digital bundles, etc.) associated with the asset. | [optional] 
**renderings** | [**[RenderingItem]**](RenderingItem.md) | List of available renderings (formats) for the asset (e.g., PDF, Scorch, MusicXML). | [optional] 
**series** | **[String]** | List of series that the asset belongs to (e.g., Best Sellers, Top Hits collections). | [optional] 
**skills** | **[String]** | List of skill levels or educational classifications associated with the asset. | [optional] 
**usergens** | [**[UsergenItem]**](UsergenItem.md) | List of user-generated content or customization options associated with the asset. | [optional] 
**prices** | [**[PriceItem]**](PriceItem.md) | List of pricing options for the asset in different currencies or for different customer segments. | [optional] 
**packages** | [**[PackageItem]**](PackageItem.md) | List of package deals or bundles that include this asset. | [optional] 


