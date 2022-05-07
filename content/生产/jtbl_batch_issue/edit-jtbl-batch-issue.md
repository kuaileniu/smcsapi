---
title: 编辑生产批次的信息
weight: 300
# GeekdocHidden: true
---

<small>更新日期: 2022-04-08</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue/edit-jtbl-batch-issue
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 生产批次ID |
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

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 148074783080001,
    "JobId": 1,
    "BatchIssueName": "生产批次名称1",
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
    "msg": "修改成功",
    "english_msg": "Success",
  
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
