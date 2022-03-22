---
title: 生成验证码图片
weight: -900
---

<small>更新日期: 2021-10-19</small>

### 基本参数
1. url : https://{domain}:{port}/api/common/captcha?T={}
2. http method : GET


### 请求数据

{{< tabs "uniqueid_request" >}}
{{< tab "request" >}} 
说明： url中携带 T 的值为调用 [获取t](/auth/get_t) 接口获取的值；

样例： https://xxx.com/api/common/captcha?T=1632660520582506
{{< /tab >}}
{{< /tabs >}}



### 返回数据

{{< tabs "uniqueid_response" >}}
{{< tab "http code:200" >}} 

http headers:
content-type: image/png
```
图片文件
```   
{{< /tab >}}

{{< tab "http code:204" >}} 
说明： 前端系统使用的域名未在服务器端预先配置，请联系系统管理人员。

body：
```
```   
{{< /tab >}}
{{< /tabs >}}