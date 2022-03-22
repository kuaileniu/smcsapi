---
title: 分页获取我的项目信息
weight: 500
# GeekdocHidden: true
---

<small>更新日期: 2021-12-12</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff-job/my-job-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | xxxxx  | 搜索文本内容 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "search":"",
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
            "Id": 144095520480001,
            "JobNo": "项目号1",
            "JobTitle": "项目名称1",
            "ClientId": 1,
            "Active": false,
            "OrderNo": "OrderNo1",
            "ContractNo": "ContractNo1",
            "JobType": "structure",
            "UserId": 123,
            "IsModule": false,
            "IsUniqSpoolNo": true,
            "ImportWholeSpoolNo": true,
            "TemplateAreaId": 4,
            "MasterAreaId": 6,
            "ProjectManagerId": 7,
            "UOM": "公制",
            "ShowClientSpoolNo": false,
            "NDTAutoNumbering": false,
            "MaxWeldRepairCount": 8,
            "WeldUniqueNoPrefix": "xxx1",
            "ShowWeldUniqueNo": true,
            "SiteWelderPrefix": "xx2",
            "WeldUniqueNoPrefixSite": "xx3",
            "JobConsumableCertificatesFolder": "xx4",
            "MaterialCertFolder": "xx5",
            "ShowCertOrigin": false,
            "IssuedForFab": 10,
            "CutComp": 12,
            "FitUpComp": 13,
            "WeldComp": 14,
            "WeldNDTComp": 15,
            "SentPaint": 16,
            "PaintComp": 17,
            "Packed": 18,
            "SentSite": 19,
            "ReceivedSite": 20,
            "MaterialMargin": 8.4,
            "PaintMargin": 8.5,
            "WeldMargin": 8.6,
            "NDTMargin": 8.8,
            "PWHTMargin": 9.1,
            "HydroTestMargin": 9.2,
            "SOFMachiningMargin": 9.3,
            "GraceDaysRecieved": 3,
            "GraceDaysNotRecieved": 4,
            "NDTReportType": "b1",
            "SpoolBarcodeType": "b2",
            "BarcodePrinter": "b3",
            "PShotTagMessage": "b4",
            "Currency": 1,
            "Note": "备注备注备注备注备注",
            "CreateTime": "2021-12-11 01:20:04",
            "ModifyTime": "2021-12-11 01:20:04",
            "OrganisationName": "武当山02"
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
|  Id  | number  | 144095520480001  | 项目ID |
|  JobNo  | string  | xxx  | 项目号 |
|  JobTitle  | string  | xxx  | 项目名称 |
|  ClientId  | number  | 1  | 客户id |
|  Active  | boolean  | true | 激活 |
|  OrderNo  | string  | xxx | 订单号 |
|  ContractNo  | string  | xxx | 合同号 |
|  JobType  | string  | xxx | 项目类型:pipeline代表管道，structure代表结构，other其它或多专业 |
|  UserId  | number  | 123 | 用户ID |
|  IsModule  | boolean  | false 或 true | 是模块项目 |
|  IsUniqSpoolNo  | boolean  | false 或 true | 是管段号唯一 |
|  ImportWholeSpoolNo  | boolean  | false 或 true | 是导入整个管段号 |
|  TemplateAreaId  | number  | 123 | 模板区域ID |
|  MasterAreaId  | number  | 123 | 复制区域ID |
|  ProjectManagerId  | number  | 123 | 项目经理ID |
|  UOM  | string  | xxx | 单位 |
|  ShowClientSpoolNo  | boolean  | false 或 true | 显示客户管段号 |
|  NDTAutoNumbering  | boolean  | false 或 true | 探伤报告自动编号 |
|  MaxWeldRepairCount  | number  | 123 | 焊接返修最大次数 |
|  WeldUniqueNoPrefix  | string  | xxx | 焊接返修最大次数 |
|  ShowWeldUniqueNo  | boolean  | false 或 true | 显示焊缝唯一号 |
|  SiteWelderPrefix  | string  | xxxx | 现场焊工前缀 |
|  WeldUniqueNoPrefixSite  | string  | xxxx | 现场焊缝唯一号前缀 |
|  JobConsumableCertificatesFolder  | string  | xxxx | 项目耗材证书文件夹 |
|  MaterialCertFolder  | string  | xxxx | 材质证书文件夹 |
|  ShowCertOrigin  | boolean  | false 或 true | 显示原产地 |
|  IssuedForFab  | 正整数  | 45 | 图纸下发百分比,例如45%时向服务器端提交45 |
|  CutComp  | 正整数  | 45 | 下料完成百分比,例如45%时向服务器端提交45 |
|  FitUpComp  | 正整数  | 45 | 组对完成百分比,例如45%时向服务器端提交45 |
|  WeldComp  | 正整数  | 45 | 焊接完成百分比,例如45%时向服务器端提交45 |
|  WeldNDTComp  | 正整数  | 45 | 探伤完成百分比,例如45%时向服务器端提交45 |
|  SentPaint  | 正整数  | 45 | 发往油漆百分比,例如45%时向服务器端提交45 |
|  PaintComp  | 正整数  | 45 | 油漆完成百分比,例如45%时向服务器端提交45 |
|  Packed  | 正整数  | 45 | 打包完成百分比,例如45%时向服务器端提交45 |
|  SentSite  | 正整数  | 45 | 发往现场百分比,例如45%时向服务器端提交45 |
|  ReceivedSite  | 正整数  | 45 | 现场收货百分比,例如45%时向服务器端提交45 |
|  MaterialMargin  | float  | 3.2 | 材料利润 |
|  PaintMargin  | float  | 3.2 | 油漆利润 |
|  WeldMargin  | float  | 3.2 | 焊接利润 |
|  NDTMargin  | float  | 3.2 | 探伤利润 |
|  PWHTMargin  | float  | 3.2 | 热处理利润 |
|  HydroTestMargin  | float  | 3.2 | 水压测试利润 |
|  SOFMachiningMargin  | float  | 3.2 | 法兰加工利润 |
|  GraceDaysRecieved  |  正整数 | 2 | 宽限天数-接收的 |
|  GraceDaysNotRecieved  |  正整数 | 2 | 宽限天数-未接收的 |
|  NDTReportType  |  string | xxxx | 探伤报告类型 |
|  SpoolBarcodeType  |  string | xxxx | 管段条码类型 |
|  BarcodePrinter  |  string | xxxx | 条码打印机 |
|  PShotTagMessage  |  string | xxxx | 惩罚标签信息 |
|  Currency  |  string | xxxx | 货币 |
|  Note  |  string | xxxx | 备注 |
|  OrganisationName  |  string | 武当山0 | 业主客户名称 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
