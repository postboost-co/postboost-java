

# PreflightResult


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**valid** | **Boolean** | True when create-post with the same body would succeed. |  |
|**errors** | **Map&lt;String, List&lt;String&gt;&gt;** | Validation and network-requirement errors keyed by field, as create-post would report them in a &#x60;422&#x60;. |  |
|**issues** | [**List&lt;GuardrailError&gt;**](GuardrailError.md) | Guardrail problems, in the order create-post would report the first of them. |  |
|**publishAt** | **OffsetDateTime** | UTC time the post would publish at; null for a draft. |  |
|**accounts** | [**List&lt;AccountHealth&gt;**](AccountHealth.md) |  |  |



