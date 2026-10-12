

# ReportExportInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**format** | [**FormatEnum**](#FormatEnum) |  |  |
|**dataset** | [**DatasetEnum**](#DatasetEnum) | CSV rows; default &#x60;posts&#x60;. Ignored for PDF. |  [optional] |
|**period** | [**PeriodEnum**](#PeriodEnum) | Default &#x60;last_month&#x60;. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are sent. |  [optional] |
|**dateFrom** | **LocalDate** |  |  [optional] |
|**dateTo** | **LocalDate** | At most 366 days after &#x60;date_from&#x60;. |  [optional] |
|**accountIds** | **List&lt;Integer&gt;** | Limit the report to these accounts; default all. |  [optional] |



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



## Enum: PeriodEnum

| Name | Value |
|---- | -----|
| THIS_WEEK | &quot;this_week&quot; |
| LAST_WEEK | &quot;last_week&quot; |
| THIS_MONTH | &quot;this_month&quot; |
| LAST_MONTH | &quot;last_month&quot; |
| LAST_3_MONTHS | &quot;last_3_months&quot; |
| THIS_YEAR | &quot;this_year&quot; |



