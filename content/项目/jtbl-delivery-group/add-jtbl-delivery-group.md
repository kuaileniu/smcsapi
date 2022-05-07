---
title: 新增发货组
weight: 100
---

<small>更新日期: 2021-12-11</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-delivery-group/add-jtbl-delivery-group
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | xxx  | 项目ID |
|  DeliveryGroupName  | string  | xxx  | 发货组名称 |
|  DeliveryGroupDesc  | string  | xxx  | 发货组描述 |
|  RequiredOnSiteDate  | string  | 2021-11-22 12:13:09 | 到达现场日期 |
|  ModuleStartNumber  | number  | 1 | 模块开始数字 |
|  ModuleEndNumber  |  number | 123 | 模块结束数字 |
|  Note  |  string | xxxx | 备注 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "DeliveryGroupName": "DeliveryGroupName2",
    "DeliveryGroupDesc": "DeliveryGroupDesc2",
    "RequiredOnSiteDate": "2021-11-22",
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
    "msg": "添加成功",
    "english_msg": "Add success",
    "data": {
        "Id": 144099490310001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,分区名称重复。",
    "english_msg": "Add failed,duplicate AreaName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 分区id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
