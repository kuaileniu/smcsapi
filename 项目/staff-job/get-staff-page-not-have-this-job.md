---
title: 分页查询未拥有此项目的用户列表
weight: 400
---

<small>更新日期: 2021-12-11</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff-job/get-staff-page-not-have-this-job
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  search  | string  | xxxxx  | 搜索文本内容 |

{{< /tab >}}
{{< tab "样例" >}}

body： 

```json
{
    "JobId": 143083874570001,
    "search": "",
    "page": 1,
    "limit": 30
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
            "Id": 1,
            "LoginName": "1565296",
            "EmployeeNo": "a123",
            "ChineseName": "冯先生",
            "EnglishName": "Tao",
            "Del": false
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
    "msg": "JobId 不可为空",
    "english_msg": "JobId can't be empty."
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

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
