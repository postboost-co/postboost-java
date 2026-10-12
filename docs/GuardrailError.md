

# GuardrailError


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**message** | **String** |  |  |
|**code** | [**CodeEnum**](#CodeEnum) |  |  [optional] |
|**accountId** | **Integer** | The account the problem is about. |  [optional] |
|**existingPostUuid** | **UUID** | &#x60;duplicate_post&#x60; only: the earlier post with the same content. |  [optional] |
|**limit** | **Integer** | &#x60;account_daily_cap_reached&#x60; only: the account&#39;s daily cap. |  [optional] |
|**used** | **Integer** | &#x60;account_daily_cap_reached&#x60; only: posts already counted on that UTC day. |  [optional] |



## Enum: CodeEnum

| Name | Value |
|---- | -----|
| DUPLICATE_POST | &quot;duplicate_post&quot; |
| ACCOUNT_DAILY_CAP_REACHED | &quot;account_daily_cap_reached&quot; |
| ACCOUNT_UNAUTHORIZED | &quot;account_unauthorized&quot; |
| ACCOUNT_TOKEN_MISSING | &quot;account_token_missing&quot; |
| X_MONTHLY_CAP_REACHED | &quot;x_monthly_cap_reached&quot; |



