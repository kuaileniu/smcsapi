---
title: 获取用户信息(分页)
weight: 500
# GeekdocHidden: true
---

<small>更新日期: 2021-10-23</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/get-staff-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | zhangsan  | 搜索文本内容 |

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/staff/get-staff-page

body： 

```json
{
    "search":"1",
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
            "Id": 143065864980001,
            "LoginName": "zhangsan",
            "EmployeeNo": "1001",
            "ChineseName": "张三",
            "EnglishName": "tom",
            "Email": "1@163.com",
            "Telephone": "010-8888888",
            "Cellphone": "156",
            "WorkingLocation": "华盛顿",
            "PermanentAddress": "北京",
            "Postcode": "273867",
            "StaffType": "a",
            "Position": "经理",
            "IDNumber": "2910101",
            "IDType": "a",
            "Nationality": "小日本",
            "Language": "日语",
            "CostCenter": "A",
            "Comments": "哈哈",
            "AppToken": "xxxx",
            "AppClientId": "yyyy",
            "LoginTimes": 0,
            "LastLoginIp": "",
            "LastLoginTime": "",
            "OrderNum": 19,
            "CreateTime": "2021-11-07 14:57:29",
            "ModifyTime": "2021-11-07 14:57:29",
            "CompanyId": 3001,
            "Company": "",
            "DeptId": 143055278870002,
            "Department": "IT部",
            "Del": false
        },
        {
            "Id": 143055294270001,
            "LoginName": "15652963646",
            "EmployeeNo": "a123",
            "ChineseName": "冯先生",
            "EnglishName": "Tao",
            "Email": "a@163.com",
            "Telephone": "",
            "Cellphone": "",
            "WorkingLocation": "",
            "PermanentAddress": "",
            "Postcode": "",
            "StaffType": "",
            "Position": "",
            "IDNumber": "",
            "IDType": "",
            "Nationality": "",
            "Language": "",
            "CostCenter": "",
            "Comments": "",
            "AppToken": "",
            "AppClientId": "",
            "LoginTimes": 0,
            "LastLoginIp": "",
            "LastLoginTime": "",
            "OrderNum": 20211106093542,
            "CreateTime": "2021-11-06 09:35:42",
            "ModifyTime": "2021-11-06 09:35:42",
            "CompanyId": 143055278870004,
            "Company": "中石化",
            "DeptId": 143055278870003,
            "Department": "销售部",
            "Del": false
        }
    ],
    "count": 2
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

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
|  Id  | number  | 是  | 2109300032090001  | 用户的id  |
|  LoginName  | string  | 是 | hggfjt  | 用户名(登录账号)  |
|  EmployeeNo  |  string  | - | a123  | 员工号  |
|  ChineseName  |  string  | - | 张三  | 中文名  |
|  EnglishName  |  string  | - | san.zhang  | 英文名  |
|  Email  |  string  | - |  a@163.com | 英文名  |
|  Telephone  |  string  | - |  010-8888888 | 电话  |
|  Cellphone  |  string  | - |  130111122222 | 手机  |
|  WorkingLocation  |  string  | - |  天津 | 地点  |
|  PermanentAddress  |  string  | - |  xxx | 地址  |
|  Postcode  |  string  | - |  xxx | 邮编  |
|  StaffType  |  string  | - |  xxx | 类型  |
|  Position  |  string  | - |  xxx | 职位  |
|  IDNumber  | string  | - | xx  | ID号码 |
|  DeptId  |  number  | - |  123 | 部门ID(正整数)  |
|  Department  |  string  | - | xxx  | 部门名称  |
|  IDType  |  string  | - |  xxx |  ID类型  |
|  Nationality  |  string  | - |  xxx |  国籍  |
|  Language  |  string  | - |  xxx |  语言  |
|  CostCenter  |  string  | - |  xxx |  成本中心  |
|  CompanyId  |  string  | - |  xxx |  公司ID  |
|  Company  |  string  | - |  xxx |  公司名称  |
|  Comments  |  string  | - |  xxx |  备注  |
|  AppToken  |  string  | - |  xxx |  App令牌  |
|  AppClientId  |  string  | - |  xxx |  App客户端ID  |
|  LoginTimes  |  number  | - |  xxx |  登录次数(正整数)  |
|  LastLoginIp  |  string  | - |  xxx |  上次登录ip  |
|  OrderNum  |  number  | - |  xxx |  排序号  |
|  CreateTime  |  string  | - |  2021-10-22 12:28:45 |  创建时间  |
|  ModifyTime  |  string  | - |  2021-10-22 12:28:45 |  修改时间  |
|  Del  |  boolean  | - |  true |  true表示被删除(未启用)  |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
