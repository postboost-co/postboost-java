

# FreeToolGetVideoSpecsResponseSpecsInnerLimits

The row as numbers, for checking a video.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**minSeconds** | **BigDecimal** | Shortest length. Null when the source states no figure. |  [optional] |
|**maxSeconds** | **BigDecimal** | Longest length. Null when the source states no figure. |  [optional] |
|**warnOverSeconds** | **BigDecimal** | Longer videos need a check (account type, reach), see &#x60;length&#x60;. Null when the source states no figure. |  [optional] |
|**minRatio** | **BigDecimal** | Narrowest width / height. Null when the source states no figure. |  [optional] |
|**maxRatio** | **BigDecimal** | Widest width / height. Null when the source states no figure. |  [optional] |
|**recommendedRatio** | **String** | Recommended ratio, e.g. &#x60;9:16&#x60;. |  [optional] |
|**maxMb** | **BigDecimal** | Largest file in MB. Null when the source states no figure. |  [optional] |



