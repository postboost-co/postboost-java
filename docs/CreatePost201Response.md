

# CreatePost201Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**uuid** | **UUID** |  |  |
|**status** | **PostStatus** |  |  |
|**publishProgress** | [**PublishProgress**](PublishProgress.md) | Only present while the post is publishing. |  [optional] |
|**accounts** | [**List&lt;Account&gt;**](Account.md) |  |  |
|**versions** | [**List&lt;PostVersion&gt;**](PostVersion.md) |  |  |
|**tags** | [**List&lt;Tag&gt;**](Tag.md) |  |  |
|**scheduledAt** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). |  [optional] |
|**publishedAt** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). |  [optional] |
|**createdAt** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). |  |
|**trashed** | **Boolean** |  |  |
|**warnings** | [**List&lt;PostWarning&gt;**](PostWarning.md) | Present only when there is at least one warning. |  [optional] |



