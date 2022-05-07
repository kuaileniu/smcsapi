---
title:  根据构件批量修改批次下发日期
weight: 1000
# geekdocHidden: true
---

<small>更新日期: 2022-04-24</small>

#### 接口说明
 
#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/edit-batch-issue-date-by-assembly
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目id |
|  BatchIssueDate  | 日期  | 2000-11-22  | 下发日期 |
|  AssemblyIDS  | number数组  | [1]  | 构件id数组|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchIssueDate": "2000-11-22",
    "AssemblyIDS": [
        1,
        147180927480001,
        147180927480002,
        147180927480003
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
    "msg": "成功。",
    "english_msg": "Success."
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "BatchIssueDate 不可为空",
    "english_msg": "BatchIssueDate can't be empty."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
