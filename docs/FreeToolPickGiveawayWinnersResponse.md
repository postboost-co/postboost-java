

# FreeToolPickGiveawayWinnersResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**winners** | **List&lt;String&gt;** | Entrant keys in the drawn order. |  [optional] |
|**alternates** | **List&lt;String&gt;** | Entrant keys drawn after the winners, in order. |  [optional] |
|**entrantsBefore** | **Integer** | Comments received. |  [optional] |
|**entrantsAfter** | **Integer** | Entries left after the filters: the length of entrant_list. |  [optional] |
|**entrantList** | **List&lt;String&gt;** | The canonical entrant list to publish: keys sorted by UTF-8 bytes. Joined with \&quot;\\n\&quot; it is what entrants_hash hashes. |  [optional] |
|**entrantsHash** | **String** | SHA-256 (hex) of the canonical entrant list. |  [optional] |
|**fingerprint** | **String** | SHA-256 (hex) of the seed bytes: what to publish before the entries close. |  [optional] |
|**seed** | **String** | The seed used, lowercase hex. Publish it after the draw. |  [optional] |
|**preCommitted** | **Boolean** | False when the seed was generated for this draw, so no fingerprint could be published before it. |  [optional] |
|**algorithm** | [**AlgorithmEnum**](#AlgorithmEnum) |  |  [optional] |
|**warnings** | [**List&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: not_enough_entrants, not_pre_committed. |  [optional] |



## Enum: AlgorithmEnum

| Name | Value |
|---- | -----|
| PB_DRAW_V1 | &quot;pb-draw-v1&quot; |



