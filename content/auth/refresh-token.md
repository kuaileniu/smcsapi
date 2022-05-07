---
title: 刷新令牌
weight: -700
---
<small>更新日期: 2022-04-20</small>

#### 基本参数
1. url : https://{domain}:{port}/api/common/refresh-token
2. http method : POST

#### 请求数据

{{< tabs "uniqueid_request" >}}
{{< tab "说明" >}} 
 
1. access-token:  调用 [用户登录](/auth/login) 接口获取的 access-token 值；
2. refresh-token: 调用 [用户登录](/auth/login) 接口获取的 refresh-token 值；


{{< /tab >}}
{{< tab "样例" >}} 

URL： https://xxx.com/api/common/refresh-token

body： 

```
{
    "access-token": "WVjhtoqU1Nok0iUBAlrj0SsiwH9nv6tcC7dcjwo5XjiQb52bIEG98YvP8uKSIhpG%2FR8cggbs1UpYzKkLpIA0m2UcCS3J5PiC2KjXKR2XLlk5tVT%2FMP5iILMzYQlwxFlFPP3PBBTVoxe2gLADOQULuKSOCqmjQ7l%2BbZGhbdtcnPoyn%2FhukxAdlzTWHAkX9lQcvuLpUGsN%2BWF4qmLliss7xSW2S9qto39QoFtKjzAMs67ED2%2BPZSY0OOzf9azlw%2FjGPEQK9f8bZr1Mx%2BoyucHUaA%3D%3D",
    "refresh-token": "WVjhtoqU1Nok0iUBAlrj0TZtVkoNs8DyJq7nPNlkyc%2B1LfZTSK%2F%2FQcJvge48iAcSLVIG%2F7qkcpqD5izo3iEKrUFDuheiPIg7uCHZfQU%2BiD0%3D"
}
```
{{< /tab >}}
{{< /tabs >}}


#### 返回数据

{{< tabs "uniqueid_response" >}}
{{< tab "http code:200" >}} 
```
{
    "status": 0,
    "access-token": "WVjhtoqU1Nok0iUBAlrj0SsiwH9nv6tcC7dcjwo5XjhLJxJqjVlUikJ5Uu1EkPs5Go8ycmloNRMprHzRAWhmi48UVD3urEN5ndcGAYL3I%2BVB47WxODfLcnDhjgUIfLNUtyAlCq19UOR%2B0HBY9FbejHZzrRm1oQ3QtTFXdIr3e10Fmmg4Z9kPvwzoG9bErjQMkRWqYfGRANBLBTjeD3aiFIo%2FeTUW3yqSyIcIID3l7CPzJQYHbX2cKAZDKKxo7LWTjwT%2BWyr1%2B5PEKbH1ZSmW2Q%3D%3D",
    "refresh-token": "WVjhtoqU1Nok0iUBAlrj0dlzlwmfoLRcKUVgPJlQpc3ha%2Bqn6BDOcyFIMLLgQQm0JV4tLaXlLAZjkVRk0pfmo6H91Qdr58T0cL%2FhFlqD1r8%3D"
}
```   
{{< /tab >}}

{{< tab "http code:401" >}} 
```
{
    "status": 2,
    "msg": "An exception occurred while decoding the access token"
}
```  
或
```
{
    "status": 2,
    "msg": "refresh_token expired"
}
```
{{< /tab >}}
{{< /tabs >}}