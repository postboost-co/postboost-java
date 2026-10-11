# AnalyticsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getAccountAnalytics**](AnalyticsApi.md#getAccountAnalytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics |
| [**getAnalyticsSummary**](AnalyticsApi.md#getAnalyticsSummary) | **GET** /{workspaceUuid}/analytics | Get analytics summary |
| [**getBestPostingTimes**](AnalyticsApi.md#getBestPostingTimes) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times |
| [**getPostAnalytics_0**](AnalyticsApi.md#getPostAnalytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**getPostingTimes**](AnalyticsApi.md#getPostingTimes) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap |


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

