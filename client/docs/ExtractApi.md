# CloudmersiveDocumentaiApiClient::ExtractApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extract_all_fields_and_tables**](ExtractApi.md#extract_all_fields_and_tables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
[**extract_barcodes**](ExtractApi.md#extract_barcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
[**extract_classification**](ExtractApi.md#extract_classification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
[**extract_classification_advanced**](ExtractApi.md#extract_classification_advanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
[**extract_fields**](ExtractApi.md#extract_fields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
[**extract_fields_advanced**](ExtractApi.md#extract_fields_advanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
[**extract_split**](ExtractApi.md#extract_split) | **POST** /document-ai/document/extract/split | Intelligently Split a Combined Document into Sub-Documents using AI
[**extract_summary**](ExtractApi.md#extract_summary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
[**extract_tables**](ExtractApi.md#extract_tables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
[**extract_text**](ExtractApi.md#extract_text) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI


# **extract_all_fields_and_tables**
> ExtractFieldsAndTablesResponse extract_all_fields_and_tables(opts)

Extract All Fields and Tables of Data from a Document using AI

Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
  preprocessing: 'preprocessing_example', # String | Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are 'Auto' (default), 'Paged', and 'Compatability'.  Use 'Paged' to treat each page as a separate document for extraction (requires Advanced recognitionMode).  Default is Auto.
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
 **preprocessing** | **String**| Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are &#39;Auto&#39; (default), &#39;Paged&#39;, and &#39;Compatability&#39;.  Use &#39;Paged&#39; to treat each page as a separate document for extraction (requires Advanced recognitionMode).  Default is Auto. | [optional] 
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

Extract all barcodes from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG, HEIC and WEBP.  Consumes 100 API calls per page.

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

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
> ExtractFieldsAdvancedResponse extract_fields_advanced(opts)

Extract Field Values from a Document using Advanced AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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

[**ExtractFieldsAdvancedResponse**](ExtractFieldsAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json



# **extract_split**
> SplitDocumentResponse extract_split(opts)

Intelligently Split a Combined Document into Sub-Documents using AI

Analyzes a document containing multiple sub-documents (such as a scanned batch of ID cards, forms, or mixed documents) and intelligently splits it into separate sub-documents.  Uses AI to detect document boundaries based on visual content, headers, names, and document types.  Returns the page ranges and PDF bytes for each identified sub-document.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
  input_file: File.new('/path/to/file.txt') # File | Input document containing multiple sub-documents to split
}

begin
  #Intelligently Split a Combined Document into Sub-Documents using AI
  result = api_instance.extract_split(opts)
  p result
rescue CloudmersiveDocumentaiApiClient::ApiError => e
  puts "Exception when calling ExtractApi->extract_split: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **File**| Input document containing multiple sub-documents to split | [optional] 

### Return type

[**SplitDocumentResponse**](SplitDocumentResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



# **extract_summary**
> SummarizeDocumentResponse extract_summary(opts)

Extract Summary from a Document using AI

Creates a 1 paragraph summary of the input document using Artificial Intelligence.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
  language: 'language_example', # String | Optional; Three-letter language code (ISO 639) for the summary.  Default is ENG.  Possible language codes are: AAR,ABK,ACE,ACH,ADA,ADY,AFA,AFH,AFR,AIN,AKA,AKK,ALB,ALE,ALG,ALT,AMH,ANG,ANP,APA,ARA,ARC,ARG,ARM,ARN,ARP,ART,ARW,ASM,AST,ATH,AUS,AVA,AVE,AWA,AYM,AZE,BAD,BAI,BAK,BAL,BAM,BAN,BAQ,BAS,BAT,BEJ,BEL,BEM,BEN,BER,BHO,BIH,BIK,BIN,BIS,BLA,BNT,BOD,BOS,BRA,BRE,BTK,BUA,BUG,BUL,BUR,BYN,CAD,CAI,CAR,CAT,CAU,CEB,CEL,CES,CHA,CHB,CHE,CHG,CHI,CHK,CHM,CHN,CHO,CHP,CHR,CHU,CHV,CHY,CMC,CNR,COP,COR,COS,CPE,CPF,CPP,CRE,CRH,CRP,CSB,CUS,CYM,CZE,DAK,DAN,DAR,DAY,DEL,DEN,DEU,DGR,DIN,DIV,DOI,DRA,DSB,DUA,DUM,DUT,DYU,DZO,EFI,EGY,EKA,ELL,ELX,ENG,ENM,EPO,EST,EUS,EWE,EWO,FAN,FAO,FAS,FAT,FIJ,FIL,FIN,FIU,FON,FRA,FRE,FRM,FRO,FRR,FRS,FRY,FUL,FUR,GAA,GAY,GBA,GEM,GEO,GER,GEZ,GIL,GLA,GLE,GLG,GLV,GMH,GOH,GON,GOR,GOT,GRB,GRC,GRE,GRN,GSW,GUJ,GWI,HAI,HAT,HAU,HAW,HEB,HER,HIL,HIM,HIN,HIT,HMN,HMO,HRV,HSB,HUN,HUP,HYE,IBA,IBO,ICE,IDO,III,IJO,IKU,ILE,ILO,INA,INC,IND,INE,INH,IPK,IRA,IRO,ISL,ITA,JAV,JBO,JPN,JPR,JRB,KAA,KAB,KAC,KAL,KAM,KAN,KAR,KAS,KAT,KAU,KAW,KAZ,KBD,KHA,KHI,KHM,KHO,KIK,KIN,KIR,KMB,KOK,KOM,KON,KOR,KOS,KPE,KRC,KRL,KRO,KRU,KUA,KUM,KUR,KUT,LAD,LAH,LAM,LAO,LAT,LAV,LEZ,LIM,LIN,LIT,LOL,LOZ,LTZ,LUA,LUB,LUG,LUI,LUN,LUO,LUS,MAC,MAD,MAG,MAH,MAI,MAK,MAL,MAN,MAO,MAP,MAR,MAS,MAY,MDF,MDR,MEN,MGA,MIC,MIN,MIS,MKD,MKH,MLG,MLT,MNC,MNI,MNO,MOH,MON,MOS,MRI,MSA,MUL,MUN,MUS,MWL,MWR,MYA,MYN,MYV,NAH,NAI,NAP,NAU,NAV,NBL,NDE,NDO,NDS,NEP,NEW,NIA,NIC,NIU,NLD,NNO,NOB,NOG,NON,NOR,NQO,NSO,NUB,NWC,NYA,NYM,NYN,NYO,NZI,OCI,OJI,ORI,ORM,OSA,OSS,OTA,OTO,PAA,PAG,PAL,PAM,PAN,PAP,PAU,PEO,PER,PHI,PHN,PLI,POL,PON,POR,PRA,PRO,PUS,QUE,RAJ,RAP,RAR,ROA,ROH,ROM,RON,RUM,RUN,RUP,RUS,SAD,SAG,SAH,SAI,SAL,SAM,SAN,SAS,SAT,SCN,SCO,SEL,SEM,SGA,SGN,SHN,SID,SIN,SIO,SIT,SLA,SLK,SLO,SLV,SMA,SME,SMI,SMJ,SMN,SMO,SMS,SNA,SND,SNK,SOG,SOM,SON,SOT,SPA,SQI,SRD,SRN,SRP,SRR,SSA,SSW,SUK,SUN,SUS,SUX,SWA,SWE,SYC,SYR,TAH,TAI,TAM,TAT,TEL,TEM,TER,TET,TGK,TGL,THA,TIB,TIG,TIR,TIV,TKL,TLH,TLI,TMH,TOG,TON,TPI,TSI,TSN,TSO,TUK,TUM,TUP,TUR,TUT,TVL,TWI,TYV,UDM,UGA,UIG,UKR,UMB,UND,URD,UZB,VAI,VEN,VIE,VOL,VOT,WAK,WAL,WAR,WAS,WEL,WEN,WLN,WOL,XAL,XHO,YAO,YAP,YID,YOR,YPK,ZAP,ZBL,ZEN,ZGH,ZHA,ZHO,ZND,ZUL,ZUN,ZXX,ZZA.
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
 **language** | **String**| Optional; Three-letter language code (ISO 639) for the summary.  Default is ENG.  Possible language codes are: AAR,ABK,ACE,ACH,ADA,ADY,AFA,AFH,AFR,AIN,AKA,AKK,ALB,ALE,ALG,ALT,AMH,ANG,ANP,APA,ARA,ARC,ARG,ARM,ARN,ARP,ART,ARW,ASM,AST,ATH,AUS,AVA,AVE,AWA,AYM,AZE,BAD,BAI,BAK,BAL,BAM,BAN,BAQ,BAS,BAT,BEJ,BEL,BEM,BEN,BER,BHO,BIH,BIK,BIN,BIS,BLA,BNT,BOD,BOS,BRA,BRE,BTK,BUA,BUG,BUL,BUR,BYN,CAD,CAI,CAR,CAT,CAU,CEB,CEL,CES,CHA,CHB,CHE,CHG,CHI,CHK,CHM,CHN,CHO,CHP,CHR,CHU,CHV,CHY,CMC,CNR,COP,COR,COS,CPE,CPF,CPP,CRE,CRH,CRP,CSB,CUS,CYM,CZE,DAK,DAN,DAR,DAY,DEL,DEN,DEU,DGR,DIN,DIV,DOI,DRA,DSB,DUA,DUM,DUT,DYU,DZO,EFI,EGY,EKA,ELL,ELX,ENG,ENM,EPO,EST,EUS,EWE,EWO,FAN,FAO,FAS,FAT,FIJ,FIL,FIN,FIU,FON,FRA,FRE,FRM,FRO,FRR,FRS,FRY,FUL,FUR,GAA,GAY,GBA,GEM,GEO,GER,GEZ,GIL,GLA,GLE,GLG,GLV,GMH,GOH,GON,GOR,GOT,GRB,GRC,GRE,GRN,GSW,GUJ,GWI,HAI,HAT,HAU,HAW,HEB,HER,HIL,HIM,HIN,HIT,HMN,HMO,HRV,HSB,HUN,HUP,HYE,IBA,IBO,ICE,IDO,III,IJO,IKU,ILE,ILO,INA,INC,IND,INE,INH,IPK,IRA,IRO,ISL,ITA,JAV,JBO,JPN,JPR,JRB,KAA,KAB,KAC,KAL,KAM,KAN,KAR,KAS,KAT,KAU,KAW,KAZ,KBD,KHA,KHI,KHM,KHO,KIK,KIN,KIR,KMB,KOK,KOM,KON,KOR,KOS,KPE,KRC,KRL,KRO,KRU,KUA,KUM,KUR,KUT,LAD,LAH,LAM,LAO,LAT,LAV,LEZ,LIM,LIN,LIT,LOL,LOZ,LTZ,LUA,LUB,LUG,LUI,LUN,LUO,LUS,MAC,MAD,MAG,MAH,MAI,MAK,MAL,MAN,MAO,MAP,MAR,MAS,MAY,MDF,MDR,MEN,MGA,MIC,MIN,MIS,MKD,MKH,MLG,MLT,MNC,MNI,MNO,MOH,MON,MOS,MRI,MSA,MUL,MUN,MUS,MWL,MWR,MYA,MYN,MYV,NAH,NAI,NAP,NAU,NAV,NBL,NDE,NDO,NDS,NEP,NEW,NIA,NIC,NIU,NLD,NNO,NOB,NOG,NON,NOR,NQO,NSO,NUB,NWC,NYA,NYM,NYN,NYO,NZI,OCI,OJI,ORI,ORM,OSA,OSS,OTA,OTO,PAA,PAG,PAL,PAM,PAN,PAP,PAU,PEO,PER,PHI,PHN,PLI,POL,PON,POR,PRA,PRO,PUS,QUE,RAJ,RAP,RAR,ROA,ROH,ROM,RON,RUM,RUN,RUP,RUS,SAD,SAG,SAH,SAI,SAL,SAM,SAN,SAS,SAT,SCN,SCO,SEL,SEM,SGA,SGN,SHN,SID,SIN,SIO,SIT,SLA,SLK,SLO,SLV,SMA,SME,SMI,SMJ,SMN,SMO,SMS,SNA,SND,SNK,SOG,SOM,SON,SOT,SPA,SQI,SRD,SRN,SRP,SRR,SSA,SSW,SUK,SUN,SUS,SUX,SWA,SWE,SYC,SYR,TAH,TAI,TAM,TAT,TEL,TEM,TER,TET,TGK,TGL,THA,TIB,TIG,TIR,TIV,TKL,TLH,TLI,TMH,TOG,TON,TPI,TSI,TSN,TSO,TUK,TUM,TUP,TUR,TUT,TVL,TWI,TYV,UDM,UGA,UIG,UKR,UMB,UND,URD,UZB,VAI,VEN,VIE,VOL,VOT,WAK,WAL,WAR,WAS,WEL,WEN,WLN,WOL,XAL,XHO,YAO,YAP,YID,YOR,YPK,ZAP,ZBL,ZEN,ZGH,ZHA,ZHO,ZND,ZUL,ZUN,ZXX,ZZA. | [optional] 
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

Extract Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumeds 100 API calls per page.

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

Extract raw text from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Supports a wide range of languages.  Consumes 100 API calls per page.

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
  recognition_mode: 'recognition_mode_example', # String | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images.  Set to Deterministic to directly extract text from digital documents without using AI.
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
 **recognition_mode** | **String**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images.  Set to Deterministic to directly extract text from digital documents without using AI. | [optional] 
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTextResponse**](ExtractTextResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json



