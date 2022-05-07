---
title: 分页获取报告组信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-26</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-report-grouping/get-jtbl-report-grouping-page
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
            "Id": 144230403280001,
            "JobId": 1,
            "ReportGroupingName": "报告分组名称1",
            "CleaningSpec": "清理规范",
            "CreatedBy": "15652963646",
            "ModifiedBy": "15652963646",
            "CreateTime": "2021-12-26 16:00:32",
            "ModifyTime": "2021-12-26 16:02:48"
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
|  Id  | number  | 144095520480001  | 报告组ID |
|  JobId  | number  | xxx  | 项目ID |
|  ReportGroupingName  | string  | xxx  | 报告组名称 |
|  CleaningSpec  | string  | xxx  | 清理规范 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="report-groupingnos=table,hl_report-groupings=0-6,report-groupingnostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="report-groupingnos=table,hl_report-groupings=0-6,report-groupingnostart=3">}}
