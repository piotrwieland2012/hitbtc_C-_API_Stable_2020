# IO.Swagger.Api.AccountApi

All URIs are relative to *https://api.hitbtc.com/api/2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AccountBalanceGet**](AccountApi.md#accountbalanceget) | **GET** /account/balance | Get main acccount balance
[**AccountCryptoAddressCurrencyGet**](AccountApi.md#accountcryptoaddresscurrencyget) | **GET** /account/crypto/address/{currency} | Get deposit crypro address
[**AccountCryptoAddressCurrencyPost**](AccountApi.md#accountcryptoaddresscurrencypost) | **POST** /account/crypto/address/{currency} | Create new deposit crypro address
[**AccountCryptoWithdrawIdDelete**](AccountApi.md#accountcryptowithdrawiddelete) | **DELETE** /account/crypto/withdraw/{id} | Rollback withdraw crypro
[**AccountCryptoWithdrawIdPut**](AccountApi.md#accountcryptowithdrawidput) | **PUT** /account/crypto/withdraw/{id} | Commit withdraw crypro
[**AccountCryptoWithdrawPost**](AccountApi.md#accountcryptowithdrawpost) | **POST** /account/crypto/withdraw | Withdraw crypro
[**AccountTransactionsGet**](AccountApi.md#accounttransactionsget) | **GET** /account/transactions | Get account transactions
[**AccountTransactionsIdGet**](AccountApi.md#accounttransactionsidget) | **GET** /account/transactions/{id} | Get account transaction by id
[**AccountTransferPost**](AccountApi.md#accounttransferpost) | **POST** /account/transfer | Transfer amount to trading


<a name="accountbalanceget"></a>
# **AccountBalanceGet**
> List<Balance> AccountBalanceGet ()

Get main acccount balance

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountBalanceGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();

            try
            {
                // Get main acccount balance
                List&lt;Balance&gt; result = apiInstance.AccountBalanceGet();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountBalanceGet: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List<Balance>**](Balance.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accountcryptoaddresscurrencyget"></a>
# **AccountCryptoAddressCurrencyGet**
> Address AccountCryptoAddressCurrencyGet (string currency)

Get deposit crypro address

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountCryptoAddressCurrencyGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var currency = currency_example;  // string | 

            try
            {
                // Get deposit crypro address
                Address result = apiInstance.AccountCryptoAddressCurrencyGet(currency);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountCryptoAddressCurrencyGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **currency** | **string**|  | 

### Return type

[**Address**](Address.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accountcryptoaddresscurrencypost"></a>
# **AccountCryptoAddressCurrencyPost**
> Address AccountCryptoAddressCurrencyPost (string currency)

Create new deposit crypro address

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountCryptoAddressCurrencyPostExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var currency = currency_example;  // string | 

            try
            {
                // Create new deposit crypro address
                Address result = apiInstance.AccountCryptoAddressCurrencyPost(currency);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountCryptoAddressCurrencyPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **currency** | **string**|  | 

### Return type

[**Address**](Address.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accountcryptowithdrawiddelete"></a>
# **AccountCryptoWithdrawIdDelete**
> WithdrawConfirm AccountCryptoWithdrawIdDelete (string id)

Rollback withdraw crypro

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountCryptoWithdrawIdDeleteExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var id = id_example;  // string | 

            try
            {
                // Rollback withdraw crypro
                WithdrawConfirm result = apiInstance.AccountCryptoWithdrawIdDelete(id);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountCryptoWithdrawIdDelete: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**WithdrawConfirm**](WithdrawConfirm.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accountcryptowithdrawidput"></a>
# **AccountCryptoWithdrawIdPut**
> WithdrawConfirm AccountCryptoWithdrawIdPut (string id)

Commit withdraw crypro

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountCryptoWithdrawIdPutExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var id = id_example;  // string | 

            try
            {
                // Commit withdraw crypro
                WithdrawConfirm result = apiInstance.AccountCryptoWithdrawIdPut(id);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountCryptoWithdrawIdPut: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**WithdrawConfirm**](WithdrawConfirm.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accountcryptowithdrawpost"></a>
# **AccountCryptoWithdrawPost**
> void AccountCryptoWithdrawPost (string currency, string amount, string address, string paymentId = null, string networkFee = null, bool? includeFee = null, bool? autoCommit = null)

Withdraw crypro

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountCryptoWithdrawPostExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var currency = currency_example;  // string | 
            var amount = amount_example;  // string | 
            var address = address_example;  // string | 
            var paymentId = paymentId_example;  // string |  (optional) 
            var networkFee = networkFee_example;  // string | Suggest preferred network fee. (optional) 
            var includeFee = true;  // bool? | If enabled, then fee will be subtracted from amount. (optional)  (default to false)
            var autoCommit = true;  // bool? | If (optional)  (default to true)

            try
            {
                // Withdraw crypro
                apiInstance.AccountCryptoWithdrawPost(currency, amount, address, paymentId, networkFee, includeFee, autoCommit);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountCryptoWithdrawPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **currency** | **string**|  | 
 **amount** | **string**|  | 
 **address** | **string**|  | 
 **paymentId** | **string**|  | [optional] 
 **networkFee** | **string**| Suggest preferred network fee. | [optional] 
 **includeFee** | **bool?**| If enabled, then fee will be subtracted from amount. | [optional] [default to false]
 **autoCommit** | **bool?**| If | [optional] [default to true]

### Return type

void (empty response body)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accounttransactionsget"></a>
# **AccountTransactionsGet**
> List<Transaction> AccountTransactionsGet (string currency = null, string sort = null, string by = null, string from = null, string till = null, int? limit = null, int? offset = null)

Get account transactions

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountTransactionsGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var currency = currency_example;  // string |  (optional) 
            var sort = sort_example;  // string | Sort direction (optional)  (default to DESC)
            var by = by_example;  // string | Filter field (optional)  (default to timestamp)
            var from = from_example;  // string | Datetime in iso format or timestamp in millisecond, or index. (optional) 
            var till = till_example;  // string | Datetime in iso format or timestamp in millisecond, or index. (optional) 
            var limit = 56;  // int? |  (optional)  (default to 100)
            var offset = 56;  // int? |  (optional) 

            try
            {
                // Get account transactions
                List&lt;Transaction&gt; result = apiInstance.AccountTransactionsGet(currency, sort, by, from, till, limit, offset);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountTransactionsGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **currency** | **string**|  | [optional] 
 **sort** | **string**| Sort direction | [optional] [default to DESC]
 **by** | **string**| Filter field | [optional] [default to timestamp]
 **from** | **string**| Datetime in iso format or timestamp in millisecond, or index. | [optional] 
 **till** | **string**| Datetime in iso format or timestamp in millisecond, or index. | [optional] 
 **limit** | **int?**|  | [optional] [default to 100]
 **offset** | **int?**|  | [optional] 

### Return type

[**List<Transaction>**](Transaction.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accounttransactionsidget"></a>
# **AccountTransactionsIdGet**
> Transaction AccountTransactionsIdGet (string id)

Get account transaction by id

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountTransactionsIdGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var id = id_example;  // string | 

            try
            {
                // Get account transaction by id
                Transaction result = apiInstance.AccountTransactionsIdGet(id);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountTransactionsIdGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Transaction**](Transaction.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="accounttransferpost"></a>
# **AccountTransferPost**
> InlineResponse400 AccountTransferPost (string currency, string amount, string type)

Transfer amount to trading

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AccountTransferPostExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new AccountApi();
            var currency = currency_example;  // string | 
            var amount = amount_example;  // string | 
            var type = type_example;  // string | 

            try
            {
                // Transfer amount to trading
                InlineResponse400 result = apiInstance.AccountTransferPost(currency, amount, type);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccountApi.AccountTransferPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **currency** | **string**|  | 
 **amount** | **string**|  | 
 **type** | **string**|  | 

### Return type

[**InlineResponse400**](InlineResponse400.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

