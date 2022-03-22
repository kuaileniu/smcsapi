---
title: 批量编辑构件的信息
weight: 202203222324
---

<small>更新日期: 2022-03-22</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-assembly/edit-jtbl-assembly-batch
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  Description  | string  | xxx  | 构件号描述 |
|  DrawingNo  | string  | xxx  | 图纸号 |
|  Rev  | string  | xxx  | 版本 |
|  RevDate  | 日期  | 2022-03-01  | 版本日期 |
|  RevRef  | string  | xxxx  | 版本说明 |
|  Quantity  | 整数  | 1  | 数量 |
|  WorkPackageID  | 整数  | 1  | 工作包Id |
|  BatchIssueID  | 整数  | 1  | 生产批次Id |
|  BatchIssueDate  | 日期  | 2022-03-01  | 批次下发日期 |
|  TransmittalNo  | string  | xxxx  | 传送单号 |
|  TransmittalDate  | 日期  | 2022-03-01  | 传送日期 |
|  AreaID  | 整数  | 1  | 分区Id |
|  WBSID  | 整数  | 1  | 工作分解结构Id |
|  PriorityID  | 整数  | 1  | 优先级Id |
|  DeliveryGroupID  | 整数  | 1  | 发货组Id |
|  BatchGroupID  | 整数  | 1  | 批次组Id |
|  FabCategory  | string  | xxxx  | 加工类别 |
|  WeightEach  | float  | 1.3  | 单重kg |
|  WeightTotal  | float  | 1.3  | 总重kg |
|  MainProfile  | string  | xxxx  | 主材 |
|  MaterialGrade  | string  | xxxx  | 材质 |
|  PaintSpec  | string  | xxxx  | 油漆规范 |
|  GeneralArrangement  | string  | xxxx  | 布置图 |
|  CostCode  | string  | xxxx  | 成本代码 |
|  LengthEach  | float  | 1.3  | 长 |
|  WidthEach  | float  | 1.3  | 宽 |
|  HeightEach  | float  | 1.3  | 高 |
|  AreaEach  | float  | 1.3  | 面积m2 |
|  VolumeEach  | float  | 1.3  | 体积m3 |
|  UOM  | string  | xxxx  | 计量单位 |
|  WeightPerMetre  | float  | 1.3  | 每米重量 |
|  QtyIssued  | float  | 1.3  | 图纸下发数量 |
|  QtyProcessed  | float  | 1.3  | 下料数量 |
|  QtyFitUp  | float  | 1.3  | 组对数量 |
|  QtyWelded  | float  | 1.3  | 焊接数量 |
|  QtyGround  | float  | 1.3  | 打磨数量 |
|  QtyDimInspected  | float  | 1.3  | 尺寸检验数量 |
|  QtySentToSurfaceTrmt  | float  | 1.3  | 发往表面处理数量 |
|  QtyPainted  | float  | 1.3  | 油漆完成数量 |
|  QtyPreAssemblied  | float  | 1.3  | 拼装完成数量 |
|  QtyPacked  | float  | 1.3  | 打包数量 |
|  QtyPunchListed  | float  | 1.3  | 核查表数量 |
|  QtySignedOff  | float  | 1.3  | 放行数量 |
|  QtySentToSite  | float  | 1.3  | 发往现场数量 |
|  QtyDocCompleted  | float  | 1.3  | 交工文档完成数量 |
|  Schedule  | string  | xxx  | 计划表 |
|  PaintRepNo  | string  | xxxx  | 油漆报告号 |
|  LaydownArea  | string  | xxxx  | 放置区域 |
|  PreAssemblyNo  | string  | xxxx  | 预拼装号 |
|  PreAssemblyLocation  | string  | xxxx  | 预拼装地点 |
|  NDTRequired  | boolean  | false  | 需探伤 |
|  Hold  | boolean  | false  | 暂停 |
|  HoldDate  | 日期  | 2022-03-01  | 暂停日期 |
|  HoldRef  | string  | xxx  | 暂停说明 |
|  ReleaseDate  | 日期  | 2022-03-01  | 释放日期 |
|  ReleaseRef  | string  | xxx  | 释放说明 |
|  ReferToTQ  | string  | xxx  | 技术询问 |
|  FreeIssueItem  | boolean  | false  | 甲供项 |
|  ExcludeFromProgress  | boolean  | false  | 进度统计排除 |
|  Comment  | string  | xxxx  | 备注 |
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
    "JobId": 1,
    "Description": "构件号描述",
    "DrawingNo": "图纸号1",
    "Rev": "版本v1",
    "RevDate": "2022-03-01",
    "RevRef": "版本说明",
    "Quantity": 1,
    "WorkPackageID": 1,
    "BatchIssueID": 1,
    "BatchIssueDate": "2022-03-01",
    "TransmittalNo": "传送单号1",
    "TransmittalDate": "2022-03-01",
    "AreaID": 1,
    "WBSID": 1,
    "PriorityID": 1,
    "DeliveryGroupID": 1,
    "BatchGroupID": 1,
    "FabCategory": "加工类别",
    "WeightEach": 5.1,
    "WeightTotal": 5.1,
    "MainProfile": "主材",
    "MaterialGrade": "材质",
    "PaintSpec": "油漆规范",
    "GeneralArrangement": "布置图",
    "CostCode": "成本代码1",
    "LengthEach": 1.1,
    "WidthEach": 2.1,
    "HeightEach": 3.1,
    "AreaEach": 4.1,
    "VolumeEach": 5.4,
    "UOM": "计量单位",
    "WeightPerMetre": 3.4,
    "QtyIssued": 1.1,
    "QtyProcessed": 1.1,
    "QtyFitUp": 1.1,
    "QtyWelded": 1.1,
    "QtyGround": 1.1,
    "QtyDimInspected": 1.1,
    "QtySentToSurfaceTrmt": 1.1,
    "QtyPainted": 1.1,
    "QtyPreAssemblied": 1.1,
    "QtyPacked": 1.1,
    "QtyPunchListed": 1.1,
    "QtySignedOff": 1.1,
    "QtySentToSite": 1.1,
    "QtyDocCompleted": 1.1,
    "Schedule": "计划表",
    "PaintRepNo": "油漆报告号",
    "LaydownArea": "放置区域",
    "PreAssemblyNo": "预拼装号",
    "PreAssemblyLocation": "预拼装地点",
    "NDTRequired": false,
    "Hold": false,
    "HoldDate": "2022-03-01",
    "HoldRef": "暂停说明",
    "ReleaseDate": "2022-03-01",
    "ReleaseRef": "释放说明",
    "ReferToTQ": "技术询问",
    "FreeIssueItem": false,
    "ExcludeFromProgress": false,
    "Comment": "",
    "Spare1": "",
    "Spare2": "",
    "Spare3": "",
    "Spare4": ""
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
    "msg": "xxx不可为空。",
    "english_msg": "xxx can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
