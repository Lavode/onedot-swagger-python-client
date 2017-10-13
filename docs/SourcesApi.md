# swagger_client.SourcesApi

All URIs are relative to *https://api.wealthport.com/gateway/public/endpoints/1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_source**](SourcesApi.md#create_source) | **POST** /sources | Create Source
[**delete_source**](SourcesApi.md#delete_source) | **DELETE** /sources/{id} | Delete Source
[**get_download_url**](SourcesApi.md#get_download_url) | **GET** /sources/{id}/download | Download File
[**get_upload_url**](SourcesApi.md#get_upload_url) | **PUT** /sources/upload | Upload File
[**retrieve_source**](SourcesApi.md#retrieve_source) | **GET** /sources/{id} | Retrieve Source
[**retrieve_sources**](SourcesApi.md#retrieve_sources) | **GET** /sources | Retrieve Sources
[**update_source**](SourcesApi.md#update_source) | **PUT** /sources/{id} | Update Source


# **create_source**
> str create_source(body=body)

Create Source

Creates the specified Source.<p>Sources are either uploaded files or a reference to a database. They are referenced in orders to specify which data needs processing.</p><p>Most clients should probably use the Upload File API which implicitly creates a new source on successful file upload.</p>

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
api_instance = swagger_client.SourcesApi()
body = swagger_client.SourceRequest() # SourceRequest | JSON (optional)

try: 
    # Create Source
    api_response = api_instance.create_source(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SourcesApi->create_source: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SourceRequest**](SourceRequest.md)| JSON | [optional] 

### Return type

**str**

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_source**
> delete_source(id)

Delete Source

Deletes the specified Source.

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
api_instance = swagger_client.SourcesApi()
id = 'id_example' # str | Source ID of the Source to delete

try: 
    # Delete Source
    api_instance.delete_source(id)
except ApiException as e:
    print("Exception when calling SourcesApi->delete_source: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Source ID of the Source to delete | 

### Return type

void (empty response body)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_download_url**
> str get_download_url(id)

Download File

Initiates a file download and returns the URL where to download the file from.<p>Calling this API generates a secure, unique and time-restricted URL where the file can be downloaded from. The URL is available in the <pre>Location</pre> HTTP header of the response. The time restriction of the URL is availablein the <pre>Cache-Control</pre> HTTP header of the response.Clients may perform a <pre>HTTP GET</pre> request on the URL to download the file.</p>

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
api_instance = swagger_client.SourcesApi()
id = 'id_example' # str | Source ID of file to download

try: 
    # Download File
    api_response = api_instance.get_download_url(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SourcesApi->get_download_url: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Source ID of file to download | 

### Return type

**str**

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_upload_url**
> str get_upload_url(name, source=source, folder=folder, content_type=content_type, encoding=encoding)

Upload File

Initiates a file upload and returns the URL where to upload the file to.<p>Calling this API generates a secure, unique and time-restricted URL where the file can be uploaded to. The URL is available in the <pre>Location</pre> HTTP header of the response. The temporal validity of the URL is available in the <pre>Cache-Control</pre> HTTP header of the response.Clients may perform a <pre>HTTP PUT</pre> request on the URL to upload the file using a form where a file <pre>sample.csv</pre> is passed as property <pre>file=sample.csv</pre>. For security reasons, clients must pass all HTTP headers as returned by the <pre>X-WP-Upload-Headers</pre> in the response, together with their values. This procedure ensures a secure, encrypted file upload.</p><p>Note that calling this API automatically generates a Source, there is no need to call the Create Source API.</p>

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
api_instance = swagger_client.SourcesApi()
name = 'name_example' # str | Name of the source to create. The name must correspond to the exact file name of the file being uploaded.
source = 'source_example' # str | Existing source ID to create a new version from (optional)
folder = 'folder_example' # str | Folder ID where to upload source to (optional)
content_type = 'content_type_example' # str | MIME type of the source file (optional)
encoding = 'encoding_example' # str | Encoding of the source file (optional)

try: 
    # Upload File
    api_response = api_instance.get_upload_url(name, source=source, folder=folder, content_type=content_type, encoding=encoding)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SourcesApi->get_upload_url: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| Name of the source to create. The name must correspond to the exact file name of the file being uploaded. | 
 **source** | **str**| Existing source ID to create a new version from | [optional] 
 **folder** | **str**| Folder ID where to upload source to | [optional] 
 **content_type** | **str**| MIME type of the source file | [optional] 
 **encoding** | **str**| Encoding of the source file | [optional] 

### Return type

**str**

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_source**
> ExistingSource retrieve_source(id)

Retrieve Source

Retrieves the specified Source.

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
api_instance = swagger_client.SourcesApi()
id = 'id_example' # str | Source ID of the source to retrieve

try: 
    # Retrieve Source
    api_response = api_instance.retrieve_source(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SourcesApi->retrieve_source: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Source ID of the source to retrieve | 

### Return type

[**ExistingSource**](ExistingSource.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_sources**
> list[ExistingSource] retrieve_sources()

Retrieve Sources

Retrieves all Sources stored in the Data Inventory.

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
api_instance = swagger_client.SourcesApi()

try: 
    # Retrieve Sources
    api_response = api_instance.retrieve_sources()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SourcesApi->retrieve_sources: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ExistingSource]**](ExistingSource.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_source**
> update_source(id, body=body)

Update Source

Updates the specified Source.

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
api_instance = swagger_client.SourcesApi()
id = 'id_example' # str | Source ID of Source to update
body = swagger_client.SourceRequest() # SourceRequest | JSON (optional)

try: 
    # Update Source
    api_instance.update_source(id, body=body)
except ApiException as e:
    print("Exception when calling SourcesApi->update_source: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Source ID of Source to update | 
 **body** | [**SourceRequest**](SourceRequest.md)| JSON | [optional] 

### Return type

void (empty response body)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

