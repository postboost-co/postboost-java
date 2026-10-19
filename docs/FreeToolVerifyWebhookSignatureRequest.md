

# FreeToolVerifyWebhookSignatureRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**body** | **String** | The raw request body exactly as received (up to 64 KB). Use a test payload, not production data. |  |
|**secret** | **String** | The webhook secret. Use a test secret: never send a production secret to any third-party service. |  |
|**signature** | **String** | The received signature header value, e.g. X-Signature. |  |
|**algorithm** | [**AlgorithmEnum**](#AlgorithmEnum) |  |  [optional] |
|**encoding** | [**EncodingEnum**](#EncodingEnum) |  |  [optional] |
|**prefix** | **String** | A prefix the sender puts before the signature, e.g. \&quot;sha256&#x3D;\&quot; (GitHub). |  [optional] |



## Enum: AlgorithmEnum

| Name | Value |
|---- | -----|
| SHA256 | &quot;sha256&quot; |
| SHA1 | &quot;sha1&quot; |
| SHA512 | &quot;sha512&quot; |



## Enum: EncodingEnum

| Name | Value |
|---- | -----|
| HEX | &quot;hex&quot; |
| BASE64 | &quot;base64&quot; |



