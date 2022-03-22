---
title: 编辑发货组的信息
weight: 300
---

<small>更新日期: 2021-12-11</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-delivery-group/edit-jtbl-delivery-group
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 发货组ID |
|  JobId  | number  | xxx  | 项目ID |
|  DeliveryGroupName  | string  | xxx  | 发货组名称,当修改此值时需带上JobId |
|  DeliveryGroupDesc  | string  | xxx  | 发货组描述,当修改此值时需带上JobId|
|  RequiredOnSiteDate  | string  | 2021-11-22 12:13:09 | 到达现场日期 |
|  ModuleStartNumber  | number  | 1 | 模块开始数字 |
|  ModuleEndNumber  |  number | 123 | 模块结束数字 |
|  Note  |  string | xxxx | 备注 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 144099838280001,
    "JobId": 1,
    "DeliveryGroupName": "DeliveryGroupName2",
    "DeliveryGroupDesc": "DeliveryGroupDesc2",
    "RequiredOnSiteDate": "2021-11-22 00:00:00",
    "ModuleStartNumber": 1,
    "ModuleEndNumber": 4,
    "Note": "Note1"
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
    "msg": "发货组名称不可为空。",
    "english_msg": "DeliveryGroupName can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
