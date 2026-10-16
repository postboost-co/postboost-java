# FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**buildUtmUrl**](FreeToolsApi.md#buildUtmUrl) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL |
| [**calculateCrop**](FreeToolsApi.md#calculateCrop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size |
| [**calculateEngagementRate**](FreeToolsApi.md#calculateEngagementRate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate |
| [**checkPost**](FreeToolsApi.md#checkPost) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules |
| [**cleanText**](FreeToolsApi.md#cleanText) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown |
| [**countCharacters**](FreeToolsApi.md#countCharacters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them |
| [**formatLinkedInPost**](FreeToolsApi.md#formatLinkedInPost) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists |
| [**generateCaption**](FreeToolsApi.md#generateCaption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits) |
| [**generateFancyText**](FreeToolsApi.md#generateFancyText) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles |
| [**generateHashtags**](FreeToolsApi.md#generateHashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits) |
| [**getBestTimesToPost**](FreeToolsApi.md#getBestTimesToPost) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources |
| [**getImageSizes**](FreeToolsApi.md#getImageSizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source |
| [**listFreeTools**](FreeToolsApi.md#listFreeTools) | **GET** /tools | List the free tools |
| [**previewPost**](FreeToolsApi.md#previewPost) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook |
| [**splitThread**](FreeToolsApi.md#splitThread) | **POST** /tools/x-thread-maker | Split long text into a thread |


<a id="buildUtmUrl"></a>
# **buildUtmUrl**
> FreeToolBuildUtmUrlResponse buildUtmUrl(freeToolBuildUtmUrlRequest)

Build a UTM-tagged campaign URL

Build a UTM-tagged campaign URL. The same logic as the free web tool at https://postboost.co/tools/utm-builder. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolBuildUtmUrlRequest freeToolBuildUtmUrlRequest = new FreeToolBuildUtmUrlRequest(); // FreeToolBuildUtmUrlRequest | 
    try {
      FreeToolBuildUtmUrlResponse result = apiInstance.buildUtmUrl(freeToolBuildUtmUrlRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#buildUtmUrl");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolBuildUtmUrlRequest** | [**FreeToolBuildUtmUrlRequest**](FreeToolBuildUtmUrlRequest.md)|  | |

### Return type

[**FreeToolBuildUtmUrlResponse**](FreeToolBuildUtmUrlResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="calculateCrop"></a>
# **calculateCrop**
> FreeToolCalculateCropResponse calculateCrop(freeToolCalculateCropRequest)

Calculate the crop box that fits an image to a social media size

Calculate the crop box that fits an image to a social media size. The same logic as the free web tool at https://postboost.co/tools/social-media-image-sizes. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolCalculateCropRequest freeToolCalculateCropRequest = new FreeToolCalculateCropRequest(); // FreeToolCalculateCropRequest | 
    try {
      FreeToolCalculateCropResponse result = apiInstance.calculateCrop(freeToolCalculateCropRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateCrop");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolCalculateCropRequest** | [**FreeToolCalculateCropRequest**](FreeToolCalculateCropRequest.md)|  | |

### Return type

[**FreeToolCalculateCropResponse**](FreeToolCalculateCropResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="calculateEngagementRate"></a>
# **calculateEngagementRate**
> FreeToolCalculateEngagementRateResponse calculateEngagementRate(freeToolCalculateEngagementRateRequest)

Calculate an engagement rate

Calculate an engagement rate. The same logic as the free web tool at https://postboost.co/tools/engagement-rate-calculator. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolCalculateEngagementRateRequest freeToolCalculateEngagementRateRequest = new FreeToolCalculateEngagementRateRequest(); // FreeToolCalculateEngagementRateRequest | 
    try {
      FreeToolCalculateEngagementRateResponse result = apiInstance.calculateEngagementRate(freeToolCalculateEngagementRateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateEngagementRate");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolCalculateEngagementRateRequest** | [**FreeToolCalculateEngagementRateRequest**](FreeToolCalculateEngagementRateRequest.md)|  | |

### Return type

[**FreeToolCalculateEngagementRateResponse**](FreeToolCalculateEngagementRateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="checkPost"></a>
# **checkPost**
> FreeToolCheckPostResponse checkPost(freeToolCheckPostRequest)

Check a post against each network&#39;s publishing rules

Check a post against each network&#39;s publishing rules. The same logic as the free web tool at https://postboost.co/tools/social-media-post-checker. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolCheckPostRequest freeToolCheckPostRequest = new FreeToolCheckPostRequest(); // FreeToolCheckPostRequest | 
    try {
      FreeToolCheckPostResponse result = apiInstance.checkPost(freeToolCheckPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#checkPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolCheckPostRequest** | [**FreeToolCheckPostRequest**](FreeToolCheckPostRequest.md)|  | |

### Return type

[**FreeToolCheckPostResponse**](FreeToolCheckPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="cleanText"></a>
# **cleanText**
> FreeToolCleanTextResponse cleanText(freeToolCleanTextRequest)

Clean AI-written text: dashes, quotes, invisible characters, markdown

Clean AI-written text: dashes, quotes, invisible characters, markdown. The same logic as the free web tool at https://postboost.co/tools/ai-text-cleaner. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolCleanTextRequest freeToolCleanTextRequest = new FreeToolCleanTextRequest(); // FreeToolCleanTextRequest | 
    try {
      FreeToolCleanTextResponse result = apiInstance.cleanText(freeToolCleanTextRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#cleanText");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolCleanTextRequest** | [**FreeToolCleanTextRequest**](FreeToolCleanTextRequest.md)|  | |

### Return type

[**FreeToolCleanTextResponse**](FreeToolCleanTextResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="countCharacters"></a>
# **countCharacters**
> FreeToolCountCharactersResponse countCharacters(freeToolCountCharactersRequest)

Count characters as each network counts them

Count characters as each network counts them. The same logic as the free web tool at https://postboost.co/tools/social-media-character-counter. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolCountCharactersRequest freeToolCountCharactersRequest = new FreeToolCountCharactersRequest(); // FreeToolCountCharactersRequest | 
    try {
      FreeToolCountCharactersResponse result = apiInstance.countCharacters(freeToolCountCharactersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#countCharacters");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolCountCharactersRequest** | [**FreeToolCountCharactersRequest**](FreeToolCountCharactersRequest.md)|  | |

### Return type

[**FreeToolCountCharactersResponse**](FreeToolCountCharactersResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="formatLinkedInPost"></a>
# **formatLinkedInPost**
> FreeToolFormatLinkedInPostResponse formatLinkedInPost(freeToolFormatLinkedInPostRequest)

Format a LinkedIn post with bold, italic and lists

Format a LinkedIn post with bold, italic and lists. The same logic as the free web tool at https://postboost.co/tools/linkedin-post-formatter. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolFormatLinkedInPostRequest freeToolFormatLinkedInPostRequest = new FreeToolFormatLinkedInPostRequest(); // FreeToolFormatLinkedInPostRequest | 
    try {
      FreeToolFormatLinkedInPostResponse result = apiInstance.formatLinkedInPost(freeToolFormatLinkedInPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#formatLinkedInPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolFormatLinkedInPostRequest** | [**FreeToolFormatLinkedInPostRequest**](FreeToolFormatLinkedInPostRequest.md)|  | |

### Return type

[**FreeToolFormatLinkedInPostResponse**](FreeToolFormatLinkedInPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="generateCaption"></a>
# **generateCaption**
> FreeToolGenerateCaptionResponse generateCaption(freeToolGenerateCaptionRequest)

Write three post captions for a topic with AI (needs a token, spends AI credits)

Write three post captions for a topic with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-caption-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolGenerateCaptionRequest freeToolGenerateCaptionRequest = new FreeToolGenerateCaptionRequest(); // FreeToolGenerateCaptionRequest | 
    try {
      FreeToolGenerateCaptionResponse result = apiInstance.generateCaption(freeToolGenerateCaptionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateCaption");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolGenerateCaptionRequest** | [**FreeToolGenerateCaptionRequest**](FreeToolGenerateCaptionRequest.md)|  | |

### Return type

[**FreeToolGenerateCaptionResponse**](FreeToolGenerateCaptionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** | No API token, or an invalid one. The body has &#x60;register_url&#x60; to create a free account. |  -  |
| **403** | &#x60;workspace&#x60; is not a workspace you belong to, or your account has no workspace, or a scoped API key lacks the &#x60;ai&#x60; ability or is bound to another workspace (&#x60;code: insufficient_scope&#x60;). |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | The workspace has no AI credits left this billing cycle (&#x60;code: ai_credits_exhausted&#x60;, &#x60;upgrade_url&#x60;), or the per-minute limit was reached. Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
| **502** | The AI provider failed or timed out. No credit was spent. |  -  |
| **503** | AI tools are switched off right now. |  -  |

<a id="generateFancyText"></a>
# **generateFancyText**
> FreeToolGenerateFancyTextResponse generateFancyText(freeToolGenerateFancyTextRequest)

Convert text to fancy Unicode styles

Convert text to fancy Unicode styles. The same logic as the free web tool at https://postboost.co/tools/fancy-text-generator. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolGenerateFancyTextRequest freeToolGenerateFancyTextRequest = new FreeToolGenerateFancyTextRequest(); // FreeToolGenerateFancyTextRequest | 
    try {
      FreeToolGenerateFancyTextResponse result = apiInstance.generateFancyText(freeToolGenerateFancyTextRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateFancyText");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolGenerateFancyTextRequest** | [**FreeToolGenerateFancyTextRequest**](FreeToolGenerateFancyTextRequest.md)|  | |

### Return type

[**FreeToolGenerateFancyTextResponse**](FreeToolGenerateFancyTextResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="generateHashtags"></a>
# **generateHashtags**
> FreeToolGenerateHashtagsResponse generateHashtags(freeToolGenerateHashtagsRequest)

Generate hashtags for a post topic with AI (needs a token, spends AI credits)

Generate hashtags for a post topic with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-hashtag-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolGenerateHashtagsRequest freeToolGenerateHashtagsRequest = new FreeToolGenerateHashtagsRequest(); // FreeToolGenerateHashtagsRequest | 
    try {
      FreeToolGenerateHashtagsResponse result = apiInstance.generateHashtags(freeToolGenerateHashtagsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateHashtags");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolGenerateHashtagsRequest** | [**FreeToolGenerateHashtagsRequest**](FreeToolGenerateHashtagsRequest.md)|  | |

### Return type

[**FreeToolGenerateHashtagsResponse**](FreeToolGenerateHashtagsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** | No API token, or an invalid one. The body has &#x60;register_url&#x60; to create a free account. |  -  |
| **403** | &#x60;workspace&#x60; is not a workspace you belong to, or your account has no workspace, or a scoped API key lacks the &#x60;ai&#x60; ability or is bound to another workspace (&#x60;code: insufficient_scope&#x60;). |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | The workspace has no AI credits left this billing cycle (&#x60;code: ai_credits_exhausted&#x60;, &#x60;upgrade_url&#x60;), or the per-minute limit was reached. Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
| **502** | The AI provider failed or timed out. No credit was spent. |  -  |
| **503** | AI tools are switched off right now. |  -  |

<a id="getBestTimesToPost"></a>
# **getBestTimesToPost**
> FreeToolGetBestTimesToPostResponse getBestTimesToPost(network)

Get the best times to post per network from published studies, with sources

Get the best times to post per network from published studies, with sources. The same logic as the free web tool at https://postboost.co/tools/best-time-to-post. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    String network = "network_example"; // String | 
    try {
      FreeToolGetBestTimesToPostResponse result = apiInstance.getBestTimesToPost(network);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#getBestTimesToPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **network** | **String**|  | [optional] |

### Return type

[**FreeToolGetBestTimesToPostResponse**](FreeToolGetBestTimesToPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="getImageSizes"></a>
# **getImageSizes**
> FreeToolGetImageSizesResponse getImageSizes(network)

Get social media image sizes per network, each with its source

Get social media image sizes per network, each with its source. The same logic as the free web tool at https://postboost.co/tools/social-media-image-sizes. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    String network = "network_example"; // String | 
    try {
      FreeToolGetImageSizesResponse result = apiInstance.getImageSizes(network);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#getImageSizes");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **network** | **String**|  | [optional] |

### Return type

[**FreeToolGetImageSizesResponse**](FreeToolGetImageSizesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="listFreeTools"></a>
# **listFreeTools**
> FreeToolList listFreeTools()

List the free tools

Every free tool the API serves, with its operationId and web page. No token needed.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    try {
      FreeToolList result = apiInstance.listFreeTools();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#listFreeTools");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**FreeToolList**](FreeToolList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The free tools. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="previewPost"></a>
# **previewPost**
> FreeToolPreviewPostResponse previewPost(freeToolPreviewPostRequest)

Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook

Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook. The same logic as the free web tool at https://postboost.co/tools/social-media-post-preview. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolPreviewPostRequest freeToolPreviewPostRequest = new FreeToolPreviewPostRequest(); // FreeToolPreviewPostRequest | 
    try {
      FreeToolPreviewPostResponse result = apiInstance.previewPost(freeToolPreviewPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#previewPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolPreviewPostRequest** | [**FreeToolPreviewPostRequest**](FreeToolPreviewPostRequest.md)|  | |

### Return type

[**FreeToolPreviewPostResponse**](FreeToolPreviewPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="splitThread"></a>
# **splitThread**
> FreeToolSplitThreadResponse splitThread(freeToolSplitThreadRequest)

Split long text into a thread

Split long text into a thread. The same logic as the free web tool at https://postboost.co/tools/x-thread-maker. No account needed: call it without a token, or with any API token.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.models.*;
import com.postboost.api.FreeToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");

    FreeToolsApi apiInstance = new FreeToolsApi(defaultClient);
    FreeToolSplitThreadRequest freeToolSplitThreadRequest = new FreeToolSplitThreadRequest(); // FreeToolSplitThreadRequest | 
    try {
      FreeToolSplitThreadResponse result = apiInstance.splitThread(freeToolSplitThreadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#splitThread");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **freeToolSplitThreadRequest** | [**FreeToolSplitThreadRequest**](FreeToolSplitThreadRequest.md)|  | |

### Return type

[**FreeToolSplitThreadResponse**](FreeToolSplitThreadResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** |  |  -  |
| **413** | The request body is larger than 128 KB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

