# PostsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addPostToQueue**](PostsApi.md#addPostToQueue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue |
| [**approvePost**](PostsApi.md#approvePost) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post |
| [**createPost**](PostsApi.md#createPost) | **POST** /{workspaceUuid}/posts | Create post |
| [**deletePost**](PostsApi.md#deletePost) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post |
| [**deletePostsBulk**](PostsApi.md#deletePostsBulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk) |
| [**getPost**](PostsApi.md#getPost) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post |
| [**getPostAnalytics**](PostsApi.md#getPostAnalytics) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**listPosts**](PostsApi.md#listPosts) | **GET** /{workspaceUuid}/posts | List posts |
| [**retryPostAccount**](PostsApi.md#retryPostAccount) | **POST** /{workspaceUuid}/posts/retry/{postUuid}/{accountUuid} | Retry publishing to one account |
| [**schedulePost**](PostsApi.md#schedulePost) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post |
| [**updatePost**](PostsApi.md#updatePost) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post |


<a id="addPostToQueue"></a>
# **addPostToQueue**
> ScheduleResult addPostToQueue(workspaceUuid, postUuid, addPostToQueueRequest)

Add post to queue

Add an existing post to the smart publishing queue. Each account of the post gets its own next free queue slot. Returns &#x60;422&#x60; when the post has no accounts, the posting schedule has no available times, or provider requirements are not met. 

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
    AddPostToQueueRequest addPostToQueueRequest = new AddPostToQueueRequest(); // AddPostToQueueRequest | 
    try {
      ScheduleResult result = apiInstance.addPostToQueue(workspaceUuid, postUuid, addPostToQueueRequest);
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
| **422** |  |  -  |

<a id="approvePost"></a>
# **approvePost**
> ScheduleResult approvePost(workspaceUuid, postUuid, approvePostRequest)

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
    ApprovePostRequest approvePostRequest = new ApprovePostRequest(); // ApprovePostRequest | 
    try {
      ScheduleResult result = apiInstance.approvePost(workspaceUuid, postUuid, approvePostRequest);
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
> Post createPost(workspaceUuid, postInput)

Create post

Create a new post. Use &#x60;schedule: true&#x60; with &#x60;date&#x60; and &#x60;time&#x60; to schedule, &#x60;schedule_now: true&#x60; to publish immediately, or &#x60;queue: true&#x60; to add to the smart publishing queue (each account gets its own queue slot).  &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in &#x60;timezone&#x60; when given, otherwise in the workspace timezone. Use &#x60;accounts_schedule&#x60; to give individual accounts their own departure time.  Post bodies may reference mentions with &#x60;{{mention:&lt;reference&gt;}}&#x60; (see the Mentions endpoints). When the post is scheduled, provider requirements (for example a network that requires media) are validated up front and reported as &#x60;422&#x60;. 

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
      Post result = apiInstance.createPost(workspaceUuid, postInput);
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
| **201** | Created post |  -  |
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

<a id="retryPostAccount"></a>
# **retryPostAccount**
> RetryPostAccountResult retryPostAccount(workspaceUuid, postUuid, accountUuid)

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
    try {
      RetryPostAccountResult result = apiInstance.retryPostAccount(workspaceUuid, postUuid, accountUuid);
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
> ScheduleResult schedulePost(workspaceUuid, postUuid, schedulePostRequest)

Schedule post

Schedule an existing post. Optionally move it with &#x60;date&#x60;/&#x60;time&#x60; (read in &#x60;timezone&#x60;) and give accounts their own times with &#x60;accounts_schedule&#x60;. Set &#x60;postNow: true&#x60; to publish immediately; publishing starts within the request and any per-account times are dropped. Provider requirements are validated and reported as &#x60;422&#x60;. 

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
    try {
      ScheduleResult result = apiInstance.schedulePost(workspaceUuid, postUuid, schedulePostRequest);
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
| **422** |  |  -  |

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
| **422** |  |  -  |

