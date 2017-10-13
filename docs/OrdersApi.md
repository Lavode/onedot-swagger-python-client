# swagger_client.OrdersApi

All URIs are relative to *https://api.wealthport.com/gateway/public/endpoints/1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_order**](OrdersApi.md#create_order) | **POST** /orders | Create Order
[**delete_order**](OrdersApi.md#delete_order) | **DELETE** /orders/{id} | Delete Order
[**get_result**](OrdersApi.md#get_result) | **GET** /jobs/{id}/result | Get Result
[**get_status**](OrdersApi.md#get_status) | **GET** /jobs/{id}/status | Get Status
[**retrieve_order**](OrdersApi.md#retrieve_order) | **GET** /orders/{id} | Retrieve Order
[**retrieve_orders**](OrdersApi.md#retrieve_orders) | **GET** /orders | Retrieve Orders
[**submit_order**](OrdersApi.md#submit_order) | **POST** /orders/{id}/submit | Submit Order
[**update_order**](OrdersApi.md#update_order) | **PUT** /orders/{id} | Update Order


# **create_order**
> str create_order(body=body)

Create Order

Creates a new Order to be submitted.<p>Orders reference one or more Sources, e.g. uploaded files, as well as one or more Folders (which again can contain Sources).The Recipe describes what to do with the referenced sources and where to publish the processing result to.</p>

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
body = swagger_client.OrderRequest() # OrderRequest | JSON (optional)

try: 
    # Create Order
    api_response = api_instance.create_order(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrdersApi->create_order: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**OrderRequest**](OrderRequest.md)| JSON | [optional] 

### Return type

**str**

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_order**
> delete_order(id)

Delete Order

Deletes the specified Order.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
id = 'id_example' # str | Order ID of the order to delete

try: 
    # Delete Order
    api_instance.delete_order(id)
except ApiException as e:
    print("Exception when calling OrdersApi->delete_order: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Order ID of the order to delete | 

### Return type

void (empty response body)

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_result**
> str get_result(id)

Get Result

Returns the result of a finished Job.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
id = 'id_example' # str | Job ID of the job to retrieve its result

try: 
    # Get Result
    api_response = api_instance.get_result(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrdersApi->get_result: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Job ID of the job to retrieve its result | 

### Return type

**str**

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_status**
> str get_status(id)

Get Status

Retrieves the status of a Job.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
id = 'id_example' # str | Job ID of the job to retrieve its status

try: 
    # Get Status
    api_response = api_instance.get_status(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrdersApi->get_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Job ID of the job to retrieve its status | 

### Return type

**str**

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_order**
> ExistingOrder retrieve_order(id)

Retrieve Order

Retrieves the specified Order.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
id = 'id_example' # str | Order ID of the order to retrieve

try: 
    # Retrieve Order
    api_response = api_instance.retrieve_order(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrdersApi->retrieve_order: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Order ID of the order to retrieve | 

### Return type

[**ExistingOrder**](ExistingOrder.md)

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_orders**
> list[ExistingOrder] retrieve_orders()

Retrieve Orders

Retrieves all previously submitted Orders.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()

try: 
    # Retrieve Orders
    api_response = api_instance.retrieve_orders()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OrdersApi->retrieve_orders: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ExistingOrder]**](ExistingOrder.md)

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submit_order**
> submit_order(id)

Submit Order

Submits the specified Order for processing and launches a corresponding job.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
id = 'id_example' # str | Order ID of the order to submit for processing

try: 
    # Submit Order
    api_instance.submit_order(id)
except ApiException as e:
    print("Exception when calling OrdersApi->submit_order: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Order ID of the order to submit for processing | 

### Return type

void (empty response body)

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_order**
> update_order(id, body=body)

Update Order

Updates the specified Order.

### Example 
```python
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'
# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.OrdersApi()
id = 'id_example' # str | Order ID of the order to update
body = swagger_client.OrderRequest() # OrderRequest | JSON (optional)

try: 
    # Update Order
    api_instance.update_order(id, body=body)
except ApiException as e:
    print("Exception when calling OrdersApi->update_order: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Order ID of the order to update | 
 **body** | [**OrderRequest**](OrderRequest.md)| JSON | [optional] 

### Return type

void (empty response body)

### Authorization

[Using URL Query Parameter](../README.md#Using URL Query Parameter), [Using HTTP Header](../README.md#Using HTTP Header)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

