---
title: 分页获取设备区域信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-plant-area/get-jtbl-plant-area-page
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
            "Id": 144138284680001,
            "JobId": 1,
            "PlantAreaName": "PlantAreaName40",
            "PlantAreaDesc": "PlantAreaDesc40",
            "DateDueOnSite": "2021-12-30 00:00:00",
            "PlantAreaTypeId": 2,
            "IsometricsRequired": 9990,
            "CreatedBy": "15652963xxx",
            "ModifiedBy": "1565296xxx",
            "CreateTime": "2021-12-16 00:07:26",
            "ModifyTime": "2021-12-16 00:08:08",
            "PlantAreaTypeChineseName": "单独复制",
            "PlantAreaTypeEnglishName": "Copy Separately"
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
|  Id  | number  | 144095520480001  | 设备区域ID |
|  JobId  |  number | 21999000 | 项目id |
|  PlantAreaName  | string  | xxx  | 设备区域名称 |
|  PlantAreaDesc  | string  | xxx  | 设备区域描述 |
|  DateDueOnSite  | string  | 2021-12-30 | 到达现场日期 |
|  IsometricsRequired  | number  | 5 | 所含单线图数量 |
|  PlantAreaTypeId  | number  | 21999001 | 设备区域类型ID |
|  PlantAreaTypeChineseName  | string  | 单独复制 | 设备区域类型中文名称 |
|  PlantAreaTypeEnglishName  | string  | Copy Separately | 设备区域类型英文名称 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
