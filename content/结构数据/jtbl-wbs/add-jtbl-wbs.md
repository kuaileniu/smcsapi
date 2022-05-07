---
title: 新增工作分解结构
weight: 100
---

<small>更新日期: 2022-03-30</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-wbs/add-jtbl-wbs
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  WBS  | string  |  xxxx | 结构 |
|  WBSDescription  | string  | xxx  | 结构描述 |


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "WBS": "结构1",
    "WBSDescription": "结构1的描述"
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
        "Id": 147016911980001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,工作分解结构重复。",
    "english_msg": "Add failed,duplicate WBS."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 工作分解结构id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
