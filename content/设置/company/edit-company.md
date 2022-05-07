---
title: 编辑公司的信息
weight: 500
# GeekdocHidden: true
---

<small>更新日期: 2021-10-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/company/edit-company
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  必含 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  | ----  |
|  Id  | number  | 是  | 143050937780001  | 公司ID |
|  Code  | string  | - | xxx  | 编码  |
|  Name  |  string  | - | xxx  | 名称  |
|  OrderNum  |  number  | - | 8  | 排序号  |
|  Description  |  string  | - | xxxx  | 描述  |

{{< /tab >}}
{{< tab "样例" >}}

body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 143050937780001,
    "Code": "code2",
    "Name": "美孚2",
    "Description": "他家有钱?",
    "OrderNum": 2
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
    "msg": "修改成功。",
    "english_msg": "Success."
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "Id不可为空",
    "english_msg": "Id can't be empty"
}
```
{{< /tab >}}
{{< /tabs >}}


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
