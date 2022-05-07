---
title: 根据发货单查询包装清单(结构，管道，原材料)
weight: 500
# GeekdocHidden: true
---

<small>更新日期: 2022-04-22</small>


#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-delivery-docket/get-package-str-by-delivery-docket
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
- 查询 与给定的包装id相同或与给定的包装号相同的包装清单
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  | 
|  JobId  | number  | 1  | 项目id |
|  DeliveryDocketId  | number  | 1  | 包装id |
|  DeliveryDocketNo  | string  | xxx  | 包装号 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    
    "JobId": 1,
    "DeliveryDocketId": 1,
    "DeliveryDocketNo": "d1"
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
        "DeliveryDocketId": 1,
        "DeliveryDocketNo": "d1",
        "ItemStrArray": [
            {
                "PackageNo": "NO1",
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "10",
                "Quantity": 10
            },
            {
                "PackageNo": "NO1",
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "100",
                "Quantity": 99910
            },
            {
                "PackageNo": "NO1",
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "11",
                "Quantity": 99910
            },
            {
                "PackageNo": "NO1",
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "Rev": "v1",
                "WeightEach": 5.1,
                "TotalQuantity": 1,
                "AssemblyItemNo": "b",
                "Quantity": 99910
            }
        ],
        "Comment": "后面可能添加包装清单（管道）、包装清单（原材料）到此对象中"
    }
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
|  JobId  | number  | 1  | 项目ID |
|  JobNo  | string  | xxx  | 项目号 |
|  JobTitle  | string  | xxx  | 项目名称 |
|  DeliveryDocketId  | number  |  1 | 发货单Id |
|  DeliveryDocketNo  | string  |  1xxx | 发货单号 |
|  ItemStrArray  | 数组(包装清单（结构）的数据)  |   | 见样例 |
|  AssemblyNo  | string  | xxx  | 构件号 |
|  Rev  | string  | xxx  | 版本 |
|  AssemblyItemNo  | string  | xxx  | 构件编码 |
|  Description  | string  | xxx  | 描述 |
|  WeightEach  | float  | 1.1  | 单重kg |
|  Quantity  | 整数  | 1  | 数量 |
|  TotalQuantity  | 整数  | 1 | 总数量 |
|  Comment  | string  |  xxxxx | 备注 | 

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
