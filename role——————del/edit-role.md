---
title: 编辑角色信息
weight: 500
# GeekdocHidden: true
---

<small>更新日期: 2021-11-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/role/edit-role
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

 

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
|  Id  | number  | 是  | 2109300032090001  | 角色的id  |
|  Name  | string  | - | 管理员  | 名称  |
|  Description  |  string  | - | 这是个有权利的角色  | 描述  |
|  Code  |  string  | - | xx  | 编码  |
|  Internal  |  boolean  | - | true  | 是内部的  |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 143083874570001,
    "Code": "R01",
    "Name": "管理员",
    "Description": "拥有至高无上的权力",
    "Internal": false,
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
