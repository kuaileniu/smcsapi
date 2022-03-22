---
title: 分页获取管段物料信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-03-10</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-spool-material/get-jtbl-spool-material-page
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
            "Id": 147092017580001,
            "IsometricID": 1,
            "SpoolID": 1,
            "JobId": 1,
            "PartNo": "PartNo",
            "StockNo": "StockNo",
            "ComponentID": 1,
            "MaterialCode": "MaterialCode",
            "MaterialDescription": "MaterialDescription",
            "QtyReqd": 1.3,
            "QtyAllocated": 1.4,
            "QtyUsed": 1.2,
            "Length": 1,
            "HasBeenCut": false,
            "EndPrep1": "EndPrep1",
            "EndPrep2": "",
            "TotalQty": 1.1,
            "TotalLength": 1.3,
            "TotalWeight": 1.4,
            "UOM": "UOM",
            "UnitWeight": 1.4,
            "UnitSurfaceArea": 1.9,
            "SerialNumberID": 1,
            "SkipFlag": false,
            "CreatedBy": "15652963646",
            "ModifiedBy": "15652963646",
            "CreateTime": "2022-03-10 15:36:15",
            "ModifyTime": "2022-03-10 15:55:08",
            "IsometricNo": "",
            "SpoolNo": "",
            "ComponentCode": "",
            "ComponentDesc": "",
            "SerialNumber": ""
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
|  Id  | number  | 144095520480001  | 管段物料ID |
|  JobId  | number  | 1  | 项目ID |
|  IsometricID  | number  | 1  | 单线ID |
|  SpoolID  | number  | 1  | 管段ID |
|  PartNo  | string  |  xx | 组件号 |
|  StockNo  | string  | xxx  | 库存编号 |
|  IsometricID  | number  | 1  | 组件ID |
|  MaterialCode  | string  | xxxxxx  | 物料编码 |
|  MaterialDescription  | string  | xxxx  | 物料描述 |
|  QtyReqd  | number  | 1.1  | 所需数量 |
|  QtyAllocated  | number  | 1.1  | 分配数量 |
|  QtyUsed  | number  | 1.1  | 使用数量 |
|  Length  | number  | 1.1  | 长度 |
|  HasBeenCut  | boolean  | true  | 已经下料 |
|  EndPrep1  | string  | xxxxxx  | 端面1 |
|  EndPrep2  | string  | xxxxxx  | 端面2 |
|  TotalQty  | number  | 1.1  | 总数量 |
|  TotalLength  | number  | 1.1  | 总长度 |
|  TotalWeight  | number  | 1.1  | 总重量 |
|  UOM  | string  | xxxxxx  | 计量单位 |
|  UnitWeight  | number  | 1.1  | 单量 |
|  UnitSurfaceArea  | number  | 1.1  | 单表面积 |
|  SerialNumberID  | number  | 1.1  | 物料序列号ID |
|  SkipFlag  | boolean  | true  | 跳过标记 |
|  IsometricNo  | string  | xxx  | 单线号 |
|  SpoolNo  | string  | xxx  | 管段号 |
|  ComponentCode  | string  | xxx  | 组件编码 |
|  ComponentDesc  | string  | xxx  | 组件描述 |
|  SerialNumber  | string  | xxx  | 序列号 |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
