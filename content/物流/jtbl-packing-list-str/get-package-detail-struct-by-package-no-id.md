---
title: 根据包装号ID查询结构包装清单
weight: 800
# geekdocHidden: true
---

<small>更新日期: 2022-04-18</small>

#### 接口说明
1. 若干构件编码id数组中有已经被其它包装号关联的，则不受影响。
#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-packing-list-str/get-package-detail-struct-by-package-no-id
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目id |
|  PackageNoID  | number  | 1  | 包装号id|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
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
    "data": {
        "JobId": 1,
        "JobNo": "项目号1",
        "JobTitle": "项目名称1",
        "Length": 2.1,
        "Width": 2.1,
        "Height": 2.1,
        "Volume": 2.1,
        "ExtraWeight": 2.1,
        "NetWeight": 2.1,
        "GrossWeight": 2.1,
        "WeighOutWeight": 2.1,
        "Comment": "xxxxxxxx",
        "ItemArray": [
            {
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "DrawingNo": "图纸号1",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "10",
                "Quantity": 10
            },
            {
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "DrawingNo": "图纸号1",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "11",
                "Quantity": 10
            },
            {
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "DrawingNo": "图纸号1",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "b",
                "Quantity": 10
            }
        ]
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "项目ID不可为空。",
    "english_msg": "JobId can't be blank."
}

```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  JobNo  | string  | xxx  | 项目号 |
|  JobTitle  | string  | xxx  | 项目名称 |
|  Length  | float  | 1.1  | 长 |
|  Width  | float  | 1.1  | 宽 |
|  Height  | float  | 1.1  | 高 |
|  Volume  | float  | 1.1  | 体积 |
|  ExtraWeight  | float  | 1.1  | 包装重量kg |
|  NetWeight  | float  | 1.1  | 净重kg |
|  GrossWeight  | float  | 1.1  | 过磅重量kg |
|  Comment  | string  | 1.1  | 备注 |
|  ItemArray  | 数组  |   | 见样例 |
|  AssemblyNo  | string  | xxx  | 构件号 |
|  Rev  | string  | xxx  | 版本 |
|  AssemblyItemNo  | string  | xxx  | 构件编码 |
|  Description  | string  | xxx  | 描述 |
|  DrawingNo  | string  | xxx  | 图纸号 |
|  WeightEach  | float  | 1.1  | 单重kg |
|  Quantity  | 整数  | 1  | 数量 |
|  TotalQuantity  | 整数  | 1 | 总数量 |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
