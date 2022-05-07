---
title: 编辑组件的信息
weight: 300
---

<small>更新日期: 2022-03-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-component/edit-jtbl-component
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 组件ID |
|  JobId  | number  | 1  | 项目ID |
|  ComponentCode  | string  |  xx | 组件编码 |
|  ComponentDesc  | string  | xxx  | 组件描述 |
|  ComponentCategory  | string  | xxx  | 组件类别 |
|  MaterialCode  | string  | xxxxxx  | 物料编码 |
|  MaterialDescription  | string  | xxxx  | 物料描述 |
|  UMI  | string  | xxx  |  |
|  PresRequired  | boolean  | true  |  |
|  PresDaysPeriod  | 整数  | 1  |  |
|  IsUniqStock  | boolean  | true  |  |
|  UsedForMatReceipt  | boolean  | true  |  应用于收料|
|  Comment  | string  | xxxx  | 备注 |
|  Spare1  | string  | xxxx  | 自定义字段1 |
|  Spare2  | string  | xxxx  | 自定义字段2 |
|  Spare3  | string  | xxxx  | 自定义字段3 |
|  Spare4  | string  | xxxx  | 自定义字段4 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
        {
            "Id": 147085093780001,
            "JobId": 1,
            "ComponentCode": "ComponentCode",
            "ComponentDesc": "ComponentDesc",
            "ComponentCategory": "ComponentCategory",
            "MaterialCode": "MaterialCode",
            "MaterialDescription": "MaterialDescription",
            "UMI": "UMI",
            "PresRequired": false,
            "PresDaysPeriod": 1,
            "IsUniqStock": true,
            "UsedForMatReceipt": true,
            "Comment": "Comment",
            "Spare1": "Spare1",
            "Spare2": "Spare2",
            "Spare3": "Spare3",
            "Spare4": "Spare4",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2022-03-09 20:22:17",
            "ModifyTime": "2022-03-09 20:22:17"
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
