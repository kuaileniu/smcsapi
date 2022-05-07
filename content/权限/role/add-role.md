---
title: 新增角色
weight: 100
---

<small>更新日期: 2021-11-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/role/add-role
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Code  | string  | xxx  | 编码 |
|  Name  | string  | xxx  | 名称 |
|  Description  | string  | xxx  | 描述 |
|  OrderNum  | number  | 1  | 排序号 |
|  Internal  | boolean  | true  | 是内部角色 |
 

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "Code": "R007",
    "Name": "技术员1",
    "Internal": true,
    "OrderNum": 20211104231054,
    "Description": "干技术活的"
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
        "Id": 2110221205490001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "名称不可用",
    "english_msg": "Name can't be used"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 角色的id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
