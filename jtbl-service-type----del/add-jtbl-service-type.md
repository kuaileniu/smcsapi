---
title: 新增介质类型
weight: 100
---

<small>更新日期: 2021-12-24</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-service-type/add-jtbl-service-type
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  ServiceType  | string  | xxx  | 介质类型 |
|  OrderNum  | number  | 1 | 排序号 | 
 


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "ServiceType": "介质类型1",
    "OrderNum": 1
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
        "Id": 144099490310001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,介质类型重复。",
    "english_msg": "Add failed,duplicate ServiceType."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 介质类型id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
