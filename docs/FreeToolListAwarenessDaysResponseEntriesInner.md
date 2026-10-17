

# FreeToolListAwarenessDaysResponseEntriesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Name of the holiday or observance. |  [optional] |
|**type** | [**TypeEnum**](#TypeEnum) | Entry type. |  [optional] |
|**date** | **LocalDate** | The day, or the first day of a week or month. |  [optional] |
|**end** | **LocalDate** | Last day of a week or month (inclusive); null for a single day. |  [optional] |
|**countries** | **List&lt;String&gt;** | Country codes, or &#x60;global&#x60;. |  [optional] |
|**topics** | **List&lt;String&gt;** | Topics. |  [optional] |
|**source** | **URI** | Official or organiser page the date comes from. |  [optional] |
|**note** | **String** | Regional scope or a day off that differs from the date. |  [optional] |
|**idea** | **String** | A one-line post idea. |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| PUBLIC_HOLIDAY | &quot;public-holiday&quot; |
| AWARENESS_DAY | &quot;awareness-day&quot; |
| AWARENESS_WEEK | &quot;awareness-week&quot; |
| AWARENESS_MONTH | &quot;awareness-month&quot; |
| SOCIAL_MEDIA_DAY | &quot;social-media-day&quot; |



