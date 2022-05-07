---
title: 为用户变更项目
weight: 200
---

<small>更新日期: 2021-12-11</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff-job/change-job-for-staff
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
| StaffId  | number  | xxx  | 用户ID |
|  JobIds  | number 数组 | [143083874570001 ] | 最终拥有的项目ID数组 |


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "StaffId": 88888,
    "JobIds": [
        1,
        9999
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
    "msg": "操作成功",
    "english_msg": "Success"
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "JobId 不可为空",
    "english_msg": "JobId can't be empty"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |


#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
