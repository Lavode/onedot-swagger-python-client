# swagger_client.RecipesApi

All URIs are relative to *https://api.wealthport.com/gateway/public/endpoints/1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**retrieve_instructions**](RecipesApi.md#retrieve_instructions) | **GET** /recipes/{id}/instructions | Retrieve Instructions
[**retrieve_recipe**](RecipesApi.md#retrieve_recipe) | **GET** /recipes/{id} | Retrieve Recipe
[**retrieve_recipes**](RecipesApi.md#retrieve_recipes) | **GET** /recipes | Retrieve Recipes
[**update_instructions**](RecipesApi.md#update_instructions) | **PUT** /recipes/{id}/instructions | Update Instructions


# **retrieve_instructions**
> str retrieve_instructions(id)

Retrieve Instructions

Retrieves the instructions of the specified Recipe.

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
api_instance = swagger_client.RecipesApi()
id = 'id_example' # str | Recipe ID of the recipe whose instructions to retrieve

try: 
    # Retrieve Instructions
    api_response = api_instance.retrieve_instructions(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RecipesApi->retrieve_instructions: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Recipe ID of the recipe whose instructions to retrieve | 

### Return type

**str**

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_recipe**
> ExistingRecipe retrieve_recipe(id)

Retrieve Recipe

Retrieves the specified Recipe.

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
api_instance = swagger_client.RecipesApi()
id = 'id_example' # str | Recipe ID of the recipe to retrieve

try: 
    # Retrieve Recipe
    api_response = api_instance.retrieve_recipe(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RecipesApi->retrieve_recipe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Recipe ID of the recipe to retrieve | 

### Return type

[**ExistingRecipe**](ExistingRecipe.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_recipes**
> list[ExistingRecipe] retrieve_recipes()

Retrieve Recipes

Retrieves all available Recipes.

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
api_instance = swagger_client.RecipesApi()

try: 
    # Retrieve Recipes
    api_response = api_instance.retrieve_recipes()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RecipesApi->retrieve_recipes: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ExistingRecipe]**](ExistingRecipe.md)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_instructions**
> update_instructions(id, body=body)

Update Instructions

Updates the instructions of the specified Recipe.

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
api_instance = swagger_client.RecipesApi()
id = 'id_example' # str | Recipe ID of the recipe whose instructions to update
body = 'body_example' # str | JSON instructions to update the Recipe (optional)

try: 
    # Update Instructions
    api_instance.update_instructions(id, body=body)
except ApiException as e:
    print("Exception when calling RecipesApi->update_instructions: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Recipe ID of the recipe whose instructions to update | 
 **body** | **str**| JSON instructions to update the Recipe | [optional] 

### Return type

void (empty response body)

### Authorization

[Using HTTP Header](../README.md#Using HTTP Header), [Using URL Query Parameter](../README.md#Using URL Query Parameter)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

