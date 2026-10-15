

# AccountConnectionHealthReconnectReason

Why the daily token check found the account's token dead, for an account that needs a reconnect; null otherwise. Codes: `meta_190_<subcode>` (Facebook, Instagram), `refresh_expired` (TikTok, Pinterest), `linkedin_revoked`, `linkedin_expired`, `google_revoked` (YouTube). 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**code** | **String** |  |  |
|**message** | **String** | The reason in plain language. |  |
|**foundAt** | **OffsetDateTime** | When the check first found the token dead. |  |



