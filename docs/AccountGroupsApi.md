# AccountGroupsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAccountGroup**](AccountGroupsApi.md#createAccountGroup) | **POST** /{workspaceUuid}/account-groups | Create an account group |
| [**deleteAccountGroup**](AccountGroupsApi.md#deleteAccountGroup) | **DELETE** /{workspaceUuid}/account-groups/{accountGroupUuid} | Delete an account group |
| [**getAccountGroup**](AccountGroupsApi.md#getAccountGroup) | **GET** /{workspaceUuid}/account-groups/{accountGroupUuid} | Get an account group |
| [**listAccountGroups**](AccountGroupsApi.md#listAccountGroups) | **GET** /{workspaceUuid}/account-groups | List account groups |
| [**updateAccountGroup**](AccountGroupsApi.md#updateAccountGroup) | **PUT** /{workspaceUuid}/account-groups/{accountGroupUuid} | Update an account group |


<a id="createAccountGroup"></a>
# **createAccountGroup**
> CreateAccountGroup201Response createAccountGroup(workspaceUuid, accountGroupInput)

Create an account group

Creates a named set of accounts of this workspace. Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountGroupsApi apiInstance = new AccountGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    AccountGroupInput accountGroupInput = new AccountGroupInput(); // AccountGroupInput | 
    try {
      CreateAccountGroup201Response result = apiInstance.createAccountGroup(workspaceUuid, accountGroupInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountGroupsApi#createAccountGroup");
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
| **accountGroupInput** | [**AccountGroupInput**](AccountGroupInput.md)|  | |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The new account group |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteAccountGroup"></a>
# **deleteAccountGroup**
> deleteAccountGroup(workspaceUuid, accountGroupUuid)

Delete an account group

Deletes the group, not its accounts. Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountGroupsApi apiInstance = new AccountGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String accountGroupUuid = "accountGroupUuid_example"; // String | The account group `uuid`.
    try {
      apiInstance.deleteAccountGroup(workspaceUuid, accountGroupUuid);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountGroupsApi#deleteAccountGroup");
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
| **accountGroupUuid** | **String**| The account group &#x60;uuid&#x60;. | |

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

<a id="getAccountGroup"></a>
# **getAccountGroup**
> CreateAccountGroup201Response getAccountGroup(workspaceUuid, accountGroupUuid)

Get an account group

One account group. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountGroupsApi apiInstance = new AccountGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String accountGroupUuid = "accountGroupUuid_example"; // String | The account group `uuid`.
    try {
      CreateAccountGroup201Response result = apiInstance.getAccountGroup(workspaceUuid, accountGroupUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountGroupsApi#getAccountGroup");
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
| **accountGroupUuid** | **String**| The account group &#x60;uuid&#x60;. | |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The account group |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listAccountGroups"></a>
# **listAccountGroups**
> ListAccountGroups200Response listAccountGroups(workspaceUuid, page, perPage)

List account groups

Named sets of accounts, sorted by name, with their account ids. Pass &#x60;account_ids&#x60; as &#x60;accounts&#x60; when you create a post to publish to the whole group. Paginated with &#x60;page&#x60; and &#x60;per_page&#x60; (default 100). A key limited to some accounts only sees groups whose accounts are all among its accounts, and &#x60;meta.total&#x60; counts only those. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountGroupsApi apiInstance = new AccountGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer page = 1; // Integer | Page number (1-based).
    Integer perPage = 100; // Integer | Items per page, 1-100.
    try {
      ListAccountGroups200Response result = apiInstance.listAccountGroups(workspaceUuid, page, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountGroupsApi#listAccountGroups");
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

[**ListAccountGroups200Response**](ListAccountGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account groups, paginated (&#x60;links&#x60; and &#x60;meta&#x60; as on the other list endpoints) |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="updateAccountGroup"></a>
# **updateAccountGroup**
> CreateAccountGroup201Response updateAccountGroup(workspaceUuid, accountGroupUuid, accountGroupInput)

Update an account group

Replaces the name and the accounts of the group (accounts you leave out are removed). Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AccountGroupsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountGroupsApi apiInstance = new AccountGroupsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String accountGroupUuid = "accountGroupUuid_example"; // String | The account group `uuid`.
    AccountGroupInput accountGroupInput = new AccountGroupInput(); // AccountGroupInput | 
    try {
      CreateAccountGroup201Response result = apiInstance.updateAccountGroup(workspaceUuid, accountGroupUuid, accountGroupInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountGroupsApi#updateAccountGroup");
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
| **accountGroupUuid** | **String**| The account group &#x60;uuid&#x60;. | |
| **accountGroupInput** | [**AccountGroupInput**](AccountGroupInput.md)|  | |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated account group |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

