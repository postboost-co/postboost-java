

# InboxConversation


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Conversation UUID. |  |
|**provider** | **String** |  |  |
|**type** | [**TypeEnum**](#TypeEnum) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**unread** | **Boolean** |  |  |
|**sentiment** | **String** |  |  [optional] |
|**aiLabel** | **String** |  |  [optional] |
|**isSpam** | **Boolean** |  |  [optional] |
|**isHidden** | **Boolean** |  |  [optional] |
|**providerPostId** | **String** |  |  [optional] |
|**account** | [**InboxConversationAccount**](InboxConversationAccount.md) |  |  [optional] |
|**author** | [**InboxMessageAuthor**](InboxMessageAuthor.md) |  |  [optional] |
|**latestMessage** | **Object** | Only in lists. |  [optional] |
|**messages** | [**List&lt;InboxMessage&gt;**](InboxMessage.md) | Only on &#x60;GET inbox/conversations/{conversationId}&#x60;. |  [optional] |
|**lastMessageAt** | **OffsetDateTime** |  |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| COMMENT | &quot;comment&quot; |
| MENTION | &quot;mention&quot; |
| REVIEW | &quot;review&quot; |
| QA | &quot;qa&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| OPEN | &quot;open&quot; |
| RESOLVED | &quot;resolved&quot; |



