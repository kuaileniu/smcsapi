---
title: 导入用户(们)的信息
weight: 800
# GeekdocHidden: true
---

<small>更新日期: 2021-11-07</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/import-staff
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 
 
 form-data :

    key: file

    value: 选择Excel文件

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/staff/import-staff
 
 form-data :

    key: file

    value: 选择Excel文件

{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "成功" >}} 
```json
 
{
    "status": 0,
    "msg": "导入成功",
    "english_msg": "Import success."
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "导入失败",
    "english_msg": "Failed."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |
 

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
