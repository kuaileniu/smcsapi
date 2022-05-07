---
title: 分页获取设备区域类型信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/plant-area-type/get-plant-area-type-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | xxxxx  | 搜索文本内容 |


{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "search":"",
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
            "Id": 1,
            "ChineseName": "整体复制",
            "EnglishName": "Copy Overall"
        },
        {
            "Id": 2,
            "ChineseName": "单独复制",
            "EnglishName": "Copy Separately"
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
|  Id  | number  | xxx  | 设备区域类型ID |
|  ChineseName  | string  | xxx  | 中文名称 |
|  EnglishName  | string  | xxx  | 英文名称 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
