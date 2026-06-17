# VisualTestsApi

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createVisualTest**](VisualTestsApi.md#createVisualTest) | **POST** /visual-tests | Create a visual test |
| [**createVisualTestVersion**](VisualTestsApi.md#createVisualTestVersion) | **POST** /visual-tests/{id}/versions | Create a new version of a visual test |
| [**deleteVisualTest**](VisualTestsApi.md#deleteVisualTest) | **DELETE** /visual-tests/{id} | Delete a visual test |
| [**getVisualTest**](VisualTestsApi.md#getVisualTest) | **GET** /visual-tests/{id} | Get a visual test by id |
| [**getVisualTestVersion**](VisualTestsApi.md#getVisualTestVersion) | **GET** /visual-tests/{id}/versions/{versionId} | Get a specific visual test version |
| [**listVisualTestVersions**](VisualTestsApi.md#listVisualTestVersions) | **GET** /visual-tests/{id}/versions | List versions of a visual test |
| [**listVisualTests**](VisualTestsApi.md#listVisualTests) | **GET** /visual-tests | List visual tests |
| [**rollbackVisualTestVersion**](VisualTestsApi.md#rollbackVisualTestVersion) | **POST** /visual-tests/{id}/versions/{versionId}/rollback | Roll a visual test back to a specific version |
| [**updateVisualTest**](VisualTestsApi.md#updateVisualTest) | **PUT** /visual-tests/{id} | Update a visual test |
| [**updateVisualTestVersion**](VisualTestsApi.md#updateVisualTestVersion) | **PUT** /visual-tests/{id}/versions/{versionId} | Update a specific visual test version |


<a id="createVisualTest"></a>
# **createVisualTest**
> SuccessEnvelope createVisualTest(requestBody)

Create a visual test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.createVisualTest(requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#createVisualTest");
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

<a id="createVisualTestVersion"></a>
# **createVisualTestVersion**
> SuccessEnvelope createVisualTestVersion(id, body)

Create a new version of a visual test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    Object body = null; // Object | 
    try {
      SuccessEnvelope result = apiInstance.createVisualTestVersion(id, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#createVisualTestVersion");
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

<a id="deleteVisualTest"></a>
# **deleteVisualTest**
> deleteVisualTest(id)

Delete a visual test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.deleteVisualTest(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#deleteVisualTest");
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

<a id="getVisualTest"></a>
# **getVisualTest**
> SuccessEnvelope getVisualTest(id)

Get a visual test by id

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getVisualTest(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#getVisualTest");
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

<a id="getVisualTestVersion"></a>
# **getVisualTestVersion**
> SuccessEnvelope getVisualTestVersion(id, versionId)

Get a specific visual test version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getVisualTestVersion(id, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#getVisualTestVersion");
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

<a id="listVisualTestVersions"></a>
# **listVisualTestVersions**
> SuccessEnvelope listVisualTestVersions(id)

List versions of a visual test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.listVisualTestVersions(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#listVisualTestVersions");
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

<a id="listVisualTests"></a>
# **listVisualTests**
> SuccessEnvelope listVisualTests(page, limit, search)

List visual tests

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    Integer page = 1; // Integer | 1-based page number.
    Integer limit = 20; // Integer | Items per page (max 100).
    String search = "search_example"; // String | Free-text search filter.
    try {
      SuccessEnvelope result = apiInstance.listVisualTests(page, limit, search);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#listVisualTests");
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
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="rollbackVisualTestVersion"></a>
# **rollbackVisualTestVersion**
> SuccessEnvelope rollbackVisualTestVersion(id, versionId)

Roll a visual test back to a specific version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.rollbackVisualTestVersion(id, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#rollbackVisualTestVersion");
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

<a id="updateVisualTest"></a>
# **updateVisualTest**
> SuccessEnvelope updateVisualTest(id, requestBody)

Update a visual test

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.updateVisualTest(id, requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#updateVisualTest");
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

<a id="updateVisualTestVersion"></a>
# **updateVisualTestVersion**
> SuccessEnvelope updateVisualTestVersion(id, versionId, body)

Update a specific visual test version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.VisualTestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    VisualTestsApi apiInstance = new VisualTestsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    Object body = null; // Object | 
    try {
      SuccessEnvelope result = apiInstance.updateVisualTestVersion(id, versionId, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VisualTestsApi#updateVisualTestVersion");
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

