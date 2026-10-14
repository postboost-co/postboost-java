# PostsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addPostToQueue**](PostsApi.md#addPostToQueue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue |
| [**approvePost**](PostsApi.md#approvePost) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post |
| [**createPost**](PostsApi.md#createPost) | **POST** /{workspaceUuid}/posts | Create post |
| [**createRecyclingRule**](PostsApi.md#createRecyclingRule) | **POST** /{workspaceUuid}/recycling-rules | Create a recycling rule |
| [**createRssFeed**](PostsApi.md#createRssFeed) | **POST** /{workspaceUuid}/rss-feeds | Add an RSS feed |
| [**deletePost**](PostsApi.md#deletePost) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post |
| [**deletePostsBulk**](PostsApi.md#deletePostsBulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk) |
| [**deleteRecyclingRule**](PostsApi.md#deleteRecyclingRule) | **DELETE** /{workspaceUuid}/recycling-rules/{ruleUuid} | Delete a recycling rule |
| [**deleteRssFeed**](PostsApi.md#deleteRssFeed) | **DELETE** /{workspaceUuid}/rss-feeds/{feedUuid} | Delete an RSS feed |
| [**getPost**](PostsApi.md#getPost) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post |
| [**getPostAnalytics**](PostsApi.md#getPostAnalytics) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**getRecyclingRule**](PostsApi.md#getRecyclingRule) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid} | Get a recycling rule |
| [**getRssFeed**](PostsApi.md#getRssFeed) | **GET** /{workspaceUuid}/rss-feeds/{feedUuid} | Get an RSS feed |
| [**listPosts**](PostsApi.md#listPosts) | **GET** /{workspaceUuid}/posts | List posts |
| [**listRecyclingRules**](PostsApi.md#listRecyclingRules) | **GET** /{workspaceUuid}/recycling-rules | List recycling rules |
| [**listRecyclingRuns**](PostsApi.md#listRecyclingRuns) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid}/runs | List a recycling rule&#39;s runs |
| [**listRssFeeds**](PostsApi.md#listRssFeeds) | **GET** /{workspaceUuid}/rss-feeds | List RSS feeds |
| [**pollRssFeed**](PostsApi.md#pollRssFeed) | **POST** /{workspaceUuid}/rss-feeds/{feedUuid}/poll | Check an RSS feed now |
| [**recyclePost**](PostsApi.md#recyclePost) | **POST** /{workspaceUuid}/posts/{postUuid}/recycle | Recycle a post on an interval |
| [**retryPostAccount**](PostsApi.md#retryPostAccount) | **POST** /{workspaceUuid}/posts/retry/{postUuid}/{accountUuid} | Retry publishing to one account |
| [**schedulePost**](PostsApi.md#schedulePost) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post |
| [**updatePost**](PostsApi.md#updatePost) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post |
| [**updateRecyclingRule**](PostsApi.md#updateRecyclingRule) | **PUT** /{workspaceUuid}/recycling-rules/{ruleUuid} | Update, pause or resume a recycling rule |
| [**updateRssFeed**](PostsApi.md#updateRssFeed) | **PUT** /{workspaceUuid}/rss-feeds/{feedUuid} | Update, pause or resume an RSS feed |
| [**validatePost**](PostsApi.md#validatePost) | **POST** /{workspaceUuid}/posts/validate | Validate post (dry run) |


<a id="addPostToQueue"></a>
# **addPostToQueue**
> ScheduleResult addPostToQueue(workspaceUuid, postUuid, idempotencyKey, addPostToQueueRequest)

Add post to queue

Add an existing post to the smart publishing queue. Each account of the post gets its own next free queue slot. Returns &#x60;422&#x60; when the post has no accounts, the posting schedule has no available times, or provider requirements are not met. The guardrails check the saved post as publishing at the queue slot it will get (the earliest next free slot of its accounts), as on create: &#x60;409&#x60; duplicate (override with &#x60;X-Allow-Duplicate: true&#x60;), &#x60;422&#x60; account cannot publish, &#x60;429&#x60; daily cap on that slot&#39;s UTC day or X cap. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    AddPostToQueueRequest addPostToQueueRequest = new AddPostToQueueRequest(); // AddPostToQueueRequest | 
    try {
      ScheduleResult result = apiInstance.addPostToQueue(workspaceUuid, postUuid, idempotencyKey, addPostToQueueRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#addPostToQueue");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |
| **addPostToQueueRequest** | [**AddPostToQueueRequest**](AddPostToQueueRequest.md)|  | [optional] |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Queue confirmation |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="approvePost"></a>
# **approvePost**
> ScheduleResult approvePost(workspaceUuid, postUuid, idempotencyKey, approvePostRequest)

Approve post

Approve a post that is pending review. The approver may move the post with &#x60;date&#x60;/&#x60;time&#x60; (read in &#x60;timezone&#x60;) and set per-account times with &#x60;accounts_schedule&#x60;; without them the post keeps the time it was submitted with. Provider requirements are validated and reported as &#x60;422&#x60;. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    ApprovePostRequest approvePostRequest = new ApprovePostRequest(); // ApprovePostRequest | 
    try {
      ScheduleResult result = apiInstance.approvePost(workspaceUuid, postUuid, idempotencyKey, approvePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#approvePost");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |
| **approvePostRequest** | [**ApprovePostRequest**](ApprovePostRequest.md)|  | [optional] |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Approval confirmation |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="createPost"></a>
# **createPost**
> Post createPost(workspaceUuid, postInput, idempotencyKey)

Create post

Create a new post. Use &#x60;schedule: true&#x60; with &#x60;date&#x60; and &#x60;time&#x60; to schedule, &#x60;schedule_now: true&#x60; to publish immediately, or &#x60;queue: true&#x60; to add to the smart publishing queue (each account gets its own queue slot).  &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in &#x60;timezone&#x60; when given, otherwise in the workspace timezone. Use &#x60;accounts_schedule&#x60; to give individual accounts their own departure time.  Post bodies may reference mentions with &#x60;{{mention:&lt;reference&gt;}}&#x60; (see the Mentions endpoints). When the post is scheduled, provider requirements (for example a network that requires media) are validated up front and reported as &#x60;422&#x60;.  **First comment and threads.** A version&#39;s &#x60;content&#x60; is an ordered array. Item 0 is the post. Add a second item to publish a first comment on Facebook Page, Instagram and LinkedIn, or to continue a thread on X, Threads, Bluesky, Mastodon and Pixelfed:  &#x60;&#x60;&#x60;json {   \&quot;accounts\&quot;: [12],   \&quot;schedule_now\&quot;: true,   \&quot;versions\&quot;: [{     \&quot;account_id\&quot;: 0,     \&quot;is_original\&quot;: true,     \&quot;content\&quot;: [       { \&quot;body\&quot;: \&quot;Our API 1.8 is live.\&quot;, \&quot;media\&quot;: [345] },       { \&quot;body\&quot;: \&quot;Full changelog: https://postboost.co/docs/changelog/\&quot; }     ]   }] } &#x60;&#x60;&#x60;  The comment is posted right after the post goes live. If the comment fails, the post stays published and the account&#39;s entry on the post reports the error. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    PostInput postInput = new PostInput(); // PostInput | 
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    try {
      Post result = apiInstance.createPost(workspaceUuid, postInput, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#createPost");
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
| **postInput** | [**PostInput**](PostInput.md)|  | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created post |  * Idempotent-Replayed -  <br>  |
| **400** |  |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **409** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="createRecyclingRule"></a>
# **createRecyclingRule**
> CreateRecyclingRule201Response createRecyclingRule(workspaceUuid, recyclingRuleInput)

Create a recycling rule

Recycles one post (&#x60;post_uuid&#x60;) or a tag pool (&#x60;type: tag_pool&#x60; + &#x60;tag_uuid&#x60;) every &#x60;interval_days&#x60;. The first run is &#x60;start_at&#x60;, or one interval from now. Copies are never published immediately: &#x60;placement: queue&#x60; (default) takes each account&#39;s next free queue slot, &#x60;same_time&#x60; schedules at the source post&#39;s time of day, &#x60;draft&#x60; leaves a draft.  Copies pass the same guardrails as posts created through the API (duplicate guard, per-account daily caps, disconnected accounts, X monthly allowance). A refused copy is not created; the run is logged with the guard&#39;s code (see the runs endpoint). X accounts are left out of copies because X rejects repeated text. Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    RecyclingRuleInput recyclingRuleInput = new RecyclingRuleInput(); // RecyclingRuleInput | 
    try {
      CreateRecyclingRule201Response result = apiInstance.createRecyclingRule(workspaceUuid, recyclingRuleInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#createRecyclingRule");
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
| **recyclingRuleInput** | [**RecyclingRuleInput**](RecyclingRuleInput.md)|  | |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The rule was created |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="createRssFeed"></a>
# **createRssFeed**
> CreateRssFeed201Response createRssFeed(workspaceUuid, rssFeedInput)

Add an RSS feed

Checks the feed every 30 minutes and turns each item published after the feed was added into a post for &#x60;account_ids&#x60;: a draft (&#x60;mode: draft&#x60;, default) or a queued post (&#x60;mode: queue&#x60;). The text comes from &#x60;template&#x60; with &#x60;{title}&#x60;, &#x60;{link}&#x60; and &#x60;{summary}&#x60; placeholders. Each item becomes at most one post, at most &#x60;max_items_per_run&#x60; per check and 20 per workspace per day. Posts pass the same guardrails as API-created posts. Only public http(s) URLs are accepted. Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    RssFeedInput rssFeedInput = new RssFeedInput(); // RssFeedInput | 
    try {
      CreateRssFeed201Response result = apiInstance.createRssFeed(workspaceUuid, rssFeedInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#createRssFeed");
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
| **rssFeedInput** | [**RssFeedInput**](RssFeedInput.md)|  | |

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The feed was added |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deletePost"></a>
# **deletePost**
> DeleteResult deletePost(workspaceUuid, postUuid, deletePostRequest)

Delete post

Deletes a post. Use &#x60;delete_mode&#x60; to control whether to also remove the published content from social platforms.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    DeletePostRequest deletePostRequest = new DeletePostRequest(); // DeletePostRequest | 
    try {
      DeleteResult result = apiInstance.deletePost(workspaceUuid, postUuid, deletePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deletePost");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **deletePostRequest** | [**DeletePostRequest**](DeletePostRequest.md)|  | [optional] |

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deletion result |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="deletePostsBulk"></a>
# **deletePostsBulk**
> DeleteResult deletePostsBulk(workspaceUuid, deletePostsBulkRequest)

Delete posts (bulk)

Delete multiple posts at once.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    DeletePostsBulkRequest deletePostsBulkRequest = new DeletePostsBulkRequest(); // DeletePostsBulkRequest | 
    try {
      DeleteResult result = apiInstance.deletePostsBulk(workspaceUuid, deletePostsBulkRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deletePostsBulk");
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
| **deletePostsBulkRequest** | [**DeletePostsBulkRequest**](DeletePostsBulkRequest.md)|  | |

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Deletion result |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="deleteRecyclingRule"></a>
# **deleteRecyclingRule**
> Object deleteRecyclingRule(workspaceUuid, ruleUuid)

Delete a recycling rule

Deletes the rule and its run log. Copies it already created stay. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID ruleUuid = UUID.randomUUID(); // UUID | UUID of the recycling rule.
    try {
      Object result = apiInstance.deleteRecyclingRule(workspaceUuid, ruleUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deleteRecyclingRule");
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
| **ruleUuid** | **UUID**| UUID of the recycling rule. | |

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
| **404** |  |  -  |

<a id="deleteRssFeed"></a>
# **deleteRssFeed**
> Object deleteRssFeed(workspaceUuid, feedUuid)

Delete an RSS feed

Stops the feed. Posts it already created stay. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID feedUuid = UUID.randomUUID(); // UUID | UUID of the RSS feed.
    try {
      Object result = apiInstance.deleteRssFeed(workspaceUuid, feedUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deleteRssFeed");
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
| **feedUuid** | **UUID**| UUID of the RSS feed. | |

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
| **404** |  |  -  |

<a id="getPost"></a>
# **getPost**
> Post getPost(workspaceUuid, postUuid)

Get post

Returns a single post with all its versions and associated accounts.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    try {
      Post result = apiInstance.getPost(workspaceUuid, postUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#getPost");
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
| **postUuid** | **UUID**| UUID of the post. | |

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post details |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getPostAnalytics"></a>
# **getPostAnalytics**
> PostAnalytics getPostAnalytics(workspaceUuid, postUuid)

Get post analytics

Engagement metrics for a published post across its accounts (also works for trashed posts), with totals, trends and the best-performing account.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    try {
      PostAnalytics result = apiInstance.getPostAnalytics(workspaceUuid, postUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#getPostAnalytics");
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
| **postUuid** | **UUID**| UUID of the post. | |

### Return type

[**PostAnalytics**](PostAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post analytics |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getRecyclingRule"></a>
# **getRecyclingRule**
> CreateRecyclingRule201Response getRecyclingRule(workspaceUuid, ruleUuid)

Get a recycling rule

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID ruleUuid = UUID.randomUUID(); // UUID | UUID of the recycling rule.
    try {
      CreateRecyclingRule201Response result = apiInstance.getRecyclingRule(workspaceUuid, ruleUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#getRecyclingRule");
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
| **ruleUuid** | **UUID**| UUID of the recycling rule. | |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The rule |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getRssFeed"></a>
# **getRssFeed**
> CreateRssFeed201Response getRssFeed(workspaceUuid, feedUuid)

Get an RSS feed

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID feedUuid = UUID.randomUUID(); // UUID | UUID of the RSS feed.
    try {
      CreateRssFeed201Response result = apiInstance.getRssFeed(workspaceUuid, feedUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#getRssFeed");
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
| **feedUuid** | **UUID**| UUID of the RSS feed. | |

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The feed |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listPosts"></a>
# **listPosts**
> ListPosts200Response listPosts(workspaceUuid, page)

List posts

Returns a paginated list of posts in the workspace.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer page = 1; // Integer | 
    try {
      ListPosts200Response result = apiInstance.listPosts(workspaceUuid, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#listPosts");
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
| **page** | **Integer**|  | [optional] [default to 1] |

### Return type

[**ListPosts200Response**](ListPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of posts |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="listRecyclingRules"></a>
# **listRecyclingRules**
> ListRecyclingRules200Response listRecyclingRules(workspaceUuid)

List recycling rules

Evergreen recycling rules of the workspace, newest first. A rule copies a post (or the least recently recycled published post with a tag) every &#x60;interval_days&#x60; and places the copy in the queue. Copies are ordinary posts: they show in the calendar and the queue. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListRecyclingRules200Response result = apiInstance.listRecyclingRules(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#listRecyclingRules");
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

[**ListRecyclingRules200Response**](ListRecyclingRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The workspace&#39;s recycling rules |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="listRecyclingRuns"></a>
# **listRecyclingRuns**
> ListRecyclingRuns200Response listRecyclingRuns(workspaceUuid, ruleUuid)

List a recycling rule&#39;s runs

The latest 100 runs of the rule, newest first: the copy each run created, or why it skipped (&#x60;source_unavailable&#x60;, &#x60;no_eligible_post&#x60;, &#x60;no_accounts&#x60;, &#x60;queue_full&#x60;, &#x60;x_skipped_identical_text&#x60;, or a guardrail code such as &#x60;duplicate_post&#x60; or &#x60;account_daily_cap_reached&#x60;). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID ruleUuid = UUID.randomUUID(); // UUID | UUID of the recycling rule.
    try {
      ListRecyclingRuns200Response result = apiInstance.listRecyclingRuns(workspaceUuid, ruleUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#listRecyclingRuns");
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
| **ruleUuid** | **UUID**| UUID of the recycling rule. | |

### Return type

[**ListRecyclingRuns200Response**](ListRecyclingRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The rule&#39;s runs |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listRssFeeds"></a>
# **listRssFeeds**
> ListRssFeeds200Response listRssFeeds(workspaceUuid)

List RSS feeds

RSS and Atom feeds whose new items become posts, newest first.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListRssFeeds200Response result = apiInstance.listRssFeeds(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#listRssFeeds");
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

[**ListRssFeeds200Response**](ListRssFeeds200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The workspace&#39;s feeds |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="pollRssFeed"></a>
# **pollRssFeed**
> PollRssFeed200Response pollRssFeed(workspaceUuid, feedUuid)

Check an RSS feed now

Reads the feed immediately instead of waiting for the next check. Limited to 6 calls per minute. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID feedUuid = UUID.randomUUID(); // UUID | UUID of the RSS feed.
    try {
      PollRssFeed200Response result = apiInstance.pollRssFeed(workspaceUuid, feedUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#pollRssFeed");
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
| **feedUuid** | **UUID**| UUID of the RSS feed. | |

### Return type

[**PollRssFeed200Response**](PollRssFeed200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The feed was read |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** | The feed could not be read (HTTP error, not a feed, larger than 2 MB, private address). |  -  |

<a id="recyclePost"></a>
# **recyclePost**
> CreateRecyclingRule201Response recyclePost(workspaceUuid, postUuid, recyclingRuleSettings)

Recycle a post on an interval

Shortcut for creating a &#x60;post&#x60; recycling rule for this post. Same body as &#x60;createRecyclingRule&#x60; without &#x60;type&#x60;, &#x60;post_uuid&#x60; and &#x60;tag_uuid&#x60;. Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    RecyclingRuleSettings recyclingRuleSettings = new RecyclingRuleSettings(); // RecyclingRuleSettings | 
    try {
      CreateRecyclingRule201Response result = apiInstance.recyclePost(workspaceUuid, postUuid, recyclingRuleSettings);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#recyclePost");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **recyclingRuleSettings** | [**RecyclingRuleSettings**](RecyclingRuleSettings.md)|  | |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The rule was created |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="retryPostAccount"></a>
# **retryPostAccount**
> RetryPostAccountResult retryPostAccount(workspaceUuid, postUuid, accountUuid, idempotencyKey)

Retry publishing to one account

Re-publishes a post to a single account whose publishing failed. Returns &#x60;422&#x60; when the account is not on the post, the post is still publishing, or the account did not fail.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    UUID accountUuid = UUID.randomUUID(); // UUID | UUID of the social media account.
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    try {
      RetryPostAccountResult result = apiInstance.retryPostAccount(workspaceUuid, postUuid, accountUuid, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#retryPostAccount");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **accountUuid** | **UUID**| UUID of the social media account. | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**RetryPostAccountResult**](RetryPostAccountResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Retry started |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="schedulePost"></a>
# **schedulePost**
> ScheduleResult schedulePost(workspaceUuid, postUuid, schedulePostRequest, idempotencyKey)

Schedule post

Schedule an existing post. Optionally move it with &#x60;date&#x60;/&#x60;time&#x60; (read in &#x60;timezone&#x60;) and give accounts their own times with &#x60;accounts_schedule&#x60;. Set &#x60;postNow: true&#x60; to publish immediately; publishing starts within the request and any per-account times are dropped. Provider requirements are validated and reported as &#x60;422&#x60;. The guardrails check the saved post at the time it would publish, as on create: &#x60;409&#x60; duplicate (override with &#x60;X-Allow-Duplicate: true&#x60;), &#x60;422&#x60; account cannot publish, &#x60;429&#x60; daily or X cap. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    SchedulePostRequest schedulePostRequest = new SchedulePostRequest(); // SchedulePostRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    try {
      ScheduleResult result = apiInstance.schedulePost(workspaceUuid, postUuid, schedulePostRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#schedulePost");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **schedulePostRequest** | [**SchedulePostRequest**](SchedulePostRequest.md)|  | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Schedule confirmation |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="updatePost"></a>
# **updatePost**
> Object updatePost(workspaceUuid, postUuid, postInput)

Update post

Replaces a post&#39;s versions, accounts, tags, and scheduling options. The post must not be in a published state. &#x60;timezone&#x60; is honoured: &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in it. When the post stays scheduled, provider requirements are validated and reported as &#x60;422&#x60;. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    PostInput postInput = new PostInput(); // PostInput | 
    try {
      Object result = apiInstance.updatePost(workspaceUuid, postUuid, postInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#updatePost");
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
| **postUuid** | **UUID**| UUID of the post. | |
| **postInput** | [**PostInput**](PostInput.md)|  | |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** |  |  -  |
| **422** |  |  -  |
| **429** |  |  -  |

<a id="updateRecyclingRule"></a>
# **updateRecyclingRule**
> CreateRecyclingRule201Response updateRecyclingRule(workspaceUuid, ruleUuid, recyclingRuleUpdate)

Update, pause or resume a recycling rule

Changes the interval, limit, placement or accounts, or pauses (&#x60;active: false&#x60;) and resumes the rule. Fields you leave out keep their value. A rule that reached &#x60;max_runs&#x60; resumes only with a higher &#x60;max_runs&#x60;. Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID ruleUuid = UUID.randomUUID(); // UUID | UUID of the recycling rule.
    RecyclingRuleUpdate recyclingRuleUpdate = new RecyclingRuleUpdate(); // RecyclingRuleUpdate | 
    try {
      CreateRecyclingRule201Response result = apiInstance.updateRecyclingRule(workspaceUuid, ruleUuid, recyclingRuleUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#updateRecyclingRule");
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
| **ruleUuid** | **UUID**| UUID of the recycling rule. | |
| **recyclingRuleUpdate** | [**RecyclingRuleUpdate**](RecyclingRuleUpdate.md)|  | |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated rule |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="updateRssFeed"></a>
# **updateRssFeed**
> CreateRssFeed201Response updateRssFeed(workspaceUuid, feedUuid, rssFeedUpdate)

Update, pause or resume an RSS feed

Fields you leave out keep their value. Resuming (&#x60;active: true&#x60;) clears the error backoff. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID feedUuid = UUID.randomUUID(); // UUID | UUID of the RSS feed.
    RssFeedUpdate rssFeedUpdate = new RssFeedUpdate(); // RssFeedUpdate | 
    try {
      CreateRssFeed201Response result = apiInstance.updateRssFeed(workspaceUuid, feedUuid, rssFeedUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#updateRssFeed");
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
| **feedUuid** | **UUID**| UUID of the RSS feed. | |
| **rssFeedUpdate** | [**RssFeedUpdate**](RssFeedUpdate.md)|  | |

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated feed |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="validatePost"></a>
# **validatePost**
> PreflightResult validatePost(workspaceUuid, postInput)

Validate post (dry run)

Runs everything create-post checks without creating anything: request validation, network requirements (text length, media count and type, links) for every given account, whether or not the post is scheduled, and the guardrails (duplicate content, daily caps, account health). Always answers &#x60;200&#x60;; read &#x60;valid&#x60;. Any workspace member, including viewers, may call it. Recommended agent loop: account health, validate, then create. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    PostInput postInput = new PostInput(); // PostInput | 
    try {
      PreflightResult result = apiInstance.validatePost(workspaceUuid, postInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#validatePost");
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
| **postInput** | [**PostInput**](PostInput.md)|  | |

### Return type

[**PreflightResult**](PreflightResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation result |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

