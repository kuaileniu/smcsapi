---
title: 编辑优先级的信息
weight: 300
---

<small>更新日期: 2021-12-21</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-priority/edit-jtbl-priority
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

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

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
 
{
    "Id": 144138284680001,
    "JobId": 1,
    "Priority": 1,
    "PriorityDesc": "一级",
    "RequiredOnSiteDate": "2021-12-30",
    "ModuleStartNumber": 1,
    "ModuleEndNumber": 90,
    "WorkshopId": 1,
    "PlantAreaId": 1,
    "Note": "Note1"
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
    "msg": "修改失败,优先级不可为空。",
    "english_msg": "Priority can't be blank.."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
