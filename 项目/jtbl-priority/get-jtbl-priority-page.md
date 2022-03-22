---
title: 分页获取优先级信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-21</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-priority/get-jtbl-priority-page
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
            "Id": 144189652580001,
            "Priority": 1,
            "PriorityDesc": "一级",
            "RequiredOnSiteDate": "2021-12-30 00:00:00",
            "ModuleStartNumber": 1,
            "ModuleEndNumber": 90,
            "JobId": 1,
            "WorkshopId": 1,
            "PlantAreaId": 1,
            "Note": "Note1",
            "CreatedBy": "156529636xxx",
            "CreateTime": "2021-12-21 22:48:45",
            "ModifyTime": "2021-12-21 22:48:45",
            "WorkshopName": "WorkshopName1",
            "PlantAreaName": "AreaName1"
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
|  Id  | number  | 144095520480001  | 优先级ID |
|  JobId  |  number | 21999000 | 项目id |
|  Priority  | number  | 1  | 等级 |
|  PriorityDesc  | string  | xxx  | 等级描述 |
|  RequiredOnSiteDate  | string  | 2021-12-30 | 要求现场交货日期 |
|  ModuleStartNumber  | number  | 5 | 模块开始数字 |
|  ModuleEndNumber  | number  | 90 | 模块结束数字 |
|  WorkshopId  | number  | 1 | 工厂/车间ID |
|  PlantAreaId  | number  | 90 | 设备区域ID |
|  Note  | string  | 90 | 备注 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
