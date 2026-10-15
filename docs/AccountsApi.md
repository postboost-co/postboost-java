# AccountsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**connectChannel**](AccountsApi.md#connectChannel) | **POST** /{workspaceUuid}/accounts/connect/{provider} | Connect a Telegram, Discord or Slack channel |
| [**createConnectLink**](AccountsApi.md#createConnectLink) | **POST** /{workspaceUuid}/accounts/connect-links | Create a connect link |
| [**createReconnectLink**](AccountsApi.md#createReconnectLink) | **POST** /{workspaceUuid}/accounts/{accountUuid}/reconnect-links | Create a reconnect link |
| [**getAccount**](AccountsApi.md#getAccount) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account |
| [**getAccountHealth**](AccountsApi.md#getAccountHealth) | **GET** /{workspaceUuid}/account-health | Account health |
| [**listAccounts**](AccountsApi.md#listAccounts) | **GET** /{workspaceUuid}/accounts | List accounts |


<a id="connectChannel"></a>
# **connectChannel**
> ChannelAccount connectChannel(workspaceUuid, provider, connectChannelInput)

Connect a Telegram, Discord or Slack channel

Connects a channel that uses a bot token or a webhook URL instead of a login. The credentials are checked against the network first, stored encrypted and never returned. Connecting the same channel again updates it (&#x60;200&#x60;) instead of adding a second account. Workspace admins only; counts toward the plan&#39;s social account limit.  - **telegram**: &#x60;bot_token&#x60; from @BotFather and &#x60;chat&#x60; (the channel&#39;s &#x60;@username&#x60;, or its   numeric id such as &#x60;-1001234567890&#x60; for a private channel). The bot must be an administrator   of the channel allowed to post messages. - **discord**: &#x60;webhook_url&#x60; from Channel settings → Integrations → Webhooks   (&#x60;https://discord.com/api/webhooks/…&#x60;). - **slack**: &#x60;webhook_url&#x60; of an incoming webhook (&#x60;https://hooks.slack.com/services/…&#x60;) and an   optional display &#x60;name&#x60;. Slack posts cannot be deleted from PostBoost, and images must be   publicly reachable.  Webhook URLs on any other host are refused (&#x60;422&#x60;) before any request is made. 

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
    String provider = "telegram"; // String | 
    ConnectChannelInput connectChannelInput = new ConnectChannelInput(); // ConnectChannelInput | 
    try {
      ChannelAccount result = apiInstance.connectChannel(workspaceUuid, provider, connectChannelInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#connectChannel");
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
| **provider** | **String**|  | [enum: telegram, discord, slack] |
| **connectChannelInput** | [**ConnectChannelInput**](ConnectChannelInput.md)|  | |

### Return type

[**ChannelAccount**](ChannelAccount.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Channel connected. |  -  |
| **200** | The channel was already connected; its details and credentials were updated. |  -  |
| **401** |  |  -  |
| **403** | The caller is not a workspace admin, or the plan&#39;s social account limit is reached. |  -  |
| **404** | Unknown provider, or the channel is switched off on this instance. |  -  |
| **422** |  |  -  |

<a id="createConnectLink"></a>
# **createConnectLink**
> ConnectLink createConnectLink(workspaceUuid, createConnectLinkRequest)

Create a connect link

Creates a single-use link (valid 15 minutes) that lets the user connect a new account on an OAuth network to this workspace. Ask the user to open this link in their browser while logged in to PostBoost, wait until they confirm, then call &#x60;list-accounts&#x60; to get the new account id. The link signs no one in: only the user who created it, while a workspace admin, can use it. Telegram, Discord and Slack need no browser: connect them with &#x60;connectChannel&#x60;. Mastodon, Pixelfed and Bluesky ask for a server or handle first, so the user connects them in the app. Workspace admins only; at most 10 links per minute. 

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
    CreateConnectLinkRequest createConnectLinkRequest = new CreateConnectLinkRequest(); // CreateConnectLinkRequest | 
    try {
      ConnectLink result = apiInstance.createConnectLink(workspaceUuid, createConnectLinkRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#createConnectLink");
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
| **createConnectLinkRequest** | [**CreateConnectLinkRequest**](CreateConnectLinkRequest.md)|  | |

### Return type

[**ConnectLink**](ConnectLink.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Link created. The URL is shown only once. |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |
| **429** | Too many connect links in the last minute. |  -  |

<a id="createReconnectLink"></a>
# **createReconnectLink**
> ReconnectLink createReconnectLink(workspaceUuid, accountUuid)

Create a reconnect link

Creates a single-use link (valid 7 days) that lets someone without a PostBoost login, such as an agency&#39;s client, re-authorize this one account on its network. The link only refreshes the connection of this account; signing in as a different profile or page changes nothing. Workspace admins only. Available for Facebook Pages, Instagram, Threads, LinkedIn, TikTok, YouTube and Pinterest. Returns &#x60;404&#x60; while the feature is not enabled on this instance. 

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
      ReconnectLink result = apiInstance.createReconnectLink(workspaceUuid, accountUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#createReconnectLink");
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

[**ReconnectLink**](ReconnectLink.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Link created. The URL is shown only once. |  -  |
| **401** |  |  -  |
| **403** | The caller is not a workspace admin, or not a member of the workspace. |  -  |
| **404** | Unknown account, or reconnect links are not enabled. |  -  |
| **422** | Reconnect links are not available for this account&#39;s network. |  -  |

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

<a id="getAccountHealth"></a>
# **getAccountHealth**
> GetAccountHealth200Response getAccountHealth(workspaceUuid)

Account health

Pre-flight health of every account in the workspace: whether it is authorized and holds an access token, how much of its daily post cap (per UTC day, scheduled, awaiting approval and published posts) is used today, and its connection health: predicted token expiry, latest publish outcome and where to reconnect it. The &#x60;account.token_expiring&#x60; and &#x60;account.disconnected&#x60; webhooks report changes as they happen. 

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
    try {
      GetAccountHealth200Response result = apiInstance.getAccountHealth(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#getAccountHealth");
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

[**GetAccountHealth200Response**](GetAccountHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Health per account |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

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

