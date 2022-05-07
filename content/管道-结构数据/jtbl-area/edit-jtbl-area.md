---
title: 编辑分区的信息
weight: 300
---

<small>更新日期: 2021-12-11</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-area/edit-jtbl-area
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 分区ID |
|  JobId  | number  | xxx  | 项目ID |
|  AreaName  | string  | xxx  | 分区名称,当修改此值时需带上JobId |
|  AreaDescription  | string  | xxx  | 描述,当修改此值时需带上JobId |
|  LastCopiedSpool  | number  | 123 | 最后复制管段号 |
|  OnSkidArea  | number  | xxx | 撬上区域 | 
|  DeliveryGroupId  |  number | 123 | 发货组ID |
|  Spare1  |  string | xxxx | 自定义字段1 |
|  Spare2  |  string | xxxx | 自定义字段2 |
|  Spare3  |  string | xxxx | 自定义字段3 |
|  Spare4  |  string | xxxx | 自定义字段4 |
 
{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 144099490310001,
    "JobId": 1,
    "AreaName": "AreaName1",
    "AreaDescription": "AreaDescription1",
    "LastCopiedSpool": 4,
    "OnSkidArea": 5,
    "DeliveryGroupId": 6,
    "Spare1": "s",
    "Spare2": "x",
    "Spare3": "e",
    "Spare4": "h"
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
    "msg": "修改成功",
    "english_msg": "Success",
  
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "分区名称不可为空。",
    "english_msg": "AreaName can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
