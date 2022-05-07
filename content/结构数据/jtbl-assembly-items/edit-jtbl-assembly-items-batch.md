---
title: 批量编辑构件编码的信息
weight: 202203232027
---

<small>更新日期: 2022-03-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-assembly-items/edit-jtbl-assembly-items-batch
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
- 说明： 与提供的JobId相同的，对数组 Ids 或 AssemblyItemNos 包含的构件编码都进行修改。
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Ids  | 整型数组  | [1,2]  | 构件编码ID列表 |
|  AssemblyItemNos  | string数组  | ["n1","n2"]  | 构件编码数组 |
|  JobId  | number  | 1  | 项目ID |
|  AssemblyID  | number  |  1 | 构件ID |
|  Quantity  | 整数  | 1  | 数量 |
|  IssuedForFabDate  | 日期  | 2022-03-01  | 图纸下发日期 |
|  CutCompDate  | 日期  | 2022-03-01  | 下料日期 |
|  FitUpDate  | 日期  | 2022-03-01  | 组对日期 |
|  WeldCompDate  | 日期  | 2022-03-01  | 焊接完成日期 |
|  GroundDate  | 日期  | 2022-03-01  | 打磨完成日期 |
|  DimInspectedDate  | 日期  | 2022-03-01  | 尺寸检验日期 |
|  SentPaintDate  | 日期  | 2022-03-01  | 发往油漆日期 |
|  PaintCompDate  | 日期  | 2022-03-01  | 油漆完成日期 |
|  PreAssemblyDate  | 日期  | 2022-03-01  | 预拼装日期 |
|  PackedDate  | 日期  | 2022-03-01  | 打包日期 |
|  TruckNo  | string  | xxx  | 转运车号 |
|  BoxNo  | string  | xxx  | 箱号 |
|  PunchListedDate  | 日期  | 2022-03-01  | 核查表日期 |
|  SignedOffDate  | 日期  | 2022-03-01  | 放行日期 |
|  SentSiteDate  | 日期  | 2022-03-01  | 发往现场日期 |
|  DocCompletedDate  | 日期  | 2022-03-01  | 交工文档完成日期 |
|  PaintRepNo  | string  | xxx  | 油漆报告号 |
|  LaydownArea  | string  | xxx  | 放置区域 |
|  PreAssemblyNo  | string  | xxx  | 预拼装号 |
|  PreAssemblyLocation  | string  | xxx  | 预拼装地点 |
|  WorkPackageID  | 整数  | 1  | 工作包Id |
|  PackageNoID  | 整数  | 1  | 包装号Id |
|  BatchIssueID  | 整数  | 1  | 生产批次Id |
|  BarcodePrinted  | bool  | true  | 条码已打印 |
|  ReferToModel  | string  | xxx  | 链接模型 |
|  ExcludeFromProgress  | bool  | true  | 进度统计排除 |
|  Comment  | string  | xxxx  | 备注 |
|  AttachSli  | json数组  | []  | 请看样例 |
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
    "Ids":[1,2],
    "JobId": 1,
    "AssemblyID": 5,
    "Quantity": 10,
    "IssuedForFabDate": "2022-01-11",
    "CutCompDate": "2022-03-01",
    "FitUpDate": "2022-03-01",
    "WeldCompDate": "2022-03-01",
    "GroundDate": "2022-03-01",
    "DimInspectedDate": "2022-03-01",
    "SentPaintDate": "2022-03-01",
    "PaintCompDate": "2022-03-01",
    "PreAssemblyDate": "2022-03-01",
    "PackedDate": "2022-03-01",
    "PackageNoID": 1,
    "TruckNo": "xxx",
    "BoxNo": "xxx",
    "PunchListedDate": "2022-03-01",
    "SignedOffDate": "2022-03-01",
    "SentSiteDate": "2022-03-01",
    "DocCompletedDate": "2022-03-01",
    "PaintRepNo": "11",
    "LaydownArea": "xxx",
    "PreAssemblyNo": "xxx",
    "PreAssemblyLocation": "xxxx",
    "WorkPackageID": 1,
    "BatchIssueID": 1,
    "BarcodePrinted": false,
    "ReferToModel": "xxxx",
    "ExcludeFromProgress": false,
    "Comment": "xxxxx",
    "AttachSli": [
        {
            "OriginName": "清明上河图.jpg",
            "Path": "https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/b5f02682d8b69471b70ec415acc9965e_1895.png",
            "Size": 1895
        },
        {
            "OriginName": "清明上河图.jpg",
            "Path": "https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/341bdf1f96e41c2da848770b89110909_1241.png",
            "Size": 1241
        }
    ],
    "Spare1": "xxx",
    "Spare2": "xxxxx",
    "Spare3": "xxxxxx",
    "Spare4": "xxxxxxxx"
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
    "msg": "1 条数据修改成功。",
    "english_msg": "1 success."
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
