---
title: 分页获取未分配包装号的构件编码信息
weight: 500
# geekdocHidden: true
---

<small>更新日期: 2022-04-04</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-packing-list-str/get-jtbl-assembly-items-page-not-have-this-package-no
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | xxxxx  | 搜索文本内容 |
|  JobId  | number  | 1  | 项目id |
|  PackageNoID  | number  | 1  | 包装号id （暂时需要传此值以备产品功能改动）|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "search": "",
    "page": 1,
    "limit": 3,
    "JobId": 1,
    "PackageNoID": 1 
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
            "Id": 147264964080001,
            "JobId": 1,
            "AssemblyID": 1,
            "AssemblyItemNo": "b",
            "IssuedForFabDate": "2022-03-01",
            "CutCompDate": "2022-03-01",
            "FitUpDate": "2022-03-01",
            "WeldCompDate": "2022-03-01",
            "GroundDate": "2022-03-01",
            "DimInspectedDate": "2022-03-01",
            "SentPaintDate": "2022-03-01",
            "PaintCompDate": "2022-03-01",
            "PreAssemblyDate": "2022-03-01",
            "PackedDate": "2022-03-01",
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
            "Spare4": "xxxxxxxx",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2022-03-30 16:00:40",
            "ModifyTime": "2022-03-30 16:00:40",
            "PackageNo": "NO1",
            "AssemblyNo": "1010-1200-PL0009",
            "Rev": "v1",
            "Description": "构件号描述",
            "WeightEach": 5.1,
            "Quantity": 10,
            "TotalReqdQty": 1,
            "WeightTotal": 0
        }
    ],
    "count": 5
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
|  Id  | number  | 144095520480001  | 构件编码ID |
|  JobId  | number  | 1  | 项目ID |
|  AssemblyID  | number  |  1 | 构件ID |
|  Rev  | string  | xxx  | 版本 |
|  AssemblyItemNo  | string  | xxx  | 构件编码 |
|  Description  | string  | xxxxxx  | 描述 |
|  WeightEach  | float  | xxxx  | 单重kg |
|  MainProfile  | string  | xxx  | 主材 |
|  PaintSpec  | string  | xxx  | 油漆规范 |
|  Quantity  | 整数  | 1  | 数量 |
|  TotalReqdQty  | 整数  | 1  | 总数量 |
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
|  AssemblyNo  | string  | xxxx  | 构件号 |
|  JobNo  | string  | xxxx  | 项目号 |
|  JobTitle  | string  | xxxx  | 项目名称 |
|  WorkPackage  | string  | xxxx  | 工作包 |
|  BatchIssueNo  | string  | xxxx  | 生产批次号 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
