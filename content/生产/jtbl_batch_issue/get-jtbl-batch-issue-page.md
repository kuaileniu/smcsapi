---
title: 分页获取生产批次信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-04-14</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/get-jtbl-batch-issue-page
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
            "Id": 148124437480001,
            "JobId": 1,
            "BatchIssueNo": 3,
            "BatchIssueNameID": 1,
            "Rev": "x",
            "WorkPackageID": 1,
            "BatchIssueDate": "2022-09-11",
            "BatchIssueSent": false,
            "TransmittalDate": "2022-09-11",
            "WorkshopID": 1,
            "SentToEmployeeID": 1,
            "Comment": "兄弟们累了的话就休息休息吧",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2022-04-14 09:39:34",
            "ModifyTime": "2022-04-14 09:39:34",
            "BatchIssueName": "",
            "WorkPackage": "",
            "SubContractorCode": "",
            "SubContractorName": "",
            "WorkshopCode": "Code1",
            "WorkshopName": "WorkshopName1",
            "EmployeeCode": "",
            "EmployeeName": ""
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
||  Id  | number  | 144095520480001  | 生产批次ID |
|  JobId  | number  | 1  | 项目ID |
|  BatchIssueNo  | number  | 1  | 生产批次号 |
|  BatchIssueNameID  | number  | 1  | 生产批次名称ID |
|  Rev  | string  | xx  | 版本 |
|  WorkPackageID  | number  | xx  | 工作包ID |
|  BatchIssueDate  | 日期  | 2022-09-11  | 批次下发日期 |
|  BatchIssueSent  | boolean  | true  | 批次已下发 |
|  TransmittalNo  | string  | true  | 传送单号 |
|  TransmittalDate  | 日期  | 2022-09-11  | 传送日期 |
|  SubcontractorID  | number  | xx  | 员工ID，JtblEmployee的ID |
|  Comment  | string  | xxxx  | 备注 |
|  BatchIssueName  | string  | xxxx  | 生产批次名称 |
|  WorkPackage  | string  | xxxx  | 工作包 |
|  SubContractorCode  | string  | xxxx  | 分包商代码 |
|  SubContractorName  | string  | xxxx  | 分包商名称 |
|  WorkshopID  | number  | 1  | 工厂/车间ID |
|  WorkshopCode  | string  | xxxx  | 工厂/车间代码 |
|  WorkshopName  | string  | xxxx  | 工厂/车间名称 |
|  EmployeeCode  | string  | xxxx  | 员工号 |
|  EmployeeName  | string  | xxxx  | 员工名字 |
	 
 
#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
