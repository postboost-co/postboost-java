

# FreeToolCalculateSmmPricingResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**currency** | **String** |  |  [optional] |
|**pricingModel** | [**PricingModelEnum**](#PricingModelEnum) |  |  [optional] |
|**postsPerMonth** | **BigDecimal** | Networks × posts per week × 52 ÷ 12, 1 decimal. |  [optional] |
|**hoursPerMonth** | **BigDecimal** | Estimated working hours a month, 1 decimal. |  [optional] |
|**hourlyRate** | **BigDecimal** |  |  [optional] |
|**monthlyRetainer** | **BigDecimal** | Hours a month × hourly rate, whole currency units. |  [optional] |
|**perPost** | **BigDecimal** | Monthly retainer ÷ posts a month, 2 decimals; null with no posts. |  [optional] |
|**range** | [**FreeToolCalculateSmmPricingResponseRange**](FreeToolCalculateSmmPricingResponseRange.md) |  |  [optional] |
|**lineItems** | [**List&lt;FreeToolCalculateSmmPricingResponseLineItemsInner&gt;**](FreeToolCalculateSmmPricingResponseLineItemsInner.md) | Every task with hours above 0. |  [optional] |
|**assumptions** | **List&lt;String&gt;** |  |  [optional] |



## Enum: PricingModelEnum

| Name | Value |
|---- | -----|
| HOURLY | &quot;hourly&quot; |
| RETAINER | &quot;retainer&quot; |
| PER_POST | &quot;per_post&quot; |



