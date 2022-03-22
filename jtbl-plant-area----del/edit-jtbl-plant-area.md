---
title: 编辑设备区域的信息
weight: 300
---

<small>更新日期: 2021-12-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-plant-area/edit-jtbl-plant-area
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 设备区域ID |
|  JobId  |  number | 21999000 | 项目id |
|  PlantAreaName  | string  | xxx  | 设备区域名称 |
|  PlantAreaDesc  | string  | xxx  | 设备区域描述 |
|  DateDueOnSite  | string  | 2021-12-30 | 到达现场日期 |
|  IsometricsRequired  | number  | 5 | 所含单线图数量 |
|  PlantAreaTypeId  | number  | 21999001 | 设备区域类型ID |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
 
{
    "Id": 144138284680001,
    "JobId": 1,
    "PlantAreaName": "PlantAreaName40",
    "PlantAreaDesc": "PlantAreaDesc40",
    "DateDueOnSite": "2021-12-30",
    "PlantAreaTypeId": 2,
    "IsometricsRequired": 9990
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
    "msg": "修改失败,设备区域名称重复。",
    "english_msg": "Failed,duplicate PlantAreaName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
