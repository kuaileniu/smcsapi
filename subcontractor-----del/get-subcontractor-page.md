---
title: 分页获取分包商信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-13</small>

#### 基本参数
1. url : https://{domain}:{port}/api/subcontractor/get-subcontractor-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | xxxxx  | 搜索文本内容 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "search":"",
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
            "Id": 144115823780002,
            "SubContractorCode": "分包商代码2",
            "SubContractorName": "分包商名称(描述)1",
            "Active": true,
            "Address": "江苏省xxxx",
            "Email": "xx@qq.com",
            "Postcode": "272412",
            "ContactName": "张三",
            "ContactTitle": "经理",
            "PhoneNo": "020-66688899",
            "FaxNo": "020-66688877",
            "Note": "备注xx",
            "CreatedBy": "15652963xxx",
            "ModifiedBy": "15652963xxx",
            "CreateTime": "2021-12-13 09:43:57",
            "ModifyTime": "2021-12-13 09:43:57"
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
|  Id  | number  | xxx  | 分包商ID |
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

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
