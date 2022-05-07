---
title: 新增包装清单(结构)
weight: 100
geekdocHidden: true
---

<small>更新日期: 2022-04-01</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-packing-list-str/add-jtbl-packing-list-str
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  PackageNoID  | number  |  1 | 包装号ID |
|  MaterialID  | number  |  1 | 构件编码ID | 

	 
{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "PackageNoID": 1,
    "AssemblyItemsID": 1
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
    "msg": "添加失败,包装清单(结构)重复。",
    "english_msg": "Add failed,duplicate PackageNo."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 包装清单(结构)id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
