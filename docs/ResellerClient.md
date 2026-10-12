

# ResellerClient


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** | The client workspace UUID; use it as &#x60;workspaceUuid&#x60; for the client&#39;s own endpoints. |  |
|**name** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**accounts** | **Integer** |  |  |
|**accountsNeedingReconnect** | **Integer** |  |  |
|**members** | **Integer** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**archivedAt** | **OffsetDateTime** |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;active&quot; |
| ARCHIVED | &quot;archived&quot; |



