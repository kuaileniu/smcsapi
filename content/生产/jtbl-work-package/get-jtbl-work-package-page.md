---
title: 分页获取工作包信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-04-08</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-work-package/get-jtbl-work-package-page
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
            "Id": 148074386080001,
            "JobId": 1,
            "WorkPackage": "包1xxxx",
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
            "ActualFabCompleteDate": "2025-04-07",
            "CreatedBy": "15652963646",
            "ModifiedBy": "15652963646",
            "CreateTime": "2022-04-08 14:37:40",
            "ModifyTime": "2022-04-08 14:50:33",
            "SubContractorCode": "",
            "SubContractorName": "",
            "WorkshopCode": "Code1",
            "WorkshopName": "WorkshopName1",
            "Priority": 2,
            "PriorityDesc": "3",
            "AreaName": ""
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
|  Id  | number  | 144095520480001  | 工作包ID |
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
|  SubContractorCode  | string  | xxxx  | 分包商代码 | 
|  SubContractorName  | string  | xxxx  | 分包商名称 | 
|  WorkshopCode  | string  | xxxx  | 工厂/车间代码 | 
|  WorkshopName  | string  | xxxx  | 工厂/车间名称 | 
|  Priority  | number  | xxxx  | 优先级 | 
|  PriorityDesc  | string  | xxxx  | 优先级描述 |
|  AreaName  | string  | xxxx  | 分区/区域名称 |
|  ActualFabStartDate  | 日期  | 2022-04-07  | 实际开工日期 |
|  ActualFabCompleteDate  | 日期  | 2022-04-07  | 实际完工日期 |
#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
