# ProgramsApi

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProgram**](ProgramsApi.md#createProgram) | **POST** /programs | Create a program |
| [**createProgramTag**](ProgramsApi.md#createProgramTag) | **POST** /programs/tags | Create a program tag |
| [**createProgramVersion**](ProgramsApi.md#createProgramVersion) | **POST** /programs/{id}/versions | Create a new version of a program |
| [**deleteProgram**](ProgramsApi.md#deleteProgram) | **DELETE** /programs/{id} | Delete a program |
| [**deleteProgramTag**](ProgramsApi.md#deleteProgramTag) | **DELETE** /programs/tags/{tagId} | Delete a program tag |
| [**getProgram**](ProgramsApi.md#getProgram) | **GET** /programs/{id} | Get a program by id |
| [**getProgramTags**](ProgramsApi.md#getProgramTags) | **GET** /programs/{id}/tags | Get tags assigned to a program |
| [**getProgramVersion**](ProgramsApi.md#getProgramVersion) | **GET** /programs/{id}/versions/{versionId} | Get a specific program version |
| [**listProgramTags**](ProgramsApi.md#listProgramTags) | **GET** /programs/tags | List program tags |
| [**listProgramVersions**](ProgramsApi.md#listProgramVersions) | **GET** /programs/{id}/versions | List versions of a program |
| [**listPrograms**](ProgramsApi.md#listPrograms) | **GET** /programs | List programs |
| [**rollbackProgramVersion**](ProgramsApi.md#rollbackProgramVersion) | **POST** /programs/{id}/versions/{versionId}/rollback | Roll a program back to a specific version |
| [**setProgramTags**](ProgramsApi.md#setProgramTags) | **PUT** /programs/{id}/tags | Replace the tags assigned to a program |
| [**updateProgram**](ProgramsApi.md#updateProgram) | **PUT** /programs/{id} | Update a program |
| [**updateProgramTag**](ProgramsApi.md#updateProgramTag) | **PUT** /programs/tags/{tagId} | Update a program tag |
| [**updateProgramVersion**](ProgramsApi.md#updateProgramVersion) | **PUT** /programs/{id}/versions/{versionId} | Update a specific program version |


<a id="createProgram"></a>
# **createProgram**
> SuccessEnvelope createProgram(requestBody)

Create a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.createProgram(requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#createProgram");
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
| **201** | A single program. |  -  |
| **400** | Request payload failed validation. |  -  |
| **401** | Missing or invalid API key. |  -  |
| **403** | API key is valid but not authorised for this resource (scope). |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="createProgramTag"></a>
# **createProgramTag**
> SuccessEnvelope createProgramTag(createProgramTagRequest)

Create a program tag

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    CreateProgramTagRequest createProgramTagRequest = new CreateProgramTagRequest(); // CreateProgramTagRequest | 
    try {
      SuccessEnvelope result = apiInstance.createProgramTag(createProgramTagRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#createProgramTag");
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
| **createProgramTagRequest** | [**CreateProgramTagRequest**](CreateProgramTagRequest.md)|  | |

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

<a id="createProgramVersion"></a>
# **createProgramVersion**
> SuccessEnvelope createProgramVersion(id, body)

Create a new version of a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    Object body = null; // Object | 
    try {
      SuccessEnvelope result = apiInstance.createProgramVersion(id, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#createProgramVersion");
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
| **401** | Missing or invalid API key. |  -  |
| **404** | Resource not found. |  -  |

<a id="deleteProgram"></a>
# **deleteProgram**
> deleteProgram(id)

Delete a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.deleteProgram(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#deleteProgram");
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
| **401** | Missing or invalid API key. |  -  |
| **403** | API key is valid but not authorised for this resource (scope). |  -  |
| **404** | Resource not found. |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="deleteProgramTag"></a>
# **deleteProgramTag**
> deleteProgramTag(tagId)

Delete a program tag

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String tagId = "tagId_example"; // String | 
    try {
      apiInstance.deleteProgramTag(tagId);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#deleteProgramTag");
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
| **tagId** | **String**|  | |

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

<a id="getProgram"></a>
# **getProgram**
> SuccessEnvelope getProgram(id)

Get a program by id

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getProgram(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#getProgram");
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
| **200** | A single program. |  -  |
| **401** | Missing or invalid API key. |  -  |
| **403** | API key is valid but not authorised for this resource (scope). |  -  |
| **404** | Resource not found. |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="getProgramTags"></a>
# **getProgramTags**
> SuccessEnvelope getProgramTags(id)

Get tags assigned to a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getProgramTags(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#getProgramTags");
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

<a id="getProgramVersion"></a>
# **getProgramVersion**
> SuccessEnvelope getProgramVersion(id, versionId)

Get a specific program version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getProgramVersion(id, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#getProgramVersion");
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

<a id="listProgramTags"></a>
# **listProgramTags**
> SuccessEnvelope listProgramTags()

List program tags

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    try {
      SuccessEnvelope result = apiInstance.listProgramTags();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#listProgramTags");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

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

<a id="listProgramVersions"></a>
# **listProgramVersions**
> SuccessEnvelope listProgramVersions(id)

List versions of a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.listProgramVersions(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#listProgramVersions");
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
| **401** | Missing or invalid API key. |  -  |
| **404** | Resource not found. |  -  |

<a id="listPrograms"></a>
# **listPrograms**
> ListPrograms200Response listPrograms(page, limit, search)

List programs

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    Integer page = 1; // Integer | 1-based page number.
    Integer limit = 20; // Integer | Items per page (max 100).
    String search = "search_example"; // String | Free-text search filter.
    try {
      ListPrograms200Response result = apiInstance.listPrograms(page, limit, search);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#listPrograms");
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

[**ListPrograms200Response**](ListPrograms200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A page of programs. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |
| **401** | Missing or invalid API key. |  -  |
| **403** | API key is valid but not authorised for this resource (scope). |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="rollbackProgramVersion"></a>
# **rollbackProgramVersion**
> SuccessEnvelope rollbackProgramVersion(id, versionId)

Roll a program back to a specific version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.rollbackProgramVersion(id, versionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#rollbackProgramVersion");
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

<a id="setProgramTags"></a>
# **setProgramTags**
> SuccessEnvelope setProgramTags(id, setProgramTagsRequest)

Replace the tags assigned to a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    SetProgramTagsRequest setProgramTagsRequest = new SetProgramTagsRequest(); // SetProgramTagsRequest | 
    try {
      SuccessEnvelope result = apiInstance.setProgramTags(id, setProgramTagsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#setProgramTags");
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
| **setProgramTagsRequest** | [**SetProgramTagsRequest**](SetProgramTagsRequest.md)|  | |

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

<a id="updateProgram"></a>
# **updateProgram**
> SuccessEnvelope updateProgram(id, requestBody)

Update a program

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      SuccessEnvelope result = apiInstance.updateProgram(id, requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#updateProgram");
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
| **200** | A single program. |  -  |
| **400** | Request payload failed validation. |  -  |
| **401** | Missing or invalid API key. |  -  |
| **403** | API key is valid but not authorised for this resource (scope). |  -  |
| **404** | Resource not found. |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

<a id="updateProgramTag"></a>
# **updateProgramTag**
> SuccessEnvelope updateProgramTag(tagId, updateProgramTagRequest)

Update a program tag

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String tagId = "tagId_example"; // String | 
    UpdateProgramTagRequest updateProgramTagRequest = new UpdateProgramTagRequest(); // UpdateProgramTagRequest | 
    try {
      SuccessEnvelope result = apiInstance.updateProgramTag(tagId, updateProgramTagRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#updateProgramTag");
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
| **tagId** | **String**|  | |
| **updateProgramTagRequest** | [**UpdateProgramTagRequest**](UpdateProgramTagRequest.md)|  | |

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

<a id="updateProgramVersion"></a>
# **updateProgramVersion**
> SuccessEnvelope updateProgramVersion(id, versionId, body)

Update a specific program version

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.ProgramsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ProgramsApi apiInstance = new ProgramsApi(defaultClient);
    String id = "id_example"; // String | 
    String versionId = "versionId_example"; // String | 
    Object body = null; // Object | 
    try {
      SuccessEnvelope result = apiInstance.updateProgramVersion(id, versionId, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProgramsApi#updateProgramVersion");
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
| **404** | Resource not found. |  -  |

