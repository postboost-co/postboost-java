

# FreeToolFormatLinkedInPostRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** |  |  |
|**style** | [**StyleEnum**](#StyleEnum) | Unicode style for the whole text, e.g. bold. |  [optional] |
|**_list** | [**ListEnum**](#ListEnum) | Prefix every non-empty line with \&quot;• \&quot; or \&quot;1. \&quot;, \&quot;2. \&quot; (plain digits). |  [optional] |



## Enum: StyleEnum

| Name | Value |
|---- | -----|
| BOLD | &quot;bold&quot; |
| ITALIC | &quot;italic&quot; |
| BOLD_ITALIC | &quot;bold_italic&quot; |
| SANS_BOLD | &quot;sans_bold&quot; |
| SANS_ITALIC | &quot;sans_italic&quot; |
| SCRIPT | &quot;script&quot; |
| BOLD_SCRIPT | &quot;bold_script&quot; |
| FRAKTUR | &quot;fraktur&quot; |
| DOUBLE_STRUCK | &quot;double_struck&quot; |
| MONOSPACE | &quot;monospace&quot; |
| SMALL_CAPS | &quot;small_caps&quot; |
| CIRCLED | &quot;circled&quot; |
| SQUARED | &quot;squared&quot; |
| UPSIDE_DOWN | &quot;upside_down&quot; |
| STRIKETHROUGH | &quot;strikethrough&quot; |



## Enum: ListEnum

| Name | Value |
|---- | -----|
| BULLET | &quot;bullet&quot; |
| NUMBERED | &quot;numbered&quot; |



