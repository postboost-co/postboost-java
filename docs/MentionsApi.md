# MentionsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createMention**](MentionsApi.md#createMention) | **POST** /{workspaceUuid}/mentions | Create mention |
| [**deleteMention**](MentionsApi.md#deleteMention) | **DELETE** /{workspaceUuid}/mentions/{mentionId} | Delete mention |
| [**getMention**](MentionsApi.md#getMention) | **GET** /{workspaceUuid}/mentions/{mentionId} | Get mention |
| [**listMentions**](MentionsApi.md#listMentions) | **GET** /{workspaceUuid}/mentions | List mentions |
| [**updateMention**](MentionsApi.md#updateMention) | **PUT** /{workspaceUuid}/mentions/{mentionId} | Update mention |


<a id="createMention"></a>
# **createMention**
> CreateMention201Response createMention(workspaceUuid, mentionInput, idempotencyKey)

Create mention

Adds a person or page to the mention book. When one of the submitted identities already belongs to a stored mention, that mention is reused and the identities are added to it (status &#x60;200&#x60; instead of &#x60;201&#x60;). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MentionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MentionsApi apiInstance = new MentionsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    MentionInput mentionInput = new MentionInput(); // MentionInput | 
    String idempotencyKey = "idempotencyKey_example"; // String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
    try {
      CreateMention201Response result = apiInstance.createMention(workspaceUuid, mentionInput, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MentionsApi#createMention");
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
| **mentionInput** | [**MentionInput**](MentionInput.md)|  | |
| **idempotencyKey** | **String**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created mention |  -  |
| **200** | Existing mention reused |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteMention"></a>
# **deleteMention**
> Object deleteMention(workspaceUuid, mentionId)

Delete mention

Removes a mention from the mention book. &#x60;success&#x60; is false when nothing was deleted.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MentionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MentionsApi apiInstance = new MentionsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID mentionId = UUID.randomUUID(); // UUID | The mention's `id` (a UUID).
    try {
      Object result = apiInstance.deleteMention(workspaceUuid, mentionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MentionsApi#deleteMention");
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
| **mentionId** | **UUID**| The mention&#39;s &#x60;id&#x60; (a UUID). | |

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

<a id="getMention"></a>
# **getMention**
> CreateMention201Response getMention(workspaceUuid, mentionId)

Get mention

Returns a single mention with its identities.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MentionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MentionsApi apiInstance = new MentionsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID mentionId = UUID.randomUUID(); // UUID | The mention's `id` (a UUID).
    try {
      CreateMention201Response result = apiInstance.getMention(workspaceUuid, mentionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MentionsApi#getMention");
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
| **mentionId** | **UUID**| The mention&#39;s &#x60;id&#x60; (a UUID). | |

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Mention |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listMentions"></a>
# **listMentions**
> ListMentions200Response listMentions(workspaceUuid, q, perPage, page)

List mentions

Returns a paginated list of the workspace&#39;s mention book, ranked, with each entry&#39;s network identities.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MentionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MentionsApi apiInstance = new MentionsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String q = "q_example"; // String | Search keyword.
    Integer perPage = 25; // Integer | 
    Integer page = 1; // Integer | 
    try {
      ListMentions200Response result = apiInstance.listMentions(workspaceUuid, q, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MentionsApi#listMentions");
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
| **q** | **String**| Search keyword. | [optional] |
| **perPage** | **Integer**|  | [optional] [default to 25] |
| **page** | **Integer**|  | [optional] [default to 1] |

### Return type

[**ListMentions200Response**](ListMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of mentions |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="updateMention"></a>
# **updateMention**
> CreateMention201Response updateMention(workspaceUuid, mentionId, mentionInput)

Update mention

Replaces the mention&#39;s name, avatar and identities. Identities for providers not in the payload are removed. An identity already held by another mention returns &#x60;422&#x60;.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MentionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MentionsApi apiInstance = new MentionsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID mentionId = UUID.randomUUID(); // UUID | The mention's `id` (a UUID).
    MentionInput mentionInput = new MentionInput(); // MentionInput | 
    try {
      CreateMention201Response result = apiInstance.updateMention(workspaceUuid, mentionId, mentionInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MentionsApi#updateMention");
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
| **mentionId** | **UUID**| The mention&#39;s &#x60;id&#x60; (a UUID). | |
| **mentionInput** | [**MentionInput**](MentionInput.md)|  | |

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated mention |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

