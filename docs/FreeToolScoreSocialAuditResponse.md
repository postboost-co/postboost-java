

# FreeToolScoreSocialAuditResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**score** | **Integer** | Overall score: all points over the maximum, as 0-100 rounded half up. |  [optional] |
|**networks** | [**List&lt;FreeToolScoreSocialAuditResponseNetworksInner&gt;**](FreeToolScoreSocialAuditResponseNetworksInner.md) | One row per audited network, in a fixed network order. |  [optional] |
|**topFixes** | [**List&lt;FreeToolScoreSocialAuditResponseTopFixesInner&gt;**](FreeToolScoreSocialAuditResponseTopFixesInner.md) | Up to 3 questions with the fewest points over all audited networks (ties: checklist order); only questions answered below yes somewhere. |  [optional] |
|**reportMarkdown** | **String** | The scorecard as a Markdown report: overall score, top fixes and every answer per network. |  [optional] |



