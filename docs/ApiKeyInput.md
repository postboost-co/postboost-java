

# ApiKeyInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** |  |  |
|**abilities** | **List&lt;ApiKeyAbility&gt;** |  |  |
|**accountIds** | **List&lt;Integer&gt;** | Limit the key to these account ids of the workspace. Omit or null for every account. A limited key must send &#x60;account_ids&#x60; on recycling rules, report exports and AI drafts, and its lists show only its accounts. |  [optional] |
|**expiresAt** | **LocalDate** | Last day the key works. Must be after today. Omit for no expiry. |  [optional] |



