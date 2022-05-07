---
title: 编辑员工的信息
weight: 300
---

<small>更新日期: 2022-04-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-employee/edit-jtbl-employee
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 员工ID |
|  EmployeeCode  | string  |  xx | 员工代码 |
|  EmployeeName  | string  | xxx  | 员工名字 |
|  PipeFitterNo  | string  | xxx  | 铆工号 |
|  WelderNo  | string  | xxx  | 焊工号 |
|  InspectorNo  | string  | xxx  | 检验员号 |
|  StaffID  | number  | 1  | 用户ID(staff表id) |
|  SiteShop  | string  | xxxxxx  |   |
|  SiteCode  | string  | xxxxxx  |   |
|  Activate  | boolean  | true  | 激活 |
|  AttachSli  | json数组  | []  | 附件，请看样例 |


{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 148077596180001,
    "EmployeeCode": "a",
    "EmployeeName": "b",
    "PipeFitterNo": "c",
    "WelderNo": "d",
    "InspectorNo": "e",
    "StaffID": 1,
    "SiteShop": "sss",
    "SiteCode": "ddd",
    "Activate": false,
    "AttachSli": [
        {
            "OriginName": "bb.jpg",
            "Path": "https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/b5f02682d8b69471b70ec415acc9965e_1895.png",
            "Size": 1895
        },
        {
            "OriginName": "a.jpg",
            "Path": "https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/341bdf1f96e41c2da848770b89110909_1241.png",
            "Size": 1241
        }
    ]
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
    "english_msg": "Success",
  
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "修改失败,员工代码重复。",
    "english_msg": "Edit failed,duplicate EmployeeCode."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
