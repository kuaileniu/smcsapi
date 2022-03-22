---
title: 新增设备区域
weight: 100
---

<small>更新日期: 2021-12-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-plant-area/add-jtbl-plant-area
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  |  number | 21999000 | 项目id |
|  PlantAreaName  | string  | xxx  | 设备区域名称 |
|  PlantAreaDesc  | string  | xxx  | 设备区域描述 |
|  DateDueOnSite  | string  | 2021-12-30 | 到达现场日期 |
|  IsometricsRequired  | number  | 5 | 所含单线图数量 |
|  PlantAreaTypeId  | number  | 21999001 | 设备区域类型ID |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 10,
    "PlantAreaName": "PlantAreaName1",
    "PlantAreaDesc": "PlantAreaDesc1",
    "DateDueOnSite": "2021-12-30",
    "IsometricsRequired": 30,
    "PlantAreaTypeId": 1
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
        "Id": 144099490310001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "项目ID不可为空。",
    "english_msg": "JobId can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 设备区域id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
