---
title: 分页获取员工信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-04-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-employee/get-jtbl-employee-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | xxxxx  | 搜索文本内容 |
|  JobId  | number  | 1  | 项目id |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "search":"",
    "JobId":1,
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
            "Id": 148081070380001,
            "EmployeeCode": "a",
            "EmployeeName": "b",
            "PipeFitterNo": "c",
            "WelderNo": "d",
            "InspectorNo": "e",
            "StaffID": 1,
            "SiteShop": "",
            "SiteCode": "",
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
            ],
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2022-04-09 09:11:43",
            "ModifyTime": "2022-04-09 09:11:43",
            "LoginName": "15652963646",
            "EmployeeNo": "a123",
            "ChineseName": "冯先生",
            "EnglishName": "Tao"
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
    "msg": "查询数据发生异常请稍后重试",
    "english_msg": "Error occurs when finding data"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

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
|  LoginName  | string  | xxxxxx  | 用户名(登录名)  |
|  EmployeeNo  | string  | xxxxxx  | 员工号  |
|  ChineseName  | string  | xxxxxx  | 中文名  |
|  EnglishName  | string  | xxxxxx  |  英文名 |



#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
