---
title: 为包装号关联构件编码
weight: 600
# geekdocHidden: true
---

<small>更新日期: 2022-04-20</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-packing-list-str/add-assembly-items-for-package-no
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
- 说明： 与提供的JobId相同的，对数组 AssemblyItemsIDS 或 AssemblyItemNos 包含的构件编码都进行关联。
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目id |
|  PackageNoID  | number  | 1  | 包装号id|
|  AssemblyItemsIDS  | number数组  | [1]  | 构件编码id数组|
|  AssemblyItemNos  | string数组  | ["a","b"]  | 构件编码数组|

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "PackageNoID": 1,
    "AssemblyItemsIDS": [
        1,
        147259178080001,
        147264964080001,
        147264966880001,
        147264971580001
    ],
     "AssemblyItemNos":["n1","n2"]
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
    "msg": "成功。",
    "english_msg": "Success."
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "关联失败",
    "english_msg": "Failed."
}



{
    "status": 1,
    "msg": "构件编码[100,a]已经被其它包装号关联。",
    "english_msg": "AssemblyItemNo[100,a] were Associated with other packageNo."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
