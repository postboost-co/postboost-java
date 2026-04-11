# AiApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**blogToSocial**](AiApi.md#blogToSocial) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post |
| [**imageAltText**](AiApi.md#imageAltText) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI |
| [**imageEdit**](AiApi.md#imageEdit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI |
| [**imageGenerate**](AiApi.md#imageGenerate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption |
| [**imagePrompt**](AiApi.md#imagePrompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption |
| [**imageVariations**](AiApi.md#imageVariations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image |


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

<a id="imageAltText"></a>
# **imageAltText**
> ImageAltText200Response imageAltText(workspaceUuid, imageAltTextInput)

Generate alt text for a media image using AI

Analyzes an existing workspace media item and generates accessible alt text. The alt text is saved back to the media record. Costs 1 AI credit per call. 

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
    ImageAltTextInput imageAltTextInput = new ImageAltTextInput(); // ImageAltTextInput | 
    try {
      ImageAltText200Response result = apiInstance.imageAltText(workspaceUuid, imageAltTextInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#imageAltText");
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
| **imageAltTextInput** | [**ImageAltTextInput**](ImageAltTextInput.md)|  | |

### Return type

[**ImageAltText200Response**](ImageAltText200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Alt text generated and saved to media record |  -  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="imageEdit"></a>
# **imageEdit**
> ImageGenerate200Response imageEdit(workspaceUuid, imageEditInput)

Edit an existing media image using AI

Edits an existing workspace media item using the source image and a text prompt. Optionally accepts a mask (transparent areas are replaced). Saves results to the media library. Credits: &#x60;count × credit_weight&#x60;. 

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
    ImageEditInput imageEditInput = new ImageEditInput(); // ImageEditInput | 
    try {
      ImageGenerate200Response result = apiInstance.imageEdit(workspaceUuid, imageEditInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#imageEdit");
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
| **imageEditInput** | [**ImageEditInput**](ImageEditInput.md)|  | |

### Return type

[**ImageGenerate200Response**](ImageGenerate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Images edited and saved to media library |  -  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="imageGenerate"></a>
# **imageGenerate**
> ImageGenerate200Response imageGenerate(workspaceUuid, imageGenerateInput)

Generate social media images from a caption

Generates one or more images and saves them immediately to the workspace media library.  **Standard mode** (recommended): provide &#x60;caption&#x60; + &#x60;platform&#x60;. PostBoost builds a professional image prompt internally using platform-specific templates. No prompt engineering required.  **Developer mode**: provide &#x60;prompt&#x60; directly to bypass prompt building. If both &#x60;caption&#x60; and &#x60;prompt&#x60; are sent, standard mode runs.  Credits: &#x60;count x credit_weight&#x60; (default: 5 per image). 

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
    ImageGenerateInput imageGenerateInput = new ImageGenerateInput(); // ImageGenerateInput | 
    try {
      ImageGenerate200Response result = apiInstance.imageGenerate(workspaceUuid, imageGenerateInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#imageGenerate");
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
| **imageGenerateInput** | [**ImageGenerateInput**](ImageGenerateInput.md)|  | |

### Return type

[**ImageGenerate200Response**](ImageGenerate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Images generated and saved to media library |  -  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** | AI credits exhausted for this billing period |  -  |

<a id="imagePrompt"></a>
# **imagePrompt**
> ImagePrompt200Response imagePrompt(workspaceUuid, imagePromptInput)

Build an optimized image prompt from a social media caption

Builds a professional image generation prompt from a caption and platform. No image is generated. Use this to preview the prompt before calling &#x60;image-generate&#x60;. Costs 1 AI credit per call.  When &#x60;image-generate&#x60; builds the prompt internally (standard mode), no credit is charged for the prompt step. 

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
    ImagePromptInput imagePromptInput = new ImagePromptInput(); // ImagePromptInput | 
    try {
      ImagePrompt200Response result = apiInstance.imagePrompt(workspaceUuid, imagePromptInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#imagePrompt");
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
| **imagePromptInput** | [**ImagePromptInput**](ImagePromptInput.md)|  | |

### Return type

[**ImagePrompt200Response**](ImagePrompt200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Prompt built successfully |  -  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** | AI credits exhausted for this billing period |  -  |

<a id="imageVariations"></a>
# **imageVariations**
> ImageVariations200Response imageVariations(workspaceUuid, imageVariationsInput)

Generate variations of an existing media image

Creates one or more variations of an existing workspace media item. Saves results to the media library. Credits: &#x60;count × credit_weight&#x60;. 

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
    ImageVariationsInput imageVariationsInput = new ImageVariationsInput(); // ImageVariationsInput | 
    try {
      ImageVariations200Response result = apiInstance.imageVariations(workspaceUuid, imageVariationsInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#imageVariations");
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
| **imageVariationsInput** | [**ImageVariationsInput**](ImageVariationsInput.md)|  | |

### Return type

[**ImageVariations200Response**](ImageVariations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Variations generated and saved to media library |  -  |
| **401** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

