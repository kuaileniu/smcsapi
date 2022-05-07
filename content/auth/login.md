---
title: 用户登录
weight: -800
---
<small>更新日期: 2021-10-20</small>

#### 步骤：
> 1. 通过 [获取t](/auth/get_t) 接口取得t ;
> 2. 使用T,通过调用 [生成验证码图片](/auth/captcha) 接口来生成验证码;
> 3. 调用 [用户登录](/auth/login) 接口,获取访问令牌和刷新令牌;
> 4. 保存访问令牌和保存刷新令牌到客户端或浏览器。
#### 登录流程图：

{{< columns >}}

{{< mermaid class="text-center" >}}
graph TD
    开始 --> 获取t;
    获取t --> |成功|获取验证码图片 -->  |成功|登录 --> |成功|保存访问令牌和保存刷新令牌到客户端或浏览器 --> 结束;
    获取t --> |失败|获取t;
    获取验证码图片 -->|失败|获取t;
    登录 --> |失败|获取t;

{{< /mermaid >}}
<--->
{{< /columns >}}
#### 基本参数
1. url : https://{domain}:{port}/api/common/login
2. http method : POST


#### 请求数据

{{< tabs "uniqueid_request" >}}
{{< tab "说明" >}} 
 
1. T ：调用 [获取t](/auth/get_t) 接口获取的值；
1. Vercode ：调用 [生成验证码图片](/auth/captcha) 接口获取的图片中显示的值；
1. Username ：用户登录名
1. Password ： 用户登录密码


{{< /tab >}}
{{< tab "样例" >}} 

URL： https://xxx.com/api/common/login

body： 

```
{
    "T": "1234567",
    "Username": "15652963646",
    "Password": "123456",
    "Vercode": "6666"
}
```
{{< /tab >}}
{{< /tabs >}}


#### 返回数据

{{< tabs "uniqueid_response" >}}
{{< tab "http code:200" >}} 
```
{
    "status": 0,
    "access-token": "WVjhtoqU1Nok0iUBAlrj0SsiwH9nv6tcC7dcjwo5XjiQb52bIEG98YvP8uKSIhpG8cBGI8fvHTAhPejPNEPoNg17vAEsBT8xBwlvFOa6mp1tVSIC6H9w%2FimTVefx3rX5OKP0BqXMTtRuBqZjE0UYqhH%2FzLzEv035GeC50RdigctnGOk7miyhsumvnrxNlO6vMAuEnv3hBBTO7cSw2BFerw%2FUZUdxgmCy9rjq1zmCKMH3fSyTYxSC17KWgDUZGkG%2F0Y95Hq8m2fattLTbqJyAXg%3D%3D",
    "refresh-token": "WVjhtoqU1Nok0iUBAlrj0fAtPxSm7atc30xcr%2FhJFx6qLyN8%2FDykjJSjpM4MyJje%2FoYI19mACC3h%2FkbeOYiR%2FQ%3D%3D"
}
```   
{{< /tab >}}

{{< tab "http code:401" >}} 
```
{
    "status": 1,
    "msg": "Verification code error"
}
```   
{{< /tab >}}
{{< /tabs >}}

#### 返回数据中的通用参数

{{< include file="/_includes/include_response_body_common.md">}}