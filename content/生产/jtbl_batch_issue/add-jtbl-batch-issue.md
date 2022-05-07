---
title: 新增生产批次
weight: 100
# GeekdocHidden: true
---

<small>更新日期: 2022-04-08</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/add-jtbl-batch-issue
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  BatchIssueNameID  | number  | 1  | 生产批次名称ID |
|  Rev  | string  | xx  | 版本 |
|  WorkPackageID  | number  | xx  | 工作包ID |
|  BatchIssueDate  | 日期  | 2022-09-11  | 批次下发日期 |
|  BatchIssueSent  | boolean  | true  | 批次已下发 |
|  TransmittalNo  | string  | true  | 传送单号 |
|  TransmittalDate  | 日期  | 2022-09-11  | 传送日期 |
|  SubcontractorID  | number  | xx  | 员工ID，JtblEmployee的ID |
|  Comment  | string  | xxxx  | 备注 |
|  WorkshopID  | number  | xx  | 工厂/车间ID |


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchIssueNo": 1,
    "BatchIssueNameID": 1,
    "Rev": "x",
    "WorkPackageID": 1,
    "BatchIssueDate": "2022-09-11",
    "BatchIssueSent": false,
    "TransmittalDate": "2022-09-11",
    "SentToEmployeeID": 1,
    "Comment": "兄弟们累了的话就休息休息吧"
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
    "msg": "添加成功",
    "english_msg": "Add success",
    "data": {
        "Id": 147016911980001
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

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 生产批次名称id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
