# CompetitorsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addCompetitor**](CompetitorsApi.md#addCompetitor) | **POST** /{workspaceUuid}/competitors | Track a competitor |
| [**deleteCompetitor**](CompetitorsApi.md#deleteCompetitor) | **DELETE** /{workspaceUuid}/competitors/{competitorId} | Stop tracking a competitor |
| [**getCompetitor**](CompetitorsApi.md#getCompetitor) | **GET** /{workspaceUuid}/competitors/{competitorId} | Get a competitor |
| [**listCompetitors**](CompetitorsApi.md#listCompetitors) | **GET** /{workspaceUuid}/competitors | List competitors |


<a id="addCompetitor"></a>
# **addCompetitor**
> AddCompetitor202Response addCompetitor(workspaceUuid, competitorInput)

Track a competitor

Starts tracking a public Instagram business or creator account from one of your Instagram accounts (connected through a Facebook Page). Returns &#x60;202&#x60; at once; followers, snapshots and recent media appear after the background import. &#x60;409&#x60; if that account already tracks the username. Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.CompetitorsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CompetitorsApi apiInstance = new CompetitorsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    CompetitorInput competitorInput = new CompetitorInput(); // CompetitorInput | 
    try {
      AddCompetitor202Response result = apiInstance.addCompetitor(workspaceUuid, competitorInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompetitorsApi#addCompetitor");
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
| **competitorInput** | [**CompetitorInput**](CompetitorInput.md)|  | |

### Return type

[**AddCompetitor202Response**](AddCompetitor202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Tracking started; the import runs in the background |  -  |
| **409** | Already tracked |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteCompetitor"></a>
# **deleteCompetitor**
> deleteCompetitor(workspaceUuid, competitorId)

Stop tracking a competitor

Deletes the competitor with its snapshots and media. Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.CompetitorsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CompetitorsApi apiInstance = new CompetitorsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer competitorId = 56; // Integer | The competitor `id`.
    try {
      apiInstance.deleteCompetitor(workspaceUuid, competitorId);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompetitorsApi#deleteCompetitor");
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
| **competitorId** | **Integer**| The competitor &#x60;id&#x60;. | |

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

<a id="getCompetitor"></a>
# **getCompetitor**
> GetCompetitor200Response getCompetitor(workspaceUuid, competitorId)

Get a competitor

The competitor with daily follower snapshots for the last 90 days and its 12 most recent posts. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.CompetitorsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CompetitorsApi apiInstance = new CompetitorsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer competitorId = 56; // Integer | The competitor `id`.
    try {
      GetCompetitor200Response result = apiInstance.getCompetitor(workspaceUuid, competitorId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompetitorsApi#getCompetitor");
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
| **competitorId** | **Integer**| The competitor &#x60;id&#x60;. | |

### Return type

[**GetCompetitor200Response**](GetCompetitor200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The competitor |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listCompetitors"></a>
# **listCompetitors**
> ListCompetitors200Response listCompetitors(workspaceUuid, accountId)

List competitors

Instagram business or creator accounts the workspace tracks, by follower count. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.CompetitorsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CompetitorsApi apiInstance = new CompetitorsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer accountId = 56; // Integer | Only competitors tracked from this Instagram account `id`.
    try {
      ListCompetitors200Response result = apiInstance.listCompetitors(workspaceUuid, accountId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CompetitorsApi#listCompetitors");
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
| **accountId** | **Integer**| Only competitors tracked from this Instagram account &#x60;id&#x60;. | [optional] |

### Return type

[**ListCompetitors200Response**](ListCompetitors200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Competitors |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

