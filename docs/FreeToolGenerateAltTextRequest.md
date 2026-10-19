

# FreeToolGenerateAltTextRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**imageBase64** | **String** | The image itself, base64-encoded without a &#x60;data:&#x60; prefix: JPEG, PNG, WebP or GIF (first frame), up to 5 MB. On the API you can upload the file as &#x60;image&#x60; in a multipart/form-data body instead. A request to the MCP server at /mcp/tools may be at most 1.5 MB, so send larger images as &#x60;image_url&#x60; there. Send this or &#x60;image_url&#x60;. |  [optional] |
|**imageUrl** | **String** | A public https URL of the image, up to 5 MB. Fetched once and never stored; each fetch also counts against the daily limit of the tools that load a URL. Send this or &#x60;image_base64&#x60;. |  [optional] |
|**context** | **String** | Optional: what the post is about, so the text describes what matters for it. |  [optional] |
|**length** | [**LengthEnum**](#LengthEnum) | short (up to 125 characters) or detailed (up to 250). |  [optional] |
|**workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). |  [optional] |



## Enum: LengthEnum

| Name | Value |
|---- | -----|
| SHORT | &quot;short&quot; |
| DETAILED | &quot;detailed&quot; |



