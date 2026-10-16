

# FreeToolCalculateXApiCostResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**lineItems** | [**List&lt;FreeToolCalculateXApiCostResponseLineItemsInner&gt;**](FreeToolCalculateXApiCostResponseLineItemsInner.md) | One row per billed resource: count × unit price. |  [optional] |
|**totalUsd** | **BigDecimal** | Sum of every line item. |  [optional] |
|**linkPremiumUsd** | **BigDecimal** | What the link posts cost on top of the plain post price. |  [optional] |
|**notes** | **List&lt;String&gt;** |  |  [optional] |
|**pricesLastVerified** | **LocalDate** | When the prices were last checked against the source. |  [optional] |
|**source** | **URI** |  |  [optional] |



