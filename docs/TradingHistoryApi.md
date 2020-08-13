# IO.Swagger.Api.TradingHistoryApi

All URIs are relative to *https://api.hitbtc.com/api/2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**HistoryOrderGet**](TradingHistoryApi.md#historyorderget) | **GET** /history/order | Get historical orders
[**HistoryOrderIdTradesGet**](TradingHistoryApi.md#historyorderidtradesget) | **GET** /history/order/{id}/trades | Get historical trades by specified order
[**HistoryTradesGet**](TradingHistoryApi.md#historytradesget) | **GET** /history/trades | Get historical trades


<a name="historyorderget"></a>
# **HistoryOrderGet**
> List<Order> HistoryOrderGet (string symbol = null, string from = null, string till = null, int? limit = null, int? offset = null, string clientOrderId = null)

Get historical orders

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class HistoryOrderGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingHistoryApi();
            var symbol = symbol_example;  // string |  (optional) 
            var from = from_example;  // string | Datetime in iso format or timestamp in millisecond. (optional) 
            var till = till_example;  // string | Datetime in iso format or timestamp in millisecond. (optional) 
            var limit = 56;  // int? |  (optional)  (default to 100)
            var offset = 56;  // int? |  (optional) 
            var clientOrderId = clientOrderId_example;  // string |  (optional) 

            try
            {
                // Get historical orders
                List&lt;Order&gt; result = apiInstance.HistoryOrderGet(symbol, from, till, limit, offset, clientOrderId);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingHistoryApi.HistoryOrderGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | [optional] 
 **from** | **string**| Datetime in iso format or timestamp in millisecond. | [optional] 
 **till** | **string**| Datetime in iso format or timestamp in millisecond. | [optional] 
 **limit** | **int?**|  | [optional] [default to 100]
 **offset** | **int?**|  | [optional] 
 **clientOrderId** | **string**|  | [optional] 

### Return type

[**List<Order>**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="historyorderidtradesget"></a>
# **HistoryOrderIdTradesGet**
> List<Trade> HistoryOrderIdTradesGet (int? id)

Get historical trades by specified order

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class HistoryOrderIdTradesGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingHistoryApi();
            var id = 56;  // int? | 

            try
            {
                // Get historical trades by specified order
                List&lt;Trade&gt; result = apiInstance.HistoryOrderIdTradesGet(id);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingHistoryApi.HistoryOrderIdTradesGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int?**|  | 

### Return type

[**List<Trade>**](Trade.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="historytradesget"></a>
# **HistoryTradesGet**
> List<Trade> HistoryTradesGet (string symbol = null, string sort = null, string by = null, string from = null, string till = null, int? limit = null, int? offset = null)

Get historical trades

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class HistoryTradesGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingHistoryApi();
            var symbol = symbol_example;  // string |  (optional) 
            var sort = sort_example;  // string | Sort direction (optional)  (default to DESC)
            var by = by_example;  // string | Filter field (optional)  (default to timestamp)
            var from = from_example;  // string | If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id (optional) 
            var till = till_example;  // string | If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id (optional) 
            var limit = 56;  // int? |  (optional)  (default to 100)
            var offset = 56;  // int? |  (optional) 

            try
            {
                // Get historical trades
                List&lt;Trade&gt; result = apiInstance.HistoryTradesGet(symbol, sort, by, from, till, limit, offset);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingHistoryApi.HistoryTradesGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | [optional] 
 **sort** | **string**| Sort direction | [optional] [default to DESC]
 **by** | **string**| Filter field | [optional] [default to timestamp]
 **from** | **string**| If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id | [optional] 
 **till** | **string**| If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id | [optional] 
 **limit** | **int?**|  | [optional] [default to 100]
 **offset** | **int?**|  | [optional] 

### Return type

[**List<Trade>**](Trade.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

