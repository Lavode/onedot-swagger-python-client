# ExistingOrder

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique ID of the order | 
**name** | **str** | Name of the order | 
**created** | **datetime** | ISO 8601 Date when the order has been created | 
**creator** | **str** | User ID of the user who created the order | 
**sources** | **list[str]** | Array of source IDs to be referenced by the order | [optional] 
**folders** | **list[str]** | Array of folder IDs to be referenced by the order | [optional] 
**recipe** | **str** | Recipe to use when processing the order | [optional] 
**bytes** | **int** | Size of the order (in bytes) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


