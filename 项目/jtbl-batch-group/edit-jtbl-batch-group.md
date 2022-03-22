---
title: 编辑批次组的信息
weight: 300
---

<small>更新日期: 2021-12-23</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-group/edit-jtbl-batch-group
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 批次组ID |
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

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 144206674180001,
    "JobId": 1,
    "BatchGroup": "批次组名称",
    "BatchGroupDesc": "批次组描述",
    "RequiredOnSiteDate": "2022-11-30 00:00:00",
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
    "msg": "修改成功",
    "english_msg": "Success",
  
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "批次组名称不可为空。",
    "english_msg": "AreaName can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
