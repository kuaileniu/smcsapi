---
title: 分页获取单线信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2021-12-27</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-isometric/get-jtbl-isometric-page
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
            "Id": 144240978580001,
            "AreaId": 1,
            "ServiceId": 1,
            "LineId": 1,
            "JobId": 1,
            "IsometricNo": "IsometricNo1",
            "Rev": "版本",
            "RevDate": "2021-11-22 00:00:00",
            "RevRef": "升版原因",
            "MatHold": false,
            "NDTHold": false,
            "RevHold": false,
            "ColourCode": "色码",
            "LineClass": "管线等级",
            "PipeSpec": "钢管规格",
            "PaintSpec": "油漆规范",
            "PipingSpec": "管道材料等级",
            "InsulationSpec": "保温规范",
            "InsulationThickness": "保温厚度",
            "PlantAreaId": 1,
            "PriorityId": 1,
            "EmployeeCode": "员工代码",
            "PID": "PID111",
            "TestPressure": "测试压力",
            "DesignPressure": "设计压力",
            "OperatingPressure": "工作压力",
            "TestMedium": "测试介质",
            "DesignTemp": "设计温度",
            "System": "系统",
            "SubSystem": "子系统",
            "OperatingTemp": "工作温度",
            "PWHT": "焊后热处理",
            "NDTHoldSite": false,
            "LastCopiedIsoSpool": 0,
            "ApplyDG": false,
            "ApplyBG": false,
            "IsoDrawingRate": 0,
            "MiscRate1": 0,
            "MiscRate2": 0,
            "MiscRate3": 0,
            "MiscRate4": 0,
            "TempalteIso": false,
            "Spare1": "",
            "Spare2": "",
            "Spare3": "",
            "Spare4": "",
            "CreatedBy": "15652963646",
            "ModifiedBy": "",
            "CreateTime": "2021-12-27 21:23:05",
            "ModifyTime": "2021-12-27 21:23:05",
            "AreaName": "AreaName1",
            "ServiceName": "",
            "LineName": ""
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
|  Id  | number  | 144095520480001  | 单线ID |
|  JobId  | number  | 1  | 项目ID |
|  AreaId  | number  | 1  | 分区ID |
|  ServiceId  | number  | 1  | 介质ID |
|  LineId  | number  | 1  | 管线ID |
|  IsometricNo  | string  | xxx  | 单线号 |
|  Rev  | string  | xxx  | 版本 |
|  RevDate  | 日期  | 2021-11-22  | 版本日期 |
|  MatHold  | boolean  | true  | 材料暂停 |
|  NDTHold  | boolean  | true  | 探伤暂停 |
|  RevHold  | boolean  | true  | 版本暂停 |
|  ColourCode  | string  | xxx  | 色码 |
|  LineClass  | string  | xxx  | 管线等级 |
|  PipeSpec  | string  | xxx  | 钢管规格 |
|  PaintSpec  | string  | xxx  | 油漆规范 |
|  InsulationSpec  | string  | xxx  | 保温规范 |
|  InsulationThickness  | string  | xxx  | 保温厚度 |
|  PlantAreaId  | number  | 1  | 设备区域ID |
|  PriorityId  | number  | 1  | 优先级ID |
|  EmployeeCode  | string  | xxxx  | 员工代码 |
|  PID  | string  | xxxx  | PID |
|  TestPressure  | string  | xxxx  | 测试压力 |
|  DesignPressure  | string  | xxxx  | 设计压力 |
|  OperatingPressure  | string  | xxxx  | 工作压力 |
|  TestMedium  | string  | xxxx  | 测试介质 |
|  DesignTemp  | string  | xxxx  | 设计温度 |
|  System  | string  | xxxx  | 系统 |
|  SubSystem  | string  | xxxx  | 子系统 |
|  OperatingTemp  | string  | xxxx  | 工作温度 |
|  PWHT  | string  | xxxx  | 焊后热处理 |
|  NDTHoldSite  | boolean  | true  | 探伤现场暂停 |
|  LastCopiedIsoSpool  | number  | 1  | 最后一个复制的管段号 |
|  ApplyDG  | boolean  | true  | 应用于发货组 |
|  ApplyBG  | boolean  | true  | 应用于批次组 |
|  IsoDrawingRate  | number  | true  | 单线图纸费率,45%时传45 |
|  MiscRate1  | number  | true  | 杂项费率1,45%时传45 |
|  MiscRate2  | number  | true  | 杂项费率2,45%时传45 |
|  MiscRate3  | number  | true  | 杂项费率3,45%时传45 |
|  MiscRate4  | number  | true  | 杂项费率4,45%时传45 |
|  TempalteIso  | boolean  | false  | 是模板ISO |
|  Spare1  | string  | xxx  | 备用行1 |
|  Spare2  | string  | xxx  | 备用行2 |
|  Spare3  | string  | xxx  | 备用行3 |
|  Spare4  | string  | xxx  | 备用行4 |
|  AreaName  | string  | xxx  | 区域名 |
|  ServiceName  | string  | xxx  | 介质名 |
|  LineName  | string  | xxx  | 管线名 |

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
