# CloudmersiveDocumentaiApiClient::AnalyzeApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**answer_questions**](AnalyzeApi.md#answer_questions) | **POST** /document-ai/document/analyze/answer-questions | Answer Questions about a Document in a structured way using Advanced AI
[**apply_rules**](AnalyzeApi.md#apply_rules) | **POST** /document-ai/document/analyze/enforce-policy | Enforce Policies to a Document to allow or block it using Advanced AI


# **answer_questions**
> DocumentQuestionAnswersResult answer_questions(opts)

Answer Questions about a Document in a structured way using Advanced AI

Answer boolean (yes/no), multiple-choice and free-response questions about the contents of a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Consumes 100 API calls per page.

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

api_instance = CloudmersiveDocumentaiApiClient::AnalyzeApi.new

opts = { 
  body: CloudmersiveDocumentaiApiClient::DocumentQuestionsRequest.new # DocumentQuestionsRequest | Input request, including document and questions
}

begin
  #Answer Questions about a Document in a structured way using Advanced AI
  result = api_instance.answer_questions(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling AnalyzeApi->answer_questions: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DocumentQuestionsRequest**](DocumentQuestionsRequest.md)| Input request, including document and questions | [optional] 

### Return type

[**DocumentQuestionAnswersResult**](DocumentQuestionAnswersResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **apply_rules**
> DocumentPolicyResult apply_rules(opts)

Enforce Policies to a Document to allow or block it using Advanced AI

Enforce Policies to a Document to allow or block it using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Consumes 100 API calls per page.

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

api_instance = CloudmersiveDocumentaiApiClient::AnalyzeApi.new

opts = { 
  body: CloudmersiveDocumentaiApiClient::DocumentPolicyRequest.new # DocumentPolicyRequest | Input request, including document and policy rules
}

begin
  #Enforce Policies to a Document to allow or block it using Advanced AI
  result = api_instance.apply_rules(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling AnalyzeApi->apply_rules: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DocumentPolicyRequest**](DocumentPolicyRequest.md)| Input request, including document and policy rules | [optional] 

### Return type

[**DocumentPolicyResult**](DocumentPolicyResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



