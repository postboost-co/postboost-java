# InboxApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**approveInboxReplyDraft**](InboxApi.md#approveInboxReplyDraft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/approve | Approve and send a reply draft |
| [**createInboxReplyDraft**](InboxApi.md#createInboxReplyDraft) | **POST** /{workspaceUuid}/inbox/conversations/{conversationId}/drafts | Draft a reply |
| [**deleteInboxReplyDraft**](InboxApi.md#deleteInboxReplyDraft) | **DELETE** /{workspaceUuid}/inbox/drafts/{draftId} | Withdraw a reply draft |
| [**getInboxConversation**](InboxApi.md#getInboxConversation) | **GET** /{workspaceUuid}/inbox/conversations/{conversationId} | Get an inbox conversation |
| [**getInboxReplyDraft**](InboxApi.md#getInboxReplyDraft) | **GET** /{workspaceUuid}/inbox/drafts/{draftId} | Get a reply draft |
| [**listInboxConversations**](InboxApi.md#listInboxConversations) | **GET** /{workspaceUuid}/inbox/conversations | List inbox conversations |
| [**listInboxReplyDrafts**](InboxApi.md#listInboxReplyDrafts) | **GET** /{workspaceUuid}/inbox/drafts | List reply drafts |
| [**rejectInboxReplyDraft**](InboxApi.md#rejectInboxReplyDraft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/reject | Reject a reply draft |
| [**updateInboxConversation**](InboxApi.md#updateInboxConversation) | **PATCH** /{workspaceUuid}/inbox/conversations/{conversationId} | Update an inbox conversation |
| [**updateInboxReplyDraft**](InboxApi.md#updateInboxReplyDraft) | **PUT** /{workspaceUuid}/inbox/drafts/{draftId} | Edit a reply draft |


<a id="approveInboxReplyDraft"></a>
# **approveInboxReplyDraft**
> CreateInboxReplyDraft201Response approveInboxReplyDraft(workspaceUuid, draftId, inboxReplyDraftApprove)

Approve and send a reply draft

Sends the draft to the network (optionally with an edited &#x60;body&#x60;). Ends as &#x60;sent&#x60;, or &#x60;failed&#x60; with &#x60;error&#x60;. Needs the &#x60;publish&#x60; ability; the API key that wrote the draft cannot approve it (&#x60;403&#x60;, &#x60;code: self_approval&#x60;). A draft is sent at most once: approving again returns &#x60;409&#x60;. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String draftId = "draftId_example"; // String | The draft `id`.
    InboxReplyDraftApprove inboxReplyDraftApprove = new InboxReplyDraftApprove(); // InboxReplyDraftApprove | 
    try {
      CreateInboxReplyDraft201Response result = apiInstance.approveInboxReplyDraft(workspaceUuid, draftId, inboxReplyDraftApprove);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#approveInboxReplyDraft");
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
| **draftId** | **String**| The draft &#x60;id&#x60;. | |
| **inboxReplyDraftApprove** | [**InboxReplyDraftApprove**](InboxReplyDraftApprove.md)|  | [optional] |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The reviewed draft |  -  |
| **401** |  |  -  |
| **403** | Not allowed: not a workspace admin or member, a scoped key without the &#x60;publish&#x60; ability (&#x60;code: insufficient_scope&#x60;), or the key that wrote the draft (&#x60;code: self_approval&#x60;).  |  -  |
| **404** |  |  -  |
| **409** | The draft was already reviewed. |  -  |
| **422** |  |  -  |

<a id="createInboxReplyDraft"></a>
# **createInboxReplyDraft**
> CreateInboxReplyDraft201Response createInboxReplyDraft(workspaceUuid, conversationId, inboxReplyDraftInput)

Draft a reply

Proposes a reply. Nothing is posted: a person approves the draft in the app (Reply drafts page) or another API key with the &#x60;publish&#x60; ability approves it. &#x60;in_reply_to&#x60; defaults to the latest incoming message. The body limit depends on the network (Bluesky 300, Mastodon 500, LinkedIn 1250, Google 4000). Needs the &#x60;write&#x60; ability. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String conversationId = "conversationId_example"; // String | The conversation `id`.
    InboxReplyDraftInput inboxReplyDraftInput = new InboxReplyDraftInput(); // InboxReplyDraftInput | 
    try {
      CreateInboxReplyDraft201Response result = apiInstance.createInboxReplyDraft(workspaceUuid, conversationId, inboxReplyDraftInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#createInboxReplyDraft");
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
| **conversationId** | **String**| The conversation &#x60;id&#x60;. | |
| **inboxReplyDraftInput** | [**InboxReplyDraftInput**](InboxReplyDraftInput.md)|  | |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The pending draft |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="deleteInboxReplyDraft"></a>
# **deleteInboxReplyDraft**
> deleteInboxReplyDraft(workspaceUuid, draftId)

Withdraw a reply draft

Deletes a pending draft. &#x60;409&#x60; once it was reviewed. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String draftId = "draftId_example"; // String | The draft `id`.
    try {
      apiInstance.deleteInboxReplyDraft(workspaceUuid, draftId);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#deleteInboxReplyDraft");
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
| **draftId** | **String**| The draft &#x60;id&#x60;. | |

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
| **409** | The draft was already reviewed. |  -  |

<a id="getInboxConversation"></a>
# **getInboxConversation**
> GetInboxConversation200Response getInboxConversation(workspaceUuid, conversationId)

Get an inbox conversation

The conversation with its 50 most recent messages, oldest first. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String conversationId = "conversationId_example"; // String | The conversation `id`.
    try {
      GetInboxConversation200Response result = apiInstance.getInboxConversation(workspaceUuid, conversationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#getInboxConversation");
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
| **conversationId** | **String**| The conversation &#x60;id&#x60;. | |

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The conversation |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getInboxReplyDraft"></a>
# **getInboxReplyDraft**
> CreateInboxReplyDraft201Response getInboxReplyDraft(workspaceUuid, draftId)

Get a reply draft

One draft. Poll it to see whether it was approved and sent. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String draftId = "draftId_example"; // String | The draft `id`.
    try {
      CreateInboxReplyDraft201Response result = apiInstance.getInboxReplyDraft(workspaceUuid, draftId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#getInboxReplyDraft");
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
| **draftId** | **String**| The draft &#x60;id&#x60;. | |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The draft |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listInboxConversations"></a>
# **listInboxConversations**
> ListInboxConversations200Response listInboxConversations(workspaceUuid, status, accountId, provider, unread, sentiment, aiLabel, since, page)

List inbox conversations

Comments, mentions and reviews on your accounts, most recent activity first, 25 per page. Available for Bluesky, Mastodon, LinkedIn Pages and Google Business Profile. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String status = "open"; // String | Conversation status.
    Integer accountId = 56; // Integer | Account `id`.
    String provider = "provider_example"; // String | Network, for example `bluesky`.
    Boolean unread = true; // Boolean | Only unread (`true`) or read (`false`) conversations.
    String sentiment = "negative"; // String | AI sentiment.
    String aiLabel = "question"; // String | AI label.
    OffsetDateTime since = OffsetDateTime.now(); // OffsetDateTime | Only conversations with activity at or after this time.
    Integer page = 1; // Integer | Page number.
    try {
      ListInboxConversations200Response result = apiInstance.listInboxConversations(workspaceUuid, status, accountId, provider, unread, sentiment, aiLabel, since, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#listInboxConversations");
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
| **status** | **String**| Conversation status. | [optional] [enum: open, resolved] |
| **accountId** | **Integer**| Account &#x60;id&#x60;. | [optional] |
| **provider** | **String**| Network, for example &#x60;bluesky&#x60;. | [optional] |
| **unread** | **Boolean**| Only unread (&#x60;true&#x60;) or read (&#x60;false&#x60;) conversations. | [optional] |
| **sentiment** | **String**| AI sentiment. | [optional] [enum: negative, neutral, positive] |
| **aiLabel** | **String**| AI label. | [optional] [enum: question, complaint, praise, lead, other] |
| **since** | **OffsetDateTime**| Only conversations with activity at or after this time. | [optional] |
| **page** | **Integer**| Page number. | [optional] [default to 1] |

### Return type

[**ListInboxConversations200Response**](ListInboxConversations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Conversations |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="listInboxReplyDrafts"></a>
# **listInboxReplyDrafts**
> ListInboxReplyDrafts200Response listInboxReplyDrafts(workspaceUuid, status, conversationId, page)

List reply drafts

Reply drafts, newest first, 25 per page. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String status = "pending"; // String | Draft status.
    String conversationId = "conversationId_example"; // String | Only drafts for this conversation `id`.
    Integer page = 1; // Integer | Page number.
    try {
      ListInboxReplyDrafts200Response result = apiInstance.listInboxReplyDrafts(workspaceUuid, status, conversationId, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#listInboxReplyDrafts");
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
| **status** | **String**| Draft status. | [optional] [enum: pending, approved, rejected, sent, failed] |
| **conversationId** | **String**| Only drafts for this conversation &#x60;id&#x60;. | [optional] |
| **page** | **Integer**| Page number. | [optional] [default to 1] |

### Return type

[**ListInboxReplyDrafts200Response**](ListInboxReplyDrafts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Drafts |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="rejectInboxReplyDraft"></a>
# **rejectInboxReplyDraft**
> CreateInboxReplyDraft201Response rejectInboxReplyDraft(workspaceUuid, draftId)

Reject a reply draft

Rejects a pending draft; nothing is sent. Needs the &#x60;publish&#x60; ability. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String draftId = "draftId_example"; // String | The draft `id`.
    try {
      CreateInboxReplyDraft201Response result = apiInstance.rejectInboxReplyDraft(workspaceUuid, draftId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#rejectInboxReplyDraft");
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
| **draftId** | **String**| The draft &#x60;id&#x60;. | |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The rejected draft |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** | The draft was already reviewed. |  -  |

<a id="updateInboxConversation"></a>
# **updateInboxConversation**
> GetInboxConversation200Response updateInboxConversation(workspaceUuid, conversationId, inboxConversationUpdate)

Update an inbox conversation

Marks the conversation open or resolved, read or unread. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String conversationId = "conversationId_example"; // String | The conversation `id`.
    InboxConversationUpdate inboxConversationUpdate = new InboxConversationUpdate(); // InboxConversationUpdate | 
    try {
      GetInboxConversation200Response result = apiInstance.updateInboxConversation(workspaceUuid, conversationId, inboxConversationUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#updateInboxConversation");
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
| **conversationId** | **String**| The conversation &#x60;id&#x60;. | |
| **inboxConversationUpdate** | [**InboxConversationUpdate**](InboxConversationUpdate.md)|  | |

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The conversation |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="updateInboxReplyDraft"></a>
# **updateInboxReplyDraft**
> CreateInboxReplyDraft201Response updateInboxReplyDraft(workspaceUuid, draftId, inboxReplyDraftEdit)

Edit a reply draft

Changes the text of a pending draft. &#x60;409&#x60; once it was reviewed. Requires the inbox API to be enabled for the workspace (otherwise &#x60;404&#x60;). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.InboxApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InboxApi apiInstance = new InboxApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String draftId = "draftId_example"; // String | The draft `id`.
    InboxReplyDraftEdit inboxReplyDraftEdit = new InboxReplyDraftEdit(); // InboxReplyDraftEdit | 
    try {
      CreateInboxReplyDraft201Response result = apiInstance.updateInboxReplyDraft(workspaceUuid, draftId, inboxReplyDraftEdit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InboxApi#updateInboxReplyDraft");
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
| **draftId** | **String**| The draft &#x60;id&#x60;. | |
| **inboxReplyDraftEdit** | [**InboxReplyDraftEdit**](InboxReplyDraftEdit.md)|  | |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The draft |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** | The draft was already reviewed. |  -  |
| **422** |  |  -  |

