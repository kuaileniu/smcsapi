---
title: 新增分包商
weight: 100
---

<small>更新日期: 2021-12-13</small>

#### 基本参数
1. url : https://{domain}:{port}/api/subcontractor/add-subcontractor
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  SubContractorCode  | string  | xxx  | 分包商代码 |
|  SubContractorName  | string  | xxx  | 分包商名称(描述) |
|  Active  | boolean  | true  | 已经启用 |
|  Address  | string  | xxx,xxx | 地址 |
|  Email  | string  | xxx | 电子邮箱地址 |
|  Postcode  |  string | 123 | 邮编 |
|  ContactName  |  string | xxx | 联系人名称 |
|  ContactTitle  |  string | xxx | 联系人职务 |
|  PhoneNo  |  string | xxx | 电话 |
|  FaxNo  |  string | xxx | 传真 |
|  Note  |  string | xxx | 备注 |
 

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "SubContractorCode": "分包商代码1",
    "SubContractorName": "分包商名称(描述)1",
    "Active": true,
    "Address": "江苏省xxxx",
    "Email": "xx@qq.com",
    "Postcode": "272412",
    "ContactName": "张三",
    "ContactTitle": "经理",
    "PhoneNo": "020-66688899",
    "FaxNo": "020-66688877",
    "Note": "备注xx"
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
        "Id": 144115764880001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "分包商代码不可为空",
    "english_msg": "SubContractorCode can't be blank"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 分包商id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
