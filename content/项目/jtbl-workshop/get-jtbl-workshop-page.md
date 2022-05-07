---
title: 分页获取工厂/车间信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-14</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-workshop/get-jtbl-workshop-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | xxxxx  | 搜索文本内容 |
|  JobId  | number  | 1  | 项目id |
{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "search":"",
    "JobId":1,
    "page":1,
    "limit":2
}
```
{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "成功" >}} 
```json
{
    "status": 0,
    "data": [
        {
            "Id": 144128693780001,
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
            "JobId": 10,
            "CreatedBy": "xxx",
            "ModifiedBy": "xxxxxxx",
            "CreateTime": "2021-12-14 21:28:57",
            "ModifyTime": "2021-12-14 21:28:57"
        }
    ],
    "count": 1
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "查询数据发生异常请稍后重试",
    "english_msg": "Error occurs when finding data"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 工厂/车间ID |
|  Code  | string  | xxx  | 工厂/车间代码 |
|  WorkshopName  | string  | xxx  | 工厂/车间名称 |
|  Active  | boolean  | true  |  激活 |
|  Address  | string  | xxx | 地址 |
|  Email  | string  | 1@qq.com | 邮箱地址 |
|  Post  | string  | xxx | 邮编 |
|  ContactName  | string  | xxx | 联系人姓名 |
|  ContactTitle  | string  | xxx | 联系人职务 |
|  PhoneNo  | string  | xxx | 电话 |
|  Note  |  string | xxxx | 备注 |
|  JobId  |  number | 21999000 | 项目id |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
