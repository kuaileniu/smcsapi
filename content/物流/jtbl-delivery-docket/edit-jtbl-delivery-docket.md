---
title: 编辑发货单信息
weight: 300
---

<small>更新日期: 2022-04-01</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-delivery-docket/edit-jtbl-delivery-docket
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 发货单ID |
|  JobId  | number  | 1  | 项目ID |
|  DeliveryDocketNo  | string  |  1xxx | 发货单号 |
|  OrderNo  | string  |  1xxx | 订单号 |
|  Consignee  | string  |  1xxx | 收货人 |
|  Fabricator  | string  |  1xxx | 制造商 |
|  Supplier  | string  |  1xxx | 供应商 |
|  SentSiteDate  | 日期  |  2022-03-01 | 发往现场日期 |
|  NetWeight  | float  |  1.1 | 净重kg |
|  GrossWeight  | float  |  1.2 | 总重量kg,毛重 |
|  WeighOutWeight  | float  |  1.2 | 过d重量kg |
|  Volume  | float  |  1.2 | 体积(m³) |
|  Comment  | string  |  xxxxx | 备注 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 148012433980001,
    "JobId": 1,
    "DeliveryDocketNo": "d1",
    "OrderNo": "o1",
    "Consignee": "张三",
    "Fabricator": "里斯",
    "Supplier": "问问",
    "SentSiteDate": "2022-04-01",
    "NetWeight": 10.1,
    "GrossWeight": 4.9,
    "WeighOutWeight": 3.3,
    "Volume": 40.99,
    "Comment": "xxxxx"
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
    "msg": "修改失败",
    "english_msg": "Failed."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
