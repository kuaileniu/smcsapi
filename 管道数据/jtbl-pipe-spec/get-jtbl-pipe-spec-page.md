---
title: 分页获取管道规范信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-pipe-spec/get-jtbl-pipe-spec-page
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
            "Id": 144233214280001,
            "PipeSpec": "管道规范名称",
            "JobId": 1,
            "MachineSOF": true,
            "NDTPercent": 45,
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2021-12-26 23:49:02",
            "ModifyTime": "2021-12-26 23:49:02"
        }
    ],
    "count": 1
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
|  Id  | number  | 144095520480001  | 管道规范ID |
|  JobId  | number  | xxx  | 项目ID |
|  PipeSpec  | string  | xxx  | 管道规范名称 |
|  MachineSOF  | boolean  | true  | 是机加工SO法兰 |
|  NDTPercent  | 正整数  | 45  | 无损检测比例,例如45%时传45 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
