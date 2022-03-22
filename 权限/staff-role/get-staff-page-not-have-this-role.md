---
title: 查询 不 拥有此角色的用户信息(分页)
weight: 200
# GeekdocHidden: true
---

<small>更新日期: 2021-10-23</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff-role/get-staff-page-not-have-this-role
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  RoleId  | number  | 143083874570001  | 角色ID |

{{< /tab >}}
{{< tab "样例" >}}



body： 

```json
{
    "RoleId":143083874570001,
    "page":0,
    "limit":3
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
            "LoginName": "caocao",
            "EmployeeNo": "1",
            "ChineseName": "曹操",
            "EnglishName": "cao",
            "Del": false
        },
        {
            "Id": 2,
            "LoginName": "zhuge",
            "EmployeeNo": "2",
            "ChineseName": "诸葛孔明",
            "EnglishName": "kong",
            "Del": false
        },
        {
            "Id": 3,
            "LoginName": "liubei",
            "EmployeeNo": "3",
            "ChineseName": "刘备",
            "EnglishName": "liu",
            "Del": false
        }
    ],
    "count": 4
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


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
