# IO.Swagger.Api.TradingApi

All URIs are relative to *https://api.hitbtc.com/api/2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**OrderClientOrderIdDelete**](TradingApi.md#orderclientorderiddelete) | **DELETE** /order/{clientOrderId} | Cancel order
[**OrderClientOrderIdGet**](TradingApi.md#orderclientorderidget) | **GET** /order/{clientOrderId} | Get a single order by clientOrderId
[**OrderClientOrderIdPatch**](TradingApi.md#orderclientorderidpatch) | **PATCH** /order/{clientOrderId} | Cancel Replace order
[**OrderClientOrderIdPut**](TradingApi.md#orderclientorderidput) | **PUT** /order/{clientOrderId} | Create new order
[**OrderDelete**](TradingApi.md#orderdelete) | **DELETE** /order | Cancel all open orders
[**OrderGet**](TradingApi.md#orderget) | **GET** /order | List your current open orders
[**OrderPost**](TradingApi.md#orderpost) | **POST** /order | Create new order
[**TradingBalanceGet**](TradingApi.md#tradingbalanceget) | **GET** /trading/balance | Get trading balance
[**TradingFeeSymbolGet**](TradingApi.md#tradingfeesymbolget) | **GET** /trading/fee/{symbol} | Get trading fee rate


<a name="orderclientorderiddelete"></a>
# **OrderClientOrderIdDelete**
> Order OrderClientOrderIdDelete (string clientOrderId)

Cancel order

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderClientOrderIdDeleteExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var clientOrderId = clientOrderId_example;  // string | 

            try
            {
                // Cancel order
                Order result = apiInstance.OrderClientOrderIdDelete(clientOrderId);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderClientOrderIdDelete: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientOrderId** | **string**|  | 

### Return type

[**Order**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="orderclientorderidget"></a>
# **OrderClientOrderIdGet**
> Order OrderClientOrderIdGet (string clientOrderId, int? wait = null)

Get a single order by clientOrderId

The Ticker endpoint returns last 24H information about symbols. 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderClientOrderIdGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var clientOrderId = clientOrderId_example;  // string | 
            var wait = 56;  // int? | Long polling wait timeout in milliseconds. Max 60000. (optional) 

            try
            {
                // Get a single order by clientOrderId
                Order result = apiInstance.OrderClientOrderIdGet(clientOrderId, wait);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderClientOrderIdGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientOrderId** | **string**|  | 
 **wait** | **int?**| Long polling wait timeout in milliseconds. Max 60000. | [optional] 

### Return type

[**Order**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="orderclientorderidpatch"></a>
# **OrderClientOrderIdPatch**
> Order OrderClientOrderIdPatch (string clientOrderId, string quantity, string requestClientId, string price = null)

Cancel Replace order

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderClientOrderIdPatchExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var clientOrderId = clientOrderId_example;  // string | 
            var quantity = quantity_example;  // string | 
            var requestClientId = requestClientId_example;  // string | 
            var price = price_example;  // string |  (optional) 

            try
            {
                // Cancel Replace order
                Order result = apiInstance.OrderClientOrderIdPatch(clientOrderId, quantity, requestClientId, price);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderClientOrderIdPatch: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientOrderId** | **string**|  | 
 **quantity** | **string**|  | 
 **requestClientId** | **string**|  | 
 **price** | **string**|  | [optional] 

### Return type

[**Order**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="orderclientorderidput"></a>
# **OrderClientOrderIdPut**
> Order OrderClientOrderIdPut (string clientOrderId, string symbol, string side, string timeInForce, string quantity, string type = null, string price = null, string stopPrice = null, DateTime? expireTime = null, bool? strictValidate = null)

Create new order

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderClientOrderIdPutExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var clientOrderId = clientOrderId_example;  // string | 
            var symbol = symbol_example;  // string | 
            var side = side_example;  // string |  (default to sell)
            var timeInForce = timeInForce_example;  // string |  (default to GTC)
            var quantity = quantity_example;  // string | 
            var type = type_example;  // string |  (optional)  (default to limit)
            var price = price_example;  // string |  (optional) 
            var stopPrice = stopPrice_example;  // string |  (optional) 
            var expireTime = 2013-10-20T19:20:30+01:00;  // DateTime? |  (optional) 
            var strictValidate = true;  // bool? | Strict validate amount and price precision without rounding (optional)  (default to false)

            try
            {
                // Create new order
                Order result = apiInstance.OrderClientOrderIdPut(clientOrderId, symbol, side, timeInForce, quantity, type, price, stopPrice, expireTime, strictValidate);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderClientOrderIdPut: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientOrderId** | **string**|  | 
 **symbol** | **string**|  | 
 **side** | **string**|  | [default to sell]
 **timeInForce** | **string**|  | [default to GTC]
 **quantity** | **string**|  | 
 **type** | **string**|  | [optional] [default to limit]
 **price** | **string**|  | [optional] 
 **stopPrice** | **string**|  | [optional] 
 **expireTime** | **DateTime?**|  | [optional] 
 **strictValidate** | **bool?**| Strict validate amount and price precision without rounding | [optional] [default to false]

### Return type

[**Order**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="orderdelete"></a>
# **OrderDelete**
> List<Order> OrderDelete (string symbol = null)

Cancel all open orders

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderDeleteExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var symbol = symbol_example;  // string |  (optional) 

            try
            {
                // Cancel all open orders
                List&lt;Order&gt; result = apiInstance.OrderDelete(symbol);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderDelete: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | [optional] 

### Return type

[**List<Order>**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="orderget"></a>
# **OrderGet**
> List<Order> OrderGet (string symbol = null)

List your current open orders

List of your currently open orders.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var symbol = symbol_example;  // string |  (optional) 

            try
            {
                // List your current open orders
                List&lt;Order&gt; result = apiInstance.OrderGet(symbol);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | [optional] 

### Return type

[**List<Order>**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="orderpost"></a>
# **OrderPost**
> Order OrderPost (OrderCommand _event = null)

Create new order

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class OrderPostExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var _event = new OrderCommand(); // OrderCommand | Open order request (optional) 

            try
            {
                // Create new order
                Order result = apiInstance.OrderPost(_event);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.OrderPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **_event** | [**OrderCommand**](OrderCommand.md)| Open order request | [optional] 

### Return type

[**Order**](Order.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="tradingbalanceget"></a>
# **TradingBalanceGet**
> List<Balance> TradingBalanceGet ()

Get trading balance

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class TradingBalanceGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();

            try
            {
                // Get trading balance
                List&lt;Balance&gt; result = apiInstance.TradingBalanceGet();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.TradingBalanceGet: " + e.Message );
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

<a name="tradingfeesymbolget"></a>
# **TradingFeeSymbolGet**
> TradingFee TradingFeeSymbolGet (string symbol)

Get trading fee rate

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class TradingFeeSymbolGetExample
    {
        public void main()
        {
            // Configure HTTP basic authorization: BasicAuth
            Configuration.Default.Username = "YOUR_USERNAME";
            Configuration.Default.Password = "YOUR_PASSWORD";

            var apiInstance = new TradingApi();
            var symbol = symbol_example;  // string | 

            try
            {
                // Get trading fee rate
                TradingFee result = apiInstance.TradingFeeSymbolGet(symbol);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TradingApi.TradingFeeSymbolGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | 

### Return type

[**TradingFee**](TradingFee.md)

### Authorization

[BasicAuth](../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

