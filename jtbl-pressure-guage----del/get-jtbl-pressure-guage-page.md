---
title: 分页获取压力表信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-01-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-pressure-guage/get-jtbl-pressure-guage-page
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
            "Id": 145136071280001,
            "JobId": 1,
            "SerialNumber": "s1",
            "PressureRange": "50-80",
            "CalibrationCertNo": "a1",
            "CalibrationExpiry": "2025-01-20 00:00:00",
            "CreatedBy": "156529636",
            "ModifiedBy": "15652963",
            "CreateTime": "2022-01-15 17:58:32",
            "ModifyTime": "2022-01-15 18:06:34"
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
|  Id  | number  | 144095520480001  | 压力表ID |
|  JobId  | number  | 1  | 项目ID |
|  SerialNumber  | string  | xxxx  | 序列号 |
|  PressureRange  | string  | 40-89  | 压力范围 |
|  CalibrationCertNo  | string  | x1111  | 校验证书号 |
|  CalibrationExpiry  | 日期  | 2021-11-22  | 校验到期 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
