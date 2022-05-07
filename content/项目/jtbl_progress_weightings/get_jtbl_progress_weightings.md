---
title: 获取进度权重信息
weight: 100
---

<small>更新日期: 2022-01-13</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl_progress_weightings/get_jtbl_progress_weightings
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  JobId  | number  | 1  | 项目ID |

{{< /tab >}}
{{< tab "样例" >}}


body： 

```json
{
    "JobId": 1
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
    "data": {
        "JobId": 1,
        "IssuedForFab": 20.6,
        "CutComp": 3,
        "FitUpComp": 0.4,
        "WeldComp": 5,
        "Ground": 6,
        "DimInspected": 0.7,
        "WeldNDTComp": 0.8,
        "SentPaint": 9,
        "PaintComp": 10,
        "PreAssemblied":0.34,
        "Packed": 11,
        "PunchListed": 12,
        "SignedOff": 13,
        "SentSite": 14,
        "DocComplete": 15,
        "CreatedBy": "15652963",
        "ModifiedBy": "1565296",
        "CreateTime": "2022-01-13 22:10:33",
        "ModifyTime": "2022-01-13 23:17:32"
    }
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "JobId 不可为空",
    "english_msg": "JobId is incorrect"
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
|  JobId  | number  | 1  | 项目id |
|  IssuedForFab  | 浮点数  | 0.34  | 图纸下发 |
|  CutComp  | 浮点数  | 0.34  | 下料完成 |
|  FitUpComp  | 浮点数  | 0.34  | 组对完成 |
|  WeldComp  | 浮点数  | 0.34  | 焊接完成 |
|  Ground  | 浮点数  | 0.34  | 打磨完成 |
|  DimInspected  | 浮点数  | 0.34  | 尺寸检验 |
|  WeldNDTComp  | 浮点数  | 0.34  | 探伤完成 |
|  SentPaint  | 浮点数  | 0.34  | 发往油漆 |
|  PaintComp  | 浮点数  | 0.34  | 油漆完成 |
|  PreAssemblied  | 浮点数  | 0.34  | 预拼装完成 |
|  Packed  | 浮点数  | 0.34  | 打包完成 |
|  PunchListed  | 浮点数  | 0.34  | 核查表完成 |
|  SignedOff  | 浮点数  | 0.34  | 签署放行 |
|  SentSite  | 浮点数  | 0.34  | 发往现场 |
|  DocComplete  | 浮点数  | 0.34  | 交工文档完成 | 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
