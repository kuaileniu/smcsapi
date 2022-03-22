---
title: 获取用户自己的基本信息
weight: 600
---

<small>更新日期: 2021-10-02</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/my-base-info
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  描述 |  举例 |
|  ----  | ----  | ----  |
{{< /tab >}}
{{< tab "样例" >}} 

URL： https://xxx.com/api/staff/my-base-info

body： 

```

```
{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "http code:200" >}} 
```
{
    "status": 0,
    "data": {
        "Id": 2110192358330001,
        "LoginName": "13022963646",
        "EmployeeNo": "",
        "ChineseName": "冯先生",
        "EnglishName": "Tao",
        "Email": "",
        "Telephone": "",
        "Cellphone": "",
        "WorkingLocation": "",
        "PermanentAddress": "",
        "Postcode": "",
        "StaffType": "",
        "Position": "",
        "DeptId": "",
        "IDType": "",
        "IDNumber": "",
        "Nationality": "",
        "Language": "",
        "CostCenter": "",
        "CompanyId": 201,
        "Comments": "",
        "LoginTimes": 2,
        "LastLoginIp": "127.0.0.1",
        "LastLoginTime": "2021-10-20 09:57:25",
        "OrderNum": 20211019235833,
        "CreateTime": "2021-10-19 23:58:33",
        "ModifyTime": "2021-10-19 23:58:33"
    }
}
```   
{{< /tab >}}

{{< tab "" >}} 
 
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 用户的id  |
|  LoginName  | string  | zhangsan  | 用户的登录账号  |
|  EmployeeNo  | string  | a4  | 员工号  |
|  ChineseName  | string  | 冯先生  | 中文名  |
|  EnglishName  | string  | Tao  | 英文名  |
|  Email  | string  | a@163.com  | 电子邮箱  |
|  Telephone  | string  | 010-70334466  | 电话  |
|  Cellphone  | string  | 13011123345  | 手机  |
|  WorkingLocation  | string  | 天津  | 工作地点  |
|  PermanentAddress  | string  | 小山沟  | 常住地址  |
|  Postcode  | string  | 292413  | 邮编  |
|  StaffType  | string  |   | 员工类型  |
|  Position  | string  | 经理  | 职位  |
|  DeptId  | string  | 210001  | 部门ID  |
|  IDNumber  | string  | xx  | ID号码 |
|  IDType  | string  |   | ID类型  |
|  Nationality  | string  |  英国 | 国籍  |
|  Language  | string  |  英语 | 语言  |
|  CostCenter  | string  |  焊工 | 成本中心  |
|  CompanyId  | number  |  201 | 公司ID  |
|  Comments  | string  |  这里是备注文字 | 备注  |
|  LoginTimes  | number  | 3  | 登录次数  |
|  LastLoginIp  | string  | 127.0.0.1  | 最近登录时的ip地址  |
|  LastLoginTime  | string  | 2021-10-20 09:57:25  | 最后登录时间  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
