# WebhooksApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createWebhookSubscription**](WebhooksApi.md#createWebhookSubscription) | **POST** /{workspaceUuid}/webhooks/subscriptions | Subscribe a webhook |
| [**deleteWebhookSubscription**](WebhooksApi.md#deleteWebhookSubscription) | **DELETE** /{workspaceUuid}/webhooks/subscriptions/{subscriptionUuid} | Unsubscribe a webhook |
| [**listWebhookSubscriptions**](WebhooksApi.md#listWebhookSubscriptions) | **GET** /{workspaceUuid}/webhooks/subscriptions | List webhook subscriptions |


<a id="createWebhookSubscription"></a>
# **createWebhookSubscription**
> CreateWebhookSubscription201Response createWebhookSubscription(workspaceUuid, webhookSubscriptionInput)

Subscribe a webhook

Registers a callback URL for the given events, the way n8n, Zapier and Make instant triggers do. Deliveries are &#x60;POST&#x60; requests with a JSON body (see [Webhooks](/webhooks) for the payload), signed with the returned &#x60;secret&#x60; in &#x60;X-Signature&#x60; (HMAC-SHA256 of the raw body, hex encoded) and attempted up to 3 times. Only public &#x60;https://&#x60; URLs are accepted. The &#x60;secret&#x60; is in this response only. Workspace admins only. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    WebhookSubscriptionInput webhookSubscriptionInput = new WebhookSubscriptionInput(); // WebhookSubscriptionInput | 
    try {
      CreateWebhookSubscription201Response result = apiInstance.createWebhookSubscription(workspaceUuid, webhookSubscriptionInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#createWebhookSubscription");
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
| **webhookSubscriptionInput** | [**WebhookSubscriptionInput**](WebhookSubscriptionInput.md)|  | |

### Return type

[**CreateWebhookSubscription201Response**](CreateWebhookSubscription201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The subscription was created |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteWebhookSubscription"></a>
# **deleteWebhookSubscription**
> Object deleteWebhookSubscription(workspaceUuid, subscriptionUuid)

Unsubscribe a webhook

Deletes the webhook and stops its deliveries. Workspace admins only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID subscriptionUuid = UUID.randomUUID(); // UUID | UUID of the webhook subscription.
    try {
      Object result = apiInstance.deleteWebhookSubscription(workspaceUuid, subscriptionUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#deleteWebhookSubscription");
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
| **subscriptionUuid** | **UUID**| UUID of the webhook subscription. | |

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

<a id="listWebhookSubscriptions"></a>
# **listWebhookSubscriptions**
> ListWebhookSubscriptions200Response listWebhookSubscriptions(workspaceUuid)

List webhook subscriptions

The workspace&#39;s webhooks, newest first: subscriptions created through this API and the ones added in **Settings → Webhooks**. Secrets are never returned here. Workspace admins only; needs the &#x60;webhooks&#x60; plan capability and, for scoped keys, the &#x60;webhooks&#x60; ability. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListWebhookSubscriptions200Response result = apiInstance.listWebhookSubscriptions(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#listWebhookSubscriptions");
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

[**ListWebhookSubscriptions200Response**](ListWebhookSubscriptions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The workspace&#39;s webhooks |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

