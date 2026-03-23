# MediaApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**abortChunkedUpload**](MediaApi.md#abortChunkedUpload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload |
| [**completeChunkedUpload**](MediaApi.md#completeChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload |
| [**deleteMediaBulk**](MediaApi.md#deleteMediaBulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk) |
| [**getMedia**](MediaApi.md#getMedia) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media |
| [**getRemoteUploadStatus**](MediaApi.md#getRemoteUploadStatus) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status |
| [**initiateChunkedUpload**](MediaApi.md#initiateChunkedUpload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload |
| [**initiateRemoteUpload**](MediaApi.md#initiateRemoteUpload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload |
| [**listMedia**](MediaApi.md#listMedia) | **GET** /{workspaceUuid}/media | List media |
| [**updateMedia**](MediaApi.md#updateMedia) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media |
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

<a id="completeChunkedUpload"></a>
# **completeChunkedUpload**
> Media completeChunkedUpload(workspaceUuid, uploadUuid)

Complete chunked upload

Signal that all chunks have been uploaded. Returns the final media object.

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
      Media result = apiInstance.completeChunkedUpload(workspaceUuid, uploadUuid);
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
| **201** | Completed media object |  -  |
| **401** |  |  -  |
| **422** |  |  -  |

<a id="deleteMediaBulk"></a>
# **deleteMediaBulk**
> Object deleteMediaBulk(workspaceUuid, deleteMediaBulkRequest)

Delete media (bulk)

Delete one or more media items by their IDs.

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
| **422** |  |  -  |

<a id="listMedia"></a>
# **listMedia**
> ListMedia200Response listMedia(workspaceUuid, page)

List media

Returns a paginated list of media assets in the workspace library.

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
    Integer page = 1; // Integer | Page number (20 items per page).
    try {
      ListMedia200Response result = apiInstance.listMedia(workspaceUuid, page);
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
| **page** | **Integer**| Page number (20 items per page). | [optional] [default to 1] |

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

<a id="updateMedia"></a>
# **updateMedia**
> Object updateMedia(workspaceUuid, mediaUuid, updateMediaRequest)

Update media

Update the alt text of a media asset.

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
| **404** |  |  -  |

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
| **422** |  |  -  |

<a id="uploadMedia"></a>
# **uploadMedia**
> Media uploadMedia(workspaceUuid, _file, altText)

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
    try {
      Media result = apiInstance.uploadMedia(workspaceUuid, _file, altText);
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
| **201** | Uploaded media object |  -  |
| **401** |  |  -  |
| **422** |  |  -  |

