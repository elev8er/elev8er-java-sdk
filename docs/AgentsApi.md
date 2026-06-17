# AgentsApi

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAgentChat**](AgentsApi.md#createAgentChat) | **POST** /agents/{id}/chats | Start a new chat with an agent |
| [**getAgent**](AgentsApi.md#getAgent) | **GET** /agents/{id} | Get an agent by id |
| [**listAgentChats**](AgentsApi.md#listAgentChats) | **GET** /agents/{id}/chats | List chats for an agent |
| [**listAgents**](AgentsApi.md#listAgents) | **GET** /agents | List agents |
| [**listChatMessages**](AgentsApi.md#listChatMessages) | **GET** /agents/{id}/chats/{chatId}/messages | Get messages in a chat |
| [**sendChatMessage**](AgentsApi.md#sendChatMessage) | **POST** /agents/{id}/chats/{chatId}/messages | Send a message to the agent and get its reply (non-streaming) |


<a id="createAgentChat"></a>
# **createAgentChat**
> SuccessEnvelope createAgentChat(id, createAgentChatRequest)

Start a new chat with an agent

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    String id = "id_example"; // String | 
    CreateAgentChatRequest createAgentChatRequest = new CreateAgentChatRequest(); // CreateAgentChatRequest | 
    try {
      SuccessEnvelope result = apiInstance.createAgentChat(id, createAgentChatRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#createAgentChat");
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
| **createAgentChatRequest** | [**CreateAgentChatRequest**](CreateAgentChatRequest.md)|  | [optional] |

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
| **404** | Resource not found. |  -  |

<a id="getAgent"></a>
# **getAgent**
> SuccessEnvelope getAgent(id)

Get an agent by id

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.getAgent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#getAgent");
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

<a id="listAgentChats"></a>
# **listAgentChats**
> SuccessEnvelope listAgentChats(id)

List chats for an agent

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      SuccessEnvelope result = apiInstance.listAgentChats(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#listAgentChats");
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

<a id="listAgents"></a>
# **listAgents**
> SuccessEnvelope listAgents(page, limit)

List agents

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    Integer page = 1; // Integer | 1-based page number.
    Integer limit = 20; // Integer | Items per page (max 100).
    try {
      SuccessEnvelope result = apiInstance.listAgents(page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#listAgents");
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

<a id="listChatMessages"></a>
# **listChatMessages**
> SuccessEnvelope listChatMessages(id, chatId, page, limit)

Get messages in a chat

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    String id = "id_example"; // String | 
    String chatId = "chatId_example"; // String | 
    Integer page = 1; // Integer | 1-based page number.
    Integer limit = 20; // Integer | Items per page (max 100).
    try {
      SuccessEnvelope result = apiInstance.listChatMessages(id, chatId, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#listChatMessages");
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
| **chatId** | **String**|  | |
| **page** | **Integer**| 1-based page number. | [optional] [default to 1] |
| **limit** | **Integer**| Items per page (max 100). | [optional] [default to 20] |

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

<a id="sendChatMessage"></a>
# **sendChatMessage**
> SuccessEnvelope sendChatMessage(id, chatId, chatMessageInput)

Send a message to the agent and get its reply (non-streaming)

Sends a user message to the agent and returns the agent&#39;s full reply in a single JSON response. Streaming is not exposed on the public API. 

### Example
```java
// Import classes:
import ai.elev8er.publicapi.ApiClient;
import ai.elev8er.publicapi.ApiException;
import ai.elev8er.publicapi.Configuration;
import ai.elev8er.publicapi.auth.*;
import ai.elev8er.publicapi.models.*;
import ai.elev8er.publicapi.api.AgentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://apidev.elev8er.ai/public/api/v1");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AgentsApi apiInstance = new AgentsApi(defaultClient);
    String id = "id_example"; // String | 
    String chatId = "chatId_example"; // String | 
    ChatMessageInput chatMessageInput = new ChatMessageInput(); // ChatMessageInput | 
    try {
      SuccessEnvelope result = apiInstance.sendChatMessage(id, chatId, chatMessageInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AgentsApi#sendChatMessage");
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
| **chatId** | **String**|  | |
| **chatMessageInput** | [**ChatMessageInput**](ChatMessageInput.md)|  | |

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
| **400** | Request payload failed validation. |  -  |
| **404** | Resource not found. |  -  |
| **429** | Rate limit exceeded. |  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset -  <br>  |

