---
title: 新增工作包
weight: 100
# GeekdocHidden: true
---

<small>更新日期: 2022-04-14</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-work-package/add-jtbl-work-package
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  WorkPackage  | string  |  xxxx | 工作包 |
|  WorkPackageDesc  | string  | xxx  | 描述 |
|  SubcontractorID  | number  | 1  | 分包商ID |
|  WorkshopID  | number  | 1  | 工厂/车间ID |
|  OrderNo  | string  | xxx  | 订单号 |
|  TransmittalNo  | string  | xxx  | 传送单号 |
|  TransmittalDate  | 日期  | 2022-04-07  | 传送日期 |
|  EstimatedTonnage  | float  | 1.3  | 预估吨位 |
|  PriorityID  | number  | 1  | 优先等级ID |
|  AreaID  | number  | 1  | 区域ID |
|  Facility  | string  | xxxx  | 设备 |
|  Schedule  | string  | xxxx  | 计划表 |
|  RequiredOnSiteDate  | 日期  | 2022-04-07  | 要求现场交货日期 |
|  ForecastFabStartDate  | 日期  | 2022-04-07  | 预计开工日期 |
|  ForecastFabCompleteDate  | 日期  | 2022-04-07  | 预计完工日期 |
|  TargetAssemblyCompleteDate  | 日期  | 2022-04-07  | 预计组装完工日期 |
|  AssemblyWorkshop  | string  | xxxx  | 预组装工厂 |
|  Comment  | string  | xxxx  | 备注 |
|  ActualFabStartDate  | 日期  | 2022-04-07  | 实际开工日期 |
|  ActualFabCompleteDate  | 日期  | 2022-04-07  | 实际完工日期 |
	 
{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "WorkPackage": "包1",
    "WorkPackageDesc": "包1说明",
    "SubcontractorID": 1,
    "WorkshopID": 1,
    "OrderNo": "no1111",
    "TransmittalNo": "f1111",
    "TransmittalDate": "2022-04-07",
    "EstimatedTonnage": 1.01,
    "PriorityID": 1,
    "AreaID": 1,
    "Facility": "ffff",
    "Schedule": "xxxx",
    "RequiredOnSiteDate": "2022-04-07",
    "ForecastFabStartDate": "2022-04-07",
    "ForecastFabCompleteDate": "2022-04-07",
    "TargetAssemblyCompleteDate": "2022-04-07",
    "AssemblyWorkshop": "预组装工厂1",
    "Comment": "xxxx",
    "ActualFabStartDate": "2024-04-07",
    "ActualFabCompleteDate": "2025-04-07"
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
        "Id": 147016911980001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,工作包重复。",
    "english_msg": "Add failed,duplicate WorkPackage."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 工作包id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
