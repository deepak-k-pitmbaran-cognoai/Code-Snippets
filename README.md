# Code-Snippets

#### 1. Exception Handling for Request Exception
- Define a variable:

  ```
  requestException = requests.exceptions.RequestException
  ```
- Exception block

  ```
    except requestException as e:
        response['status_code']    = "400"
        response['status_message'] = "API Failed! " + str(e)
        response['API_RESPONSE_PACKET']["PostProcessorContent Error"] = "API Failed! " + str(e)
        response['data']['final_response'] = result_dict['API_FAILURE_MSG']
        return response
    ```

#### 2. Request timeout exception handling

```
except requests.Timeout as e:
    response['status_code']    = "400"
    response['status_message'] = "API Failed! " + str(e)
    response['API_RESPONSE_PACKET']["PostProcessorContent Error"] = "API Failed! " + str(e)
    response['data']['final_response'] = result_dict['API_FAILURE_MSG']
    return response
```
