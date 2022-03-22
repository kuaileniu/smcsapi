---
title: 删除用户
weight: 200
---

<small>更新日期: 2021-11-06</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff/del-staff
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  Id  | number  | 143042904770001  | 用户id |
 

{{< /tab >}}
{{< tab "样例" >}}

URL： https://xxx.com/api/staff/del-staff

body： 

```json
{
    "Id": 143042904770001
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
    "msg": "删除成功",
    "english_msg": "Success."
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "删除失败",
    "english_msg": "Failed。"
}
```
{{< /tab >}}
{{< /tabs >}}
 
#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
