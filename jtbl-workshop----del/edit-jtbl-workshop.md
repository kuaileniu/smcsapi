---
title: 编辑工厂/车间的信息
weight: 300
---

<small>更新日期: 2021-12-14</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-workshop/edit-jtbl-workshop
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 工厂/车间ID |
|  Code  | string  | xxx  | 工厂/车间代码,当修改此值时需带上JobId |
|  WorkshopName  | string  | xxx  | 工厂/车间名称,当修改此值时需带上JobId |
|  Active  | boolean  | true  |  激活 |
|  Address  | string  | xxx | 地址 |
|  Email  | string  | 1@qq.com | 邮箱地址 |
|  Post  | string  | xxx | 邮编 |
|  ContactName  | string  | xxx | 联系人姓名 |
|  ContactTitle  | string  | xxx | 联系人职务 |
|  PhoneNo  | string  | xxx | 电话 |
|  Note  |  string | xxxx | 备注 |
|  JobId  |  number | 21999000 | 项目id |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 144126572280001,
    "Code": "Code1",
    "WorkshopName": "WorkshopName1",
    "Active": false,
    "Address": "Address",
    "Email": "1@173.com",
    "Post": "272412",
    "ContactName": "zhang三",
    "ContactTitle": "总监",
    "PhoneNo": "13011192345",
    "FaxNo": "010-12345678",
    "JobId": 0
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
    "msg": "修改失败,工厂/车间名称重复。",
    "english_msg": "Failed,duplicate WorkshopName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
