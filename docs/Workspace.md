

# Workspace


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** |  |  |
|**name** | **String** |  |  |
|**hexColor** | **String** | Deprecated. Workspaces no longer have a colour (workspaces now use &#x60;avatar&#x60;); the API returns the constant &#x60;4f46e5&#x60; so existing clients keep working. Will be removed in API v2. |  [optional] |
|**avatar** | **URI** | URL of the workspace avatar, or null when none is set. Supersedes &#x60;hex_color&#x60;. |  [optional] |
|**owner** | [**User**](User.md) |  |  [optional] |
|**accessStatus** | [**AccessStatusEnum**](#AccessStatusEnum) |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



## Enum: AccessStatusEnum

| Name | Value |
|---- | -----|
| SUBSCRIPTION | &quot;subscription&quot; |
| UNLIMITED | &quot;unlimited&quot; |
| LOCKED | &quot;locked&quot; |



