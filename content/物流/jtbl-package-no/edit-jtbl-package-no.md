---
title: 编辑包装号的信息
weight: 300
---

<small>更新日期: 2022-03-30</small>

#### 基本参数
1. url : https://{domain}:{port}/api/jtbl-package-no/edit-jtbl-package-no
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 144095520480001  | 包装号ID |
|  JobId  | number  | 1  | 项目ID |
|  PackageNo  | string  |  xxxx | 包装号 |
|  WBSDescription  | string  | xxx  | 结构描述 |
|  DeliveryDocketID  | number  | 1  | 发货单ID |
|  Length  | float  | 1.3  | 长 |
|  Width  | float  | 1.3  | 宽 |
|  Height  | float  | 1.3  | 高 |
|  Volume  | float  | 1.3  | 体积 |
|  ExtraWeight  | float  | 1.3  | 包装重量kg |
|  NetWeight  | float  | 1.3  | 净重kg |
|  GrossWeight  | float  | 1.3  | 总重量kg |
|  WeighOutWeight  | float  | 1.3  | 过磅重量kg |
|  Comment  | string  | xxxx  | 备注 |  
|  AttachSli  | json数组  | []  | 附件，请看样例 |

{{< /tab >}}
{{< tab "样例" >}}


body： 

不需要修改的字段请不要传给服务器端

```json
{
    "Id": 147267362580001,
    "JobId": 1,
    "PackageNo": "NO2",
    "DeliveryDocketID": 1,
    "Length": 1002.1,
    "Width": 3.1,
    "Height": 4.1,
    "Volume": 5.1,
    "ExtraWeight": 7.1,
    "NetWeight": 8.1,
    "GrossWeight": 9.1,
    "WeighOutWeight": 10.1,
    "Comment": "xxxxxxxx",
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
    ]
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
    "msg": "xxx不可为空。",
    "english_msg": "xxx can't be blank."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  示例值 |  描述 |
|  ----  | ----  | ----  |----  |
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
