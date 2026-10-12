# WorkspacesApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addUserToWorkspace**](WorkspacesApi.md#addUserToWorkspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace |
| [**createApiKey**](WorkspacesApi.md#createApiKey) | **POST** /{workspaceUuid}/api-keys | Create a scoped API key |
| [**createResellerClient**](WorkspacesApi.md#createResellerClient) | **POST** /{workspaceUuid}/clients | Create a client workspace |
| [**createWorkspace**](WorkspacesApi.md#createWorkspace) | **POST** /panel/workspaces | Create workspace |
| [**deleteApiKey**](WorkspacesApi.md#deleteApiKey) | **DELETE** /{workspaceUuid}/api-keys/{apiKeyId} | Revoke a scoped API key |
| [**deleteWorkspace**](WorkspacesApi.md#deleteWorkspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace |
| [**deleteWorkspacesBulk**](WorkspacesApi.md#deleteWorkspacesBulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk) |
| [**getWorkspace**](WorkspacesApi.md#getWorkspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace |
| [**getWorkspaceAICredits**](WorkspacesApi.md#getWorkspaceAICredits) | **GET** /panel/workspaces/{workspaceUuid}/ai-credits | Get workspace AI credits |
| [**getXUsage**](WorkspacesApi.md#getXUsage) | **GET** /{workspaceUuid}/usage/x | X (Twitter) usage |
| [**listApiKeys**](WorkspacesApi.md#listApiKeys) | **GET** /{workspaceUuid}/api-keys | List scoped API keys |
| [**listMyWorkspaces**](WorkspacesApi.md#listMyWorkspaces) | **GET** /workspaces | List my workspaces |
| [**listResellerClients**](WorkspacesApi.md#listResellerClients) | **GET** /{workspaceUuid}/clients | List client workspaces |
| [**listWorkspaces**](WorkspacesApi.md#listWorkspaces) | **GET** /panel/workspaces | List workspaces |
| [**removeUserFromWorkspace**](WorkspacesApi.md#removeUserFromWorkspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace |
| [**updateWorkspace**](WorkspacesApi.md#updateWorkspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace |
| [**updateWorkspaceUser**](WorkspacesApi.md#updateWorkspaceUser) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace |


<a id="addUserToWorkspace"></a>
# **addUserToWorkspace**
> Object addUserToWorkspace(workspaceUuid, workspaceUserInput)

Add user to workspace

Adds an existing user to the workspace with a specified role. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    WorkspaceUserInput workspaceUserInput = new WorkspaceUserInput(); // WorkspaceUserInput | 
    try {
      Object result = apiInstance.addUserToWorkspace(workspaceUuid, workspaceUserInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#addUserToWorkspace");
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
| **workspaceUserInput** | [**WorkspaceUserInput**](WorkspaceUserInput.md)|  | |

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
| **201** |  |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="createApiKey"></a>
# **createApiKey**
> CreateApiKey201Response createApiKey(workspaceUuid, apiKeyInput)

Create a scoped API key

Creates a least-privilege API key for the calling user, bound to this workspace. Pick the abilities it gets and, optionally, the accounts it may act on. The plain key is in &#x60;data.token&#x60; of this response only; store it safely.  | Ability | Allows | |---|---| | &#x60;read&#x60; | Every &#x60;GET&#x60;, plus the &#x60;posts/validate&#x60; dry run | | &#x60;write&#x60; | Creating and changing drafts, media, tags, mentions, the brand voice | | &#x60;publish&#x60; | Scheduling, queueing, publishing now, approving and retrying posts, and editing a post that is already scheduled | | &#x60;ai&#x60; | The &#x60;/ai/_*&#x60; endpoints, running agents and turning on agent AI review (they also need AI credits) | | &#x60;webhooks&#x60; | Webhook subscription endpoints |  A scoped key is refused on other workspaces, on the admin panel, on API key management and on the app&#39;s built-in MCP endpoint (use &#x60;/mcp/postboost&#x60;). With &#x60;account_ids&#x60;, it may only name those accounts (in the URL, &#x60;accounts&#x60;, &#x60;account_ids&#x60; or post versions), cannot touch posts on other accounts, and &#x60;GET accounts&#x60; / &#x60;GET posts&#x60; only list matching items (pagination counts are computed before that filter). Workspace admins only, called with an unscoped key. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    ApiKeyInput apiKeyInput = new ApiKeyInput(); // ApiKeyInput | 
    try {
      CreateApiKey201Response result = apiInstance.createApiKey(workspaceUuid, apiKeyInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#createApiKey");
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
| **apiKeyInput** | [**ApiKeyInput**](ApiKeyInput.md)|  | |

### Return type

[**CreateApiKey201Response**](CreateApiKey201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The new key, with its plain token shown once |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="createResellerClient"></a>
# **createResellerClient**
> CreateResellerClient201Response createResellerClient(workspaceUuid, resellerClientInput)

Create a client workspace

Creates a client workspace on the Reseller client plan, with the caller as its owner and admin, and links it to this workspace. Fails with &#x60;422&#x60; and &#x60;code: client_limit_reached&#x60; once the plan&#39;s client limit is used (archived clients do not count). Archive clients on the Client workspaces page. Workspace admins with an unscoped key only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    ResellerClientInput resellerClientInput = new ResellerClientInput(); // ResellerClientInput | 
    try {
      CreateResellerClient201Response result = apiInstance.createResellerClient(workspaceUuid, resellerClientInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#createResellerClient");
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
| **resellerClientInput** | [**ResellerClientInput**](ResellerClientInput.md)|  | |

### Return type

[**CreateResellerClient201Response**](CreateResellerClient201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The client workspace was created |  -  |
| **401** |  |  -  |
| **403** | Not a workspace admin, a scoped key, or the workspace is not on the Reseller plan (&#x60;code: not_a_reseller&#x60;) |  -  |
| **422** | Validation error or client limit reached (&#x60;code: client_limit_reached&#x60;) |  -  |
| **503** | Client workspaces are not set up yet (&#x60;code: client_plan_missing&#x60;) |  -  |

<a id="createWorkspace"></a>
# **createWorkspace**
> Workspace createWorkspace(workspaceInput)

Create workspace

Create a new workspace. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    WorkspaceInput workspaceInput = new WorkspaceInput(); // WorkspaceInput | 
    try {
      Workspace result = apiInstance.createWorkspace(workspaceInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#createWorkspace");
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
| **workspaceInput** | [**WorkspaceInput**](WorkspaceInput.md)|  | |

### Return type

[**Workspace**](Workspace.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created workspace |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteApiKey"></a>
# **deleteApiKey**
> Object deleteApiKey(workspaceUuid, apiKeyId)

Revoke a scoped API key

Revokes a scoped key bound to this workspace. It stops working at once. Workspace admins only, called with an unscoped key.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer apiKeyId = 56; // Integer | The key's `id` from `GET api-keys`.
    try {
      Object result = apiInstance.deleteApiKey(workspaceUuid, apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#deleteApiKey");
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
| **apiKeyId** | **Integer**| The key&#39;s &#x60;id&#x60; from &#x60;GET api-keys&#x60;. | |

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

<a id="deleteWorkspace"></a>
# **deleteWorkspace**
> Object deleteWorkspace(workspaceUuid)

Delete workspace

Permanently deletes a single workspace and all its associated data. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      Object result = apiInstance.deleteWorkspace(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#deleteWorkspace");
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

<a id="deleteWorkspacesBulk"></a>
# **deleteWorkspacesBulk**
> Object deleteWorkspacesBulk(deleteWorkspacesBulkRequest)

Delete workspaces (bulk)

Permanently deletes one or more workspaces and all their associated data. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    DeleteWorkspacesBulkRequest deleteWorkspacesBulkRequest = new DeleteWorkspacesBulkRequest(); // DeleteWorkspacesBulkRequest | 
    try {
      Object result = apiInstance.deleteWorkspacesBulk(deleteWorkspacesBulkRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#deleteWorkspacesBulk");
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
| **deleteWorkspacesBulkRequest** | [**DeleteWorkspacesBulkRequest**](DeleteWorkspacesBulkRequest.md)|  | |

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

<a id="getWorkspace"></a>
# **getWorkspace**
> Workspace getWorkspace(workspaceUuid)

Get workspace

Returns a single workspace by UUID including its subscription status. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      Workspace result = apiInstance.getWorkspace(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#getWorkspace");
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

[**Workspace**](Workspace.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Workspace details |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getWorkspaceAICredits"></a>
# **getWorkspaceAICredits**
> AICredits getWorkspaceAICredits(workspaceUuid)

Get workspace AI credits

Returns whether the workspace can use AI credits, its remaining balance, and whether the balance is low. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      AICredits result = apiInstance.getWorkspaceAICredits(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#getWorkspaceAICredits");
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

[**AICredits**](AICredits.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | AI credit status |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getXUsage"></a>
# **getXUsage**
> XUsage getXUsage(workspaceUuid)

X (Twitter) usage

The workspace&#39;s X posts this calendar month (UTC) against its monthly X allowance. Every thread part is one X post; a part with a link also counts as a link post. When the allowance is used up, scheduling to X is refused (&#x60;429&#x60;, &#x60;code: x_monthly_cap_reached&#x60;) and X posts that come due fail with \&quot;Monthly X allowance reached\&quot;. Other networks are not affected. See the X policy in the developer docs. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      XUsage result = apiInstance.getXUsage(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#getXUsage");
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

[**XUsage**](XUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Usage this month |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="listApiKeys"></a>
# **listApiKeys**
> ListApiKeys200Response listApiKeys(workspaceUuid)

List scoped API keys

Scoped API keys bound to this workspace, newest first. The secret is never shown again after creation. Workspace admins only, called with an unscoped key (a scoped key gets &#x60;403&#x60; with &#x60;code: insufficient_scope&#x60;). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListApiKeys200Response result = apiInstance.listApiKeys(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#listApiKeys");
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

[**ListApiKeys200Response**](ListApiKeys200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Scoped keys of this workspace |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="listMyWorkspaces"></a>
# **listMyWorkspaces**
> ListMyWorkspaces200Response listMyWorkspaces()

List my workspaces

Returns the workspaces the authenticated user belongs to, most recently updated first, with the caller&#39;s role in each. Use a returned &#x60;uuid&#x60; as &#x60;workspaceUuid&#x60;.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    try {
      ListMyWorkspaces200Response result = apiInstance.listMyWorkspaces();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#listMyWorkspaces");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListMyWorkspaces200Response**](ListMyWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The caller&#39;s workspaces |  -  |
| **401** |  |  -  |

<a id="listResellerClients"></a>
# **listResellerClients**
> ListResellerClients200Response listResellerClients(workspaceUuid)

List client workspaces

Client workspaces this workspace created on the Reseller plan, active first, then archived. &#x60;accounts_needing_reconnect&#x60; counts accounts whose connection must be renewed. &#x60;meta&#x60; gives the active clients and the plan&#39;s client limit. Workspace admins with an unscoped key only; other workspaces get &#x60;403&#x60; with &#x60;code: not_a_reseller&#x60;. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListResellerClients200Response result = apiInstance.listResellerClients(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#listResellerClients");
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

[**ListResellerClients200Response**](ListResellerClients200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The reseller&#39;s client workspaces |  -  |
| **401** |  |  -  |
| **403** | Not a workspace admin, a scoped key, or the workspace is not on the Reseller plan (&#x60;code: not_a_reseller&#x60;) |  -  |

<a id="listWorkspaces"></a>
# **listWorkspaces**
> ListWorkspaces200Response listWorkspaces(keyword, subscriptionStatus, accessStatus, page)

List workspaces

Returns a paginated list of all workspaces. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String keyword = "keyword_example"; // String | 
    String subscriptionStatus = "active"; // String | 
    String accessStatus = "subscription"; // String | 
    Integer page = 1; // Integer | Page number (15 items per page).
    try {
      ListWorkspaces200Response result = apiInstance.listWorkspaces(keyword, subscriptionStatus, accessStatus, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#listWorkspaces");
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
| **keyword** | **String**|  | [optional] |
| **subscriptionStatus** | **String**|  | [optional] [enum: active, trialing, past_due, paused, canceled, incomplete] |
| **accessStatus** | **String**|  | [optional] [enum: subscription, unlimited, locked] |
| **page** | **Integer**| Page number (15 items per page). | [optional] [default to 1] |

### Return type

[**ListWorkspaces200Response**](ListWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of workspaces |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="removeUserFromWorkspace"></a>
# **removeUserFromWorkspace**
> Object removeUserFromWorkspace(workspaceUuid, removeUserFromWorkspaceRequest)

Remove user from workspace

Removes a user&#39;s access to the workspace. The user account is not deleted. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    RemoveUserFromWorkspaceRequest removeUserFromWorkspaceRequest = new RemoveUserFromWorkspaceRequest(); // RemoveUserFromWorkspaceRequest | 
    try {
      Object result = apiInstance.removeUserFromWorkspace(workspaceUuid, removeUserFromWorkspaceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#removeUserFromWorkspace");
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
| **removeUserFromWorkspaceRequest** | [**RemoveUserFromWorkspaceRequest**](RemoveUserFromWorkspaceRequest.md)|  | |

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

<a id="updateWorkspace"></a>
# **updateWorkspace**
> Object updateWorkspace(workspaceUuid, workspaceInput)

Update workspace

Updates a workspace&#39;s name, owner, or access status. Admin only. &#x60;hex_color&#x60; is accepted but ignored.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    WorkspaceInput workspaceInput = new WorkspaceInput(); // WorkspaceInput | 
    try {
      Object result = apiInstance.updateWorkspace(workspaceUuid, workspaceInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#updateWorkspace");
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
| **workspaceInput** | [**WorkspaceInput**](WorkspaceInput.md)|  | |

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

<a id="updateWorkspaceUser"></a>
# **updateWorkspaceUser**
> Object updateWorkspaceUser(workspaceUuid, workspaceUserInput)

Update user role in workspace

Changes a user&#39;s role or permissions within the workspace. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    WorkspaceUserInput workspaceUserInput = new WorkspaceUserInput(); // WorkspaceUserInput | 
    try {
      Object result = apiInstance.updateWorkspaceUser(workspaceUuid, workspaceUserInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#updateWorkspaceUser");
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
| **workspaceUserInput** | [**WorkspaceUserInput**](WorkspaceUserInput.md)|  | |

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

