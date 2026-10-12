# ActivityApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listApiActivity**](ActivityApi.md#listApiActivity) | **GET** /{workspaceUuid}/activity | List API activity |


<a id="listApiActivity"></a>
# **listApiActivity**
> ListApiActivity200Response listApiActivity(workspaceUuid, outcome, client, since, page)

List API activity

Every write request (&#x60;POST&#x60;, &#x60;PUT&#x60;, &#x60;DELETE&#x60;) made through the API in this workspace, newest first, with the client that made it and its outcome. Kept for 90 days. Send an &#x60;X-PostBoost-Client&#x60; header (for example &#x60;my-agent/1.2&#x60;) to label your requests; otherwise the &#x60;User-Agent&#x60; is recorded. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ActivityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ActivityApi apiInstance = new ActivityApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    ApiActivityOutcome outcome = ApiActivityOutcome.fromValue("created"); // ApiActivityOutcome | 
    String client = "client_example"; // String | Client label prefix, for example `mcp`.
    OffsetDateTime since = OffsetDateTime.now(); // OffsetDateTime | Only entries at or after this time (UTC).
    Integer page = 1; // Integer | 
    try {
      ListApiActivity200Response result = apiInstance.listApiActivity(workspaceUuid, outcome, client, since, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ActivityApi#listApiActivity");
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
| **outcome** | [**ApiActivityOutcome**](.md)|  | [optional] [enum: created, updated, deleted, validated, replayed, blocked_duplicate, blocked_cap, blocked_unauthorized, validation_failed, error, ok] |
| **client** | **String**| Client label prefix, for example &#x60;mcp&#x60;. | [optional] |
| **since** | **OffsetDateTime**| Only entries at or after this time (UTC). | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |

### Return type

[**ListApiActivity200Response**](ListApiActivity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated activity entries (50 per page) |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

