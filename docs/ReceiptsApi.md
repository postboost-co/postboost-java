# ReceiptsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createReceipt**](ReceiptsApi.md#createReceipt) | **POST** /panel/receipts | Create receipt |
| [**deleteReceipt**](ReceiptsApi.md#deleteReceipt) | **DELETE** /panel/receipts/{receiptUuid} | Delete receipt |
| [**deleteReceiptsBulk**](ReceiptsApi.md#deleteReceiptsBulk) | **DELETE** /panel/receipts | Delete receipts (bulk) |
| [**getReceipt**](ReceiptsApi.md#getReceipt) | **GET** /panel/receipts/{receiptUuid} | Get receipt |
| [**listReceipts**](ReceiptsApi.md#listReceipts) | **GET** /panel/receipts | List receipts |
| [**updateReceipt**](ReceiptsApi.md#updateReceipt) | **PUT** /panel/receipts/{receiptUuid} | Update receipt |


<a id="createReceipt"></a>
# **createReceipt**
> Receipt createReceipt(receiptInput)

Create receipt

Creates a billing receipt record for a workspace. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReceiptsApi apiInstance = new ReceiptsApi(defaultClient);
    ReceiptInput receiptInput = new ReceiptInput(); // ReceiptInput | 
    try {
      Receipt result = apiInstance.createReceipt(receiptInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReceiptsApi#createReceipt");
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
| **receiptInput** | [**ReceiptInput**](ReceiptInput.md)|  | |

### Return type

[**Receipt**](Receipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created receipt |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="deleteReceipt"></a>
# **deleteReceipt**
> Object deleteReceipt(receiptUuid)

Delete receipt

Permanently deletes a single receipt. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReceiptsApi apiInstance = new ReceiptsApi(defaultClient);
    UUID receiptUuid = UUID.randomUUID(); // UUID | UUID of the receipt.
    try {
      Object result = apiInstance.deleteReceipt(receiptUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReceiptsApi#deleteReceipt");
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
| **receiptUuid** | **UUID**| UUID of the receipt. | |

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

<a id="deleteReceiptsBulk"></a>
# **deleteReceiptsBulk**
> Object deleteReceiptsBulk(deleteReceiptsBulkRequest)

Delete receipts (bulk)

Permanently deletes one or more receipt records. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReceiptsApi apiInstance = new ReceiptsApi(defaultClient);
    DeleteReceiptsBulkRequest deleteReceiptsBulkRequest = new DeleteReceiptsBulkRequest(); // DeleteReceiptsBulkRequest | 
    try {
      Object result = apiInstance.deleteReceiptsBulk(deleteReceiptsBulkRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReceiptsApi#deleteReceiptsBulk");
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
| **deleteReceiptsBulkRequest** | [**DeleteReceiptsBulkRequest**](DeleteReceiptsBulkRequest.md)|  | |

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

<a id="getReceipt"></a>
# **getReceipt**
> Receipt getReceipt(receiptUuid)

Get receipt

Returns a single receipt by UUID. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReceiptsApi apiInstance = new ReceiptsApi(defaultClient);
    UUID receiptUuid = UUID.randomUUID(); // UUID | UUID of the receipt.
    try {
      Receipt result = apiInstance.getReceipt(receiptUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReceiptsApi#getReceipt");
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
| **receiptUuid** | **UUID**| UUID of the receipt. | |

### Return type

[**Receipt**](Receipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Receipt details |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listReceipts"></a>
# **listReceipts**
> ListReceipts200Response listReceipts(workspaceUuid, invoiceNumber, page)

List receipts

Returns a paginated list of billing receipts. Filter by workspace UUID or invoice number. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReceiptsApi apiInstance = new ReceiptsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | 
    String invoiceNumber = "invoiceNumber_example"; // String | 
    Integer page = 1; // Integer | Page number (15 items per page).
    try {
      ListReceipts200Response result = apiInstance.listReceipts(workspaceUuid, invoiceNumber, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReceiptsApi#listReceipts");
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
| **workspaceUuid** | **UUID**|  | [optional] |
| **invoiceNumber** | **String**|  | [optional] |
| **page** | **Integer**| Page number (15 items per page). | [optional] [default to 1] |

### Return type

[**ListReceipts200Response**](ListReceipts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of receipts |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="updateReceipt"></a>
# **updateReceipt**
> Object updateReceipt(receiptUuid, receiptUpdateInput)

Update receipt

Updates a receipt&#39;s transaction details, amount, or payment date. Admin only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.ReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ReceiptsApi apiInstance = new ReceiptsApi(defaultClient);
    UUID receiptUuid = UUID.randomUUID(); // UUID | UUID of the receipt.
    ReceiptUpdateInput receiptUpdateInput = new ReceiptUpdateInput(); // ReceiptUpdateInput | 
    try {
      Object result = apiInstance.updateReceipt(receiptUuid, receiptUpdateInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReceiptsApi#updateReceipt");
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
| **receiptUuid** | **UUID**| UUID of the receipt. | |
| **receiptUpdateInput** | [**ReceiptUpdateInput**](ReceiptUpdateInput.md)|  | |

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

