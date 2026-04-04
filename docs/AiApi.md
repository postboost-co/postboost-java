# AiApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**blogToSocial**](AiApi.md#blogToSocial) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post |


<a id="blogToSocial"></a>
# **blogToSocial**
> BlogToSocial200Response blogToSocial(workspaceUuid, blogToSocialInput)

Generate social media captions from a blog post

Generates platform-specific social media captions from a blog post URL or directly provided title and excerpt. Each platform generates one caption, which consumes one AI credit from the workspace&#39;s monthly allowance.  **Input modes** (at least one required): - **URL mode**: provide &#x60;url&#x60; and the API scrapes the blog content automatically, including detecting the featured image via &#x60;og:image&#x60;. - **Direct mode**: provide &#x60;title&#x60; and &#x60;excerpt&#x60; directly (no scraping).  If both are provided, direct values take priority.  When &#x60;create_post&#x60; is &#x60;true&#x60;, a draft post is created in the workspace with per-account caption versions. If an image is available (from &#x60;image_url&#x60; or the scraped &#x60;og:image&#x60;), it is imported into the workspace media library and attached to the draft post. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AiApi apiInstance = new AiApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    BlogToSocialInput blogToSocialInput = new BlogToSocialInput(); // BlogToSocialInput | 
    try {
      BlogToSocial200Response result = apiInstance.blogToSocial(workspaceUuid, blogToSocialInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#blogToSocial");
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
| **workspaceUuid** | **UUID**| UUID of the workspace. | |
| **blogToSocialInput** | [**BlogToSocialInput**](BlogToSocialInput.md)|  | |

### Return type

[**BlogToSocial200Response**](BlogToSocial200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Captions generated successfully |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |
| **429** | AI credits exhausted for this billing period |  -  |

