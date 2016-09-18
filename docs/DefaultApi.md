# AxxellApi.DefaultApi

All URIs are relative to *https://axxell.cinaq.com/v1/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aggregateCountEvents**](DefaultApi.md#aggregateCountEvents) | **GET** /aggregates/countevents/{eventType} | 
[**aggregateEffective**](DefaultApi.md#aggregateEffective) | **GET** /aggregates/effective/{eventType} | 
[**aggregateEvents**](DefaultApi.md#aggregateEvents) | **GET** /aggregates/events/{eventType} | 
[**aggregateRecent**](DefaultApi.md#aggregateRecent) | **GET** /aggregates/recent/{eventType} | 
[**aggregateTop**](DefaultApi.md#aggregateTop) | **GET** /aggregates/top/{eventType} | 
[**authStore**](DefaultApi.md#authStore) | **POST** /auth | 
[**deleteAllEvents**](DefaultApi.md#deleteAllEvents) | **DELETE** /events | 
[**deleteAllItems**](DefaultApi.md#deleteAllItems) | **DELETE** /items | 
[**deleteItem**](DefaultApi.md#deleteItem) | **DELETE** /items/{itemid} | 
[**recommendInteresting**](DefaultApi.md#recommendInteresting) | **GET** /recommendations/interesting | 
[**recommendSimilar**](DefaultApi.md#recommendSimilar) | **GET** /recommendations/similar | 
[**registerEvent**](DefaultApi.md#registerEvent) | **POST** /events | 
[**registerItem**](DefaultApi.md#registerItem) | **POST** /items | 
[**registerStore**](DefaultApi.md#registerStore) | **POST** /store | 
[**retrieveEvents**](DefaultApi.md#retrieveEvents) | **GET** /events | 
[**retrieveItems**](DefaultApi.md#retrieveItems) | **GET** /items | 


<a name="aggregateCountEvents"></a>
# **aggregateCountEvents**
> DataPoint aggregateCountEvents(storeid, eventTypedataPeriod)



Return list of counts per event

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var eventType = "eventType_example"; // String | Valid values purchase, view or recommend

var dataPeriod = "dataPeriod_example"; // String | Valid values are last7days, last30days, today, yesterday


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.aggregateCountEvents(storeid, eventTypedataPeriod, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **eventType** | **String**| Valid values purchase, view or recommend | 
 **dataPeriod** | **String**| Valid values are last7days, last30days, today, yesterday | 

### Return type

[**DataPoint**](DataPoint.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="aggregateEffective"></a>
# **aggregateEffective**
> [DataPoint] aggregateEffective(storeid, eventType)



Return list of aggregated data points correlated with recommendationa and eventType

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var eventType = "eventType_example"; // String | Valid values purchase, view or recommend


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.aggregateEffective(storeid, eventType, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **eventType** | **String**| Valid values purchase, view or recommend | 

### Return type

[**[DataPoint]**](DataPoint.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="aggregateEvents"></a>
# **aggregateEvents**
> [DataPoint] aggregateEvents(storeid, eventType)



Return list of aggregated data points

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var eventType = "eventType_example"; // String | Valid values purchase, view or recommend


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.aggregateEvents(storeid, eventType, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **eventType** | **String**| Valid values purchase, view or recommend | 

### Return type

[**[DataPoint]**](DataPoint.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="aggregateRecent"></a>
# **aggregateRecent**
> [Item] aggregateRecent(storeid, eventType)



Returns recent products

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var eventType = "eventType_example"; // String | Valid values purchase, view or recommend


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.aggregateRecent(storeid, eventType, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **eventType** | **String**| Valid values purchase, view or recommend | 

### Return type

[**[Item]**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="aggregateTop"></a>
# **aggregateTop**
> [Item] aggregateTop(storeid, eventType)



Returns top products

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var eventType = "eventType_example"; // String | Valid values purchase, view or recommend


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.aggregateTop(storeid, eventType, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **eventType** | **String**| Valid values purchase, view or recommend | 

### Return type

[**[Item]**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="authStore"></a>
# **authStore**
> Store authStore(store)



Retrieve authentication token using password

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var store = new AxxellApi.Store(); // Store | Store


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.authStore(store, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store** | [**Store**](Store.md)| Store | 

### Return type

[**Store**](Store.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteAllEvents"></a>
# **deleteAllEvents**
> Event deleteAllEvents(storeid)



Delete all events

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.deleteAllEvents(storeid, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 

### Return type

[**Event**](Event.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteAllItems"></a>
# **deleteAllItems**
> Item deleteAllItems(storeid)



Delete all items

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.deleteAllItems(storeid, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 

### Return type

[**Item**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteItem"></a>
# **deleteItem**
> Item deleteItem(storeid, itemid)



Delete existing item

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var itemid = "itemid_example"; // String | Item identifier


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.deleteItem(storeid, itemid, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **itemid** | **String**| Item identifier | 

### Return type

[**Item**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="recommendInteresting"></a>
# **recommendInteresting**
> [Item] recommendInteresting(storeid, userid, opts)



Return list of recommended items

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var userid = "userid_example"; // String | Interesting items for visitor

var opts = { 
  'count': 1.2 // Number | Return exactly this amount of suggestions. Maximum value is 50, default is 5.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.recommendInteresting(storeid, userid, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **userid** | **String**| Interesting items for visitor | 
 **count** | **Number**| Return exactly this amount of suggestions. Maximum value is 50, default is 5. | [optional] 

### Return type

[**[Item]**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="recommendSimilar"></a>
# **recommendSimilar**
> [Item] recommendSimilar(storeid, userid, itemid, opts)



Return list of recommended items

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var userid = "userid_example"; // String | User requesting the recommendation

var itemid = "itemid_example"; // String | Similar items bought by others

var opts = { 
  'count': 1.2 // Number | Return exactly this amount of suggestions. Maximum value is 50, default is 5.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.recommendSimilar(storeid, userid, itemid, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **userid** | **String**| User requesting the recommendation | 
 **itemid** | **String**| Similar items bought by others | 
 **count** | **Number**| Return exactly this amount of suggestions. Maximum value is 50, default is 5. | [optional] 

### Return type

[**[Item]**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="registerEvent"></a>
# **registerEvent**
> Event registerEvent(storeid, event)



Register new event

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var event = new AxxellApi.Event(); // Event | Single event to register


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.registerEvent(storeid, event, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **event** | [**Event**](Event.md)| Single event to register | 

### Return type

[**Event**](Event.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="registerItem"></a>
# **registerItem**
> Item registerItem(storeid, item)



Register new item

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier

var item = new AxxellApi.Item(); // Item | Single item to register


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.registerItem(storeid, item, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 
 **item** | [**Item**](Item.md)| Single item to register | 

### Return type

[**Item**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="registerStore"></a>
# **registerStore**
> Store registerStore(store)



Register new Store

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var store = new AxxellApi.Store(); // Store | Store


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.registerStore(store, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store** | [**Store**](Store.md)| Store | 

### Return type

[**Store**](Store.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="retrieveEvents"></a>
# **retrieveEvents**
> [Event] retrieveEvents(storeid)



Get recent events

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.retrieveEvents(storeid, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 

### Return type

[**[Event]**](Event.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="retrieveItems"></a>
# **retrieveItems**
> [Item] retrieveItems(storeid)



Get recent items

### Example
```javascript
var AxxellApi = require('axxell_api');
var defaultClient = AxxellApi.ApiClient.default;

// Configure API key authorization: ApiKey
var ApiKey = defaultClient.authentications['ApiKey'];
ApiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//ApiKey.apiKeyPrefix = 'Token';

var apiInstance = new AxxellApi.DefaultApi();

var storeid = "storeid_example"; // String | Store identifier


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.retrieveItems(storeid, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storeid** | **String**| Store identifier | 

### Return type

[**[Item]**](Item.md)

### Authorization

[ApiKey](../README.md#ApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

