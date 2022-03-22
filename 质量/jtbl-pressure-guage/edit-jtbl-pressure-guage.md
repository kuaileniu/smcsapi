---
title: 编辑压力表的信息
weight: 300
---

<small>更新日期: 2022-01-15</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-pressure-guage/edit-jtbl-pressure-guage
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 压力表ID |
|  JobId  | number  | 1  | 项目ID |
|  SerialNumber  | string  | xxxx  | 序列号 |
|  PressureRange  | string  | 40-89  | 压力范围 |
|  CalibrationCertNo  | string  | x1111  | 校验证书号 |
|  CalibrationExpiry  | 日期  | 2021-11-22  | 校验到期 |
 
{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 145136071280001,
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
    "msg": "修改成功",
    "english_msg": "Success",
  
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "压力名称不可为空。",
    "english_msg": "LineName can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
