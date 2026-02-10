# CloudmersiveDocumentaiApiClient::RunBatchJobApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extract_all_fields_and_tables_from_document_batch_job**](RunBatchJobApi.md#extract_all_fields_and_tables_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/all | Extract All Fields and Tables of Data from a Document using AI as a Batch Job
[**extract_classification_from_document_batch_job**](RunBatchJobApi.md#extract_classification_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/classify | Extract Classification or Category from a Document using AI as a Batch Job
[**extract_fields_from_document_advanced_batch_job**](RunBatchJobApi.md#extract_fields_from_document_advanced_batch_job) | **POST** /document-ai/document/batch-job/extract/fields/advanced | Extract Field Values from a Document using Advanced AI as a Batch Job
[**extract_text_from_document_batch_job**](RunBatchJobApi.md#extract_text_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/text | Extract Text from a Document using AI as a Batch Job
[**get_async_job_status**](RunBatchJobApi.md#get_async_job_status) | **GET** /document-ai/document/batch-job/batch-job/status | Get the status and result of an Extract Document Batch Job


# **extract_all_fields_and_tables_from_document_batch_job**
> ExtractDocumentBatchJobResult extract_all_fields_and_tables_from_document_batch_job(opts)

Extract All Fields and Tables of Data from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Requires Managed Instance or Private Cloud deployment.

### Example
```ruby
# load the gem
require 'cloudmersive-documentai-api-client'
# setup authorization
CloudmersiveDocumentaiApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveDocumentaiApiClient::RunBatchJobApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract All Fields and Tables of Data from a Document using AI as a Batch Job
  result = api_instance.extract_all_fields_and_tables_from_document_batch_job(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling RunBatchJobApi->extract_all_fields_and_tables_from_document_batch_job: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_classification_from_document_batch_job**
> ExtractDocumentBatchJobResult extract_classification_from_document_batch_job(opts)

Extract Classification or Category from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Requires Managed Instance or Private Cloud deployment.

### Example
```ruby
# load the gem
require 'cloudmersive-documentai-api-client'
# setup authorization
CloudmersiveDocumentaiApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveDocumentaiApiClient::RunBatchJobApi.new

opts = { 
  categories: 'categories_example', # String | Desired classification to extract
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Classification or Category from a Document using AI as a Batch Job
  result = api_instance.extract_classification_from_document_batch_job(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling RunBatchJobApi->extract_classification_from_document_batch_job: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | **String**| Desired classification to extract | [optional] 
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_fields_from_document_advanced_batch_job**
> ExtractDocumentBatchJobResult extract_fields_from_document_advanced_batch_job(opts)

Extract Field Values from a Document using Advanced AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Requires Managed Instance or Private Cloud deployment.

### Example
```ruby
# load the gem
require 'cloudmersive-documentai-api-client'
# setup authorization
CloudmersiveDocumentaiApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveDocumentaiApiClient::RunBatchJobApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  body: CloudmersiveDocumentaiApiClient::AdvancedExtractFieldsRequest.new # AdvancedExtractFieldsRequest | Input document and parameters
}

begin
  #Extract Field Values from a Document using Advanced AI as a Batch Job
  result = api_instance.extract_fields_from_document_advanced_batch_job(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling RunBatchJobApi->extract_fields_from_document_advanced_batch_job: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractFieldsRequest**](AdvancedExtractFieldsRequest.md)| Input document and parameters | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **extract_text_from_document_batch_job**
> ExtractDocumentBatchJobResult extract_text_from_document_batch_job(opts)

Extract Text from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Input document formats supported include DOCX, PDF, PNG and JPG.  Supports a wide range of languages.  Requires Managed Instance or Private Cloud deployment.

### Example
```ruby
# load the gem
require 'cloudmersive-documentai-api-client'
# setup authorization
CloudmersiveDocumentaiApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveDocumentaiApiClient::RunBatchJobApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Text from a Document using AI as a Batch Job
  result = api_instance.extract_text_from_document_batch_job(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling RunBatchJobApi->extract_text_from_document_batch_job: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **get_async_job_status**
> ExtractDocumentJobStatusResult get_async_job_status(opts)

Get the status and result of an Extract Document Batch Job

Returns the result of the Async Job - possible states can be STARTED or COMPLETED.  This API is only available for Cloudmersive Managed Instance and Private Cloud deployments.

### Example
```ruby
# load the gem
require 'cloudmersive-documentai-api-client'
# setup authorization
CloudmersiveDocumentaiApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveDocumentaiApiClient::RunBatchJobApi.new

opts = { 
  async_job_id: 'async_job_id_example' # String | Job ID for the batch job to get the status of
}

begin
  #Get the status and result of an Extract Document Batch Job
  result = api_instance.get_async_job_status(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling RunBatchJobApi->get_async_job_status: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **async_job_id** | **String**| Job ID for the batch job to get the status of | [optional] 

### Return type

[**ExtractDocumentJobStatusResult**](ExtractDocumentJobStatusResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json



