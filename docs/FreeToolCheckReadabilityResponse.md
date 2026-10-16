

# FreeToolCheckReadabilityResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**supported** | **Boolean** | False for a language other than English: no scores, hints or suggestions. |  [optional] |
|**note** | **String** | Why the text was not scored, or null. |  [optional] |
|**fleschReadingEase** | **BigDecimal** | Flesch reading ease, one decimal: higher is easier, 60-70 is plain English. Null when not scored. |  [optional] |
|**fleschKincaidGrade** | **BigDecimal** | Flesch-Kincaid grade level, one decimal: the US school grade that can read the text. Null when not scored. |  [optional] |
|**sentences** | **Integer** | Sentences with at least one word. |  [optional] |
|**words** | **Integer** | Words, not counting hashtags, @mentions, links and emoji. |  [optional] |
|**syllables** | **Integer** | Syllables, by the heuristic described in the docs. |  [optional] |
|**avgWordsPerSentence** | **BigDecimal** | Words per sentence, one decimal. |  [optional] |
|**longSentences** | [**List&lt;FreeToolCheckReadabilityResponseLongSentencesInner&gt;**](FreeToolCheckReadabilityResponseLongSentencesInner.md) | Sentences of more than 25 words. |  [optional] |
|**passiveHints** | **Integer** | Possible passive phrases (\&quot;was written\&quot;, \&quot;is being reviewed\&quot;). A hint, not a grammar check. |  [optional] |
|**emojiCount** | **Integer** | Emoji (Extended_Pictographic characters). |  [optional] |
|**hashtagCount** | **Integer** | Hashtags. |  [optional] |
|**suggestions** | **List&lt;String&gt;** | Plain fixes, e.g. which sentence to split. Empty when the text reads easily. |  [optional] |



