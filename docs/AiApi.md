# AiApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**blogToSocial**](AiApi.md#blogToSocial) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post |
| [**deleteBrandVoice**](AiApi.md#deleteBrandVoice) | **DELETE** /{workspaceUuid}/brand-voice | Delete the brand voice |
| [**getAIUsage**](AiApi.md#getAIUsage) | **GET** /{workspaceUuid}/usage/ai | AI credit usage |
| [**getBrandVoice**](AiApi.md#getBrandVoice) | **GET** /{workspaceUuid}/brand-voice | Get the brand voice |
| [**getRepurposeRun**](AiApi.md#getRepurposeRun) | **GET** /{workspaceUuid}/ai/repurpose/runs/{runId} | Get a repurpose run |
| [**imageAltText**](AiApi.md#imageAltText) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI |
| [**imageEdit**](AiApi.md#imageEdit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI |
| [**imageGenerate**](AiApi.md#imageGenerate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption |
| [**imagePrompt**](AiApi.md#imagePrompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption |
| [**imageVariations**](AiApi.md#imageVariations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image |
| [**learnBrandVoice**](AiApi.md#learnBrandVoice) | **POST** /{workspaceUuid}/brand-voice/learn | Learn a brand voice from past posts |
| [**repurposeContent**](AiApi.md#repurposeContent) | **POST** /{workspaceUuid}/ai/repurpose | Repurpose long-form content into a draft post set with a carousel |
| [**updateBrandVoice**](AiApi.md#updateBrandVoice) | **PUT** /{workspaceUuid}/brand-voice | Create or update the brand voice |


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

<a id="deleteBrandVoice"></a>
# **deleteBrandVoice**
> Object deleteBrandVoice(workspaceUuid)

Delete the brand voice

Removes the workspace&#39;s brand voice. AI endpoints then run without one. Admins and members only.

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
    try {
      Object result = apiInstance.deleteBrandVoice(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#deleteBrandVoice");
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

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="getAIUsage"></a>
# **getAIUsage**
> AIUsage getAIUsage(workspaceUuid)

AI credit usage

The workspace&#39;s AI credits: text credits (captions, rewrites, outlines, alt text; counted per billing cycle) and image credits (one per generated, edited or varied image, and one per repurpose carousel; counted per calendar month, UTC). &#x60;limit&#x60; and &#x60;remaining&#x60; are &#x60;null&#x60; when the workspace has no limit. Readable when credits are used up; costs nothing.  When image credits run out, the image endpoints and carousels answer &#x60;429&#x60; with &#x60;code: image_credits_exhausted&#x60;; when text credits run out, the AI endpoints answer &#x60;429&#x60; with &#x60;code: ai_credits_exhausted&#x60;. Image endpoint responses also carry &#x60;image_credits_used&#x60; and &#x60;image_credits_remaining&#x60;; their &#x60;credits_used&#x60; counts text credits only. If the image pool is switched off (&#x60;image.enabled: false&#x60;), images cost text credits as before. 

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
    try {
      AIUsage result = apiInstance.getAIUsage(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#getAIUsage");
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

### Return type

[**AIUsage**](AIUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Credit usage |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="getBrandVoice"></a>
# **getBrandVoice**
> GetBrandVoice200Response getBrandVoice(workspaceUuid)

Get the brand voice

The workspace&#39;s brand voice: identity, audience, tone sliders, style rules and example posts. It is the same profile as the Brand Voice page in the app (one per workspace). &#x60;data&#x60; is &#x60;null&#x60; when no voice is set. Any workspace member may read it; reading costs no AI credits.  The AI endpoints apply it automatically: &#x60;blog-to-social&#x60; adds it to the caption instructions, &#x60;image-prompt&#x60; and &#x60;image-generate&#x60; turn it into a short visual tone line, and &#x60;image-edit&#x60; applies it when you send &#x60;use_brand_voice: true&#x60;. &#x60;image-variations&#x60; and &#x60;image-alt-text&#x60; never use it (alt text must describe the image literally). Send &#x60;use_brand_voice: false&#x60; to skip it on a call; responses report &#x60;meta.brand_voice_applied&#x60;. 

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
    try {
      GetBrandVoice200Response result = apiInstance.getBrandVoice(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#getBrandVoice");
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

### Return type

[**GetBrandVoice200Response**](GetBrandVoice200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The brand voice, or &#x60;null&#x60; when none is set |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="getRepurposeRun"></a>
# **getRepurposeRun**
> GetRepurposeRun200Response getRepurposeRun(workspaceUuid, runId)

Get a repurpose run

Status of a run started by &#x60;repurposeContent&#x60;. &#x60;queued&#x60; and &#x60;running&#x60; mean it is still going; poll again in a few seconds. A run that has not finished after 10 minutes reports &#x60;failed&#x60;. &#x60;result&#x60; holds the same &#x60;data&#x60; body a &#x60;200&#x60; from &#x60;repurposeContent&#x60; returns, for one hour after the run ended with &#x60;ok&#x60; or &#x60;partial&#x60;; after that it is &#x60;null&#x60; (the draft post stays). Limited to 60 calls per minute. 

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
    Integer runId = 56; // Integer | The `run_id` from `repurposeContent`.
    try {
      GetRepurposeRun200Response result = apiInstance.getRepurposeRun(workspaceUuid, runId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#getRepurposeRun");
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
| **runId** | **Integer**| The &#x60;run_id&#x60; from &#x60;repurposeContent&#x60;. | |

### Return type

[**GetRepurposeRun200Response**](GetRepurposeRun200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Run status |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

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
| **403** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="imageEdit"></a>
# **imageEdit**
> ImageGenerate200Response imageEdit(workspaceUuid, imageEditInput)

Edit an existing media image using AI

Edits an existing workspace media item using the source image and a text prompt. Optionally accepts a mask (transparent areas are replaced). Saves results to the media library. Credits: 1 image credit per image (&#x60;429 image_credits_exhausted&#x60; when the monthly pool is empty). If the image pool is switched off, &#x60;count × credit_weight&#x60; text credits instead. 

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
| **403** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="imageGenerate"></a>
# **imageGenerate**
> ImageGenerate200Response imageGenerate(workspaceUuid, imageGenerateInput)

Generate social media images from a caption

Generates one or more images and saves them immediately to the workspace media library.  **Standard mode** (recommended): provide &#x60;caption&#x60; + &#x60;platform&#x60;. PostBoost builds a professional image prompt internally using platform-specific templates. No prompt engineering required.  **Developer mode**: provide &#x60;prompt&#x60; directly to bypass prompt building. If both &#x60;caption&#x60; and &#x60;prompt&#x60; are sent, standard mode runs.  Credits: 1 image credit per image (&#x60;429 image_credits_exhausted&#x60; when the monthly pool is empty). If the image pool is switched off, &#x60;count × credit_weight&#x60; text credits instead. 

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
| **403** |  |  -  |
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
| **403** |  |  -  |
| **422** |  |  -  |
| **429** | AI credits exhausted for this billing period |  -  |

<a id="imageVariations"></a>
# **imageVariations**
> ImageVariations200Response imageVariations(workspaceUuid, imageVariationsInput)

Generate variations of an existing media image

Creates one or more variations of an existing workspace media item. Saves results to the media library. Credits: 1 image credit per image (&#x60;429 image_credits_exhausted&#x60; when the monthly pool is empty). If the image pool is switched off, &#x60;count × credit_weight&#x60; text credits instead. 

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
| **403** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="learnBrandVoice"></a>
# **learnBrandVoice**
> LearnBrandVoiceResponse learnBrandVoice(workspaceUuid, learnBrandVoiceInput)

Learn a brand voice from past posts

Reads the workspace&#39;s latest published posts (original text) and proposes a brand voice in the same shape as &#x60;GET /brand-voice&#x60;. Returns a draft and saves nothing unless &#x60;apply: true&#x60;.  Without &#x60;overwrite&#x60;, learned values only fill fields that are empty (tone sliders and styles still at their defaults count as empty); with &#x60;overwrite: true&#x60; they replace them. The first five sampled posts become &#x60;example_posts&#x60;. Needs at least 3 published posts (&#x60;422&#x60;, &#x60;code: not_enough_posts&#x60;). Costs one AI text credit per AI call (one retry when the reply is not usable). Admins and members only. A key limited to some accounts must send &#x60;account_ids&#x60;; only posts whose accounts are all among them are read. &#x60;apply&#x60; also needs the &#x60;write&#x60; ability. 

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
    LearnBrandVoiceInput learnBrandVoiceInput = new LearnBrandVoiceInput(); // LearnBrandVoiceInput | 
    try {
      LearnBrandVoiceResponse result = apiInstance.learnBrandVoice(workspaceUuid, learnBrandVoiceInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#learnBrandVoice");
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
| **learnBrandVoiceInput** | [**LearnBrandVoiceInput**](LearnBrandVoiceInput.md)|  | [optional] |

### Return type

[**LearnBrandVoiceResponse**](LearnBrandVoiceResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Proposed (or saved) brand voice |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** | Validation error, AI disabled, or fewer than 3 published posts (&#x60;code: not_enough_posts&#x60;) |  -  |
| **429** | AI text credits used up (&#x60;code: ai_credits_exhausted&#x60;) |  -  |
| **502** | The AI reply was not a usable profile (&#x60;code: ai_unusable_response&#x60;) |  -  |

<a id="repurposeContent"></a>
# **repurposeContent**
> RepurposeContent200Response repurposeContent(workspaceUuid, repurposeInput, idempotencyKey)

Repurpose long-form content into a draft post set with a carousel

Turns an article URL, a YouTube video, a PDF or pasted text into one **draft** post with a caption for every target account, plus a carousel of rendered slide images (hook, 1 to 6 idea slides, call to action; 1080×1350 PNG). Nothing is published or scheduled.  **Sources** (&#x60;source_type&#x60;): - &#x60;url&#x60;: the article is fetched and its main text extracted. - &#x60;youtube&#x60;: title, description and chapters come from YouTube; send the transcript in   &#x60;transcript&#x60; for better results (required when the description is short). - &#x60;pdf&#x60;: &#x60;pdf_url&#x60; must be a public PDF of at most 20 MB; the first 30 pages are read. - &#x60;text&#x60;: send &#x60;title&#x60; and &#x60;text&#x60;.  **Carousel per network**: Instagram, Facebook, Threads up to 10 slides; LinkedIn up to 9; X and Bluesky up to 4; other networks get the cover slide; YouTube and TikTok get none (listed in &#x60;warnings&#x60;). Without a carousel, the source image (article image or video thumbnail) is attached when available.  **AI credits**: one per target account plus one for the carousel outline. Slides are drawn without AI and cost nothing. The workspace brand voice applies unless &#x60;use_brand_voice&#x60; is &#x60;false&#x60;. Send an &#x60;Idempotency-Key&#x60; so a retried call does not create a second draft. Limited to 10 calls per minute.  **Long runs**: the run is queued. The call waits up to 20 seconds and answers &#x60;200&#x60; with the result when the run finished by then. Otherwise it answers &#x60;202&#x60; with a &#x60;run_id&#x60;; poll &#x60;getRepurposeRun&#x60; (&#x60;status_url&#x60;) every few seconds until the status is &#x60;ok&#x60;, &#x60;partial&#x60; or &#x60;failed&#x60;. Send &#x60;async: true&#x60; to get the &#x60;202&#x60; right away. Validation, account and credit errors are answered before anything is queued. 

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
    RepurposeInput repurposeInput = new RepurposeInput(); // RepurposeInput | 
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    try {
      RepurposeContent200Response result = apiInstance.repurposeContent(workspaceUuid, repurposeInput, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#repurposeContent");
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
| **repurposeInput** | [**RepurposeInput**](RepurposeInput.md)|  | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**RepurposeContent200Response**](RepurposeContent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Draft post set created |  -  |
| **202** | The run is still going (or &#x60;async&#x60; was set); poll &#x60;status_url&#x60;. |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |
| **500** | The run failed while the call waited. &#x60;getRepurposeRun&#x60; shows the error. |  -  |

<a id="updateBrandVoice"></a>
# **updateBrandVoice**
> GetBrandVoice200Response updateBrandVoice(workspaceUuid, brandVoiceInput)

Create or update the brand voice

Creates the workspace&#39;s brand voice or updates it. Fields you leave out keep their current value. Admins and members only (not viewers); the workspace must have AI enabled. 

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
    BrandVoiceInput brandVoiceInput = new BrandVoiceInput(); // BrandVoiceInput | 
    try {
      GetBrandVoice200Response result = apiInstance.updateBrandVoice(workspaceUuid, brandVoiceInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AiApi#updateBrandVoice");
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
| **brandVoiceInput** | [**BrandVoiceInput**](BrandVoiceInput.md)|  | |

### Return type

[**GetBrandVoice200Response**](GetBrandVoice200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The saved brand voice |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

