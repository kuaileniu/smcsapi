---
title: 新增用户
weight: 100
---

<small>更新日期: 2021-11-03</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/add-staff
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  LoginName  | string  | hggfjt  | 用户名 |
|  Del  |  boolean | false  | 是否启用；false表示启用(未被假删除)，true表示未启用(已被假删除)  |
|  EmployeeNo  | string  | xx  | 员工号 |
|  ChineseName  | string  | xx  | 中文名 |
|  EnglishName  | string  | xx  | 英文名 |
|  IDNumber  | string  | xx  | ID号码 |
|  Email  | string  | a@163.com  | 电子邮箱 |
|  Telephone  | string  | 010-8888888  | 电话号码 |
|  Cellphone  | string  | 13012345678  | 手机 |
|  WorkingLocation  | string  | 天津  | 地点(工作地点) |
|  PermanentAddress  | string  | xxxx小山村  | 地址(常住地址) |
|  Postcode  | string  | 282412  | 邮编 |
|  StaffType  | string  | xxx  | 员工类型 |
|  Position  | string  | yyy  | 职位 |
|  DeptId  | number  | yyy  | 部门(部门id),整数类型 |
|  IDType  | string  | uuu  | 类型(ID类型) |
|  Nationality  | string  | iii  | 国籍 |
|  Language  | string  | ooo  | 语言 |
|  CostCenter  | string  | pp  | 成本中心 |
|  CompanyId  | number  | 123  | 公司id |
|  Comments  | string  | xxxx  | 备注 |
|  OrderNum  | number  |  19 | 排序号(整数类型) |
|  AppToken  | string  |  xxxx | App令牌 |
|  AppClientId  | string  |  yyy | App客户端ID |
|  Pwd  | string  |  xxxyy | 密码 |

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/staff/add-staff

body： 

```json
{
    "LoginName": "hggfjt48",
    "Del": false,
    "Email": "",
    "Telephone": "",
    "Cellphone": "",
    "WorkingLocation": "",
    "PermanentAddress": "",
    "Postcode": "",
    "StaffType": "",
    "Position": "",
    "DeptId": 0,
    "IDNumber":"",
    "IDType": "",
    "Nationality": "",
    "Language": "",
    "CostCenter": "",
    "CompanyId": 0,
    "Comments": "",
    "OrderNum": 0,
    "AppToken":"xxxxx",
    "AppClientId":"yyyy",
    "Pwd": "123456"
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
        "Id": 2110221205490001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "用户名不可用",
    "english_msg": "Login name can't be used"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 用户的id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
