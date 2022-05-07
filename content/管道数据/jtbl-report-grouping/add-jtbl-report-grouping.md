---
title: 新增报告组
weight: 100
---

<small>更新日期: 2021-12-26</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-report-grouping/add-jtbl-report-grouping
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | xxx  | 项目ID |
|  ReportGroupingName  | string  | xxx  | 报告组名称 |
|  CleaningSpec  | string  | xxx  | 清理规范 |


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "ReportGroupingName": "报告分组名称1",
    "CleaningSpec": "清理规范"
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
        "Id": 144230022080001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,报告组号名称重复。",
    "english_msg": "Add failed,duplicate LineName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 报告组id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="report-groupingnos=table,hl_report-groupings=0-6,report-groupingnostart=3">}}
