---
title: 获取 文件/图片(非私有)
weight: 200
---

<small>更新日期: 2022-02-24</small>

#### 基本参数
1. url : https://{domain}:{port}/dfs/dl/pub/212/34/bd461e2e0e9b06898b9dc86a86f3511c_1319.png
2. http method : GET

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

https://url/xxx.jpg

需要用户为登录状态

将来可能会在文件路径尾部追加信息,例如追加 "?key=val", https://url/xxx.jpg?key=val


{{< /tab >}}
{{< tab "样例" >}}

body： 

```
https://smcsapi.zhsit.cn/dfs/dl/pub/212/34/bd461e2e0e9b06898b9dc86a86f3511c_1319.png
```
{{< /tab >}}

{{< /tabs >}}


#### 返回数据


{{< tabs "uniqueid_response" >}}
{{< tab "成功" >}} 
```
文件流
```   
{{< /tab >}}

{{< tab "失败" >}}
```
无文件流
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数



#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
