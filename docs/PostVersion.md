

# PostVersion


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**accountId** | **Integer** | Use &#x60;0&#x60; for the original/default version. |  |
|**isOriginal** | **Boolean** | Must be &#x60;true&#x60; for the first version. |  |
|**syncedWith** | **Integer** | Account ID of the version this version follows (&#x60;0&#x60; &#x3D; the original), or null when it is edited independently. Ignored on the original version. |  [optional] |
|**content** | [**List&lt;PostContent&gt;**](PostContent.md) | Ordered content items. Item 0 is the post. Item 1 is the first comment on Facebook Page, Instagram and LinkedIn, or the next thread post on X, Threads, Bluesky, Mastodon and Pixelfed. See &#x60;PostContent&#x60;.  |  |
|**options** | **PostVersionOptions** |  |  [optional] |



