

# WebhookEnvelope

Body of every webhook delivery. Verify `X-Signature` (HMAC-SHA256 of the raw body with the webhook secret) before trusting it, and de-duplicate on `id`. See [Webhooks](/webhooks). 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**event** | [**EventEnum**](#EventEnum) |  |  |
|**id** | **UUID** | Delivery ID, one per event. Retries and manual resends repeat it. |  |
|**occurredAt** | **OffsetDateTime** | When the event happened (ISO 8601, UTC). |  |
|**workspaceUuid** | **UUID** | The workspace the event belongs to (null only on instance-wide system webhooks). Also sent as the &#x60;X-PostBoost-Workspace&#x60; header. |  |
|**data** | **Map&lt;String, Object&gt;** | The post (&#x60;post.*&#x60;, as &#x60;getPost&#x60; returns it, plus &#x60;account&#x60; on per-account events), the account (&#x60;account.*&#x60;) or the reply draft (&#x60;inbox.*&#x60;). |  |



## Enum: EventEnum

| Name | Value |
|---- | -----|
| POST_CREATED | &quot;post.created&quot; |
| POST_UPDATED | &quot;post.updated&quot; |
| POST_SCHEDULED | &quot;post.scheduled&quot; |
| POST_PUBLISHED | &quot;post.published&quot; |
| POST_PUBLISHING_FAILED | &quot;post.publishing_failed&quot; |
| POST_PUBLISHED_ALL | &quot;post.published_all&quot; |
| POST_DELETED | &quot;post.deleted&quot; |
| ACCOUNT_ADDED | &quot;account.added&quot; |
| ACCOUNT_UPDATED | &quot;account.updated&quot; |
| ACCOUNT_DELETED | &quot;account.deleted&quot; |
| ACCOUNT_TOKEN_EXPIRING | &quot;account.token_expiring&quot; |
| ACCOUNT_DISCONNECTED | &quot;account.disconnected&quot; |
| INBOX_DRAFT_CREATED | &quot;inbox.draft.created&quot; |
| INBOX_DRAFT_SENT | &quot;inbox.draft.sent&quot; |



