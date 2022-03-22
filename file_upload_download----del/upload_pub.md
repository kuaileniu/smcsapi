---
title: 上传文件/图片(非私有)
weight: 100
---

<small>更新日期: 2022-02-24</small>

#### 基本参数
1. url : https://{domain}:{port}/dfs/upload-files/pub
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

采用 form-data 格式上传

|  key   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  files  | File  | 58-2.png  | 通过窗口选中文件(可单选，可多选) |


{{< /tab >}}
{{< tab "样例" >}}

body： 

```form-data
files 58_1.png
files 58_2.png
files 58_3.png 58_4.png
```
{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "成功" >}} 
```json
[
    {
        "Path": "http://127.0.0.1:8015/dfs/dl/pub/212/34/b5f02682d8b69471b70ec415acc9965e_1895.png",
        "OriginName": "58_1.png",
        "Size": 1895
    },
    {
        "Path": "http://127.0.0.1:8015/dfs/dl/pub/212/34/341bdf1f96e41c2da848770b89110909_1241.png",
        "OriginName": "58_2.png",
        "Size": 1241
    }
]
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "操作失败",
    "english_msg": "Failed."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Path  | string  | https://xxxx/xxx.png  | 文件路径  |
|  OriginName  | string  | 58_2.png  | 文件原始名称  |
|  Size  | number  | 1241  | 文件大小，字节数  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
