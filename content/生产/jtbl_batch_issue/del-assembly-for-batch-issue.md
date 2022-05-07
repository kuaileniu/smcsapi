---
title:  为批次去掉关联构件
weight: 800
# geekdocHidden: true
---

<small>更新日期: 2022-04-17</small>

#### 接口说明
1. 若干构件id数组中有已经被其它批次关联的，则不受影响。

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/del-assembly-for-batch-issue
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目id |
|  BatchIssueID  | number  | 1  | 生产批次id|
|  AssemblyIDS  | number数组  | [1]  | 构件id数组|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchIssueID": 1,
    "AssemblyIDS": [
        1,
        147259178080001,
        147264964080001,
        147264966880001,
        147264971580001
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
