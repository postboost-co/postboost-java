

# FreeToolGetGlossaryResponseTermsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**term** | **String** | The term. |  [optional] |
|**slug** | **String** | Stable key of the term, also its anchor on the page. |  [optional] |
|**category** | [**CategoryEnum**](#CategoryEnum) | Category. |  [optional] |
|**definition** | **String** | Plain-language definition in one to three sentences. |  [optional] |
|**networks** | **List&lt;String&gt;** | Networks the term is specific to (provider keys); empty when it applies to all. |  [optional] |
|**related** | **List&lt;String&gt;** | Slugs of related terms. |  [optional] |
|**url** | **URI** | The term on the glossary page. |  [optional] |
|**learnUrl** | **URI** | A PostBoost guide that goes deeper, or null. |  [optional] |
|**toolUrl** | **URI** | A free tool for the job, or null. |  [optional] |
|**featureUrl** | **URI** | The PostBoost feature page, or null. |  [optional] |
|**source** | **URI** | Where a platform rule or number in the definition comes from, or null. |  [optional] |



## Enum: CategoryEnum

| Name | Value |
|---- | -----|
| METRICS | &quot;metrics&quot; |
| CONTENT | &quot;content&quot; |
| ADS | &quot;ads&quot; |
| PLATFORMS | &quot;platforms&quot; |
| DEVELOPER | &quot;developer&quot; |
| STRATEGY | &quot;strategy&quot; |



