# CloudmersiveDocumentaiApiClient::DocumentPolicyResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**clean_result** | **BOOLEAN** | True if the document complies with all of the policies, and false if it does not | [optional] 
**risk_score** | **Float** | Risk score between 0.0 and 1.0 where values above 0.5 are increasing levels of risk | [optional] 
**rule_violations** | [**Array&lt;PolicyRuleViolation&gt;**](PolicyRuleViolation.md) | Policy violations | [optional] 


