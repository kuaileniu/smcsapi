---
title: 编辑用户(们)的信息
weight: 300
# GeekdocHidden: true
---

<small>更新日期: 2021-10-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/edit-staffs
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  必含 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  | ----  |
|  Ids  | 整型数组  | 是  | [2110222147230001,2110222148290001]  | 用户ID列表 |
|  LoginName  | string  | - | hggfjt  | 用户名(登录账号)  |
|  EmployeeNo  |  string  | - | a123  | 员工号  |
|  ChineseName  |  string  | - | 张三  | 中文名  |
|  EnglishName  |  string  | - | san.zhang  | 英文名  |
|  IDNumber  | string  | - | xx  | ID号码 |
|  Email  |  string  | - |  a@163.com | 英文名  |
|  Telephone  |  string  | - |  010-8888888 | 电话  |
|  Cellphone  |  string  | - |  130111122222 | 手机  |
|  WorkingLocation  |  string  | - |  天津 | 地点  |
|  PermanentAddress  |  string  | - |  xxx | 地址  |
|  Postcode  |  string  | - |  xxx | 邮编  |
|  StaffType  |  string  | - |  xxx | 类型  |
|  Position  |  string  | - |  xxx | 职位  |
|  DeptId  |  number  | - |  123 | 部门ID(正整数)  |
|  IDType  |  string  | - |  xxx |  ID类型  |
|  Nationality  |  string  | - |  xxx |  国籍  |
|  Language  |  string  | - |  xxx |  语言  |
|  CostCenter  |  string  | - |  xxx |  成本中心  |
|  CompanyId  |  string  | - |  xxx |  公司ID  |
|  Comments  |  string  | - |  xxx |  备注  |
|  AppToken  |  string  | - |  xxx |  App令牌  |
|  AppClientId  |  string  | - |  xxx |  App客户端ID  |
|  OrderNum  |  string  | - |  xxx |  排序号  |
|  Pwd  |  string  | - |  xxx |  密码  |
|  Del  |  boolean  | - |  true |  true表示被删除(未启用)  |
{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/staff/edit-staffs

body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Ids": [
        2110229007990001,
        2110229009390001
    ],
    "ChineseName": "小王",
    "Pwd": "1"
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
    "msg": "用户ID不可为空",
    "english_msg": "User ID can't be empty"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
 

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
