---
title: 新增压力表
weight: 100
---

<small>更新日期: 2022-01-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-pressure-guage/add-jtbl-pressure-guage
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |
|  SerialNumber  | string  | xxxx  | 序列号 |
|  PressureRange  | string  | 40-89  | 压力范围 |
|  CalibrationCertNo  | string  | x1111  | 校验证书号 |
|  CalibrationExpiry  | 日期  | 2021-11-22  | 校验到期 |

 

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1,
    "SerialNumber": "s1",
    "PressureRange": "50-80",
    "CalibrationCertNo": "a1",
    "CalibrationExpiry": "2025-01-20"
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
        "Id": 144230022080001
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "添加失败,压力名称重复。",
    "english_msg": "Add failed,duplicate PipeSpec."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  Id  | number  | 2109300032090001  | 压力id  |

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
