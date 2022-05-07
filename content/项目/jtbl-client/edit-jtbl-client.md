---
title: 编辑业主客户的信息
weight: 300
---

<small>更新日期: 2021-12-07</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-client/edit-jtbl-client
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144074477080001  | 业主客户id |
|  Code  | string  | xxx  | 业主代码 |
|  OrganisationName  | string  | xxx  | 组织名称 |
|  Active  | boolean  | true/  | 启用 |
|  Address  | string  | xxx市  | 地址 |
|  Email  | string  | x@163.com  | 邮箱 |
|  Post  | string  | xxx  | 邮编 |
|  LinkMan  | string  | 张三  | 联系人 |
|  Title  | string  | 经理  | 职务 |
|  Tel  | string  | 010-11223344  | 电话 |
|  Fax  | string  | 010-11223344  | 传真 |
|  Note  | string  | xxx  | 备注 |
 
{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id":144074477080001,
    "Code": "R03",
    "OrganisationName": "武当山02",
    "Active": true,
    "Address": "北京市xxxx",
    "Email": "1@qq.com",
    "Post": "274928",
    "LinkMan": "张三",
    "Title": "经理",
    "Tel": "010-88665544",
    "Fax": "010-xxxx",
    "Note": "备注"
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
    "english_msg": "Success"
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "客户名称不可为空",
    "english_msg": "ClientName can't be blank"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
