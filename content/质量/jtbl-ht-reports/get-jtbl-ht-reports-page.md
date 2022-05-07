---
title: 分页获取试压报告信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-01-18</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-ht-reports/get-jtbl-ht-reports-page
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
            "Id": 145163889080001,
            "JobId": 1,
            "HTReportNo": "ccc1",
            "TestCompanyCode": "c1",
            "PreparedBy": "张三",
            "TestDate": "2022-01-18 00:00:00",
            "SpecificationNo": "n1",
            "SystemQualityPackNo": "p1",
            "Location": "河北秦皇岛",
            "TestIDNo": "1",
            "TestDuration": "60 Minutes",
            "PressureGuageId1": 1,
            "PressureGuageId2": 20,
            "PressureGuageId3": 30,
            "PressureGuageSerNo1": "1-1",
            "PressureGuageSerNo2": "2-2",
            "PressureGuageSerNo3": "3-3",
            "PressureRange1": "10-20",
            "PressureRange2": "20-30",
            "PressureRange3": "30-40",
            "CalibrationCertNo1": "cc1",
            "CalibrationCertNo2": "cc2",
            "CalibrationCertNo3": "cc3",
            "CalibrationExpiry1": "2025-11-12 20:23:43",
            "CalibrationExpiry2": "2025-11-13 20:23:43",
            "CalibrationExpiry3": "2025-11-14 20:23:43",
            "SiteCode": "sc1",
            "DesignPressure": "50M",
            "TestPressure": "51M",
            "AmbientTemp": "001",
            "TestMedium": "11",
            "IsLeakTest": true,
            "Comment": "备注哦",
            "CreatedBy": "15652963646",
            "ModifiedBy": "15652963646",
            "CreateTime": "2022-01-18 23:14:50",
            "ModifyTime": "2022-01-18 23:40:00"
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
|  Id  | number  | 144095520480001  | 试压报告ID |
|  JobId  | number  | 1  | 项目ID |
|  HTReportNo  | string  | xxxx  | 报告号 |
|  TestCompanyCode  | string  | xxx  | 测试公司代码 |
|  PreparedBy  | string  | x1111  | 编制者 |
|  TestDate  | 日期  | 2021-11-22  | 测试日期 |
|  SpecificationNo  | string  | xxx  | 规范号 |
|  SystemQualityPackNo  | string  | xxx  | 系统质量包编号 |
|  Location  | string  | xxx  | 测试地点 |
|  TestIDNo  | string  | xxx  | 测试ID号码 |
|  TestDuration  | string  | 30 Minutes  | 测试时间 |
|  PressureGuageId1  | number  | 1  | 压力表1的ID |
|  PressureGuageId2  | number  | 2  | 压力表2的ID |
|  PressureGuageId3  | number  | 3  | 压力表3的ID |
|  PressureGuageSerNo1  | string  | xxxx  | 压力表序列号1 |
|  PressureGuageSerNo2  | string  | xxxx  | 压力表序列号2 |
|  PressureGuageSerNo3  | string  | xxxx  | 压力表序列号3 |
|  PressureRange1  | string  | xxxx  | 压力范围1 |
|  PressureRange2  | string  | xxxx  | 压力范围2 |
|  PressureRange3  | string  | xxxx  | 压力范围3 |
|  CalibrationCertNo1  | string  | xxxx  | 校验证书号1 |
|  CalibrationCertNo2  | string  | xxxx  | 校验证书号2 |
|  CalibrationCertNo3  | string  | xxxx  | 校验证书号3 |
|  CalibrationExpiry1  | 日期  | 2021-11-22 11:22:33  | 校验到期1 |
|  CalibrationExpiry2  | 日期  | 2021-11-22 11:22:33  | 校验到期2 |
|  CalibrationExpiry3  | 日期  | 2021-11-22 11:22:33  | 校验到期3 |
|  SiteCode  | string  | sc1  | 现场代码 |
|  DesignPressure  | string  | 50 MP  | 设计压力 |
|  TestPressure  | string  | 50 MP  | 测试压力 |
|  AmbientTemp  | string  | 50 c  | 环境温度 |
|  TestMedium  | string  | xxx  | 测试介质 |
|  IsLeakTest  | boolean  | true  | 是泄漏测试 |
|  Comment  | string  | xxxx  | 备注 |


#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
