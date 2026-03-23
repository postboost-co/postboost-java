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
| [**listPosts**](PostsApi.md#listPosts) | **GET** /{workspaceUuid}/posts | List posts |
| [**schedulePost**](PostsApi.md#schedulePost) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post |
| [**updatePost**](PostsApi.md#updatePost) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post |


<a id="addPostToQueue"></a>
# **addPostToQueue**
> ScheduleResult addPostToQueue(workspaceUuid, postUuid)

Add post to queue

Add an existing post to the smart publishing queue.

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
      ScheduleResult result = apiInstance.addPostToQueue(workspaceUuid, postUuid);
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

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Queue confirmation |  -  |
| **401** |  |  -  |
| **404** |  |  -  |

<a id="approvePost"></a>
# **approvePost**
> ScheduleResult approvePost(workspaceUuid, postUuid)

Approve post

Approve a post that is pending review.

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
      ScheduleResult result = apiInstance.approvePost(workspaceUuid, postUuid);
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

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Approval confirmation |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="createPost"></a>
# **createPost**
> Post createPost(workspaceUuid, postInput)

Create post

Create a new post. Use &#x60;schedule: true&#x60; with &#x60;date&#x60; and &#x60;time&#x60; to schedule, &#x60;schedule_now: true&#x60; to publish immediately, or &#x60;queue: true&#x60; to add to the smart publishing queue. 

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
| **200** | Created post |  -  |
| **401** |  |  -  |
| **422** |  |  -  |

<a id="deletePost"></a>
# **deletePost**
> DeleteResult deletePost(workspaceUuid, postUuid, deletePostRequest)

Delete post

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

<a id="getPost"></a>
# **getPost**
> Post getPost(workspaceUuid, postUuid)

Get post

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

<a id="schedulePost"></a>
# **schedulePost**
> ScheduleResult schedulePost(workspaceUuid, postUuid, schedulePostRequest)

Schedule post

Schedule an existing post. Set &#x60;postNow: true&#x60; to publish immediately.

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
| **404** |  |  -  |

<a id="updatePost"></a>
# **updatePost**
> Object updatePost(workspaceUuid, postUuid, postInput)

Update post

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
| **404** |  |  -  |
| **422** |  |  -  |

