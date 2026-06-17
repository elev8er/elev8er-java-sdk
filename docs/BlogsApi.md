# BlogsApi

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createBlog**](BlogsApi.md#createBlog) | **POST** /blogs | Create a blog |
| [**deleteBlog**](BlogsApi.md#deleteBlog) | **DELETE** /blogs/{id} | Delete a blog |
| [**getBlog**](BlogsApi.md#getBlog) | **GET** /blogs/{id} | Get a blog by id |
| [**listBlogs**](BlogsApi.md#listBlogs) | **GET** /blogs | List blogs |
| [**updateBlog**](BlogsApi.md#updateBlog) | **PUT** /blogs/{id} | Update a blog |


<a id="createBlog"></a>
# **createBlog**
> SuccessEnvelope createBlog(requestBody)

Create a blog

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.BlogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BlogsApi apiInstance = new BlogsApi(defaultClient);
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.createBlog(requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BlogsApi#createBlog");
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

<a id="deleteBlog"></a>
# **deleteBlog**
> deleteBlog(id)

Delete a blog

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.BlogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BlogsApi apiInstance = new BlogsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.deleteBlog(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling BlogsApi#deleteBlog");
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

<a id="getBlog"></a>
# **getBlog**
> SuccessEnvelope getBlog(id)

Get a blog by id

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.BlogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BlogsApi apiInstance = new BlogsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getBlog(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BlogsApi#getBlog");
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

<a id="listBlogs"></a>
# **listBlogs**
> SuccessEnvelope listBlogs(page, limit, search)

List blogs

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.BlogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BlogsApi apiInstance = new BlogsApi(defaultClient);
    Integer page = 1; // Integer | 1-based page number.
    Integer limit = 20; // Integer | Items per page (max 100).
    String search = "search_example"; // String | Free-text search filter.
    try {
      SuccessEnvelope result = apiInstance.listBlogs(page, limit, search);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BlogsApi#listBlogs");
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

<a id="updateBlog"></a>
# **updateBlog**
> SuccessEnvelope updateBlog(id, requestBody)

Update a blog

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.BlogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BlogsApi apiInstance = new BlogsApi(defaultClient);
    String id = "id_example"; // String | 
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.updateBlog(id, requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BlogsApi#updateBlog");
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

