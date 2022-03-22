---
title: 编辑介质的信息
weight: 300
---

<small>更新日期: 2021-12-24</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-service/edit-jtbl-service
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 介质ID |
|  JobId  | number  | xxx  | 项目ID |
|  ServiceName  | string  | xxx  | 介质名称 |
|  ServiceDescription  | string  | xxx  | 描述 |
|  NDTPercent  | 正整数  | 45  | 无损检测比例,例如45%时给服务器传45 |
|  Spare1  |  string | xxxx | 自定义字段1 |
|  Spare2  |  string | xxxx | 自定义字段2 |
|  Spare3  |  string | xxxx | 自定义字段3 |
|  Spare4  |  string | xxxx | 自定义字段4 |
 
{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 144207543780001,
    "JobId": 1,
    "ServiceName": "介质名称1",
    "ServiceDescription": "描述",
    "NDTPercent": 45,
    "ServiceTypeId": 1,
    "Spare1": "Spare1",
    "Spare2": "Spare2",
    "Spare3": "Spare3",
    "Spare4": "Spare4"
}
```
{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "成功" >}} 
```json
{
    "status": 3,
    "msg": "修改成功",
    "english_msg": "Success",
  
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "介质名称不可为空。",
    "english_msg": "AreaName can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
