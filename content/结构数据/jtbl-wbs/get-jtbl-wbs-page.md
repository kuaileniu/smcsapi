---
title: 分页获取工作分解结构信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-03-30</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-wbs/get-jtbl-wbs-page
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
            "Id": 147016911980001,
            "JobId": 1,
            "WBS": "结构2",
            "WBSDescription": "结构1的描述",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2022-03-01 22:58:39",
            "ModifyTime": "2022-03-01 22:58:39"
        },
        {
            "Id": 147016854180001,
            "JobId": 1,
            "WBS": "结构1",
            "WBSDescription": "结构1的描述",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2022-03-01 22:49:01",
            "ModifyTime": "2022-03-01 22:49:01"
        }
    ],
    "count": 2
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
|  Id  | number  | 144095520480001  | 项目工作范围ID |
|  JobId  | number  | 1  | 项目ID |
|  WBS  | string  |  xxxx | 结构 |
|  WBSDescription  | string  | xxx  | 结构描述 |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
