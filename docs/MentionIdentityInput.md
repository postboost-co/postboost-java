

# MentionIdentityInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**provider** | **String** | Mention provider key. One identity per provider. |  |
|**handle** | **String** | Profile handle; a leading &#x60;@&#x60; is stripped. |  |
|**label** | **String** |  |  [optional] |
|**token** | **String** | Sealed lookup result that names the profile&#39;s network ID. |  [optional] |
|**accountUuid** | **UUID** | A connected account of this workspace that names the profile. Wins over &#x60;token&#x60; when both are sent. |  [optional] |



