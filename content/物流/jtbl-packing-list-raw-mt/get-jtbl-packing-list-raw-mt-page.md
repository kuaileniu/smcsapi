---
title: 分页获取包装清单(原材料)信息
weight: 400
# GeekdocHidden: true
---

<small>更新日期: 2022-03-31</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-packing-list-raw-mt/get-jtbl-packing-list-raw-mt-page
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
            "Id": 147271939580001,
            "JobId": 1,
            "PackageNoID": 1,
            "MaterialID": 1,
            "MaterialQty": 10,
            "LengthEach": 20,
            "MaterialWeightEach": 30,
            "MaterialWeightTotal": 40,
            "CreatedBy": "156529",
            "ModifiedBy": "156529",
            "CreateTime": "2022-03-31 11:23:15",
            "ModifyTime": "2022-03-31 11:23:15",
            "PackageNo": "",
            "MaterialCode": "",
            "MaterialDescription": ""
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
|  Id  | number  | 144095520480001  | 包装清单(原材料)ID |
|  JobId  | number  | 1  | 项目ID |
|  PackageNoID  | number  |  1 | 包装号ID |
|  MaterialID  | number  |  1 | 物料库ID |
|  PackageNo  | string  |  xxxx | 包装号 |
|  MaterialQty  | number  |  1 | 数量 |
|  LengthEach  | float  |  1.1 | 长 |
|  MaterialWeightEach  | float  |  1.1 | 单重kg |
|  MaterialWeightTotal  | float  |  1.1 | 总重kg |
|  MaterialCode  | string  | xxxx  | 物料编码 |  
|  MaterialDescription  | string  | xxxx  | 物料描述 |  

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
