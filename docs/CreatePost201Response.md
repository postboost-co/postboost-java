

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
|**scheduledAt** | **OffsetDateTime** |  |  [optional] |
|**publishedAt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  |
|**trashed** | **Boolean** |  |  |
|**warnings** | [**List&lt;PostWarning&gt;**](PostWarning.md) | Present only when there is at least one warning. |  [optional] |



