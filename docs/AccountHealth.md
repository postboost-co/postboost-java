

# AccountHealth


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  |
|**uuid** | **UUID** |  |  |
|**name** | **String** |  |  |
|**provider** | **String** |  |  |
|**authorized** | **Boolean** | False when the account must be reconnected. |  |
|**hasToken** | **Boolean** | Whether an access token is stored for the account. |  |
|**healthy** | **Boolean** | &#x60;authorized&#x60; and &#x60;has_token&#x60;: the account can publish. |  |
|**dailyCap** | [**AccountHealthDailyCap**](AccountHealthDailyCap.md) |  |  |
|**connection** | [**AccountConnectionHealth**](AccountConnectionHealth.md) |  |  |



