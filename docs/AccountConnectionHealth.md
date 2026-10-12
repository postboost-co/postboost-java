

# AccountConnectionHealth

Connection health of an account (todo 27). Never contains token values.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | [**StatusEnum**](#StatusEnum) | &#x60;expired&#x60;: must be reconnected now. &#x60;expiring&#x60;: the connection hits its hard expiry within 7 days. &#x60;failing&#x60;: the latest publish attempt failed. &#x60;healthy&#x60;: none of these.  |  |
|**expiryKind** | [**ExpiryKindEnum**](#ExpiryKindEnum) | What limits the connection: &#x60;access&#x60; (the access token), &#x60;refresh&#x60; (the refresh token), &#x60;expired&#x60;, &#x60;unknown&#x60; (refreshed automatically, no known hard limit) or &#x60;none&#x60; (the network&#39;s connections do not expire on a schedule).  |  |
|**expiresAt** | **OffsetDateTime** | When the connection stops working unless reconnected; null without a hard expiry. |  |
|**daysLeft** | **Integer** | Whole days until &#x60;expires_at&#x60; (0 &#x3D; less than a day). |  |
|**refreshable** | **Boolean** | PostBoost refreshes the token automatically until the hard expiry. |  |
|**note** | **String** | Plain-language explanation of the prediction. |  |
|**lastSuccessAt** | **OffsetDateTime** | When the account last published successfully. |  |
|**lastError** | **String** | The error of the account&#39;s latest failed publish, shortened to 300 characters. |  |
|**reconnectUrl** | **URI** | Where a workspace member reconnects the account. |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| HEALTHY | &quot;healthy&quot; |
| FAILING | &quot;failing&quot; |
| EXPIRING | &quot;expiring&quot; |
| EXPIRED | &quot;expired&quot; |



## Enum: ExpiryKindEnum

| Name | Value |
|---- | -----|
| ACCESS | &quot;access&quot; |
| REFRESH | &quot;refresh&quot; |
| EXPIRED | &quot;expired&quot; |
| UNKNOWN | &quot;unknown&quot; |
| NONE | &quot;none&quot; |



