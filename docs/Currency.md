# IO.Swagger.Model.Currency
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Currency code | 
**FullName** | **string** |  | 
**Crypto** | **bool?** | True for cryptocurrencies, false for fiat, ICO and others. | 
**PayinEnabled** | **bool?** | True if cryptocurrency support generate adress or paymentId for deposits | 
**PayinPaymentId** | **bool?** | True if cryptocurrency requred use paymentId for deposits | 
**PayinConfirmations** | **int?** | Confirmations count for cryptocurrency deposits | 
**PayoutEnabled** | **bool?** |  | 
**PayoutFee** | **string** | Default withdraw fee | 
**PayoutIsPaymentId** | **bool?** | True if cryptocurrency allow use paymentId for withdraw | 
**Delisted** | **bool?** | True if currency delisted (stopped deposit and trading) | 
**TransferEnabled** | **bool?** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

