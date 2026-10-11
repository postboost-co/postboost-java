# MediaApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**abortChunkedUpload**](MediaApi.md#abortChunkedUpload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload |
| [**completeChunkedUpload**](MediaApi.md#completeChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload |
| [**createMediaFolder**](MediaApi.md#createMediaFolder) | **POST** /{workspaceUuid}/media/folders | Create media folder |
| [**deleteMediaBulk**](MediaApi.md#deleteMediaBulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk) |
| [**deleteMediaFolder**](MediaApi.md#deleteMediaFolder) | **DELETE** /{workspaceUuid}/media/folders/{folderUuid} | Delete media folder |
| [**getMedia**](MediaApi.md#getMedia) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media |
| [**getRemoteUploadStatus**](MediaApi.md#getRemoteUploadStatus) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status |
| [**initiateChunkedUpload**](MediaApi.md#initiateChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload |
| [**initiateRemoteUpload**](MediaApi.md#initiateRemoteUpload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload |
| [**listMedia**](MediaApi.md#listMedia) | **GET** /{workspaceUuid}/media | List media |
| [**listMediaFolders**](MediaApi.md#listMediaFolders) | **GET** /{workspaceUuid}/media/folders | List media folders |
| [**updateMedia**](MediaApi.md#updateMedia) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media |
| [**updateMediaFolder**](MediaApi.md#updateMediaFolder) | **PUT** /{workspaceUuid}/media/folders/{folderUuid} | Update media folder |
| [**uploadChunk**](MediaApi.md#uploadChunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk |
| [**uploadMedia**](MediaApi.md#uploadMedia) | **POST** /{workspaceUuid}/media | Upload media (binary) |


<a id="abortChunkedUpload"></a>
# **abortChunkedUpload**
> abortChunkedUpload(workspaceUuid, uploadUuid)

Abort chunked upload

Cancel an in-progress chunked upload session and clean up uploaded chunks.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID uploadUuid = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.abortChunkedUpload(workspaceUuid, uploadUuid);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#abortChunkedUpload");
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
| **uploadUuid** | **UUID**|  | |

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
| **204** | Upload aborted |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="completeChunkedUpload"></a>
# **completeChunkedUpload**
> Media completeChunkedUpload(workspaceUuid, uploadUuid, completeChunkedUploadRequest)

Complete chunked upload

Signal that all chunks have been uploaded. Returns the final media object. A video may come back with &#x60;is_processing&#x60; set to &#x60;true&#x60; while its conversion runs.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID uploadUuid = UUID.randomUUID(); // UUID | 
    CompleteChunkedUploadRequest completeChunkedUploadRequest = new CompleteChunkedUploadRequest(); // CompleteChunkedUploadRequest | 
    try {
      Media result = apiInstance.completeChunkedUpload(workspaceUuid, uploadUuid, completeChunkedUploadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#completeChunkedUpload");
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
| **uploadUuid** | **UUID**|  | |
| **completeChunkedUploadRequest** | [**CompleteChunkedUploadRequest**](CompleteChunkedUploadRequest.md)|  | [optional] |

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Completed media object |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="createMediaFolder"></a>
# **createMediaFolder**
> MediaFolder createMediaFolder(workspaceUuid, createMediaFolderRequest)

Create media folder

Creates a folder at the top level or under &#x60;parent&#x60;. The name must be unique among its siblings.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    CreateMediaFolderRequest createMediaFolderRequest = new CreateMediaFolderRequest(); // CreateMediaFolderRequest | 
    try {
      MediaFolder result = apiInstance.createMediaFolder(workspaceUuid, createMediaFolderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#createMediaFolder");
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
| **createMediaFolderRequest** | [**CreateMediaFolderRequest**](CreateMediaFolderRequest.md)|  | |

### Return type

[**MediaFolder**](MediaFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created folder |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteMediaBulk"></a>
# **deleteMediaBulk**
> Object deleteMediaBulk(workspaceUuid, deleteMediaBulkRequest)

Delete media (bulk)

Delete one or more media items by their numeric IDs or UUIDs (both may be mixed, up to 500 per request).

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    DeleteMediaBulkRequest deleteMediaBulkRequest = new DeleteMediaBulkRequest(); // DeleteMediaBulkRequest | 
    try {
      Object result = apiInstance.deleteMediaBulk(workspaceUuid, deleteMediaBulkRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#deleteMediaBulk");
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
| **deleteMediaBulkRequest** | [**DeleteMediaBulkRequest**](DeleteMediaBulkRequest.md)|  | |

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
| **422** |  |  -  |

<a id="deleteMediaFolder"></a>
# **deleteMediaFolder**
> Object deleteMediaFolder(workspaceUuid, folderUuid, deleteMediaFolderRequest)

Delete media folder

Deletes a folder. By default its media and sub-folders move up to the folder&#39;s parent; with &#x60;delete_media&#x60; set to true every media item below the folder is deleted as well.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID folderUuid = UUID.randomUUID(); // UUID | UUID of the media folder.
    DeleteMediaFolderRequest deleteMediaFolderRequest = new DeleteMediaFolderRequest(); // DeleteMediaFolderRequest | 
    try {
      Object result = apiInstance.deleteMediaFolder(workspaceUuid, folderUuid, deleteMediaFolderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#deleteMediaFolder");
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
| **folderUuid** | **UUID**| UUID of the media folder. | |
| **deleteMediaFolderRequest** | [**DeleteMediaFolderRequest**](DeleteMediaFolderRequest.md)|  | [optional] |

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
| **422** |  |  -  |

<a id="getMedia"></a>
# **getMedia**
> Media getMedia(workspaceUuid, mediaUuid)

Get media

Returns a single media asset.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID mediaUuid = UUID.randomUUID(); // UUID | UUID of the media asset.
    try {
      Media result = apiInstance.getMedia(workspaceUuid, mediaUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#getMedia");
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
| **mediaUuid** | **UUID**| UUID of the media asset. | |

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Media asset |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getRemoteUploadStatus"></a>
# **getRemoteUploadStatus**
> GetRemoteUploadStatus200Response getRemoteUploadStatus(workspaceUuid, downloadId)

Get remote upload status

Poll the status of an in-progress remote media download.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String downloadId = "downloadId_example"; // String | 
    try {
      GetRemoteUploadStatus200Response result = apiInstance.getRemoteUploadStatus(workspaceUuid, downloadId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#getRemoteUploadStatus");
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
| **downloadId** | **String**|  | |

### Return type

[**GetRemoteUploadStatus200Response**](GetRemoteUploadStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Download status |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="initiateChunkedUpload"></a>
# **initiateChunkedUpload**
> InitiateChunkedUpload201Response initiateChunkedUpload(workspaceUuid, initiateChunkedUploadRequest)

Initiate chunked upload

Start a chunked upload session for large files. Returns an &#x60;upload_uuid&#x60;, &#x60;chunk_size&#x60;, and &#x60;total_chunks&#x60; to use for subsequent chunk requests. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    InitiateChunkedUploadRequest initiateChunkedUploadRequest = new InitiateChunkedUploadRequest(); // InitiateChunkedUploadRequest | 
    try {
      InitiateChunkedUpload201Response result = apiInstance.initiateChunkedUpload(workspaceUuid, initiateChunkedUploadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#initiateChunkedUpload");
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
| **initiateChunkedUploadRequest** | [**InitiateChunkedUploadRequest**](InitiateChunkedUploadRequest.md)|  | |

### Return type

[**InitiateChunkedUpload201Response**](InitiateChunkedUpload201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Chunked upload session details |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="initiateRemoteUpload"></a>
# **initiateRemoteUpload**
> InitiateRemoteUpload201Response initiateRemoteUpload(workspaceUuid, initiateRemoteUploadRequest)

Initiate remote upload

Download a file from a remote URL into the media library. For small files the media object is returned immediately. For large files a &#x60;download_id&#x60; is returned — poll the status endpoint. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    InitiateRemoteUploadRequest initiateRemoteUploadRequest = new InitiateRemoteUploadRequest(); // InitiateRemoteUploadRequest | 
    try {
      InitiateRemoteUpload201Response result = apiInstance.initiateRemoteUpload(workspaceUuid, initiateRemoteUploadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#initiateRemoteUpload");
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
| **initiateRemoteUploadRequest** | [**InitiateRemoteUploadRequest**](InitiateRemoteUploadRequest.md)|  | |

### Return type

[**InitiateRemoteUpload201Response**](InitiateRemoteUpload201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Media object or download job |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="listMedia"></a>
# **listMedia**
> ListMedia200Response listMedia(workspaceUuid, page, limit, folder, mimeTypes, type, keyword, usage, favorite, sort)

List media

Returns a paginated list of media assets in the workspace library. Without &#x60;folder&#x60; every item is listed, whatever folder it is filed in. A &#x60;keyword&#x60; search always looks at the whole library and ignores &#x60;folder&#x60; and &#x60;favorite&#x60;. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    Integer page = 1; // Integer | Page number.
    Integer limit = 50; // Integer | Items per page. Values below 1 fall back to 50; values above 100 are capped at 100.
    String folder = "folder_example"; // String | Media folder UUID, or `root` for items not filed in any folder.
    List<String> mimeTypes = Arrays.asList(); // List<String> | Only these MIME types (for example `image/png`).
    String type = "image"; // String | Only this media type.
    String keyword = "keyword_example"; // String | Search media by name.
    String usage = "unused"; // String | Filter by how the media is used in posts.
    Boolean favorite = true; // Boolean | When `true`, only media the caller marked as favorite.
    String sort = "newest"; // String | 
    try {
      ListMedia200Response result = apiInstance.listMedia(workspaceUuid, page, limit, folder, mimeTypes, type, keyword, usage, favorite, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#listMedia");
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
| **page** | **Integer**| Page number. | [optional] [default to 1] |
| **limit** | **Integer**| Items per page. Values below 1 fall back to 50; values above 100 are capped at 100. | [optional] [default to 50] |
| **folder** | **String**| Media folder UUID, or &#x60;root&#x60; for items not filed in any folder. | [optional] |
| **mimeTypes** | [**List&lt;String&gt;**](String.md)| Only these MIME types (for example &#x60;image/png&#x60;). | [optional] |
| **type** | **String**| Only this media type. | [optional] [enum: image, gif, video] |
| **keyword** | **String**| Search media by name. | [optional] |
| **usage** | **String**| Filter by how the media is used in posts. | [optional] [enum: unused, draft, scheduled, published] |
| **favorite** | **Boolean**| When &#x60;true&#x60;, only media the caller marked as favorite. | [optional] |
| **sort** | **String**|  | [optional] [default to newest] [enum: newest, oldest, name, size] |

### Return type

[**ListMedia200Response**](ListMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of media |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="listMediaFolders"></a>
# **listMediaFolders**
> ListMediaFolders200Response listMediaFolders(workspaceUuid)

List media folders

Returns the whole folder tree of the media library in one response (not paginated). Rebuild the tree from each folder&#39;s &#x60;parent&#x60;.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListMediaFolders200Response result = apiInstance.listMediaFolders(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#listMediaFolders");
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

[**ListMediaFolders200Response**](ListMediaFolders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | All media folders |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="updateMedia"></a>
# **updateMedia**
> Object updateMedia(workspaceUuid, mediaUuid, updateMediaRequest)

Update media

Update the name, alt text, or folder of a media asset. Only the keys present in the body are written. Sending &#x60;folder: null&#x60; moves the item to the library root; omitting &#x60;folder&#x60; leaves it where it is. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID mediaUuid = UUID.randomUUID(); // UUID | UUID of the media asset.
    UpdateMediaRequest updateMediaRequest = new UpdateMediaRequest(); // UpdateMediaRequest | 
    try {
      Object result = apiInstance.updateMedia(workspaceUuid, mediaUuid, updateMediaRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#updateMedia");
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
| **mediaUuid** | **UUID**| UUID of the media asset. | |
| **updateMediaRequest** | [**UpdateMediaRequest**](UpdateMediaRequest.md)|  | |

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
| **422** |  |  -  |

<a id="updateMediaFolder"></a>
# **updateMediaFolder**
> MediaFolder updateMediaFolder(workspaceUuid, folderUuid, mediaFolderInput)

Update media folder

Renames a folder and/or moves it. Sending &#x60;parent&#x60; moves the folder (null &#x3D; top level); omitting it keeps the current parent. A folder cannot be moved into itself or one of its descendants.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID folderUuid = UUID.randomUUID(); // UUID | UUID of the media folder.
    MediaFolderInput mediaFolderInput = new MediaFolderInput(); // MediaFolderInput | 
    try {
      MediaFolder result = apiInstance.updateMediaFolder(workspaceUuid, folderUuid, mediaFolderInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#updateMediaFolder");
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
| **folderUuid** | **UUID**| UUID of the media folder. | |
| **mediaFolderInput** | [**MediaFolderInput**](MediaFolderInput.md)|  | |

### Return type

[**MediaFolder**](MediaFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated folder |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="uploadChunk"></a>
# **uploadChunk**
> UploadChunk201Response uploadChunk(workspaceUuid, uploadUuid, chunk, chunkIndex)

Upload a chunk

Upload a single chunk of a chunked upload session.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID uploadUuid = UUID.randomUUID(); // UUID | 
    File chunk = new File("/path/to/file"); // File | 
    Integer chunkIndex = 56; // Integer | Zero-based index of this chunk.
    try {
      UploadChunk201Response result = apiInstance.uploadChunk(workspaceUuid, uploadUuid, chunk, chunkIndex);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#uploadChunk");
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
| **uploadUuid** | **UUID**|  | |
| **chunk** | **File**|  | |
| **chunkIndex** | **Integer**| Zero-based index of this chunk. | |

### Return type

[**UploadChunk201Response**](UploadChunk201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Chunk received |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="uploadMedia"></a>
# **uploadMedia**
> Media uploadMedia(workspaceUuid, _file, altText, folder)

Upload media (binary)

Upload a file directly as multipart form data.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    File _file = new File("/path/to/file"); // File | The file to upload.
    String altText = "altText_example"; // String | Alternative text for accessibility.
    UUID folder = UUID.randomUUID(); // UUID | UUID of the media folder to file the upload in. Omit or null for the library root.
    try {
      Media result = apiInstance.uploadMedia(workspaceUuid, _file, altText, folder);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#uploadMedia");
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
| **_file** | **File**| The file to upload. | |
| **altText** | **String**| Alternative text for accessibility. | [optional] |
| **folder** | **UUID**| UUID of the media folder to file the upload in. Omit or null for the library root. | [optional] |

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Uploaded media object. A video may come back with &#x60;is_processing&#x60; set to &#x60;true&#x60; while its conversion runs. |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

