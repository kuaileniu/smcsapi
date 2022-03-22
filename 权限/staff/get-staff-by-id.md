---
title: 根据ID获取用户信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-10-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/get-staff-by-id
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  必含 |   示例 |  描述 |
|  ----  | ----  | ----  | ----  | ----  |
|  StaffId  | number  | 是  | 2110229007990001  | 用户ID |

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/staff/get-staff-by-id

body： 

```json
{
    "StaffId": 2110229007990001
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
    "data": {
        "Id": 2110229007990001,
        "LoginName": "1",
        "ChineseName": "小王",
        "Email": "",
        "Telephone": "",
        "Cellphone": "",
        "WorkingLocation": "",
        "PermanentAddress": "",
        "Postcode": "",
        "StaffType": "",
        "IDNumber": "",
        "Position": "",
        "DeptId": 9,
        "IDType": "",
        "Nationality": "",
        "Language": "",
        "CostCenter": "",
        "CompanyId": 0,
        "Comments": "",
        "AppToken": "xxxxx",
        "AppClientId": "yyyy",
        "LoginTimes": 0,
        "LastLoginIp": "",
        "LastLoginTime": "",
        "OrderNum": 0,
        "CreateTime": "2021-10-26 12:07:59",
        "ModifyTime": "2021-10-26 12:39:27",
        "Del": false
    }
}
```   
{{< /tab >}}

{{< tab "失败-1" >}}
```json
{
    "status": 1,
    "msg": "请提供有效的用户Id",
    "english_msg": "Please provide a valid Staff ID."
}
```
{{< /tab >}}

{{< tab "失败-2" >}}
```json
{
    "status": 1,
    "msg": "用户不存在",
    "english_msg": "User not exist."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
|  Id  | number  | 是  | 2109300032090001  | 用户的id  |
|  LoginName  | string  | 是 | hggfjt  | 用户名(登录账号)  |
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
|  LoginTimes  |  number  | - |  xxx |  登录次数(正整数)  |
|  LastLoginIp  |  string  | - |  xxx |  上次登录ip  |
|  OrderNum  |  number  | - |  xxx |  排序号  |
|  CreateTime  |  string  | - |  2021-10-22 12:28:45 |  创建时间  |
|  ModifyTime  |  string  | - |  2021-10-22 12:28:45 |  修改时间  |
|  Del  |  boolean  | - |  true |  true表示被删除(未启用)  |