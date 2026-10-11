

# PostVersion


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**accountId** | **Integer** | Use &#x60;0&#x60; for the original/default version. |  |
|**isOriginal** | **Boolean** | Must be &#x60;true&#x60; for the first version. |  |
|**syncedWith** | **Integer** | Account ID of the version this version follows (&#x60;0&#x60; &#x3D; the original), or null when it is edited independently. Ignored on the original version. |  [optional] |
|**content** | [**List&lt;PostContent&gt;**](PostContent.md) |  |  |
|**options** | **Object** | Platform-specific publishing options. |  [optional] |



