# CloudmersiveDocumentaiApiClient::ExtractDocumentJobStatusResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**successful** | **BOOLEAN** | True if the operation to check the status of the job was successful, false otherwise | [optional] 
**async_job_status** | **String** | Returns the job status of the Async Job, if applicable.  Possible states are STARTED and COMPLETED | [optional] 
**async_job_id** | **String** | Job ID | [optional] 
**extract_text_result** | [**ExtractTextResponse**](ExtractTextResponse.md) |  | [optional] 
**extract_fields_and_tables_result** | [**ExtractFieldsAndTablesResponse**](ExtractFieldsAndTablesResponse.md) |  | [optional] 
**extract_fields_result** | [**ExtractFieldsResponse**](ExtractFieldsResponse.md) |  | [optional] 
**extract_classification_result** | [**DocumentClassificationResult**](DocumentClassificationResult.md) |  | [optional] 
**error_message** | **String** | Error message (if any) | [optional] 


