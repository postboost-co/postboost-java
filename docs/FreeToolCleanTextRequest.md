

# FreeToolCleanTextRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**text** | **String** |  |  |
|**dashes** | [**DashesEnum**](#DashesEnum) | What replaces an em or en dash between words: \&quot;, \&quot; (comma), \&quot;-\&quot; (hyphen), \&quot; - \&quot; (spaced) or nothing (keep). Number ranges like 2020–2024 always get a hyphen. |  [optional] |
|**quotes** | **Boolean** | Curly quotes and apostrophes to straight ones. |  [optional] |
|**invisible** | **Boolean** | Remove zero-width characters and soft hyphens; turn non-breaking and thin spaces into normal spaces. |  [optional] |
|**spaces** | **Boolean** | Collapse double spaces between words and remove spaces at line ends. |  [optional] |
|**ellipsis** | **Boolean** | The ellipsis character to three dots. |  [optional] |
|**markdown** | **Boolean** | Strip **bold**, __bold__, *italic* and _italic_ markers, keeping the words. |  [optional] |
|**flagPhrases** | **Boolean** | List common AI phrases (e.g. \&quot;delve\&quot;) with their offsets. They are never changed. |  [optional] |



## Enum: DashesEnum

| Name | Value |
|---- | -----|
| COMMA | &quot;comma&quot; |
| HYPHEN | &quot;hyphen&quot; |
| SPACED | &quot;spaced&quot; |
| KEEP | &quot;keep&quot; |



