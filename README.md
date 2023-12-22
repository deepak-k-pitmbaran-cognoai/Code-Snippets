# Code-Snippets

### Exception Handling for Request Exception
```
except requestException as e:
    response['status_code']    = "400"
    response['status_message'] = "API Failed! " + str(e)
    response['API_RESPONSE_PACKET']["PostProcessorContent Error"] = "API Failed! " + str(e)
    response['data']['final_response'] = result_dict['API_FAILURE_MSG']
    return response
```
