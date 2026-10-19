

# FreeToolCalculateSmmPricingRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**networks** | **Integer** | Number of social networks managed. |  |
|**postsPerWeek** | **Integer** | Posts per week on each network. |  |
|**contentType** | [**ContentTypeEnum**](#ContentTypeEnum) | What goes into a post. Assumed minutes per post: copy 30, copy_design 60, copy_design_video 120. |  [optional] |
|**communityHoursPerWeek** | **BigDecimal** | Community management (replies, comments, DMs), hours per week. |  [optional] |
|**reportingHoursPerMonth** | **BigDecimal** | Reporting, hours per month. |  [optional] |
|**adHoursPerMonth** | **BigDecimal** | Paid social ad management, hours per month. |  [optional] |
|**hourlyRate** | **BigDecimal** | Your hourly rate. The default 50 is a round placeholder, not a market rate. |  [optional] |
|**currency** | [**CurrencyEnum**](#CurrencyEnum) | Currency for formatting only; nothing is converted. |  [optional] |
|**pricingModel** | [**PricingModelEnum**](#PricingModelEnum) | Which price leads the quote: hourly, monthly retainer or per post. |  [optional] |



## Enum: ContentTypeEnum

| Name | Value |
|---- | -----|
| COPY | &quot;copy&quot; |
| COPY_DESIGN | &quot;copy_design&quot; |
| COPY_DESIGN_VIDEO | &quot;copy_design_video&quot; |



## Enum: CurrencyEnum

| Name | Value |
|---- | -----|
| USD | &quot;USD&quot; |
| EUR | &quot;EUR&quot; |
| GBP | &quot;GBP&quot; |



## Enum: PricingModelEnum

| Name | Value |
|---- | -----|
| HOURLY | &quot;hourly&quot; |
| RETAINER | &quot;retainer&quot; |
| PER_POST | &quot;per_post&quot; |



