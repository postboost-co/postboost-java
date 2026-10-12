# PostingScheduleApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPostingSchedule**](PostingScheduleApi.md#getPostingSchedule) | **GET** /{workspaceUuid}/posting-schedule | Get the posting schedule |
| [**getRecommendedPostingTimes**](PostingScheduleApi.md#getRecommendedPostingTimes) | **GET** /{workspaceUuid}/posting-schedule/recommended | Get recommended posting times |
| [**listQueueSlots**](PostingScheduleApi.md#listQueueSlots) | **GET** /{workspaceUuid}/queue/slots | List upcoming queue slots |
| [**resetAccountPostingSchedule**](PostingScheduleApi.md#resetAccountPostingSchedule) | **DELETE** /{workspaceUuid}/posting-schedule/{accountId} | Reset an account schedule |
| [**updatePostingSchedule**](PostingScheduleApi.md#updatePostingSchedule) | **PUT** /{workspaceUuid}/posting-schedule | Set the posting schedule |


<a id="getPostingSchedule"></a>
# **getPostingSchedule**
> GetPostingSchedule200Response getPostingSchedule(workspaceUuid, accountId)

Get the posting schedule

The queue&#39;s posting times: per weekday, a list of clock times in the schedule&#39;s timezone. &#x60;account_id&#x3D;0&#x60; is the workspace schedule. An account without its own schedule follows the workspace one (&#x60;inherited: true&#x60;, &#x60;source_account_id: 0&#x60;). Posts added to the queue take the next free time. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostingScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostingScheduleApi apiInstance = new PostingScheduleApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer accountId = 0; // Integer | `0` (default) for the workspace schedule, or an account `id`.
    try {
      GetPostingSchedule200Response result = apiInstance.getPostingSchedule(workspaceUuid, accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostingScheduleApi#getPostingSchedule");
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
| **accountId** | **Integer**| &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional] [default to 0] |

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The schedule |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="getRecommendedPostingTimes"></a>
# **getRecommendedPostingTimes**
> RecommendedPostingTimes getRecommendedPostingTimes(workspaceUuid, accountId, slotsPerDay)

Get recommended posting times

Suggested posting times from past engagement, in the schedule&#39;s timezone. &#x60;has_data&#x60; is false until there is enough analytics history. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostingScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostingScheduleApi apiInstance = new PostingScheduleApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer accountId = 0; // Integer | `0` (default) for the workspace schedule, or an account `id`.
    Integer slotsPerDay = 56; // Integer | Times to suggest per day (1 to 6).
    try {
      RecommendedPostingTimes result = apiInstance.getRecommendedPostingTimes(workspaceUuid, accountId, slotsPerDay);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostingScheduleApi#getRecommendedPostingTimes");
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
| **accountId** | **Integer**| &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional] [default to 0] |
| **slotsPerDay** | **Integer**| Times to suggest per day (1 to 6). | [optional] |

### Return type

[**RecommendedPostingTimes**](RecommendedPostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Recommended times |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="listQueueSlots"></a>
# **listQueueSlots**
> QueueSlots listQueueSlots(workspaceUuid, accountId, after)

List upcoming queue slots

The queue read forward: upcoming posting times, filled by scheduled posts where they land on one. Page with &#x60;after&#x60; set to the previous &#x60;next_cursor&#x60;. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostingScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostingScheduleApi apiInstance = new PostingScheduleApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer accountId = 0; // Integer | `0` (default) for the workspace schedule, or an account `id`.
    String after = "after_example"; // String | Start after this time (`Y-m-d H:i:s`, UTC), from `next_cursor`.
    try {
      QueueSlots result = apiInstance.listQueueSlots(workspaceUuid, accountId, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostingScheduleApi#listQueueSlots");
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
| **accountId** | **Integer**| &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional] [default to 0] |
| **after** | **String**| Start after this time (&#x60;Y-m-d H:i:s&#x60;, UTC), from &#x60;next_cursor&#x60;. | [optional] |

### Return type

[**QueueSlots**](QueueSlots.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upcoming slots |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="resetAccountPostingSchedule"></a>
# **resetAccountPostingSchedule**
> GetPostingSchedule200Response resetAccountPostingSchedule(workspaceUuid, accountId)

Reset an account schedule

Removes the account&#39;s own schedule so it follows the workspace schedule again. Workspace admins only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostingScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostingScheduleApi apiInstance = new PostingScheduleApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer accountId = 56; // Integer | The account `id`.
    try {
      GetPostingSchedule200Response result = apiInstance.resetAccountPostingSchedule(workspaceUuid, accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostingScheduleApi#resetAccountPostingSchedule");
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
| **accountId** | **Integer**| The account &#x60;id&#x60;. | |

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The schedule now in effect for the account |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="updatePostingSchedule"></a>
# **updatePostingSchedule**
> GetPostingSchedule200Response updatePostingSchedule(workspaceUuid, postingScheduleInput)

Set the posting schedule

Sets the workspace schedule (&#x60;account_id: 0&#x60;) or gives one account its own schedule. Send all seven weekdays (ids 1 to 6 for Monday to Saturday, 0 for Sunday). Workspace admins only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.PostingScheduleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostingScheduleApi apiInstance = new PostingScheduleApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    PostingScheduleInput postingScheduleInput = new PostingScheduleInput(); // PostingScheduleInput | 
    try {
      GetPostingSchedule200Response result = apiInstance.updatePostingSchedule(workspaceUuid, postingScheduleInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostingScheduleApi#updatePostingSchedule");
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
| **postingScheduleInput** | [**PostingScheduleInput**](PostingScheduleInput.md)|  | |

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The schedule now in effect |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

