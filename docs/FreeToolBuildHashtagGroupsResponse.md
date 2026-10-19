

# FreeToolBuildHashtagGroupsResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**hashtags** | **List&lt;String&gt;** | Clean hashtags in input order, duplicates removed. |  [optional] |
|**removed** | [**List&lt;FreeToolBuildHashtagGroupsResponseRemovedInner&gt;**](FreeToolBuildHashtagGroupsResponseRemovedInner.md) | Entries that were dropped, with the reason. |  [optional] |
|**cap** | **Integer** | Hashtags PostBoost allows per post on the network; null &#x3D; no hard limit. |  [optional] |
|**groupSize** | **Integer** | Hashtags per group that was used. |  [optional] |
|**groups** | [**List&lt;FreeToolBuildHashtagGroupsResponseGroupsInner&gt;**](FreeToolBuildHashtagGroupsResponseGroupsInner.md) |  |  [optional] |
|**overCap** | **Boolean** | A group holds more hashtags than the cap. |  [optional] |



