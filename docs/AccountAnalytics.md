

# AccountAnalytics


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**account** | [**Account**](Account.md) |  |  |
|**type** | **String** | The analytics tab returned. |  |
|**tabs** | **List&lt;String&gt;** | Tabs this account supports; any of them can be passed as &#x60;type&#x60;. |  |
|**period** | [**AnalyticsPeriod**](AnalyticsPeriod.md) |  |  |
|**initialSync** | [**AccountAnalyticsInitialSync**](AccountAnalyticsInitialSync.md) |  |  |
|**data** | **Map&lt;String, Object&gt;** | Provider- and tab-specific metrics. Chart series are lists of &#x60;{date, value}&#x60; points. |  |



