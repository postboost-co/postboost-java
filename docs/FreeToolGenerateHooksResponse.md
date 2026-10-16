

# FreeToolGenerateHooksResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**hooks** | [**List&lt;FreeToolGenerateHooksResponseHooksInner&gt;**](FreeToolGenerateHooksResponseHooksInner.md) | &#x60;count&#x60; hooks in several styles. |  [optional] |
|**notice** | **String** | Only while AI is switched off: the hooks are templates from the free library (getHookTemplates) with the topic filled in, free of charge. |  [optional] |
|**creditsSpent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. |  [optional] |
|**cached** | **Boolean** | True when the same request was answered before (free). |  [optional] |



