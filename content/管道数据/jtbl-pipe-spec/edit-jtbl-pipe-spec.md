---
title: 编辑管道规范的信息
weight: 300
---

<small>更新日期: 2021-12-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-pipe-spec/edit-jtbl-pipe-spec
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 管道规范ID |
|  JobId  | number  | xxx  | 项目ID |
|  PipeSpec  | string  | xxx  | 管道规范名称 |
|  MachineSOF  | boolean  | true  | 是机加工SO法兰 |
|  NDTPercent  | 正整数  | 45  | 无损检测比例,例如45%时传45 |
 
{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 144233214280001,
    "PipeSpec": "管道规范名称",
    "JobId": 1,
    "MachineSOF": true,
    "NDTPercent": 45
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
    "msg": "管道规范名称不可为空。",
    "english_msg": "LineName can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
