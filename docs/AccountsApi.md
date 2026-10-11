# AccountsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getAccount**](AccountsApi.md#getAccount) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account |
| [**listAccounts**](AccountsApi.md#listAccounts) | **GET** /{workspaceUuid}/accounts | List accounts |


<a id="getAccount"></a>
# **getAccount**
> Account getAccount(workspaceUuid, accountUuid)

Get account

Returns a single social media account.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID accountUuid = UUID.randomUUID(); // UUID | UUID of the social media account.
    try {
      Account result = apiInstance.getAccount(workspaceUuid, accountUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#getAccount");
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
| **accountUuid** | **UUID**| UUID of the social media account. | |

### Return type

[**Account**](Account.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account details |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listAccounts"></a>
# **listAccounts**
> ListAccounts200Response listAccounts(workspaceUuid, keyword, group, providers, unauthorized)

List accounts

Returns all social media accounts connected to the workspace, newest first. Optional filters narrow the list.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String keyword = "keyword_example"; // String | Match the account name or username.
    String group = "group_example"; // String | Only accounts in this account group.
    List<String> providers = Arrays.asList(); // List<String> | Only accounts of these providers (for example `instagram`, `linkedin`).
    Boolean unauthorized = true; // Boolean | When `true`, only accounts that need to be reconnected.
    try {
      ListAccounts200Response result = apiInstance.listAccounts(workspaceUuid, keyword, group, providers, unauthorized);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#listAccounts");
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
| **keyword** | **String**| Match the account name or username. | [optional] |
| **group** | **String**| Only accounts in this account group. | [optional] |
| **providers** | [**List&lt;String&gt;**](String.md)| Only accounts of these providers (for example &#x60;instagram&#x60;, &#x60;linkedin&#x60;). | [optional] |
| **unauthorized** | **Boolean**| When &#x60;true&#x60;, only accounts that need to be reconnected. | [optional] |

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of accounts |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

