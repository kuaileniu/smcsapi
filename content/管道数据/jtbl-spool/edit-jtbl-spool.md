---
title: 编辑管段的信息
weight: 300
---

<small>更新日期: 2022-01-18</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-spool/edit-jtbl-spool
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 管段ID |
|  JobId  | number  | 1  | 项目ID |
|  IsometricId  | number  | 1  | 单线ID |
|  SpoolNo  | string  | xxxx  | 管段号 |
|  ClientSpoolNo  | string  | xxx  | 客户管段号 |
|  SpoolRev  | string  | v1111  | 版本号 |
|  RevDate  | 日期  | 2021-11-22  | 版本日期 |
|  RevRef  | string  | xxx  | 版本说明 |
|  SpoolDescription  | string  | xxx  | 管段描述 |
|  SpoolSize  | string  | xxx  | 管段尺寸 |
|  PaintSpec  | string  | xxx  | 油漆规范 |
|  RevHold  | boolean  | true  | 版本暂停 |
|  MatHold  | boolean  | true  | 材料暂停 |
|  NDTHold  | boolean  | true  | 探伤暂停 |
|  IssuedForFabDate  | 日期  | 2021-11-22  | 图纸下发日期 |
|  CutCompDate  | 日期  | 2021-11-22  | 下料日期 |
|  FitUpDate  | 日期  | 2021-11-22  | 组对日期 |
|  WeldCompDate  | 日期  | 2021-11-22  | 焊接完成日期 |
|  GroundDate  | 日期  | 2021-11-22  | 打磨完成日期 |
|  DimInspectedDate  | 日期  | 2021-11-22  | 尺寸检验日期 |
|  WeldNDTCompDate  | 日期  | 2021-11-22  | 探伤完成日期 |
|  SentPaintDate  | 日期  | 2021-11-22  | 发往油漆日期 |
|  PackedDate  | 日期  | 2021-11-22  | 油漆完成日期 |
|  PackageNo  | string  | xxx  | 包装号码 |
|  TruckNo  | string  | xxx  | 转运车号 |
|  PunchListedDate  | 日期  | 2021-11-22  | 核查表日期 |
|  SignedOffDate  | 日期  | 2021-11-22  | 放行日期 |
|  SentSiteDate  | 日期  | 2021-11-22  | 发往现场日期 |
|  ReceivedSiteDate  | 日期  | 2021-11-22  | 现场收货日期 |
|  DocCompleteDate  | 日期  | 2021-11-22  | 文档完成日期 |
|  PriorityId  | number  | 1  | 优先等级ID |
|  DeliveryGroupId  | number  | 1  | 发货组ID |
|  BatchGroupId  | number  | 1  | 批次组ID |
|  HTID  | number  | 1  | 试压报告ID |
|  HydroRepNo  | string  | hr1  | 水压报告号 |
|  HTIDComply  | boolean  | true  | 水压合格 |
|  PaintRepNo  | string  | pr1111  | 油漆报告号 |
|  HardnessRepNo  | string  | pr1111  | 硬度试验报告号 |
|  CurrentLayDownArea  | string  | xxxx  | 目前放置区域 |
|  ExcludeFromProgress  | boolean  | true  | 进度报告排除 |
|  Comment  | string  | xxxx  | 备注 |
|  SelectForBatch  | boolean  | true  | 批次已选择 |
|  CanBuild  | boolean  | true  | 可建造 |
|  RequestedNotTested  | boolean  | true  | 申请未检测 |
|  Installed  | boolean  | true  | 完成安装 |
|  InstalledDate  | 日期  | 2021-11-22  | 安装日期 |
|  HTIDSite  | number  | 1  | 水压测试(现场)Id |
|  HTIDSiteComply  | boolean  | 1  | 水压测试(现场)合格 |
|  HTIDLeak  | 整数  | 1  | 泄漏测试Id |
|  HTIDLeakComply  | boolean  | 1  | 泄漏测试合格 |
|  SpoolWeight  | number  | 1  | 管段重量 |
|  SplDrawingRate  | number  | 12.45  | 管段图纸费率 |
|  IDTagRate  | number  | 12.45  | 标牌费率 |
|  MiscRate1  | number  | 12.45  | 杂项费率1 |
|  MiscRate2  | number  | 12.45  | 杂项费率2 |
|  MiscRate3  | number  | 12.45  | 杂项费率3 |
|  MiscRate4  | number  | 12.45  | 杂项费率4 |
|  Spare1  | string  | xxxx  | 自定义字段1 |
|  Spare2  | string  | xxxx  | 自定义字段2 |
|  Spare3  | string  | xxxx  | 自定义字段3 |
|  Spare4  | string  | xxxx  | 自定义字段4 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 145168089380001,
    "IsometricId": 1,
    "JobId": 1,
    "SpoolNo": "s1",
    "ClientSpoolNo": "s2",
    "SpoolRev": "v1",
    "RevDate": "2022-01-18 00:00:00",
    "RevRef": "版本说明1",
    "SpoolDescription": "管段描述xxx",
    "SpoolSize": "50x20000",
    "PaintSpec": "油漆规范",
    "RevHold": false,
    "MatHold": false,
    "NDTHold": false,
    "IssuedForFabDate": "2022-01-18 00:00:00",
    "CutCompDate": "2022-01-18 00:00:00",
    "FitUpDate": "2022-01-18 00:00:00",
    "WeldCompDate": "2022-01-18 00:00:00",
    "GroundDate": "2022-01-18 00:00:00",
    "DimInspectedDate": "2022-01-18 00:00:00",
    "WeldNDTCompDate": "2022-01-18 00:00:00",
    "SentPaintDate": "2022-01-18 00:00:00",
    "PaintCompDate": "2022-01-18 00:00:00",
    "PackedDate": "2022-01-18 00:00:00",
    "PackageNo": "pn01",
    "TruckNo": "tn01",
    "PunchListedDate": "2022-01-18 00:00:00",
    "SignedOffDate": "2022-01-18 00:00:00",
    "SentSiteDate": "2022-01-18 00:00:00",
    "ReceivedSiteDate": "2022-01-18 00:00:00",
    "DocCompleteDate": "2022-01-18 00:00:00",
    "PriorityId": 1,
    "DeliveryGroupId": 1,
    "BatchGroupId": 1,
    "HTID": 1,
    "HydroRepNo": "h1",
    "HTIDComply": false,
    "PaintRepNo": "p1",
    "HardnessRepNo": "hr1",
    "CurrentLayDownArea": "xxx",
    "ExcludeFromProgress": false,
    "Comment": "xxxx",
    "SelectForBatch": false,
    "CanBuild": false,
    "RequestedNotTested": false,
    "Installed": false,
    "InstalledDate": "2022-01-18 00:00:00",
    "HTIDSite": 1,
    "HTIDSiteComply": false,
    "HTIDLeak": 0,
    "HTIDLeakComply": false,
    "SpoolWeight": 80,
    "SplDrawingRate": 50,
    "IDTagRate": 20.8,
    "MiscRate1": 20.8,
    "MiscRate2": 20.8,
    "MiscRate3": 20.8,
    "MiscRate4": 20.8,
    "Spare1": "xx1",
    "Spare2": "xx2",
    "Spare3": "xx3",
    "Spare4": "xx4"
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
    "msg": "报告号不可为空。",
    "english_msg": "HTReportNo can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
