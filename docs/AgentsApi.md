# AgentsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**approveAgentProposal**](AgentsApi.md#approveAgentProposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/approve | Approve and apply an agent proposal |
| [**createAgent**](AgentsApi.md#createAgent) | **POST** /{workspaceUuid}/agents | Switch on a background agent |
| [**deleteAgent**](AgentsApi.md#deleteAgent) | **DELETE** /{workspaceUuid}/agents/{agentUuid} | Delete a background agent |
| [**getAgentRun**](AgentsApi.md#getAgentRun) | **GET** /{workspaceUuid}/agent-runs/{runUuid} | Get an agent run with its proposals |
| [**listAgentProposals**](AgentsApi.md#listAgentProposals) | **GET** /{workspaceUuid}/agent-proposals | List agent proposals (approval queue) |
| [**listAgentRuns**](AgentsApi.md#listAgentRuns) | **GET** /{workspaceUuid}/agents/{agentUuid}/runs | Run history of an agent |
| [**listAgents**](AgentsApi.md#listAgents) | **GET** /{workspaceUuid}/agents | List background agents |
| [**rejectAgentProposal**](AgentsApi.md#rejectAgentProposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/reject | Reject an agent proposal |
| [**runAgent**](AgentsApi.md#runAgent) | **POST** /{workspaceUuid}/agents/{agentUuid}/run | Run a background agent now |
| [**updateAgent**](AgentsApi.md#updateAgent) | **PUT** /{workspaceUuid}/agents/{agentUuid} | Update a background agent |


<a id="approveAgentProposal"></a>
# **approveAgentProposal**
> ApproveAgentProposal200Response approveAgentProposal(workspaceUuid, proposalUuid, agentProposalDecision)

Approve and apply an agent proposal

Applies the proposal at once: &#x60;hold_post&#x60; moves the post back to draft, &#x60;edit_caption&#x60; replaces the caption. When the post was edited, deleted or left the schedule since the proposal was made, nothing changes and the proposal becomes &#x60;stale&#x60;. Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID proposalUuid = UUID.randomUUID(); // UUID | 
    AgentProposalDecision agentProposalDecision = new AgentProposalDecision(); // AgentProposalDecision | 
    try {
      ApproveAgentProposal200Response result = apiInstance.approveAgentProposal(workspaceUuid, proposalUuid, agentProposalDecision);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#approveAgentProposal");
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
| **proposalUuid** | **UUID**|  | |
| **agentProposalDecision** | [**AgentProposalDecision**](AgentProposalDecision.md)|  | [optional] |

### Return type

[**ApproveAgentProposal200Response**](ApproveAgentProposal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Decision recorded; read &#x60;data.status&#x60; (&#x60;applied&#x60;, &#x60;stale&#x60; or &#x60;failed&#x60;) |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** | The proposal was already decided, expired or went stale; &#x60;data&#x60; is its current state. |  -  |

<a id="createAgent"></a>
# **createAgent**
> CreateAgent201Response createAgent(workspaceUuid, workspaceAgentInput)

Switch on a background agent

Creates an agent (one per type per workspace). It first runs within five minutes, then on its &#x60;schedule&#x60;. **Pre-publish checker** looks at posts scheduled in the next &#x60;horizon_hours&#x60; and proposes holding (back to draft) posts that would fail: disconnected accounts, network requirements, daily caps, the X allowance and links that answer an error. It proposes caption edits that drop &#x60;banned_phrases&#x60;. With &#x60;ai_review: true&#x60; it also asks AI to review up to &#x60;max_ai_reviews_per_run&#x60; posts per run (one AI credit each). Admins and members only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    WorkspaceAgentInput workspaceAgentInput = new WorkspaceAgentInput(); // WorkspaceAgentInput | 
    try {
      CreateAgent201Response result = apiInstance.createAgent(workspaceUuid, workspaceAgentInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#createAgent");
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
| **workspaceAgentInput** | [**WorkspaceAgentInput**](WorkspaceAgentInput.md)|  | |

### Return type

[**CreateAgent201Response**](CreateAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Agent created |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteAgent"></a>
# **deleteAgent**
> DeleteAgent200Response deleteAgent(workspaceUuid, agentUuid)

Delete a background agent

Removes the agent. Its run history and proposals stay. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID agentUuid = UUID.randomUUID(); // UUID | 
    try {
      DeleteAgent200Response result = apiInstance.deleteAgent(workspaceUuid, agentUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#deleteAgent");
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
| **agentUuid** | **UUID**|  | |

### Return type

[**DeleteAgent200Response**](DeleteAgent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Agent deleted |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getAgentRun"></a>
# **getAgentRun**
> RunAgent202Response getAgentRun(workspaceUuid, runUuid)

Get an agent run with its proposals

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID runUuid = UUID.randomUUID(); // UUID | 
    try {
      RunAgent202Response result = apiInstance.getAgentRun(workspaceUuid, runUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#getAgentRun");
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
| **runUuid** | **UUID**|  | |

### Return type

[**RunAgent202Response**](RunAgent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Run |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listAgentProposals"></a>
# **listAgentProposals**
> ListAgentProposals200Response listAgentProposals(workspaceUuid, status, perPage, page)

List agent proposals (approval queue)

Proposals of all agents in the workspace, newest first. Defaults to &#x60;pending&#x60;.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String status = "pending"; // String | 
    Integer perPage = 20; // Integer | 
    Integer page = 56; // Integer | 
    try {
      ListAgentProposals200Response result = apiInstance.listAgentProposals(workspaceUuid, status, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#listAgentProposals");
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
| **status** | **String**|  | [optional] [default to pending] [enum: pending, applied, rejected, stale, failed, expired] |
| **perPage** | **Integer**|  | [optional] [default to 20] |
| **page** | **Integer**|  | [optional] |

### Return type

[**ListAgentProposals200Response**](ListAgentProposals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Proposals |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="listAgentRuns"></a>
# **listAgentRuns**
> ListAgentRuns200Response listAgentRuns(workspaceUuid, agentUuid, perPage, page)

Run history of an agent

Runs of the agent, newest first, with what each checked and proposed and the AI credits it used.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID agentUuid = UUID.randomUUID(); // UUID | 
    Integer perPage = 20; // Integer | 
    Integer page = 56; // Integer | 
    try {
      ListAgentRuns200Response result = apiInstance.listAgentRuns(workspaceUuid, agentUuid, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#listAgentRuns");
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
| **agentUuid** | **UUID**|  | |
| **perPage** | **Integer**|  | [optional] [default to 20] |
| **page** | **Integer**|  | [optional] |

### Return type

[**ListAgentRuns200Response**](ListAgentRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Runs |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listAgents"></a>
# **listAgents**
> ListAgents200Response listAgents(workspaceUuid)

List background agents

Background agents switched on for the workspace. Agents run on a schedule, record every run and never change a post themselves: each change is a proposal that a workspace admin or member approves. Available type: &#x60;pre_publish_checker&#x60;. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListAgents200Response result = apiInstance.listAgents(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#listAgents");
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

[**ListAgents200Response**](ListAgents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Agents |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="rejectAgentProposal"></a>
# **rejectAgentProposal**
> ApproveAgentProposal200Response rejectAgentProposal(workspaceUuid, proposalUuid, agentProposalDecision)

Reject an agent proposal

Records the rejection (and optional note); nothing changes on the post. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID proposalUuid = UUID.randomUUID(); // UUID | 
    AgentProposalDecision agentProposalDecision = new AgentProposalDecision(); // AgentProposalDecision | 
    try {
      ApproveAgentProposal200Response result = apiInstance.rejectAgentProposal(workspaceUuid, proposalUuid, agentProposalDecision);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#rejectAgentProposal");
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
| **proposalUuid** | **UUID**|  | |
| **agentProposalDecision** | [**AgentProposalDecision**](AgentProposalDecision.md)|  | [optional] |

### Return type

[**ApproveAgentProposal200Response**](ApproveAgentProposal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Proposal rejected |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** | The proposal was already decided, expired or went stale; &#x60;data&#x60; is its current state. |  -  |

<a id="runAgent"></a>
# **runAgent**
> RunAgent202Response runAgent(workspaceUuid, agentUuid)

Run a background agent now

Queues a run outside the schedule (&#x60;trigger: manual&#x60;). Six per hour. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID agentUuid = UUID.randomUUID(); // UUID | 
    try {
      RunAgent202Response result = apiInstance.runAgent(workspaceUuid, agentUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#runAgent");
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
| **agentUuid** | **UUID**|  | |

### Return type

[**RunAgent202Response**](RunAgent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Run queued |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **409** | The agent already has a queued or running run. |  -  |

<a id="updateAgent"></a>
# **updateAgent**
> CreateAgent201Response updateAgent(workspaceUuid, agentUuid, workspaceAgentUpdate)

Update a background agent

Changes the name, schedule, settings or &#x60;enabled&#x60;. Settings you leave out keep their value. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID agentUuid = UUID.randomUUID(); // UUID | 
    WorkspaceAgentUpdate workspaceAgentUpdate = new WorkspaceAgentUpdate(); // WorkspaceAgentUpdate | 
    try {
      CreateAgent201Response result = apiInstance.updateAgent(workspaceUuid, agentUuid, workspaceAgentUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#updateAgent");
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
| **agentUuid** | **UUID**|  | |
| **workspaceAgentUpdate** | [**WorkspaceAgentUpdate**](WorkspaceAgentUpdate.md)|  | |

### Return type

[**CreateAgent201Response**](CreateAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Agent updated |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

