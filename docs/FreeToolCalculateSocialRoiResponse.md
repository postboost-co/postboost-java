

# FreeToolCalculateSocialRoiResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**period** | **String** |  |  [optional] |
|**revenue** | **BigDecimal** |  |  [optional] |
|**totalCost** | **BigDecimal** | Sum of every cost, labor &#x3D; hours × hourly rate. 2 decimals. |  [optional] |
|**netReturn** | **BigDecimal** | Revenue minus total cost. 2 decimals. |  [optional] |
|**roiPercent** | **BigDecimal** | (revenue − total cost) ÷ total cost × 100, 1 decimal; null when the total cost is 0. |  [optional] |
|**costBreakdown** | [**List&lt;FreeToolCalculateSocialRoiResponseCostBreakdownInner&gt;**](FreeToolCalculateSocialRoiResponseCostBreakdownInner.md) | Every cost above 0, with its share of the total cost (percent, 1 decimal). |  [optional] |
|**warnings** | **List&lt;String&gt;** |  |  [optional] |
|**formula** | **String** |  |  [optional] |



