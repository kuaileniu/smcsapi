---
title: 获取部门信息(分页)
weight: 200
# GeekdocHidden: true
---

<small>更新日期: 2021-11-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/department/get-department-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | 中石化  | 搜索文本内容 |

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/department/get-department-page

body： 

```json
{
    "search":"",
    "page":1,
    "limit":30
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
            "Id": 143042905470001,
            "Code": "",
            "Name": "IT部",
            "Description": "",
            "DeptType": 0,
            "ManagerId": 0,
            "ParentId": 0,
            "OrderNum": 20211104231054,
            "CreateTime": "2021-11-04 23:10:54",
            "ModifyTime": "2021-11-04 23:10:54",
            "Del": false
        },
        {
            "Id": 143042905470002,
            "Code": "",
            "Name": "销售部",
            "Description": "",
            "DeptType": 0,
            "ManagerId": 0,
            "ParentId": 0,
            "OrderNum": 20211104231054,
            "CreateTime": "2021-11-04 23:10:54",
            "ModifyTime": "2021-11-04 23:10:54",
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
|  Id  | number  | 是  | 2109300032090001  | 公司的id  |
|  Name  | string  | 是 | 中石化  | 名称  |
|  Description  |  string  | - | 这是个大客户  | 描述  |
|  Code  |  string  | - | xx  | 编码  |
|  DeptType  |  number  | - | xx  | 类型  |
|  ManagerId  |  number  | - | xx  | 部门经理ID  |
|  ParentId  |  number  | - | xx  | 上级部门ID  |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
