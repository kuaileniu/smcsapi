---
title: 获取角色信息(分页)
weight: 200
# GeekdocHidden: true
---

<small>更新日期: 2021-11-09</small>

#### 基本参数
1. url : https://{domain}:{port}/api/role/get-role-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | 中石化  | 搜索文本内容 |

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
            "Id": 143083874570001,
            "Code": "R01",
            "Name": "管理员",
            "Description": "拥有至高无上的权力",
            "Internal": true,
            "OrderNum": 1,
            "CreateTime": "2021-11-09 16:59:05",
            "ModifyTime": "2021-11-09 16:59:05"
        },
        {
            "Id": 143083874670001,
            "Code": "R02",
            "Name": "技术员",
            "Description": "技术专员",
            "Internal": true,
            "OrderNum": 2,
            "CreateTime": "2021-11-09 16:59:06",
            "ModifyTime": "2021-11-09 16:59:06"
        }
    ],
    "count": 3
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

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
|  Id  | number  | 是  | 2109300032090001  | 角色的id  |
|  Name  | string  | 是 | 管理员  | 名称  |
|  Description  |  string  | - | 这是个有权利的角色  | 描述  |
|  Code  |  string  | - | xx  | 编码  |
|  Internal  |  boolean  | - | true  | 是内部的  |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
