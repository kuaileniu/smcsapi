---
title: 新增管线
weight: 100
---

<small>更新日期: 2021-12-26</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-line/add-jtbl-line
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | xxx  | 项目ID |
|  LineName  | string  | xxx  | 管线名称 |
|  LineDescription  | string  | xxx  | 描述 |
|  LineWeighting  | 正整数  | 45  | 管线权重,例如45%时传45 |
|  Spare1  |  string | xxxx | 自定义字段1 |
|  Spare2  |  string | xxxx | 自定义字段2 |
|  Spare3  |  string | xxxx | 自定义字段3 |
|  Spare4  |  string | xxxx | 自定义字段4 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "LineName": "管线2",
    "LineDescription": "管线描述2",
    "LineWeighting": 45,
    "ReportGroupingId": 1,
    "Spare1": "Spare1",
    "Spare2": "Spare2",
    "Spare3": "Spare3",
    "Spare4": "Spare4"
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
    "msg": "添加失败,管线号名称重复。",
    "english_msg": "Add failed,duplicate LineName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 管线id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
