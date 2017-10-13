# swagger_client.FoldersApi

All URIs are relative to *https://api.wealthport.com/gateway/public/endpoints/1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_folder**](FoldersApi.md#create_folder) | **POST** /folders | Create Folder
[**delete_folder**](FoldersApi.md#delete_folder) | **DELETE** /folders/{id} | Delete Folder
[**delete_folder_sources**](FoldersApi.md#delete_folder_sources) | **DELETE** /folders/{id}/sources | Delete Sources
[**retrieve_folder**](FoldersApi.md#retrieve_folder) | **GET** /folders/{id} | Retrieve Folder
[**retrieve_folder_sources**](FoldersApi.md#retrieve_folder_sources) | **GET** /folders/{id}/sources | Retrieve Sources
[**retrieve_folders**](FoldersApi.md#retrieve_folders) | **GET** /folders | Retrieve Folders
[**update_folder**](FoldersApi.md#update_folder) | **PUT** /folders/{id} | Update Folder


# **create_folder**
> str create_folder(body=body)

Create Folder

Creates the specified Folder in the Data Inventory.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()
body = swagger_client.FolderRequest() # FolderRequest | JSON (optional)

try: 
    # Create Folder
    api_response = api_instance.create_folder(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->create_folder: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**FolderRequest**](FolderRequest.md)| JSON | [optional] 

### Return type

**str**

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_folder**
> delete_folder(id)

Delete Folder

Deletes the specified Folder and all contained Sources from the Data Inventory.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()
id = 'id_example' # str | Folder ID of the Folder to delete, including any Sources contained

try: 
    # Delete Folder
    api_instance.delete_folder(id)
except ApiException as e:
    print("Exception when calling FoldersApi->delete_folder: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Folder ID of the Folder to delete, including any Sources contained | 

### Return type

void (empty response body)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_folder_sources**
> delete_folder_sources(id)

Delete Sources

Deletes all Sources in the specified Folder.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()
id = 'id_example' # str | Folder ID of the Folder to delete all Sources from

try: 
    # Delete Sources
    api_instance.delete_folder_sources(id)
except ApiException as e:
    print("Exception when calling FoldersApi->delete_folder_sources: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Folder ID of the Folder to delete all Sources from | 

### Return type

void (empty response body)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_folder**
> ExistingFolder retrieve_folder(id)

Retrieve Folder

Retrieves the specified Folder.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()
id = 'id_example' # str | Folder ID of the Folder to retrieve

try: 
    # Retrieve Folder
    api_response = api_instance.retrieve_folder(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->retrieve_folder: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Folder ID of the Folder to retrieve | 

### Return type

[**ExistingFolder**](ExistingFolder.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_folder_sources**
> ExistingSource retrieve_folder_sources(id)

Retrieve Sources

Retrieves all Sources of the specified Folder.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()
id = 'id_example' # str | Folder ID of the Folder to retrieve its Sources from

try: 
    # Retrieve Sources
    api_response = api_instance.retrieve_folder_sources(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->retrieve_folder_sources: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Folder ID of the Folder to retrieve its Sources from | 

### Return type

[**ExistingSource**](ExistingSource.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_folders**
> list[ExistingFolder] retrieve_folders()

Retrieve Folders

Retrieves all Folders in the Data Inventory.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()

try: 
    # Retrieve Folders
    api_response = api_instance.retrieve_folders()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FoldersApi->retrieve_folders: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ExistingFolder]**](ExistingFolder.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_folder**
> update_folder(id, body=body)

Update Folder

Updates the specified Folder.

### Example 
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Using HTTP Header
swagger_client.configuration.api_key['X-API-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['X-API-Key'] = 'Bearer'
# Configure API key authorization: Using URL Query Parameter
swagger_client.configuration.api_key['apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# swagger_client.configuration.api_key_prefix['apikey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.FoldersApi()
id = 'id_example' # str | Folder ID of the Folder to update
body = swagger_client.FolderRequest() # FolderRequest | JSON (optional)

try: 
    # Update Folder
    api_instance.update_folder(id, body=body)
except ApiException as e:
    print("Exception when calling FoldersApi->update_folder: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Folder ID of the Folder to update | 
 **body** | [**FolderRequest**](FolderRequest.md)| JSON | [optional] 

### Return type

void (empty response body)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

