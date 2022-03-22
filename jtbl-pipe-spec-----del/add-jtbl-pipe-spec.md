---
title: 新增管道规范
weight: 100
---

<small>更新日期: 2021-12-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-pipe-spec/add-jtbl-pipe-spec
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | xxx  | 项目ID |
|  PipeSpec  | string  | xxx  | 管道规范名称 |
|  MachineSOF  | boolean  | true  | 是机加工SO法兰 |
|  NDTPercent  | 正整数  | 45  | 无损检测比例,例如45%时传45 |
 
{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
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
    "msg": "添加成功",
    "english_msg": "Add success",
    "data": {
        "Id": 144230022080001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,管道规范名称重复。",
    "english_msg": "Add failed,duplicate PipeSpec."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 管道规范id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
