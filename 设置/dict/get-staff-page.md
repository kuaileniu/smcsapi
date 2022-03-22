---
title: 获取字典信息(分页)
weight: -9800
# GeekdocHidden: true
---

<small>更新日期: 2021-11-02</small>

#### 基本参数
1. url : https://{domain}:{port}/api/dict/get-dict-page
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  search  | string  | 公司  | 搜索文本内容 |

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/dict/get-dict-page

body： 

```json
{
    "search":"1",
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
            "Id": 2111023232370001,
            "Name": "公司",
            "Description": "",
            "DicType": "type1",
            "DicCode": "S01",
            "OrderNum": 20211102163203,
            "CreateTime": "2021-11-02 16:32:03",
            "ModifyTime": "2021-11-02 16:32:03",
            "Del": false
        },
        {
            "Id": 2111023232470001,
            "Name": "部门",
            "Description": "",
            "DicType": "type2",
            "DicCode": "S02",
            "OrderNum": 20211102163204,
            "CreateTime": "2021-11-02 16:32:04",
            "ModifyTime": "2021-11-02 16:32:04",
            "Del": false
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

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
|  Id  | number  | 是  | 2109300032090001  | 字典的id  |
|  Name  | string  | 是 | 公司  | 公司  |
|  Description  |  string  | - | 这是个大客户  | 描述  |
|  DicType  |  string  | - | type1  | 字典类型  |
|  DicCode  |  string  | - | S01  | 字典编码  |
|  OrderNum  |  number  | - |  xxx |  排序号  |
|  CreateTime  |  string  | - |  2021-10-22 12:28:45 |  创建时间  |
|  ModifyTime  |  string  | - |  2021-10-22 12:28:45 |  修改时间  |
|  Del  |  boolean  | - |  true |  true表示被删除(未启用)  |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
