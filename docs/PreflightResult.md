

# PreflightResult


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**valid** | **Boolean** | True when create-post with the same body would succeed. Warnings do not change it. |  |
|**errors** | **Map&lt;String, List&lt;String&gt;&gt;** | Validation and network-requirement errors keyed by field, as create-post would report them in a &#x60;422&#x60;. |  |
|**issues** | [**List&lt;GuardrailError&gt;**](GuardrailError.md) | Guardrail problems, in the order create-post would report the first of them. |  |
|**warnings** | [**List&lt;PostWarning&gt;**](PostWarning.md) | The warnings create-post would return for the same body (same codes and messages); empty when there are none. |  |
|**publishAt** | **OffsetDateTime** | UTC time the post would publish at; null for a draft. |  |
|**accounts** | [**List&lt;AccountHealth&gt;**](AccountHealth.md) |  |  |



