---
title: 新增批次组
weight: 100
---

<small>更新日期: 2021-12-23</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-group/add-jtbl-batch-group
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | xxx  | 项目ID |
|  BatchGroup  | string  | xxx  | 批次组名称 |
|  BatchGroupDesc  | string  | xxx  | 批次组描述 |
|  RequiredOnSiteDate  | 日期  | 2022-11-30 | 要求现场交货日期 |
|  ModuleStartNumber  | number  | 1 | 模块开始数字 | 
|  ModuleEndNumber  | number  | 2 | 模块结束数字 | 
|  Note  | string  | xxx | 备注 | 


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchGroup": "批次组名称",
    "BatchGroupDesc": "批次组描述",
    "RequiredOnSiteDate": "2022-11-30",
    "ModuleStartNumber": 4,
    "ModuleEndNumber": 30,
    "Note": "备注"
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
    "msg": "添加失败,批次组名称重复。",
    "english_msg": "Add failed,duplicate AreaName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 批次组id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
