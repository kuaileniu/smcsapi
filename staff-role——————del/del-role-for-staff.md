---
title: 为用户删除(批量)角色
weight: 600
# GeekdocHidden: true
---

<small>更新日期: 2021-11-21</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff-role/del-role-for-staff
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  RoleIds  | number数组  | [143083874570001,143083874670001]  | 角色ID数组 |
|  StaffId  | number  |  5 | 用户ID |

{{< /tab >}}
{{< tab "样例" >}}



body： 

```json
{
    "StaffId":5,
    "RoleIds":[143083874570001,143083874670001]
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
    "msg": "删除成功。",
    "english_msg": "Success."
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
{
    "status": 1,
    "msg": "RoleIds 不可为空",
    "english_msg": "RoleIds can't be empty."
}
```
{{< /tab >}}
{{< /tabs >}}
#### data 参数

|  参数   |  类型 |  必含 |  示例值 |  描述 |
|  ----  | ----  | ----  | ----  |----  |



<!-- #### 向服务器端发送数据中的通用参数 -->
<!-- {{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}} -->

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
