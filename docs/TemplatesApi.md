# TemplatesApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTemplate**](TemplatesApi.md#createTemplate) | **POST** /{workspaceUuid}/templates | Create a template |
| [**deleteTemplate**](TemplatesApi.md#deleteTemplate) | **DELETE** /{workspaceUuid}/templates/{templateId} | Delete a template |
| [**getTemplate**](TemplatesApi.md#getTemplate) | **GET** /{workspaceUuid}/templates/{templateId} | Get a template |
| [**listTemplates**](TemplatesApi.md#listTemplates) | **GET** /{workspaceUuid}/templates | List templates |
| [**updateTemplate**](TemplatesApi.md#updateTemplate) | **PUT** /{workspaceUuid}/templates/{templateId} | Update a template |


<a id="createTemplate"></a>
# **createTemplate**
> CreateTemplate201Response createTemplate(workspaceUuid, templateInput)

Create a template

Creates a post template: a name and one or more content items (body plus media ids from the media library). Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    TemplateInput templateInput = new TemplateInput(); // TemplateInput | 
    try {
      CreateTemplate201Response result = apiInstance.createTemplate(workspaceUuid, templateInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#createTemplate");
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
| **templateInput** | [**TemplateInput**](TemplateInput.md)|  | |

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The new template |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteTemplate"></a>
# **deleteTemplate**
> deleteTemplate(workspaceUuid, templateId)

Delete a template

Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String templateId = "templateId_example"; // String | The template `id`.
    try {
      apiInstance.deleteTemplate(workspaceUuid, templateId);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#deleteTemplate");
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
| **templateId** | **String**| The template &#x60;id&#x60;. | |

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

<a id="getTemplate"></a>
# **getTemplate**
> CreateTemplate201Response getTemplate(workspaceUuid, templateId)

Get a template

One template. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String templateId = "templateId_example"; // String | The template `id`.
    try {
      CreateTemplate201Response result = apiInstance.getTemplate(workspaceUuid, templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#getTemplate");
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
| **templateId** | **String**| The template &#x60;id&#x60;. | |

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The template |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listTemplates"></a>
# **listTemplates**
> ListTemplates200Response listTemplates(workspaceUuid, page, perPage)

List templates

Post templates of the workspace, newest first. The same templates as the Templates page in the app. Paginated with &#x60;page&#x60; and &#x60;per_page&#x60; (default 100). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer page = 1; // Integer | Page number (1-based).
    Integer perPage = 100; // Integer | Items per page, 1-100.
    try {
      ListTemplates200Response result = apiInstance.listTemplates(workspaceUuid, page, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#listTemplates");
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

[**ListTemplates200Response**](ListTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Templates, paginated (&#x60;links&#x60; and &#x60;meta&#x60; as on the other list endpoints) |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="updateTemplate"></a>
# **updateTemplate**
> CreateTemplate201Response updateTemplate(workspaceUuid, templateId, templateInput)

Update a template

Replaces the name and content of a template. Admins and members only (not viewers). 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String templateId = "templateId_example"; // String | The template `id`.
    TemplateInput templateInput = new TemplateInput(); // TemplateInput | 
    try {
      CreateTemplate201Response result = apiInstance.updateTemplate(workspaceUuid, templateId, templateInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#updateTemplate");
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
| **templateId** | **String**| The template &#x60;id&#x60;. | |
| **templateInput** | [**TemplateInput**](TemplateInput.md)|  | |

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The updated template |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

