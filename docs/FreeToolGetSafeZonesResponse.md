

# FreeToolGetSafeZonesResponse

Approximate: platforms do not publish official overlay sizes for organic posts, and the UI varies by device and app version. The boxes come from each platform's guidance for vertical video ads.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**platform** | **String** |  |  [optional] |
|**label** | **String** | Platform name. |  [optional] |
|**width** | **Integer** |  |  [optional] |
|**height** | **Integer** |  |  [optional] |
|**unsafeAreas** | [**List&lt;FreeToolGetSafeZonesResponseUnsafeAreasInner&gt;**](FreeToolGetSafeZonesResponseUnsafeAreasInner.md) | Areas the app&#39;s UI usually covers, in frame pixels from the top-left corner. Edges are scaled from 1080 × 1920 and rounded to the nearest pixel (halves up), so neighbouring boxes stay edge to edge. |  [optional] |
|**safeArea** | [**FreeToolGetSafeZonesResponseSafeArea**](FreeToolGetSafeZonesResponseSafeArea.md) |  |  [optional] |
|**source** | [**FreeToolGetSafeZonesResponseSource**](FreeToolGetSafeZonesResponseSource.md) |  |  [optional] |
|**lastVerified** | **String** | Date the sources were last checked (YYYY-MM-DD). |  [optional] |
|**caveat** | **String** |  |  [optional] |
|**warnings** | **List&lt;String&gt;** | Set when the frame is not 9:16, so the boxes are stretched. |  [optional] |



