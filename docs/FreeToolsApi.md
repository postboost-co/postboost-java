# FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**buildAgentSkill**](FreeToolsApi.md#buildAgentSkill) | **POST** /tools/social-media-agent-skill-builder | Build a SKILL.md, AGENTS.md or system prompt for a social media agent |
| [**buildHashtagGroups**](FreeToolsApi.md#buildHashtagGroups) | **POST** /tools/hashtag-group-builder | Clean, dedupe and split hashtags into groups that fit a network&#39;s hashtag cap |
| [**buildLinkedinCarousel**](FreeToolsApi.md#buildLinkedinCarousel) | **POST** /tools/linkedin-carousel-maker | Turn text into LinkedIn carousel (PDF document) slides |
| [**buildUtmUrl**](FreeToolsApi.md#buildUtmUrl) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL |
| [**calculateAspectRatio**](FreeToolsApi.md#calculateAspectRatio) | **POST** /tools/aspect-ratio-calculator | Calculate an aspect ratio, or the missing side of an image at a given ratio |
| [**calculateCarouselSlices**](FreeToolsApi.md#calculateCarouselSlices) | **POST** /tools/instagram-carousel-splitter | Split a wide image into seamless Instagram carousel slides |
| [**calculateCrop**](FreeToolsApi.md#calculateCrop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size |
| [**calculateEngagementRate**](FreeToolsApi.md#calculateEngagementRate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate |
| [**calculateInfluencerRate**](FreeToolsApi.md#calculateInfluencerRate) | **POST** /tools/influencer-rate-calculator | Estimate an influencer&#39;s rate for one sponsored deliverable |
| [**calculateSmmPricing**](FreeToolsApi.md#calculateSmmPricing) | **POST** /tools/social-media-manager-pricing-calculator | Estimate social media manager pricing |
| [**calculateSocialRoi**](FreeToolsApi.md#calculateSocialRoi) | **POST** /tools/social-media-roi-calculator | Calculate social media ROI |
| [**calculateXApiCost**](FreeToolsApi.md#calculateXApiCost) | **POST** /tools/x-api-cost-calculator | Calculate the monthly X API cost |
| [**checkLinkPreview**](FreeToolsApi.md#checkLinkPreview) | **POST** /tools/link-preview-checker | Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags) |
| [**checkPost**](FreeToolsApi.md#checkPost) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules |
| [**checkReadability**](FreeToolsApi.md#checkReadability) | **POST** /tools/post-readability-checker | Check the readability of a post: Flesch scores, long sentences and passive hints |
| [**checkYoutubeThumbnail**](FreeToolsApi.md#checkYoutubeThumbnail) | **POST** /tools/youtube-thumbnail-size-checker | Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements |
| [**cleanText**](FreeToolsApi.md#cleanText) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown |
| [**countCharacters**](FreeToolsApi.md#countCharacters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them |
| [**findAutomationRecipes**](FreeToolsApi.md#findAutomationRecipes) | **GET** /tools/social-media-automation-recipes | Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API |
| [**formatCrossPost**](FreeToolsApi.md#formatCrossPost) | **POST** /tools/cross-post-formatter | Format one post for X, Threads, Bluesky, Mastodon and LinkedIn |
| [**formatInstagramCaption**](FreeToolsApi.md#formatInstagramCaption) | **POST** /tools/instagram-line-break-generator | Keep blank lines in an Instagram caption with spacer lines, and count it |
| [**formatLinkedInPost**](FreeToolsApi.md#formatLinkedInPost) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists |
| [**generateAltText**](FreeToolsApi.md#generateAltText) | **POST** /tools/alt-text-generator | Write alt text for an image with AI (needs a token, spends AI credits) |
| [**generateBio**](FreeToolsApi.md#generateBio) | **POST** /tools/instagram-bio-generator | Write five profile bios with AI (needs a token, spends AI credits) |
| [**generateCaption**](FreeToolsApi.md#generateCaption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits) |
| [**generateFancyText**](FreeToolsApi.md#generateFancyText) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles |
| [**generateHashtags**](FreeToolsApi.md#generateHashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits) |
| [**generateHooks**](FreeToolsApi.md#generateHooks) | **POST** /tools/hook-generator | Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits) |
| [**generateLinkedInHeadline**](FreeToolsApi.md#generateLinkedInHeadline) | **POST** /tools/linkedin-headline-generator | Write five LinkedIn profile headlines with AI (needs a token, spends AI credits) |
| [**generateQrCode**](FreeToolsApi.md#generateQrCode) | **POST** /tools/qr-code-generator | Generate a QR code (SVG) for a link or text, with optional UTM tags |
| [**generateSocialPostsFromBlog**](FreeToolsApi.md#generateSocialPostsFromBlog) | **POST** /tools/blog-to-social-media | Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits) |
| [**generateSocialPostsFromVideo**](FreeToolsApi.md#generateSocialPostsFromVideo) | **POST** /tools/youtube-to-social-posts | Turn a YouTube video&#39;s captions into an X thread and social captions with AI (needs a token, spends AI credits) |
| [**generateUsernames**](FreeToolsApi.md#generateUsernames) | **POST** /tools/social-media-username-generator | Generate social media usernames |
| [**generateYoutubeDescription**](FreeToolsApi.md#generateYoutubeDescription) | **POST** /tools/youtube-description-generator | Write three YouTube video descriptions with AI (needs a token, spends AI credits) |
| [**generateYoutubeTitles**](FreeToolsApi.md#generateYoutubeTitles) | **POST** /tools/youtube-title-generator | Write five YouTube video titles with AI (needs a token, spends AI credits) |
| [**getBestTimesToPost**](FreeToolsApi.md#getBestTimesToPost) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources |
| [**getGlossary**](FreeToolsApi.md#getGlossary) | **GET** /tools/social-media-glossary | Look up social media terms: plain-language definitions by category, with sources and related terms |
| [**getHookTemplates**](FreeToolsApi.md#getHookTemplates) | **GET** /tools/hook-generator/library | Get free hook templates for social media posts, filtered by style and network |
| [**getImageSizes**](FreeToolsApi.md#getImageSizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source |
| [**getSafeZones**](FreeToolsApi.md#getSafeZones) | **POST** /tools/safe-zone-checker | Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame |
| [**getVideoSpecs**](FreeToolsApi.md#getVideoSpecs) | **GET** /tools/social-media-video-specs | Get social media video ratios, resolutions, lengths and file size limits per network, with sources |
| [**listAwarenessDays**](FreeToolsApi.md#listAwarenessDays) | **GET** /tools/social-media-holiday-calendar | List public holidays, awareness days and social media days by date, country, type and topic, with sources |
| [**listFreeTools**](FreeToolsApi.md#listFreeTools) | **GET** /tools | List the free tools |
| [**pickGiveawayWinners**](FreeToolsApi.md#pickGiveawayWinners) | **POST** /tools/giveaway-comment-picker | Pick giveaway winners with a draw anyone can verify |
| [**pickSocialMediaTool**](FreeToolsApi.md#pickSocialMediaTool) | **POST** /tools/social-media-tool-picker | Match your needs against social media management tools and see what each one misses |
| [**planContentCalendar**](FreeToolsApi.md#planContentCalendar) | **POST** /tools/social-media-content-calendar-generator | Plan a social media content calendar and get it as CSV and ICS |
| [**planPostingFrequency**](FreeToolsApi.md#planPostingFrequency) | **POST** /tools/posting-frequency-planner | Plan how often to post on each network |
| [**previewPost**](FreeToolsApi.md#previewPost) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook |
| [**scoreSocialAudit**](FreeToolsApi.md#scoreSocialAudit) | **POST** /tools/social-media-audit-template | Score a social media audit checklist and get the top fixes |
| [**searchEmoji**](FreeToolsApi.md#searchEmoji) | **POST** /tools/social-media-emoji-picker | Search emoji by name or keyword, to copy and paste into a post |
| [**splitThread**](FreeToolsApi.md#splitThread) | **POST** /tools/x-thread-maker | Split long text into a thread |
| [**summarizeReport**](FreeToolsApi.md#summarizeReport) | **POST** /tools/social-media-report-generator | Summarize social media post metrics into a report |
| [**verifyWebhookSignature**](FreeToolsApi.md#verifyWebhookSignature) | **POST** /tools/webhook-signature-verifier | Verify an HMAC webhook signature |


<a id="buildAgentSkill"></a>
# **buildAgentSkill**
> FreeToolBuildAgentSkillResponse buildAgentSkill(freeToolBuildAgentSkillRequest)

Build a SKILL.md, AGENTS.md or system prompt for a social media agent

Build a SKILL.md, AGENTS.md or system prompt for a social media agent. The same logic as the free web tool at https://postboost.co/tools/social-media-agent-skill-builder. No account needed: call it without a token, or with any API token.

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
    FreeToolBuildAgentSkillRequest freeToolBuildAgentSkillRequest = new FreeToolBuildAgentSkillRequest(); // FreeToolBuildAgentSkillRequest | 
    try {
      FreeToolBuildAgentSkillResponse result = apiInstance.buildAgentSkill(freeToolBuildAgentSkillRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#buildAgentSkill");
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
| **freeToolBuildAgentSkillRequest** | [**FreeToolBuildAgentSkillRequest**](FreeToolBuildAgentSkillRequest.md)|  | |

### Return type

[**FreeToolBuildAgentSkillResponse**](FreeToolBuildAgentSkillResponse.md)

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

<a id="buildHashtagGroups"></a>
# **buildHashtagGroups**
> FreeToolBuildHashtagGroupsResponse buildHashtagGroups(freeToolBuildHashtagGroupsRequest)

Clean, dedupe and split hashtags into groups that fit a network&#39;s hashtag cap

Clean, dedupe and split hashtags into groups that fit a network&#39;s hashtag cap. The same logic as the free web tool at https://postboost.co/tools/hashtag-group-builder. No account needed: call it without a token, or with any API token.

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
    FreeToolBuildHashtagGroupsRequest freeToolBuildHashtagGroupsRequest = new FreeToolBuildHashtagGroupsRequest(); // FreeToolBuildHashtagGroupsRequest | 
    try {
      FreeToolBuildHashtagGroupsResponse result = apiInstance.buildHashtagGroups(freeToolBuildHashtagGroupsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#buildHashtagGroups");
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
| **freeToolBuildHashtagGroupsRequest** | [**FreeToolBuildHashtagGroupsRequest**](FreeToolBuildHashtagGroupsRequest.md)|  | |

### Return type

[**FreeToolBuildHashtagGroupsResponse**](FreeToolBuildHashtagGroupsResponse.md)

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

<a id="buildLinkedinCarousel"></a>
# **buildLinkedinCarousel**
> FreeToolBuildLinkedinCarouselResponse buildLinkedinCarousel(freeToolBuildLinkedinCarouselRequest)

Turn text into LinkedIn carousel (PDF document) slides

Turn text into LinkedIn carousel (PDF document) slides. The same logic as the free web tool at https://postboost.co/tools/linkedin-carousel-maker. No account needed: call it without a token, or with any API token.

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
    FreeToolBuildLinkedinCarouselRequest freeToolBuildLinkedinCarouselRequest = new FreeToolBuildLinkedinCarouselRequest(); // FreeToolBuildLinkedinCarouselRequest | 
    try {
      FreeToolBuildLinkedinCarouselResponse result = apiInstance.buildLinkedinCarousel(freeToolBuildLinkedinCarouselRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#buildLinkedinCarousel");
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
| **freeToolBuildLinkedinCarouselRequest** | [**FreeToolBuildLinkedinCarouselRequest**](FreeToolBuildLinkedinCarouselRequest.md)|  | |

### Return type

[**FreeToolBuildLinkedinCarouselResponse**](FreeToolBuildLinkedinCarouselResponse.md)

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

<a id="calculateAspectRatio"></a>
# **calculateAspectRatio**
> FreeToolCalculateAspectRatioResponse calculateAspectRatio(freeToolCalculateAspectRatioRequest)

Calculate an aspect ratio, or the missing side of an image at a given ratio

Calculate an aspect ratio, or the missing side of an image at a given ratio. The same logic as the free web tool at https://postboost.co/tools/aspect-ratio-calculator. No account needed: call it without a token, or with any API token.

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
    FreeToolCalculateAspectRatioRequest freeToolCalculateAspectRatioRequest = new FreeToolCalculateAspectRatioRequest(); // FreeToolCalculateAspectRatioRequest | 
    try {
      FreeToolCalculateAspectRatioResponse result = apiInstance.calculateAspectRatio(freeToolCalculateAspectRatioRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateAspectRatio");
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
| **freeToolCalculateAspectRatioRequest** | [**FreeToolCalculateAspectRatioRequest**](FreeToolCalculateAspectRatioRequest.md)|  | |

### Return type

[**FreeToolCalculateAspectRatioResponse**](FreeToolCalculateAspectRatioResponse.md)

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

<a id="calculateCarouselSlices"></a>
# **calculateCarouselSlices**
> FreeToolCalculateCarouselSlicesResponse calculateCarouselSlices(freeToolCalculateCarouselSlicesRequest)

Split a wide image into seamless Instagram carousel slides

Split a wide image into seamless Instagram carousel slides. The same logic as the free web tool at https://postboost.co/tools/instagram-carousel-splitter. No account needed: call it without a token, or with any API token.

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
    FreeToolCalculateCarouselSlicesRequest freeToolCalculateCarouselSlicesRequest = new FreeToolCalculateCarouselSlicesRequest(); // FreeToolCalculateCarouselSlicesRequest | 
    try {
      FreeToolCalculateCarouselSlicesResponse result = apiInstance.calculateCarouselSlices(freeToolCalculateCarouselSlicesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateCarouselSlices");
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
| **freeToolCalculateCarouselSlicesRequest** | [**FreeToolCalculateCarouselSlicesRequest**](FreeToolCalculateCarouselSlicesRequest.md)|  | |

### Return type

[**FreeToolCalculateCarouselSlicesResponse**](FreeToolCalculateCarouselSlicesResponse.md)

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

<a id="calculateInfluencerRate"></a>
# **calculateInfluencerRate**
> FreeToolCalculateInfluencerRateResponse calculateInfluencerRate(freeToolCalculateInfluencerRateRequest)

Estimate an influencer&#39;s rate for one sponsored deliverable

Estimate an influencer&#39;s rate for one sponsored deliverable. The same logic as the free web tool at https://postboost.co/tools/influencer-rate-calculator. No account needed: call it without a token, or with any API token.

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
    FreeToolCalculateInfluencerRateRequest freeToolCalculateInfluencerRateRequest = new FreeToolCalculateInfluencerRateRequest(); // FreeToolCalculateInfluencerRateRequest | 
    try {
      FreeToolCalculateInfluencerRateResponse result = apiInstance.calculateInfluencerRate(freeToolCalculateInfluencerRateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateInfluencerRate");
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
| **freeToolCalculateInfluencerRateRequest** | [**FreeToolCalculateInfluencerRateRequest**](FreeToolCalculateInfluencerRateRequest.md)|  | |

### Return type

[**FreeToolCalculateInfluencerRateResponse**](FreeToolCalculateInfluencerRateResponse.md)

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

<a id="calculateSmmPricing"></a>
# **calculateSmmPricing**
> FreeToolCalculateSmmPricingResponse calculateSmmPricing(freeToolCalculateSmmPricingRequest)

Estimate social media manager pricing

Estimate social media manager pricing. The same logic as the free web tool at https://postboost.co/tools/social-media-manager-pricing-calculator. No account needed: call it without a token, or with any API token.

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
    FreeToolCalculateSmmPricingRequest freeToolCalculateSmmPricingRequest = new FreeToolCalculateSmmPricingRequest(); // FreeToolCalculateSmmPricingRequest | 
    try {
      FreeToolCalculateSmmPricingResponse result = apiInstance.calculateSmmPricing(freeToolCalculateSmmPricingRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateSmmPricing");
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
| **freeToolCalculateSmmPricingRequest** | [**FreeToolCalculateSmmPricingRequest**](FreeToolCalculateSmmPricingRequest.md)|  | |

### Return type

[**FreeToolCalculateSmmPricingResponse**](FreeToolCalculateSmmPricingResponse.md)

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

<a id="calculateSocialRoi"></a>
# **calculateSocialRoi**
> FreeToolCalculateSocialRoiResponse calculateSocialRoi(freeToolCalculateSocialRoiRequest)

Calculate social media ROI

Calculate social media ROI. The same logic as the free web tool at https://postboost.co/tools/social-media-roi-calculator. No account needed: call it without a token, or with any API token.

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
    FreeToolCalculateSocialRoiRequest freeToolCalculateSocialRoiRequest = new FreeToolCalculateSocialRoiRequest(); // FreeToolCalculateSocialRoiRequest | 
    try {
      FreeToolCalculateSocialRoiResponse result = apiInstance.calculateSocialRoi(freeToolCalculateSocialRoiRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateSocialRoi");
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
| **freeToolCalculateSocialRoiRequest** | [**FreeToolCalculateSocialRoiRequest**](FreeToolCalculateSocialRoiRequest.md)|  | |

### Return type

[**FreeToolCalculateSocialRoiResponse**](FreeToolCalculateSocialRoiResponse.md)

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

<a id="calculateXApiCost"></a>
# **calculateXApiCost**
> FreeToolCalculateXApiCostResponse calculateXApiCost(freeToolCalculateXApiCostRequest)

Calculate the monthly X API cost

Calculate the monthly X API cost. The same logic as the free web tool at https://postboost.co/tools/x-api-cost-calculator. No account needed: call it without a token, or with any API token.

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
    FreeToolCalculateXApiCostRequest freeToolCalculateXApiCostRequest = new FreeToolCalculateXApiCostRequest(); // FreeToolCalculateXApiCostRequest | 
    try {
      FreeToolCalculateXApiCostResponse result = apiInstance.calculateXApiCost(freeToolCalculateXApiCostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#calculateXApiCost");
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
| **freeToolCalculateXApiCostRequest** | [**FreeToolCalculateXApiCostRequest**](FreeToolCalculateXApiCostRequest.md)|  | |

### Return type

[**FreeToolCalculateXApiCostResponse**](FreeToolCalculateXApiCostResponse.md)

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

<a id="checkLinkPreview"></a>
# **checkLinkPreview**
> FreeToolCheckLinkPreviewResponse checkLinkPreview(freeToolCheckLinkPreviewRequest)

Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)

Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags). The same logic as the free web tool at https://postboost.co/tools/link-preview-checker. No account needed: call it without a token, or with any API token.

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
    FreeToolCheckLinkPreviewRequest freeToolCheckLinkPreviewRequest = new FreeToolCheckLinkPreviewRequest(); // FreeToolCheckLinkPreviewRequest | 
    try {
      FreeToolCheckLinkPreviewResponse result = apiInstance.checkLinkPreview(freeToolCheckLinkPreviewRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#checkLinkPreview");
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
| **freeToolCheckLinkPreviewRequest** | [**FreeToolCheckLinkPreviewRequest**](FreeToolCheckLinkPreviewRequest.md)|  | |

### Return type

[**FreeToolCheckLinkPreviewResponse**](FreeToolCheckLinkPreviewResponse.md)

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
| **429** | Rate limit reached. Without a token: 30 calls per minute and 20 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute and 200 per UTC day per user. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
| **504** | The page did not load in time, or the connection failed. |  -  |

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

<a id="checkReadability"></a>
# **checkReadability**
> FreeToolCheckReadabilityResponse checkReadability(freeToolCheckReadabilityRequest)

Check the readability of a post: Flesch scores, long sentences and passive hints

Check the readability of a post: Flesch scores, long sentences and passive hints. The same logic as the free web tool at https://postboost.co/tools/post-readability-checker. No account needed: call it without a token, or with any API token.

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
    FreeToolCheckReadabilityRequest freeToolCheckReadabilityRequest = new FreeToolCheckReadabilityRequest(); // FreeToolCheckReadabilityRequest | 
    try {
      FreeToolCheckReadabilityResponse result = apiInstance.checkReadability(freeToolCheckReadabilityRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#checkReadability");
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
| **freeToolCheckReadabilityRequest** | [**FreeToolCheckReadabilityRequest**](FreeToolCheckReadabilityRequest.md)|  | |

### Return type

[**FreeToolCheckReadabilityResponse**](FreeToolCheckReadabilityResponse.md)

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

<a id="checkYoutubeThumbnail"></a>
# **checkYoutubeThumbnail**
> FreeToolCheckYoutubeThumbnailResponse checkYoutubeThumbnail(freeToolCheckYoutubeThumbnailRequest)

Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements

Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements. The same logic as the free web tool at https://postboost.co/tools/youtube-thumbnail-size-checker. No account needed: call it without a token, or with any API token.

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
    FreeToolCheckYoutubeThumbnailRequest freeToolCheckYoutubeThumbnailRequest = new FreeToolCheckYoutubeThumbnailRequest(); // FreeToolCheckYoutubeThumbnailRequest | 
    try {
      FreeToolCheckYoutubeThumbnailResponse result = apiInstance.checkYoutubeThumbnail(freeToolCheckYoutubeThumbnailRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#checkYoutubeThumbnail");
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
| **freeToolCheckYoutubeThumbnailRequest** | [**FreeToolCheckYoutubeThumbnailRequest**](FreeToolCheckYoutubeThumbnailRequest.md)|  | |

### Return type

[**FreeToolCheckYoutubeThumbnailResponse**](FreeToolCheckYoutubeThumbnailResponse.md)

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

<a id="findAutomationRecipes"></a>
# **findAutomationRecipes**
> FreeToolFindAutomationRecipesResponse findAutomationRecipes(platform, trigger, q)

Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API

Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API. The same logic as the free web tool at https://postboost.co/tools/social-media-automation-recipes. No account needed: call it without a token, or with any API token.

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
    String platform = "n8n"; // String | 
    String trigger = "rss"; // String | 
    String q = "q_example"; // String | 
    try {
      FreeToolFindAutomationRecipesResponse result = apiInstance.findAutomationRecipes(platform, trigger, q);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#findAutomationRecipes");
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
| **platform** | **String**|  | [optional] [enum: n8n, zapier, make] |
| **trigger** | **String**|  | [optional] [enum: rss, spreadsheet, file, approval, webhook, schedule] |
| **q** | **String**|  | [optional] |

### Return type

[**FreeToolFindAutomationRecipesResponse**](FreeToolFindAutomationRecipesResponse.md)

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

<a id="formatCrossPost"></a>
# **formatCrossPost**
> FreeToolFormatCrossPostResponse formatCrossPost(freeToolFormatCrossPostRequest)

Format one post for X, Threads, Bluesky, Mastodon and LinkedIn

Format one post for X, Threads, Bluesky, Mastodon and LinkedIn. The same logic as the free web tool at https://postboost.co/tools/cross-post-formatter. No account needed: call it without a token, or with any API token.

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
    FreeToolFormatCrossPostRequest freeToolFormatCrossPostRequest = new FreeToolFormatCrossPostRequest(); // FreeToolFormatCrossPostRequest | 
    try {
      FreeToolFormatCrossPostResponse result = apiInstance.formatCrossPost(freeToolFormatCrossPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#formatCrossPost");
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
| **freeToolFormatCrossPostRequest** | [**FreeToolFormatCrossPostRequest**](FreeToolFormatCrossPostRequest.md)|  | |

### Return type

[**FreeToolFormatCrossPostResponse**](FreeToolFormatCrossPostResponse.md)

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

<a id="formatInstagramCaption"></a>
# **formatInstagramCaption**
> FreeToolFormatInstagramCaptionResponse formatInstagramCaption(freeToolFormatInstagramCaptionRequest)

Keep blank lines in an Instagram caption with spacer lines, and count it

Keep blank lines in an Instagram caption with spacer lines, and count it. The same logic as the free web tool at https://postboost.co/tools/instagram-line-break-generator. No account needed: call it without a token, or with any API token.

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
    FreeToolFormatInstagramCaptionRequest freeToolFormatInstagramCaptionRequest = new FreeToolFormatInstagramCaptionRequest(); // FreeToolFormatInstagramCaptionRequest | 
    try {
      FreeToolFormatInstagramCaptionResponse result = apiInstance.formatInstagramCaption(freeToolFormatInstagramCaptionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#formatInstagramCaption");
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
| **freeToolFormatInstagramCaptionRequest** | [**FreeToolFormatInstagramCaptionRequest**](FreeToolFormatInstagramCaptionRequest.md)|  | |

### Return type

[**FreeToolFormatInstagramCaptionResponse**](FreeToolFormatInstagramCaptionResponse.md)

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

<a id="generateAltText"></a>
# **generateAltText**
> FreeToolGenerateAltTextResponse generateAltText(freeToolGenerateAltTextRequest)

Write alt text for an image with AI (needs a token, spends AI credits)

Write alt text for an image with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/alt-text-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateAltTextRequest freeToolGenerateAltTextRequest = new FreeToolGenerateAltTextRequest(); // FreeToolGenerateAltTextRequest | 
    try {
      FreeToolGenerateAltTextResponse result = apiInstance.generateAltText(freeToolGenerateAltTextRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateAltText");
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
| **freeToolGenerateAltTextRequest** | [**FreeToolGenerateAltTextRequest**](FreeToolGenerateAltTextRequest.md)|  | |

### Return type

[**FreeToolGenerateAltTextResponse**](FreeToolGenerateAltTextResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
| **401** | No API token, or an invalid one. The body has &#x60;register_url&#x60; to create a free account. |  -  |
| **403** | &#x60;workspace&#x60; is not a workspace you belong to, or your account has no workspace, or a scoped API key lacks the &#x60;ai&#x60; ability or is bound to another workspace (&#x60;code: insufficient_scope&#x60;). |  -  |
| **413** | The request body is larger than 7 MB. |  -  |
| **422** |  |  -  |
| **429** | The workspace has no AI credits left this billing cycle (&#x60;code: ai_credits_exhausted&#x60;, &#x60;upgrade_url&#x60;), or the per-minute limit was reached. Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
| **502** | The AI provider failed or timed out. No credit was spent. |  -  |
| **503** | AI tools are switched off right now. |  -  |

<a id="generateBio"></a>
# **generateBio**
> FreeToolGenerateBioResponse generateBio(freeToolGenerateBioRequest)

Write five profile bios with AI (needs a token, spends AI credits)

Write five profile bios with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-bio-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateBioRequest freeToolGenerateBioRequest = new FreeToolGenerateBioRequest(); // FreeToolGenerateBioRequest | 
    try {
      FreeToolGenerateBioResponse result = apiInstance.generateBio(freeToolGenerateBioRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateBio");
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
| **freeToolGenerateBioRequest** | [**FreeToolGenerateBioRequest**](FreeToolGenerateBioRequest.md)|  | |

### Return type

[**FreeToolGenerateBioResponse**](FreeToolGenerateBioResponse.md)

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

<a id="generateHooks"></a>
# **generateHooks**
> FreeToolGenerateHooksResponse generateHooks(freeToolGenerateHooksRequest)

Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)

Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/hook-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateHooksRequest freeToolGenerateHooksRequest = new FreeToolGenerateHooksRequest(); // FreeToolGenerateHooksRequest | 
    try {
      FreeToolGenerateHooksResponse result = apiInstance.generateHooks(freeToolGenerateHooksRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateHooks");
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
| **freeToolGenerateHooksRequest** | [**FreeToolGenerateHooksRequest**](FreeToolGenerateHooksRequest.md)|  | |

### Return type

[**FreeToolGenerateHooksResponse**](FreeToolGenerateHooksResponse.md)

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

<a id="generateLinkedInHeadline"></a>
# **generateLinkedInHeadline**
> FreeToolGenerateLinkedInHeadlineResponse generateLinkedInHeadline(freeToolGenerateLinkedInHeadlineRequest)

Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)

Write five LinkedIn profile headlines with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/linkedin-headline-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateLinkedInHeadlineRequest freeToolGenerateLinkedInHeadlineRequest = new FreeToolGenerateLinkedInHeadlineRequest(); // FreeToolGenerateLinkedInHeadlineRequest | 
    try {
      FreeToolGenerateLinkedInHeadlineResponse result = apiInstance.generateLinkedInHeadline(freeToolGenerateLinkedInHeadlineRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateLinkedInHeadline");
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
| **freeToolGenerateLinkedInHeadlineRequest** | [**FreeToolGenerateLinkedInHeadlineRequest**](FreeToolGenerateLinkedInHeadlineRequest.md)|  | |

### Return type

[**FreeToolGenerateLinkedInHeadlineResponse**](FreeToolGenerateLinkedInHeadlineResponse.md)

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

<a id="generateQrCode"></a>
# **generateQrCode**
> FreeToolGenerateQrCodeResponse generateQrCode(freeToolGenerateQrCodeRequest)

Generate a QR code (SVG) for a link or text, with optional UTM tags

Generate a QR code (SVG) for a link or text, with optional UTM tags. The same logic as the free web tool at https://postboost.co/tools/qr-code-generator. No account needed: call it without a token, or with any API token.

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
    FreeToolGenerateQrCodeRequest freeToolGenerateQrCodeRequest = new FreeToolGenerateQrCodeRequest(); // FreeToolGenerateQrCodeRequest | 
    try {
      FreeToolGenerateQrCodeResponse result = apiInstance.generateQrCode(freeToolGenerateQrCodeRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateQrCode");
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
| **freeToolGenerateQrCodeRequest** | [**FreeToolGenerateQrCodeRequest**](FreeToolGenerateQrCodeRequest.md)|  | |

### Return type

[**FreeToolGenerateQrCodeResponse**](FreeToolGenerateQrCodeResponse.md)

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

<a id="generateSocialPostsFromBlog"></a>
# **generateSocialPostsFromBlog**
> FreeToolGenerateSocialPostsFromBlogResponse generateSocialPostsFromBlog(freeToolGenerateSocialPostsFromBlogRequest)

Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)

Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/blog-to-social-media. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). Each post spends 1 AI credit of the workspace you name (or your active workspace), so a call costs one credit per platform that comes back; results are not cached.

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
    FreeToolGenerateSocialPostsFromBlogRequest freeToolGenerateSocialPostsFromBlogRequest = new FreeToolGenerateSocialPostsFromBlogRequest(); // FreeToolGenerateSocialPostsFromBlogRequest | 
    try {
      FreeToolGenerateSocialPostsFromBlogResponse result = apiInstance.generateSocialPostsFromBlog(freeToolGenerateSocialPostsFromBlogRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateSocialPostsFromBlog");
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
| **freeToolGenerateSocialPostsFromBlogRequest** | [**FreeToolGenerateSocialPostsFromBlogRequest**](FreeToolGenerateSocialPostsFromBlogRequest.md)|  | |

### Return type

[**FreeToolGenerateSocialPostsFromBlogResponse**](FreeToolGenerateSocialPostsFromBlogResponse.md)

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

<a id="generateSocialPostsFromVideo"></a>
# **generateSocialPostsFromVideo**
> FreeToolGenerateSocialPostsFromVideoResponse generateSocialPostsFromVideo(freeToolGenerateSocialPostsFromVideoRequest)

Turn a YouTube video&#39;s captions into an X thread and social captions with AI (needs a token, spends AI credits)

Turn a YouTube video&#39;s captions into an X thread and social captions with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-to-social-posts. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateSocialPostsFromVideoRequest freeToolGenerateSocialPostsFromVideoRequest = new FreeToolGenerateSocialPostsFromVideoRequest(); // FreeToolGenerateSocialPostsFromVideoRequest | 
    try {
      FreeToolGenerateSocialPostsFromVideoResponse result = apiInstance.generateSocialPostsFromVideo(freeToolGenerateSocialPostsFromVideoRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateSocialPostsFromVideo");
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
| **freeToolGenerateSocialPostsFromVideoRequest** | [**FreeToolGenerateSocialPostsFromVideoRequest**](FreeToolGenerateSocialPostsFromVideoRequest.md)|  | |

### Return type

[**FreeToolGenerateSocialPostsFromVideoResponse**](FreeToolGenerateSocialPostsFromVideoResponse.md)

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

<a id="generateUsernames"></a>
# **generateUsernames**
> FreeToolGenerateUsernamesResponse generateUsernames(freeToolGenerateUsernamesRequest)

Generate social media usernames

Generate social media usernames. The same logic as the free web tool at https://postboost.co/tools/social-media-username-generator. No account needed: call it without a token, or with any API token.

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
    FreeToolGenerateUsernamesRequest freeToolGenerateUsernamesRequest = new FreeToolGenerateUsernamesRequest(); // FreeToolGenerateUsernamesRequest | 
    try {
      FreeToolGenerateUsernamesResponse result = apiInstance.generateUsernames(freeToolGenerateUsernamesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateUsernames");
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
| **freeToolGenerateUsernamesRequest** | [**FreeToolGenerateUsernamesRequest**](FreeToolGenerateUsernamesRequest.md)|  | |

### Return type

[**FreeToolGenerateUsernamesResponse**](FreeToolGenerateUsernamesResponse.md)

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

<a id="generateYoutubeDescription"></a>
# **generateYoutubeDescription**
> FreeToolGenerateYoutubeDescriptionResponse generateYoutubeDescription(freeToolGenerateYoutubeDescriptionRequest)

Write three YouTube video descriptions with AI (needs a token, spends AI credits)

Write three YouTube video descriptions with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-description-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateYoutubeDescriptionRequest freeToolGenerateYoutubeDescriptionRequest = new FreeToolGenerateYoutubeDescriptionRequest(); // FreeToolGenerateYoutubeDescriptionRequest | 
    try {
      FreeToolGenerateYoutubeDescriptionResponse result = apiInstance.generateYoutubeDescription(freeToolGenerateYoutubeDescriptionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateYoutubeDescription");
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
| **freeToolGenerateYoutubeDescriptionRequest** | [**FreeToolGenerateYoutubeDescriptionRequest**](FreeToolGenerateYoutubeDescriptionRequest.md)|  | |

### Return type

[**FreeToolGenerateYoutubeDescriptionResponse**](FreeToolGenerateYoutubeDescriptionResponse.md)

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

<a id="generateYoutubeTitles"></a>
# **generateYoutubeTitles**
> FreeToolGenerateYoutubeTitlesResponse generateYoutubeTitles(freeToolGenerateYoutubeTitlesRequest)

Write five YouTube video titles with AI (needs a token, spends AI credits)

Write five YouTube video titles with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-title-generator. Needs an API token (a scoped key needs the &#x60;ai&#x60; ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
    FreeToolGenerateYoutubeTitlesRequest freeToolGenerateYoutubeTitlesRequest = new FreeToolGenerateYoutubeTitlesRequest(); // FreeToolGenerateYoutubeTitlesRequest | 
    try {
      FreeToolGenerateYoutubeTitlesResponse result = apiInstance.generateYoutubeTitles(freeToolGenerateYoutubeTitlesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#generateYoutubeTitles");
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
| **freeToolGenerateYoutubeTitlesRequest** | [**FreeToolGenerateYoutubeTitlesRequest**](FreeToolGenerateYoutubeTitlesRequest.md)|  | |

### Return type

[**FreeToolGenerateYoutubeTitlesResponse**](FreeToolGenerateYoutubeTitlesResponse.md)

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

<a id="getGlossary"></a>
# **getGlossary**
> FreeToolGetGlossaryResponse getGlossary(q, category)

Look up social media terms: plain-language definitions by category, with sources and related terms

Look up social media terms: plain-language definitions by category, with sources and related terms. The same logic as the free web tool at https://postboost.co/tools/social-media-glossary. No account needed: call it without a token, or with any API token.

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
    String q = "q_example"; // String | 
    String category = "metrics"; // String | 
    try {
      FreeToolGetGlossaryResponse result = apiInstance.getGlossary(q, category);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#getGlossary");
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
| **q** | **String**|  | [optional] |
| **category** | **String**|  | [optional] [enum: metrics, content, ads, platforms, developer, strategy] |

### Return type

[**FreeToolGetGlossaryResponse**](FreeToolGetGlossaryResponse.md)

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

<a id="getHookTemplates"></a>
# **getHookTemplates**
> FreeToolGetHookTemplatesResponse getHookTemplates(topic, category, network, search)

Get free hook templates for social media posts, filtered by style and network

Get free hook templates for social media posts, filtered by style and network. The same logic as the free web tool at https://postboost.co/tools/hook-generator. No account needed: call it without a token, or with any API token.

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
    String topic = "topic_example"; // String | 
    String category = "question"; // String | 
    String network = "instagram"; // String | 
    String search = "search_example"; // String | 
    try {
      FreeToolGetHookTemplatesResponse result = apiInstance.getHookTemplates(topic, category, network, search);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#getHookTemplates");
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
| **topic** | **String**|  | [optional] |
| **category** | **String**|  | [optional] [enum: question, contrarian, list, story, mistake, how-to, curiosity, social-proof] |
| **network** | **String**|  | [optional] [enum: instagram, tiktok, linkedin, x, threads, facebook] |
| **search** | **String**|  | [optional] |

### Return type

[**FreeToolGetHookTemplatesResponse**](FreeToolGetHookTemplatesResponse.md)

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

<a id="getSafeZones"></a>
# **getSafeZones**
> FreeToolGetSafeZonesResponse getSafeZones(freeToolGetSafeZonesRequest)

Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame

Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame. The same logic as the free web tool at https://postboost.co/tools/safe-zone-checker. No account needed: call it without a token, or with any API token.

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
    FreeToolGetSafeZonesRequest freeToolGetSafeZonesRequest = new FreeToolGetSafeZonesRequest(); // FreeToolGetSafeZonesRequest | 
    try {
      FreeToolGetSafeZonesResponse result = apiInstance.getSafeZones(freeToolGetSafeZonesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#getSafeZones");
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
| **freeToolGetSafeZonesRequest** | [**FreeToolGetSafeZonesRequest**](FreeToolGetSafeZonesRequest.md)|  | |

### Return type

[**FreeToolGetSafeZonesResponse**](FreeToolGetSafeZonesResponse.md)

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

<a id="getVideoSpecs"></a>
# **getVideoSpecs**
> FreeToolGetVideoSpecsResponse getVideoSpecs(network)

Get social media video ratios, resolutions, lengths and file size limits per network, with sources

Get social media video ratios, resolutions, lengths and file size limits per network, with sources. The same logic as the free web tool at https://postboost.co/tools/social-media-video-specs. No account needed: call it without a token, or with any API token.

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
      FreeToolGetVideoSpecsResponse result = apiInstance.getVideoSpecs(network);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#getVideoSpecs");
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

[**FreeToolGetVideoSpecsResponse**](FreeToolGetVideoSpecsResponse.md)

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

<a id="listAwarenessDays"></a>
# **listAwarenessDays**
> FreeToolListAwarenessDaysResponse listAwarenessDays(from, to, country, type, topic)

List public holidays, awareness days and social media days by date, country, type and topic, with sources

List public holidays, awareness days and social media days by date, country, type and topic, with sources. The same logic as the free web tool at https://postboost.co/tools/social-media-holiday-calendar. No account needed: call it without a token, or with any API token.

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
    String from = "from_example"; // String | 
    String to = "to_example"; // String | 
    String country = "US"; // String | 
    String type = "public-holiday"; // String | 
    String topic = "business"; // String | 
    try {
      FreeToolListAwarenessDaysResponse result = apiInstance.listAwarenessDays(from, to, country, type, topic);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#listAwarenessDays");
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
| **from** | **String**|  | [optional] |
| **to** | **String**|  | [optional] |
| **country** | **String**|  | [optional] [enum: US, GB, CA, AU, IN, DE, FR, TR] |
| **type** | **String**|  | [optional] [enum: public-holiday, awareness-day, awareness-week, awareness-month, social-media-day] |
| **topic** | **String**|  | [optional] [enum: business, health, environment, food, tech, culture, social-media, family, sport] |

### Return type

[**FreeToolListAwarenessDaysResponse**](FreeToolListAwarenessDaysResponse.md)

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

<a id="pickGiveawayWinners"></a>
# **pickGiveawayWinners**
> FreeToolPickGiveawayWinnersResponse pickGiveawayWinners(freeToolPickGiveawayWinnersRequest)

Pick giveaway winners with a draw anyone can verify

Pick giveaway winners with a draw anyone can verify. The same logic as the free web tool at https://postboost.co/tools/giveaway-comment-picker. No account needed: call it without a token, or with any API token.

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
    FreeToolPickGiveawayWinnersRequest freeToolPickGiveawayWinnersRequest = new FreeToolPickGiveawayWinnersRequest(); // FreeToolPickGiveawayWinnersRequest | 
    try {
      FreeToolPickGiveawayWinnersResponse result = apiInstance.pickGiveawayWinners(freeToolPickGiveawayWinnersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#pickGiveawayWinners");
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
| **freeToolPickGiveawayWinnersRequest** | [**FreeToolPickGiveawayWinnersRequest**](FreeToolPickGiveawayWinnersRequest.md)|  | |

### Return type

[**FreeToolPickGiveawayWinnersResponse**](FreeToolPickGiveawayWinnersResponse.md)

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

<a id="pickSocialMediaTool"></a>
# **pickSocialMediaTool**
> FreeToolPickSocialMediaToolResponse pickSocialMediaTool(freeToolPickSocialMediaToolRequest)

Match your needs against social media management tools and see what each one misses

Match your needs against social media management tools and see what each one misses. The same logic as the free web tool at https://postboost.co/tools/social-media-tool-picker. No account needed: call it without a token, or with any API token.

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
    FreeToolPickSocialMediaToolRequest freeToolPickSocialMediaToolRequest = new FreeToolPickSocialMediaToolRequest(); // FreeToolPickSocialMediaToolRequest | 
    try {
      FreeToolPickSocialMediaToolResponse result = apiInstance.pickSocialMediaTool(freeToolPickSocialMediaToolRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#pickSocialMediaTool");
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
| **freeToolPickSocialMediaToolRequest** | [**FreeToolPickSocialMediaToolRequest**](FreeToolPickSocialMediaToolRequest.md)|  | |

### Return type

[**FreeToolPickSocialMediaToolResponse**](FreeToolPickSocialMediaToolResponse.md)

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

<a id="planContentCalendar"></a>
# **planContentCalendar**
> FreeToolPlanContentCalendarResponse planContentCalendar(freeToolPlanContentCalendarRequest)

Plan a social media content calendar and get it as CSV and ICS

Plan a social media content calendar and get it as CSV and ICS. The same logic as the free web tool at https://postboost.co/tools/social-media-content-calendar-generator. No account needed: call it without a token, or with any API token.

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
    FreeToolPlanContentCalendarRequest freeToolPlanContentCalendarRequest = new FreeToolPlanContentCalendarRequest(); // FreeToolPlanContentCalendarRequest | 
    try {
      FreeToolPlanContentCalendarResponse result = apiInstance.planContentCalendar(freeToolPlanContentCalendarRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#planContentCalendar");
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
| **freeToolPlanContentCalendarRequest** | [**FreeToolPlanContentCalendarRequest**](FreeToolPlanContentCalendarRequest.md)|  | |

### Return type

[**FreeToolPlanContentCalendarResponse**](FreeToolPlanContentCalendarResponse.md)

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

<a id="planPostingFrequency"></a>
# **planPostingFrequency**
> FreeToolPlanPostingFrequencyResponse planPostingFrequency(freeToolPlanPostingFrequencyRequest)

Plan how often to post on each network

Plan how often to post on each network. The same logic as the free web tool at https://postboost.co/tools/posting-frequency-planner. No account needed: call it without a token, or with any API token.

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
    FreeToolPlanPostingFrequencyRequest freeToolPlanPostingFrequencyRequest = new FreeToolPlanPostingFrequencyRequest(); // FreeToolPlanPostingFrequencyRequest | 
    try {
      FreeToolPlanPostingFrequencyResponse result = apiInstance.planPostingFrequency(freeToolPlanPostingFrequencyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#planPostingFrequency");
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
| **freeToolPlanPostingFrequencyRequest** | [**FreeToolPlanPostingFrequencyRequest**](FreeToolPlanPostingFrequencyRequest.md)|  | |

### Return type

[**FreeToolPlanPostingFrequencyResponse**](FreeToolPlanPostingFrequencyResponse.md)

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

<a id="scoreSocialAudit"></a>
# **scoreSocialAudit**
> FreeToolScoreSocialAuditResponse scoreSocialAudit(freeToolScoreSocialAuditRequest)

Score a social media audit checklist and get the top fixes

Score a social media audit checklist and get the top fixes. The same logic as the free web tool at https://postboost.co/tools/social-media-audit-template. No account needed: call it without a token, or with any API token.

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
    FreeToolScoreSocialAuditRequest freeToolScoreSocialAuditRequest = new FreeToolScoreSocialAuditRequest(); // FreeToolScoreSocialAuditRequest | 
    try {
      FreeToolScoreSocialAuditResponse result = apiInstance.scoreSocialAudit(freeToolScoreSocialAuditRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#scoreSocialAudit");
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
| **freeToolScoreSocialAuditRequest** | [**FreeToolScoreSocialAuditRequest**](FreeToolScoreSocialAuditRequest.md)|  | |

### Return type

[**FreeToolScoreSocialAuditResponse**](FreeToolScoreSocialAuditResponse.md)

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

<a id="searchEmoji"></a>
# **searchEmoji**
> FreeToolSearchEmojiResponse searchEmoji(freeToolSearchEmojiRequest)

Search emoji by name or keyword, to copy and paste into a post

Search emoji by name or keyword, to copy and paste into a post. The same logic as the free web tool at https://postboost.co/tools/social-media-emoji-picker. No account needed: call it without a token, or with any API token.

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
    FreeToolSearchEmojiRequest freeToolSearchEmojiRequest = new FreeToolSearchEmojiRequest(); // FreeToolSearchEmojiRequest | 
    try {
      FreeToolSearchEmojiResponse result = apiInstance.searchEmoji(freeToolSearchEmojiRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#searchEmoji");
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
| **freeToolSearchEmojiRequest** | [**FreeToolSearchEmojiRequest**](FreeToolSearchEmojiRequest.md)|  | |

### Return type

[**FreeToolSearchEmojiResponse**](FreeToolSearchEmojiResponse.md)

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

<a id="summarizeReport"></a>
# **summarizeReport**
> FreeToolSummarizeReportResponse summarizeReport(freeToolSummarizeReportRequest)

Summarize social media post metrics into a report

Summarize social media post metrics into a report. The same logic as the free web tool at https://postboost.co/tools/social-media-report-generator. No account needed: call it without a token, or with any API token.

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
    FreeToolSummarizeReportRequest freeToolSummarizeReportRequest = new FreeToolSummarizeReportRequest(); // FreeToolSummarizeReportRequest | 
    try {
      FreeToolSummarizeReportResponse result = apiInstance.summarizeReport(freeToolSummarizeReportRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#summarizeReport");
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
| **freeToolSummarizeReportRequest** | [**FreeToolSummarizeReportRequest**](FreeToolSummarizeReportRequest.md)|  | |

### Return type

[**FreeToolSummarizeReportResponse**](FreeToolSummarizeReportResponse.md)

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
| **413** | The request body is larger than 2 MB. |  -  |
| **422** |  |  -  |
| **429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

<a id="verifyWebhookSignature"></a>
# **verifyWebhookSignature**
> FreeToolVerifyWebhookSignatureResponse verifyWebhookSignature(freeToolVerifyWebhookSignatureRequest)

Verify an HMAC webhook signature

Verify an HMAC webhook signature. The same logic as the free web tool at https://postboost.co/tools/webhook-signature-verifier. No account needed: call it without a token, or with any API token.

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
    FreeToolVerifyWebhookSignatureRequest freeToolVerifyWebhookSignatureRequest = new FreeToolVerifyWebhookSignatureRequest(); // FreeToolVerifyWebhookSignatureRequest | 
    try {
      FreeToolVerifyWebhookSignatureResponse result = apiInstance.verifyWebhookSignature(freeToolVerifyWebhookSignatureRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FreeToolsApi#verifyWebhookSignature");
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
| **freeToolVerifyWebhookSignatureRequest** | [**FreeToolVerifyWebhookSignatureRequest**](FreeToolVerifyWebhookSignatureRequest.md)|  | |

### Return type

[**FreeToolVerifyWebhookSignatureResponse**](FreeToolVerifyWebhookSignatureResponse.md)

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

