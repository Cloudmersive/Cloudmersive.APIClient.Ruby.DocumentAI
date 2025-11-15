# CloudmersiveDocumentaiApiClient::ExtractApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extract_all_fields_and_tables**](ExtractApi.md#extract_all_fields_and_tables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
[**extract_barcodes**](ExtractApi.md#extract_barcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
[**extract_classification**](ExtractApi.md#extract_classification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
[**extract_classification_advanced**](ExtractApi.md#extract_classification_advanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
[**extract_fields**](ExtractApi.md#extract_fields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
[**extract_fields_advanced**](ExtractApi.md#extract_fields_advanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
[**extract_summary**](ExtractApi.md#extract_summary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
[**extract_tables**](ExtractApi.md#extract_tables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
[**extract_text**](ExtractApi.md#extract_text) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI


# **extract_all_fields_and_tables**
> ExtractFieldsAndTablesResponse extract_all_fields_and_tables(opts)

Extract All Fields and Tables of Data from a Document using AI

Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract All Fields and Tables of Data from a Document using AI
  result = api_instance.extract_all_fields_and_tables(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_all_fields_and_tables: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractFieldsAndTablesResponse**](ExtractFieldsAndTablesResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_barcodes**
> ExtractBarcodesAiResponse extract_barcodes(opts)

Extract Barcodes of from a Document using AI

Extract all barcodes from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Barcodes of from a Document using AI
  result = api_instance.extract_barcodes(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_barcodes: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractBarcodesAiResponse**](ExtractBarcodesAiResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_classification**
> DocumentClassificationResult extract_classification(opts)

Extract Classification or Category from a Document using AI

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  categories: 'categories_example', # String | Desired classification to extract
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Classification or Category from a Document using AI
  result = api_instance.extract_classification(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_classification: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | **String**| Desired classification to extract | [optional] 
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**DocumentClassificationResult**](DocumentClassificationResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_classification_advanced**
> DocumentAdvancedClassificationResult extract_classification_advanced(opts)

Extract Classification or Category from a Document using Advanced AI

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  body: CloudmersiveDocumentaiApiClient::AdvancedExtractClassificationRequest.new # AdvancedExtractClassificationRequest | Input request to perform the classification on
}

begin
  #Extract Classification or Category from a Document using Advanced AI
  result = api_instance.extract_classification_advanced(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_classification_advanced: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractClassificationRequest**](AdvancedExtractClassificationRequest.md)| Input request to perform the classification on | [optional] 

### Return type

[**DocumentAdvancedClassificationResult**](DocumentAdvancedClassificationResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **extract_fields**
> ExtractFieldsResponse extract_fields(opts)

Extract Field Values from a Document using AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  field_names: 'field_names_example', # String | Desired fields to extract, comma separated
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Field Values from a Document using AI
  result = api_instance.extract_fields(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_fields: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **field_names** | **String**| Desired fields to extract, comma separated | [optional] 
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractFieldsResponse**](ExtractFieldsResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_fields_advanced**
> ExtractFieldsResponse extract_fields_advanced(opts)

Extract Field Values from a Document using Advanced AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  body: CloudmersiveDocumentaiApiClient::AdvancedExtractFieldsRequest.new # AdvancedExtractFieldsRequest | Input request, including document file as byte array, and information on which fields to extract
}

begin
  #Extract Field Values from a Document using Advanced AI
  result = api_instance.extract_fields_advanced(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_fields_advanced: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractFieldsRequest**](AdvancedExtractFieldsRequest.md)| Input request, including document file as byte array, and information on which fields to extract | [optional] 

### Return type

[**ExtractFieldsResponse**](ExtractFieldsResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **extract_summary**
> SummarizeDocumentResponse extract_summary(opts)

Extract Summary from a Document using AI

Creates a 1 paragraph summary of the input document using Artificial Intelligence.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Summary from a Document using AI
  result = api_instance.extract_summary(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_summary: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**SummarizeDocumentResponse**](SummarizeDocumentResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_tables**
> ExtractTablesResponse extract_tables(opts)

Extract Tables of Data from a Document using AI

Extract Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Tables of Data from a Document using AI
  result = api_instance.extract_tables(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_tables: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTablesResponse**](ExtractTablesResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_text**
> ExtractTextResponse extract_text(opts)

Extract Text from a Document using AI

Extract raw text from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Supports a wide range of languages.

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

api_instance = CloudmersiveDocumentaiApiClient::ExtractApi.new

opts = { 
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Extract Text from a Document using AI
  result = api_instance.extract_text(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_text: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTextResponse**](ExtractTextResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



