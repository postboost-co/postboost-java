# FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**buildUtmUrl**](FreeToolsApi.md#buildUtmUrl) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL |
| [**calculateEngagementRate**](FreeToolsApi.md#calculateEngagementRate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate |
| [**checkPost**](FreeToolsApi.md#checkPost) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules |
| [**cleanText**](FreeToolsApi.md#cleanText) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown |
| [**countCharacters**](FreeToolsApi.md#countCharacters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them |
| [**formatLinkedInPost**](FreeToolsApi.md#formatLinkedInPost) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists |
| [**generateFancyText**](FreeToolsApi.md#generateFancyText) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles |
| [**listFreeTools**](FreeToolsApi.md#listFreeTools) | **GET** /tools | List the free tools |
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

