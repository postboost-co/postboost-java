# HashtagGroupsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createHashtagGroup**](HashtagGroupsApi.md#createHashtagGroup) | **POST** /{workspaceUuid}/hashtag-groups | Create a hashtag group |
| [**deleteHashtagGroup**](HashtagGroupsApi.md#deleteHashtagGroup) | **DELETE** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Delete a hashtag group |
| [**getHashtagGroup**](HashtagGroupsApi.md#getHashtagGroup) | **GET** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Get a hashtag group |
| [**listHashtagGroups**](HashtagGroupsApi.md#listHashtagGroups) | **GET** /{workspaceUuid}/hashtag-groups | List hashtag groups |
| [**updateHashtagGroup**](HashtagGroupsApi.md#updateHashtagGroup) | **PUT** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Update a hashtag group |


<a id="createHashtagGroup"></a>
# **createHashtagGroup**
> CreateHashtagGroup201Response createHashtagGroup(workspaceUuid, hashtagGroupInput)

Create a hashtag group

Saves a named set of hashtags (up to 3000 characters). Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.HashtagGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    HashtagGroupsApi apiInstance = new HashtagGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    HashtagGroupInput hashtagGroupInput = new HashtagGroupInput(); // HashtagGroupInput | 
    try {
      CreateHashtagGroup201Response result = apiInstance.createHashtagGroup(workspaceUuid, hashtagGroupInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HashtagGroupsApi#createHashtagGroup");
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
| **hashtagGroupInput** | [**HashtagGroupInput**](HashtagGroupInput.md)|  | |

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The new hashtag group |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteHashtagGroup"></a>
# **deleteHashtagGroup**
> deleteHashtagGroup(workspaceUuid, hashtagGroupId)

Delete a hashtag group

Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.HashtagGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    HashtagGroupsApi apiInstance = new HashtagGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String hashtagGroupId = "hashtagGroupId_example"; // String | The hashtag group `id`.
    try {
      apiInstance.deleteHashtagGroup(workspaceUuid, hashtagGroupId);
    } catch (ApiException e) {
      System.err.println("Exception when calling HashtagGroupsApi#deleteHashtagGroup");
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
| **hashtagGroupId** | **String**| The hashtag group &#x60;id&#x60;. | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Deleted |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getHashtagGroup"></a>
# **getHashtagGroup**
> CreateHashtagGroup201Response getHashtagGroup(workspaceUuid, hashtagGroupId)

Get a hashtag group

One hashtag group. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.HashtagGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    HashtagGroupsApi apiInstance = new HashtagGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String hashtagGroupId = "hashtagGroupId_example"; // String | The hashtag group `id`.
    try {
      CreateHashtagGroup201Response result = apiInstance.getHashtagGroup(workspaceUuid, hashtagGroupId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HashtagGroupsApi#getHashtagGroup");
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
| **hashtagGroupId** | **String**| The hashtag group &#x60;id&#x60;. | |

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The hashtag group |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listHashtagGroups"></a>
# **listHashtagGroups**
> ListHashtagGroups200Response listHashtagGroups(workspaceUuid, page, perPage)

List hashtag groups

Saved hashtag sets of the workspace, newest first. Paginated with &#x60;page&#x60; and &#x60;per_page&#x60; (default 100). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.HashtagGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    HashtagGroupsApi apiInstance = new HashtagGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer page = 1; // Integer | Page number (1-based).
    Integer perPage = 100; // Integer | Items per page, 1-100.
    try {
      ListHashtagGroups200Response result = apiInstance.listHashtagGroups(workspaceUuid, page, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HashtagGroupsApi#listHashtagGroups");
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
| **page** | **Integer**| Page number (1-based). | [optional] [default to 1] |
| **perPage** | **Integer**| Items per page, 1-100. | [optional] [default to 100] |

### Return type

[**ListHashtagGroups200Response**](ListHashtagGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hashtag groups, paginated (&#x60;links&#x60; and &#x60;meta&#x60; as on the other list endpoints) |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="updateHashtagGroup"></a>
# **updateHashtagGroup**
> CreateHashtagGroup201Response updateHashtagGroup(workspaceUuid, hashtagGroupId, hashtagGroupInput)

Update a hashtag group

Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.HashtagGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    HashtagGroupsApi apiInstance = new HashtagGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String hashtagGroupId = "hashtagGroupId_example"; // String | The hashtag group `id`.
    HashtagGroupInput hashtagGroupInput = new HashtagGroupInput(); // HashtagGroupInput | 
    try {
      CreateHashtagGroup201Response result = apiInstance.updateHashtagGroup(workspaceUuid, hashtagGroupId, hashtagGroupInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HashtagGroupsApi#updateHashtagGroup");
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
| **hashtagGroupId** | **String**| The hashtag group &#x60;id&#x60;. | |
| **hashtagGroupInput** | [**HashtagGroupInput**](HashtagGroupInput.md)|  | |

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated hashtag group |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

