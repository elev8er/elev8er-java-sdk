# TestsApi

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTest**](TestsApi.md#createTest) | **POST** /tests | Create a test |
| [**createTestVersion**](TestsApi.md#createTestVersion) | **POST** /tests/{id}/versions | Create a new version of a test |
| [**deleteTest**](TestsApi.md#deleteTest) | **DELETE** /tests/{id} | Delete a test |
| [**getTest**](TestsApi.md#getTest) | **GET** /tests/{id} | Get a test by id |
| [**getTestVersion**](TestsApi.md#getTestVersion) | **GET** /tests/{id}/versions/{versionId} | Get a specific test version |
| [**listTestVersions**](TestsApi.md#listTestVersions) | **GET** /tests/{id}/versions | List versions of a test |
| [**listTests**](TestsApi.md#listTests) | **GET** /tests | List tests |
| [**rollbackTestVersion**](TestsApi.md#rollbackTestVersion) | **POST** /tests/{id}/versions/{versionId}/rollback | Roll a test back to a specific version |
| [**updateTest**](TestsApi.md#updateTest) | **PUT** /tests/{id} | Update a test |
| [**updateTestVersion**](TestsApi.md#updateTestVersion) | **PUT** /tests/{id}/versions/{versionId} | Update a specific test version |


<a id="createTest"></a>
# **createTest**
> SuccessEnvelope createTest(requestBody)

Create a test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.createTest(requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#createTest");
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
| **requestBody** | [**Map&lt;String, Object&gt;**](Object.md)|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |
| **400** | Request payload failed validation. |  -  |

<a id="createTestVersion"></a>
# **createTestVersion**
> SuccessEnvelope createTestVersion(id, body)

Create a new version of a test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    Object body = null; // Object | 
    try {
      SuccessEnvelope result = apiInstance.createTestVersion(id, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#createTestVersion");
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
| **id** | **String**|  | |
| **body** | **Object**|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="deleteTest"></a>
# **deleteTest**
> deleteTest(id)

Delete a test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.deleteTest(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#deleteTest");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Deleted |  -  |
| **404** | Resource not found. |  -  |

<a id="getTest"></a>
# **getTest**
> SuccessEnvelope getTest(id)

Get a test by id

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getTest(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#getTest");
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
| **id** | **String**|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |
| **404** | Resource not found. |  -  |

<a id="getTestVersion"></a>
# **getTestVersion**
> SuccessEnvelope getTestVersion(id, versionId)

Get a specific test version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getTestVersion(id, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#getTestVersion");
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
| **id** | **String**|  | |
| **versionId** | **String**|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |
| **404** | Resource not found. |  -  |

<a id="listTestVersions"></a>
# **listTestVersions**
> SuccessEnvelope listTestVersions(id)

List versions of a test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.listTestVersions(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#listTestVersions");
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
| **id** | **String**|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="listTests"></a>
# **listTests**
> SuccessEnvelope listTests(page, limit, search)

List tests

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    Integer page = 1; // Integer | 1-based page number.
    Integer limit = 20; // Integer | Items per page (max 100).
    String search = "search_example"; // String | Free-text search filter.
    try {
      SuccessEnvelope result = apiInstance.listTests(page, limit, search);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#listTests");
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
| **page** | **Integer**| 1-based page number. | [optional] [default to 1] |
| **limit** | **Integer**| Items per page (max 100). | [optional] [default to 20] |
| **search** | **String**| Free-text search filter. | [optional] |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |
| **401** | Missing or invalid API key. |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="rollbackTestVersion"></a>
# **rollbackTestVersion**
> SuccessEnvelope rollbackTestVersion(id, versionId)

Roll a test back to a specific version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.rollbackTestVersion(id, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#rollbackTestVersion");
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
| **id** | **String**|  | |
| **versionId** | **String**|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="updateTest"></a>
# **updateTest**
> SuccessEnvelope updateTest(id, requestBody)

Update a test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.updateTest(id, requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#updateTest");
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
| **id** | **String**|  | |
| **requestBody** | [**Map&lt;String, Object&gt;**](Object.md)|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |
| **404** | Resource not found. |  -  |

<a id="updateTestVersion"></a>
# **updateTestVersion**
> SuccessEnvelope updateTestVersion(id, versionId, body)

Update a specific test version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.TestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TestsApi apiInstance = new TestsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    Object body = null; // Object | 
    try {
      SuccessEnvelope result = apiInstance.updateTestVersion(id, versionId, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TestsApi#updateTestVersion");
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
| **id** | **String**|  | |
| **versionId** | **String**|  | |
| **body** | **Object**|  | |

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

