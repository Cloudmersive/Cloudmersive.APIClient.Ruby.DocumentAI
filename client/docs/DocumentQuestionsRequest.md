# CloudmersiveDocumentaiApiClient::DocumentQuestionsRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_file** | **String** | Input file as a byte array | [optional] 
**questions_yes_no** | [**Array&lt;DocumentQuestionBoolean&gt;**](DocumentQuestionBoolean.md) | Optional: Yes or No boolean questions to answer about the document | [optional] 
**questions_multiple_choice** | [**Array&lt;DocumentQuestionMultipleChoice&gt;**](DocumentQuestionMultipleChoice.md) | Optional: Multiple choice questions to answer about the document | [optional] 
**questions_free_response** | [**Array&lt;DocumentQuestionFreeResponse&gt;**](DocumentQuestionFreeResponse.md) | Optional: Free response questions to answer about the document | [optional] 
**recognition_mode** | **String** | Optional; Recognition mode - Normal (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 


