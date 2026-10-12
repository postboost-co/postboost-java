

# ApiActivity


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**userId** | **Integer** |  |  [optional] |
|**tokenRef** | **String** | First 12 hex characters of the SHA-256 of the API token used, to tell tokens apart. |  [optional] |
|**client** | **String** | &#x60;X-PostBoost-Client&#x60; header, else the &#x60;User-Agent&#x60;. |  [optional] |
|**routeName** | **String** |  |  [optional] |
|**method** | **String** |  |  |
|**postUuid** | **String** |  |  [optional] |
|**outcome** | **ApiActivityOutcome** |  |  |
|**httpStatus** | **Integer** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



