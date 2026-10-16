# AnalyticsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createReportExport**](AnalyticsApi.md#createReportExport) | **POST** /{workspaceUuid}/reports/exports | Create a report export |
| [**downloadReportExport**](AnalyticsApi.md#downloadReportExport) | **GET** /{workspaceUuid}/reports/exports/{exportUuid}/download | Download a report file |
| [**getAccountAnalytics**](AnalyticsApi.md#getAccountAnalytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics |
| [**getAnalyticsSummary**](AnalyticsApi.md#getAnalyticsSummary) | **GET** /{workspaceUuid}/analytics | Get analytics summary |
| [**getBestPostingTimes**](AnalyticsApi.md#getBestPostingTimes) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times |
| [**getPostAnalytics_0**](AnalyticsApi.md#getPostAnalytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**getPostingTimes**](AnalyticsApi.md#getPostingTimes) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap |
| [**getReportBranding**](AnalyticsApi.md#getReportBranding) | **GET** /{workspaceUuid}/report-branding | Get the report branding |
| [**getReportExport**](AnalyticsApi.md#getReportExport) | **GET** /{workspaceUuid}/reports/exports/{exportUuid} | Get a report export |
| [**listReportExports**](AnalyticsApi.md#listReportExports) | **GET** /{workspaceUuid}/reports/exports | List report exports |
| [**updateReportBranding**](AnalyticsApi.md#updateReportBranding) | **PUT** /{workspaceUuid}/report-branding | Update the report branding |
| [**uploadReportBrandingLogo**](AnalyticsApi.md#uploadReportBrandingLogo) | **POST** /{workspaceUuid}/report-branding/logo | Upload the report logo |


<a id="createReportExport"></a>
# **createReportExport**
> CreateReportExport201Response createReportExport(workspaceUuid, reportExportInput)

Create a report export

Generates a report for a period (default &#x60;last_month&#x60;) or a custom &#x60;date_from&#x60;/&#x60;date_to&#x60; range: a branded PDF (summary, accounts, top 10 posts; the header uses the report branding) or a CSV with one row per published post and account (&#x60;dataset: posts&#x60;, default) or per account (&#x60;dataset: accounts&#x60;). CSV files are UTF-8 with a byte order mark. At most 500 posts per report. The file is ready when the call returns; fetch it from &#x60;download_url&#x60; with the same token. Admins and members only; 20 per minute. 

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    ReportExportInput reportExportInput = new ReportExportInput(); // ReportExportInput | 
    try {
      CreateReportExport201Response result = apiInstance.createReportExport(workspaceUuid, reportExportInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#createReportExport");
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
| **reportExportInput** | [**ReportExportInput**](ReportExportInput.md)|  | |

### Return type

[**CreateReportExport201Response**](CreateReportExport201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | The export (status &#x60;ready&#x60;, or &#x60;failed&#x60; with &#x60;error&#x60;) |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="downloadReportExport"></a>
# **downloadReportExport**
> File downloadReportExport(workspaceUuid, exportUuid)

Download a report file

The PDF or CSV file. &#x60;410&#x60; once it expired (7 days) or if the export failed.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID exportUuid = UUID.randomUUID(); // UUID | UUID of the report export.
    try {
      File result = apiInstance.downloadReportExport(workspaceUuid, exportUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#downloadReportExport");
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
| **exportUuid** | **UUID**| UUID of the report export. | |

### Return type

[**File**](File.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, text/csv, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The report file |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **410** | The file expired or the export failed. |  -  |

<a id="getAccountAnalytics"></a>
# **getAccountAnalytics**
> AccountAnalytics getAccountAnalytics(workspaceUuid, accountUuid, period, dateFrom, dateTo, type, page, perPage, sortBy, sortDir)

Get account analytics

Analytics for one account. &#x60;type&#x60; selects one of the tabs the account supports (listed in &#x60;tabs&#x60; of the response); returns &#x60;422&#x60; when the account does not support analytics.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID accountUuid = UUID.randomUUID(); // UUID | UUID of the social media account.
    String period = "this_week"; // String | Preset reporting period. Ignored when `date_from` and `date_to` are given.
    LocalDate dateFrom = LocalDate.now(); // LocalDate | Start of a custom range (Y-m-d). Required with `date_to`; the range may span at most 366 days.
    LocalDate dateTo = LocalDate.now(); // LocalDate | End of a custom range (Y-m-d). Required with `date_from`; must not be before it.
    String type = "type_example"; // String | Analytics tab. Defaults to the account's default tab.
    Integer page = 1; // Integer | Page for list-style tabs (for example per-post metrics).
    Integer perPage = 56; // Integer | 
    String sortBy = "sortBy_example"; // String | 
    String sortDir = "asc"; // String | 
    try {
      AccountAnalytics result = apiInstance.getAccountAnalytics(workspaceUuid, accountUuid, period, dateFrom, dateTo, type, page, perPage, sortBy, sortDir);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getAccountAnalytics");
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
| **period** | **String**| Preset reporting period. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are given. | [optional] [default to this_month] [enum: this_week, last_week, this_month, last_month, last_3_months, this_year] |
| **dateFrom** | **LocalDate**| Start of a custom range (Y-m-d). Required with &#x60;date_to&#x60;; the range may span at most 366 days. | [optional] |
| **dateTo** | **LocalDate**| End of a custom range (Y-m-d). Required with &#x60;date_from&#x60;; must not be before it. | [optional] |
| **type** | **String**| Analytics tab. Defaults to the account&#39;s default tab. | [optional] |
| **page** | **Integer**| Page for list-style tabs (for example per-post metrics). | [optional] [default to 1] |
| **perPage** | **Integer**|  | [optional] |
| **sortBy** | **String**|  | [optional] |
| **sortDir** | **String**|  | [optional] [default to desc] [enum: asc, desc] |

### Return type

[**AccountAnalytics**](AccountAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account analytics |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |
| **422** |  |  -  |

<a id="getAnalyticsSummary"></a>
# **getAnalyticsSummary**
> AnalyticsSummary getAnalyticsSummary(workspaceUuid, period, dateFrom, dateTo)

Get analytics summary

Cross-platform summary (followers, growth, posts, leaderboard, posting streak) over every account that supports analytics, for a preset period or a custom date range.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    String period = "this_week"; // String | Preset reporting period. Ignored when `date_from` and `date_to` are given.
    LocalDate dateFrom = LocalDate.now(); // LocalDate | Start of a custom range (Y-m-d). Required with `date_to`; the range may span at most 366 days.
    LocalDate dateTo = LocalDate.now(); // LocalDate | End of a custom range (Y-m-d). Required with `date_from`; must not be before it.
    try {
      AnalyticsSummary result = apiInstance.getAnalyticsSummary(workspaceUuid, period, dateFrom, dateTo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getAnalyticsSummary");
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
| **period** | **String**| Preset reporting period. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are given. | [optional] [default to this_month] [enum: this_week, last_week, this_month, last_month, last_3_months, this_year] |
| **dateFrom** | **LocalDate**| Start of a custom range (Y-m-d). Required with &#x60;date_to&#x60;; the range may span at most 366 days. | [optional] |
| **dateTo** | **LocalDate**| End of a custom range (Y-m-d). Required with &#x60;date_from&#x60;; must not be before it. | [optional] |

### Return type

[**AnalyticsSummary**](AnalyticsSummary.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Analytics summary |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="getBestPostingTimes"></a>
# **getBestPostingTimes**
> BestPostingTimes getBestPostingTimes(workspaceUuid, accounts, from, timezone)

Get best posting times

The next recommended date and time per account, on or after &#x60;from&#x60; (never in the past), within the next 14 days.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    List<UUID> accounts = Arrays.asList(); // List<UUID> | Account UUIDs. Defaults to every account in the workspace.
    LocalDate from = LocalDate.now(); // LocalDate | Earliest date to recommend (Y-m-d). Defaults to now.
    String timezone = "timezone_example"; // String | Timezone for `from` and the returned times. Defaults to the workspace timezone.
    try {
      BestPostingTimes result = apiInstance.getBestPostingTimes(workspaceUuid, accounts, from, timezone);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getBestPostingTimes");
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
| **accounts** | [**List&lt;UUID&gt;**](UUID.md)| Account UUIDs. Defaults to every account in the workspace. | [optional] |
| **from** | **LocalDate**| Earliest date to recommend (Y-m-d). Defaults to now. | [optional] |
| **timezone** | **String**| Timezone for &#x60;from&#x60; and the returned times. Defaults to the workspace timezone. | [optional] |

### Return type

[**BestPostingTimes**](BestPostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Best posting times |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="getPostAnalytics_0"></a>
# **getPostAnalytics_0**
> PostAnalytics getPostAnalytics_0(workspaceUuid, postUuid)

Get post analytics

Engagement metrics for a published post across its accounts (also works for trashed posts), with totals, trends and the best-performing account.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID postUuid = UUID.randomUUID(); // UUID | UUID of the post.
    try {
      PostAnalytics result = apiInstance.getPostAnalytics_0(workspaceUuid, postUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getPostAnalytics_0");
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
| **postUuid** | **UUID**| UUID of the post. | |

### Return type

[**PostAnalytics**](PostAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Post analytics |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="getPostingTimes"></a>
# **getPostingTimes**
> PostingTimes getPostingTimes(workspaceUuid, accounts, timezone)

Get posting times heatmap

Engagement scores per weekday and hour, merged across the given accounts (all accounts when none is given), in the requested timezone. Also returns up to three recommended slots.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    List<UUID> accounts = Arrays.asList(); // List<UUID> | Account UUIDs. Defaults to every account in the workspace.
    String timezone = "Europe/Istanbul"; // String | Timezone the grid is expressed in. Defaults to the workspace timezone.
    try {
      PostingTimes result = apiInstance.getPostingTimes(workspaceUuid, accounts, timezone);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getPostingTimes");
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
| **accounts** | [**List&lt;UUID&gt;**](UUID.md)| Account UUIDs. Defaults to every account in the workspace. | [optional] |
| **timezone** | **String**| Timezone the grid is expressed in. Defaults to the workspace timezone. | [optional] |

### Return type

[**PostingTimes**](PostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Posting times |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="getReportBranding"></a>
# **getReportBranding**
> GetReportBranding200Response getReportBranding(workspaceUuid)

Get the report branding

The white-label header of the workspace&#39;s PDF reports. Unset fields are &#x60;null&#x60;; the workspace name is used then.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      GetReportBranding200Response result = apiInstance.getReportBranding(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getReportBranding");
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

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The report branding |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="getReportExport"></a>
# **getReportExport**
> CreateReportExport201Response getReportExport(workspaceUuid, exportUuid)

Get a report export

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    UUID exportUuid = UUID.randomUUID(); // UUID | UUID of the report export.
    try {
      CreateReportExport201Response result = apiInstance.getReportExport(workspaceUuid, exportUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#getReportExport");
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
| **exportUuid** | **UUID**| UUID of the report export. | |

### Return type

[**CreateReportExport201Response**](CreateReportExport201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The export |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **404** |  |  -  |

<a id="listReportExports"></a>
# **listReportExports**
> ListReportExports200Response listReportExports(workspaceUuid)

List report exports

The workspace&#39;s latest 50 report exports, newest first. Files can be downloaded for 7 days.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    try {
      ListReportExports200Response result = apiInstance.listReportExports(workspaceUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#listReportExports");
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

[**ListReportExports200Response**](ListReportExports200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Recent exports |  -  |
| **401** |  |  -  |
| **403** |  |  -  |

<a id="updateReportBranding"></a>
# **updateReportBranding**
> GetReportBranding200Response updateReportBranding(workspaceUuid, reportBrandingInput)

Update the report branding

Name, colour and footer of PDF reports. Fields you leave out keep their value. Upload the logo with &#x60;uploadReportBrandingLogo&#x60; (a multipart file upload, so it is not an MCP tool). Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    ReportBrandingInput reportBrandingInput = new ReportBrandingInput(); // ReportBrandingInput | 
    try {
      GetReportBranding200Response result = apiInstance.updateReportBranding(workspaceUuid, reportBrandingInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#updateReportBranding");
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
| **reportBrandingInput** | [**ReportBrandingInput**](ReportBrandingInput.md)|  | |

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The saved branding |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

<a id="uploadReportBrandingLogo"></a>
# **uploadReportBrandingLogo**
> GetReportBranding200Response uploadReportBrandingLogo(workspaceUuid, logo)

Upload the report logo

PNG or JPEG, up to 1 MB (SVG is not accepted). Replaces the current logo. Admins and members only.

### Example
```java
// Import classes:
import com.postboost.ApiClient;
import com.postboost.ApiException;
import com.postboost.Configuration;
import com.postboost.auth.*;
import com.postboost.models.*;
import com.postboost.api.AnalyticsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://postboost.co/app/api");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AnalyticsApi apiInstance = new AnalyticsApi(defaultClient);
    UUID workspaceUuid = UUID.randomUUID(); // UUID | UUID of the workspace.
    File logo = new File("/path/to/file"); // File | 
    try {
      GetReportBranding200Response result = apiInstance.uploadReportBrandingLogo(workspaceUuid, logo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AnalyticsApi#uploadReportBrandingLogo");
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
| **logo** | **File**|  | |

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The saved branding |  -  |
| **401** |  |  -  |
| **403** |  |  -  |
| **422** |  |  -  |

