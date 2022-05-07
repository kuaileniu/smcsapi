---
title: 下载构件Excel中文模版
weight: 202203172012
---

<small>更新日期: 2022-03-17</small>

#### 基本参数
1. url : https://{domain}:{port}/api/download/download-jtbl-assembly-tpl-cn
2. http method : GET

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

| 

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/download/download-jtbl-assembly-tpl-cn
 
{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "成功" >}} 
   返回文件流

   Http.Header("Cache-Control", "no-cache")

   Http.Header("Content-Type", "application/vnd.ms-excel")

   Http.Header("Content-Disposition", "attachment;filename=")
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "下载失败",
    "english_msg": "Failed。"
}
```
{{< /tab >}}
{{< /tabs >}}
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
