---
title: 分页获取分区信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-11</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-area/get-jtbl-area-page
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
            "Id": 144099490310001,
            "JobId": 1,
            "AreaName": "AreaName1",
            "AreaDescription": "AreaDescription1",
            "LastCopiedSpool": 4,
            "OnSkidArea": 5,
            "DeliveryGroupId": 6,
            "Spare1": "",
            "Spare2": "",
            "Spare3": "",
            "Spare4": "",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2021-12-11 12:21:43",
            "ModifyTime": "2021-12-11 12:21:43",
            "DeliveryGroupName": ""
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
|  Id  | number  | xxx  | 分区ID |
|  JobId  | number  | xxx  | 项目ID |
|  AreaName  | string  | xxx  | 分区名称 |
|  AreaDescription  | string  | xxx  | 描述 |
|  LastCopiedSpool  | number  | 123 | 最后复制管段号 |
|  OnSkidArea  | number  | xxx | 撬上区域 | 
|  DeliveryGroupId  |  number | 123 | 发货组ID |
|  Spare1  |  string | xxxx | 自定义字段1 |
|  Spare2  |  string | xxxx | 自定义字段2 |
|  Spare3  |  string | xxxx | 自定义字段3 |
|  Spare4  |  string | xxxx | 自定义字段4 |
|  DeliveryGroupName  |  string | xxxx | 发货组名称 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
