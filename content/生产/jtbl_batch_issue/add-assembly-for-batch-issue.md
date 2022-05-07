---
title: 为生产批次关联构件
weight: 700
# geekdocHidden: true
---

<small>更新日期: 2022-04-20</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/add-assembly-for-batch-issue
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
- 说明： 与提供的JobId相同的，对数组 AssemblyIDS 或 AssemblyNos 包含的构件都进行关联。
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目id |
|  BatchIssueID  | number  | 1  | 生产批次id|
|  AssemblyIDS  | number数组  | [1]  | 构件id数组|
|  AssemblyNos  | string数组  | ["a","b"]  | 构件号数组|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchIssueID": 1,
    "AssemblyIDS": [
        1,2
    ],
    "AssemblyNos": [
        "1010-1200-B0001",
        "1010-1200-B0002"
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
    "msg": "关联失败",
    "english_msg": "Failed."
}



{
    "status": 1,
    "msg": "构件[1010-1200-B0001]已经被其它生产批次关联。",
    "english_msg": "AssemblyNo[1010-1200-B0001] were Associated with other BatchIssue."
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
