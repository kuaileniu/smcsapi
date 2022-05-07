---
title: 新增生产批次名称
weight: 100
# GeekdocHidden: true
---

<small>更新日期: 2022-04-08</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-batch-issue-name/add-jtbl-batch-issue-name
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  BatchIssueName  | string  |  xxxx | 生产批次名称 |
|  Comment  | string  | xxxx  | 备注 |

	 
{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "BatchIssueName": "生产批次名称1",
    "Comment": "兄弟们累了的话就休息休息吧"
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
    "msg": "添加失败,生产批次名称重复。",
    "english_msg": "Add failed,duplicate BatchIssueName."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 生产批次名称id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
