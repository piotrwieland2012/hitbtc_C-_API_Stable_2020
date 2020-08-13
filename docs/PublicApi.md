# IO.Swagger.Api.PublicApi

All URIs are relative to *https://api.hitbtc.com/api/2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**PublicCandlesSymbolGet**](PublicApi.md#publiccandlessymbolget) | **GET** /public/candles/{symbol} | Candles
[**PublicCurrencyCurrencyGet**](PublicApi.md#publiccurrencycurrencyget) | **GET** /public/currency/{currency} | Get currency info
[**PublicCurrencyGet**](PublicApi.md#publiccurrencyget) | **GET** /public/currency | Available Currencies
[**PublicOrderbookSymbolGet**](PublicApi.md#publicorderbooksymbolget) | **GET** /public/orderbook/{symbol} | Orderbook
[**PublicSymbolGet**](PublicApi.md#publicsymbolget) | **GET** /public/symbol | Available Currency Symbols
[**PublicSymbolSymbolGet**](PublicApi.md#publicsymbolsymbolget) | **GET** /public/symbol/{symbol} | Get symbol info
[**PublicTickerGet**](PublicApi.md#publictickerget) | **GET** /public/ticker | Ticker list for all symbols
[**PublicTickerSymbolGet**](PublicApi.md#publictickersymbolget) | **GET** /public/ticker/{symbol} | Ticker for symbol
[**PublicTradesSymbolGet**](PublicApi.md#publictradessymbolget) | **GET** /public/trades/{symbol} | Trades


<a name="publiccandlessymbolget"></a>
# **PublicCandlesSymbolGet**
> List<Candle> PublicCandlesSymbolGet (string symbol, int? limit = null, string period = null)

Candles

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicCandlesSymbolGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();
            var symbol = symbol_example;  // string | 
            var limit = 56;  // int? |  (optional)  (default to 100)
            var period = period_example;  // string |  (optional)  (default to M30)

            try
            {
                // Candles
                List&lt;Candle&gt; result = apiInstance.PublicCandlesSymbolGet(symbol, limit, period);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicCandlesSymbolGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | 
 **limit** | **int?**|  | [optional] [default to 100]
 **period** | **string**|  | [optional] [default to M30]

### Return type

[**List<Candle>**](Candle.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publiccurrencycurrencyget"></a>
# **PublicCurrencyCurrencyGet**
> Currency PublicCurrencyCurrencyGet (string currency)

Get currency info

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicCurrencyCurrencyGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();
            var currency = currency_example;  // string | 

            try
            {
                // Get currency info
                Currency result = apiInstance.PublicCurrencyCurrencyGet(currency);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicCurrencyCurrencyGet: " + e.Message );
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

[**Currency**](Currency.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publiccurrencyget"></a>
# **PublicCurrencyGet**
> List<Currency> PublicCurrencyGet ()

Available Currencies

Get list of avialable Symbols (Currency Pairs). You can read more info at http://www.investopedia.com/terms/c/currencypair.asp 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicCurrencyGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();

            try
            {
                // Available Currencies
                List&lt;Currency&gt; result = apiInstance.PublicCurrencyGet();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicCurrencyGet: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List<Currency>**](Currency.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publicorderbooksymbolget"></a>
# **PublicOrderbookSymbolGet**
> Orderbook PublicOrderbookSymbolGet (string symbol, int? limit = null)

Orderbook

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicOrderbookSymbolGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();
            var symbol = symbol_example;  // string | 
            var limit = 56;  // int? | 0 - full orderbook otherwise number of levels (optional)  (default to 100)

            try
            {
                // Orderbook
                Orderbook result = apiInstance.PublicOrderbookSymbolGet(symbol, limit);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicOrderbookSymbolGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | 
 **limit** | **int?**| 0 - full orderbook otherwise number of levels | [optional] [default to 100]

### Return type

[**Orderbook**](Orderbook.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publicsymbolget"></a>
# **PublicSymbolGet**
> List<Symbol> PublicSymbolGet ()

Available Currency Symbols

Get list of avialable Symbols (Currency Pairs). You can read more info at http://www.investopedia.com/terms/c/currencypair.asp 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicSymbolGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();

            try
            {
                // Available Currency Symbols
                List&lt;Symbol&gt; result = apiInstance.PublicSymbolGet();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicSymbolGet: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List<Symbol>**](Symbol.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publicsymbolsymbolget"></a>
# **PublicSymbolSymbolGet**
> Symbol PublicSymbolSymbolGet (string symbol)

Get symbol info

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicSymbolSymbolGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();
            var symbol = symbol_example;  // string | 

            try
            {
                // Get symbol info
                Symbol result = apiInstance.PublicSymbolSymbolGet(symbol);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicSymbolSymbolGet: " + e.Message );
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

[**Symbol**](Symbol.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publictickerget"></a>
# **PublicTickerGet**
> List<Ticker> PublicTickerGet ()

Ticker list for all symbols

The Ticker endpoint returns last 24H information about of all symbol. 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicTickerGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();

            try
            {
                // Ticker list for all symbols
                List&lt;Ticker&gt; result = apiInstance.PublicTickerGet();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicTickerGet: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List<Ticker>**](Ticker.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publictickersymbolget"></a>
# **PublicTickerSymbolGet**
> Ticker PublicTickerSymbolGet (string symbol)

Ticker for symbol

The Ticker endpoint returns last 24H information about symbol. 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicTickerSymbolGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();
            var symbol = symbol_example;  // string | 

            try
            {
                // Ticker for symbol
                Ticker result = apiInstance.PublicTickerSymbolGet(symbol);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicTickerSymbolGet: " + e.Message );
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

[**Ticker**](Ticker.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="publictradessymbolget"></a>
# **PublicTradesSymbolGet**
> List<PublicTrade> PublicTradesSymbolGet (string symbol, string sort = null, string by = null, string from = null, string till = null, int? limit = null, int? offset = null)

Trades

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PublicTradesSymbolGetExample
    {
        public void main()
        {
            var apiInstance = new PublicApi();
            var symbol = symbol_example;  // string | 
            var sort = sort_example;  // string | Sort direction (optional)  (default to DESC)
            var by = by_example;  // string | Filter field (optional)  (default to timestamp)
            var from = from_example;  // string | If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id (optional) 
            var till = till_example;  // string | If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id (optional) 
            var limit = 56;  // int? |  (optional)  (default to 100)
            var offset = 56;  // int? |  (optional) 

            try
            {
                // Trades
                List&lt;PublicTrade&gt; result = apiInstance.PublicTradesSymbolGet(symbol, sort, by, from, till, limit, offset);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PublicApi.PublicTradesSymbolGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **symbol** | **string**|  | 
 **sort** | **string**| Sort direction | [optional] [default to DESC]
 **by** | **string**| Filter field | [optional] [default to timestamp]
 **from** | **string**| If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id | [optional] 
 **till** | **string**| If filter by timestamp, then datetime in iso format or timestamp in millisecond otherwise trade id | [optional] 
 **limit** | **int?**|  | [optional] [default to 100]
 **offset** | **int?**|  | [optional] 

### Return type

[**List<PublicTrade>**](PublicTrade.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

