# 

Simple calculator API hosted on APIMATIC



## Base URL

The Base URL for this API is `https://examples-apimatic-io-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket-runscope-net-testbucket.runscope.net/apps/test`




## Global API Errors
Global API errors are applied across all endpoints.

**500** 
> test global error

**501** 
> test global error 2




# <a name="api_reference"></a>API Reference

* [Simple Calculator Group](#simple_calculator_group)

## <a name="simple_calculator_group"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Simple Calculator Group") Simple Calculator Group


### <a name="calculate"></a>![Endpoint: ](https://apidocs.io/img/method.png "Calculate") Calculate


**`GET`** `/{operation}`

> Calculates the expression using the specified operation.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| operation | `Operation Type` |  ``` Required ```  | The operator to apply on the variables | `"SUM"` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| x | `precision` |  ``` Required ```  | The LHS value | `93.2163026431651` | 
| y | `precision` |  ``` Required ```  | The RHS value | `93.2163026431651` | 

#### Responses
**200** 

Body (_precision_) 
```
93.2163026431651
```


[Back to API Reference](#api_reference)

