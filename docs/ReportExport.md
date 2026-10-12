

# ReportExport


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**uuid** | **UUID** |  |  |
|**format** | [**FormatEnum**](#FormatEnum) |  |  |
|**dataset** | [**DatasetEnum**](#DatasetEnum) |  |  |
|**period** | **String** |  |  |
|**dateFrom** | **LocalDate** |  |  |
|**dateTo** | **LocalDate** |  |  |
|**accountIds** | **List&lt;Integer&gt;** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**error** | **String** |  |  |
|**bytes** | **Integer** |  |  |
|**downloadUrl** | **URI** | Authenticated download URL while the file is available. |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**expiresAt** | **OffsetDateTime** |  |  |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| CSV | &quot;csv&quot; |
| PDF | &quot;pdf&quot; |



## Enum: DatasetEnum

| Name | Value |
|---- | -----|
| POSTS | &quot;posts&quot; |
| ACCOUNTS | &quot;accounts&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| READY | &quot;ready&quot; |
| FAILED | &quot;failed&quot; |
| EXPIRED | &quot;expired&quot; |



