---
title: 根据生产批次查询构件清单(生产批次报告)
weight: 900
# geekdocHidden: true
---

<small>更新日期: 2022-04-24</small>

#### 接口说明
1. 若干构件编码id数组中有已经被其它包装号关联的，则不受影响。
#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/get-struct-by-batch-issue
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目id |
|  BatchIssueID  | number  | 1  | 生产批次id|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchIssueID": 1
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
        "JobNo": "项目号1",
        "JobTitle": "项目名称1",
        "WorkPackage": "包1xxxx",
        "SubContractorCode": "分包商代码1",
        "SubContractorName": "分包商名称(描述)1",
        "BatchIssueNo": 2,
        "BatchIssueName": "生产批次名称1",
        "BatchIssueDate": "2022-09-11",
        "BatchIssueComment": "兄弟们累了的话就休息休息吧",
        "WorkshopCode": "Code1",
        "WorkshopName": "WorkshopName1",
        "EmployeeCode": "a",
        "EmployeeName": "b",
        "ItemStrArray": [
            {
                "AssemblyNo": "1010-1200-B0002",
                "Description": "构件号描述",
                "DrawingNo": "图纸号1",
                "Rev": "v1",
                "WeightEach": 5.1,
                "WeightTotal": 4.1,
                "Quantity": 1
            },
            {
                "AssemblyNo": "1010-1200-PL0009",
                "Description": "构件号描述",
                "DrawingNo": "图纸号1",
                "Rev": "v1",
                "WeightEach": 5.1,
                "WeightTotal": 4.1,
                "Quantity": 1
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
|  JobNo  | string  | xxx  | 项目号 |
|  JobTitle  | string  | xxx  | 项目名称 |
|  WorkPackage  | string  | xxx  | 工作包 |
|  SubContractorCode  | string  | xxx  | 分包商代码 |
|  SubContractorName  | string  | xxx  | 分包商名称(描述) |
|  BatchIssueNo  | int64  | xxx  | 生产批次号 |
|  BatchIssueName  | string  | xxx  | 生产批次名称 |
|  BatchIssueDate  | 日期  | 2022-09-11  | 批次下发日期 |
|  BatchIssueComment  | string  | xxx  | 备注(生产批次的备注) |
|  WorkshopCode  | string  | xxx  | 工厂/车间代码 |
|  WorkshopName  | string  | xxx  | 工厂/车间名称 |
|  EmployeeCode  | string  | xxx  | 员工代码 |
|  EmployeeName  | string  | xxx  | 员工名字 |
|  ItemStrSli  | 结构数组  |   | 见样例 |
|  AssemblyNo  | string  | xxx  | 构件号 |
|  Rev  | string  | xxx  | 版本 |
|  AssemblyItemNo  | string  | xxx  | 构件编码 |
|  Description  | string  | xxx  | 描述 |
|  DrawingNo  | string  | xxx  | 图纸号 |
|  WeightEach  | float  | 1.1  | 单重kg |
|  WeightTotal  | float  | 1.1  | 总重kg |
|  Quantity  | 整数  | 1  | 数量 |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
