

# FreeToolCalculateInfluencerRateResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**tier** | [**TierEnum**](#TierEnum) |  |  [optional] |
|**tierLabel** | **String** |  |  [optional] |
|**deliverable** | [**DeliverableEnum**](#DeliverableEnum) |  |  [optional] |
|**guideLow** | **Integer** | USD, low end of the vendor price-guide range after the adjustments. |  [optional] |
|**guideHigh** | **Integer** | USD, high end; null when the guide is open-ended (e.g. 10,000+). |  [optional] |
|**guideSource** | [**FreeToolCalculateInfluencerRateResponseGuideSource**](FreeToolCalculateInfluencerRateResponseGuideSource.md) |  |  [optional] |
|**marketplaceMedian** | **Integer** | USD, the measured median paid deliverable for this tier, all networks, before adjustments. |  [optional] |
|**marketplaceNote** | **String** |  |  [optional] |
|**marketplaceSource** | [**FreeToolCalculateInfluencerRateResponseGuideSource**](FreeToolCalculateInfluencerRateResponseGuideSource.md) |  |  [optional] |
|**cpmEstimate** | **Integer** | USD, avg_views / 1,000 × cpm_usd (half up); null without both. |  [optional] |
|**multipliers** | [**List&lt;FreeToolCalculateInfluencerRateResponseMultipliersInner&gt;**](FreeToolCalculateInfluencerRateResponseMultipliersInner.md) | Every adjustment applied, as a percent of the base price. |  [optional] |
|**method** | **String** |  |  [optional] |
|**warnings** | **List&lt;String&gt;** |  |  [optional] |
|**currency** | [**CurrencyEnum**](#CurrencyEnum) |  |  [optional] |
|**lastVerified** | **LocalDate** |  |  [optional] |



## Enum: TierEnum

| Name | Value |
|---- | -----|
| UNDER_NANO | &quot;under-nano&quot; |
| NANO | &quot;nano&quot; |
| MICRO | &quot;micro&quot; |
| MID | &quot;mid&quot; |
| MACRO | &quot;macro&quot; |
| MEGA | &quot;mega&quot; |



## Enum: DeliverableEnum

| Name | Value |
|---- | -----|
| POST | &quot;post&quot; |
| REEL | &quot;reel&quot; |
| CAROUSEL | &quot;carousel&quot; |
| VIDEO | &quot;video&quot; |
| INTEGRATION | &quot;integration&quot; |
| DEDICATED | &quot;dedicated&quot; |
| SHORT | &quot;short&quot; |



## Enum: CurrencyEnum

| Name | Value |
|---- | -----|
| USD | &quot;USD&quot; |



