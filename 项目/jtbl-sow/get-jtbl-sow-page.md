---
title: 分页获取项目工作范围信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-02-25</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-sow/get-jtbl-sow-page
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
            "Id": 146216199380001,
            "JobId": 1,
            "SOWNo": 1,
            "SOWDescription": "图纸注意事项图纸注意事项图纸注意事项图纸注意事项图纸注意事项图纸注意事项图纸注意事项",
            "Status": "更新",
            "Date": "2022-02-24 00:00:00",
            "Discipline": "管道",
            "DueDate": "2022-02-23 00:00:00",
            "EstimatedTonnage": 38.9,
            "OutOfScopeWork": "超出范围工作一点点",
            "QADocNotes": "质量文档说明在这里",
            "Clarifications": "澄清说明一下",
            "AttachSli": [
                {
                    "OriginName": "清明上河图.jpg",
                    "Path": "https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/b5f02682d8b69471b70ec415acc9965e_1895.png",
                    "Size": 1895
                },
                {
                    "OriginName": "清明上河图.jpg",
                    "Path": "https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/341bdf1f96e41c2da848770b89110909_1241.png",
                    "Size": 1241
                }
            ],
            "CreatedBy": "15652963646",
            "ModifiedBy": "15652963646",
            "CreateTime": "2022-02-25 00:33:13",
            "ModifyTime": "2022-02-25 00:34:07"
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
|  Id  | number  | 144095520480001  | 项目工作范围ID |
|  JobId  | number  | 1  | 项目ID |
|  SOWNo  | number  | 1  | 序号 |
|  SOWDescription  | string  | xxx  | 描述 图纸，材料，机加，油漆等 |
|  Status  | string  | xxx  | 状态：更新，作废 |
|  Date  | 日期  | 2021-11-22  | 存储状态更改的日期 |
|  Discipline  | string  | xxx  | 专业管道，结构 |
|  DueDate  | 日期  | 2029-11-22  | 到期日 |
|  EstimatedTonnage  | float  | 2029-11-22  | 预估重量 |
|  OutOfScopeWork  | string  | xxx  | 超出范围工作 |
|  QADocNotes  | string  | xxx  | 质量文档说明 |
|  Clarifications  | string  | xxx  | 澄清 |
|  AttachSli  | json数组  | []  | 请看样例 |
|  OriginName  | string  | a.jpg  | 原文件名称 |
|  Path  | string  | https://xx2/34/_1895.png  | 文件路径 |
|  Size  | number  | 1287 | 文件大小(字节) |




#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
