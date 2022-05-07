---
title: 为角色变更权限
weight: 200
# GeekdocHidden: true
---

<small>更新日期: 2021-11-26</small>

权限说明：此处的权限包含菜单、目录、按钮；
#### 基本参数
1. url : https://{domain}:{port}/api/role-permission/change-permission-for-role
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  RoleId  | number  | 143083874570001  | 角色ID |
|  PermissionIds  | number 数组 | [143083874570001 ] | 最终拥有的权限ID数组 |

{{< /tab >}}
{{< tab "样例" >}}



body： 

```json
{
    "RoleId": 143083874570001,
    "PermissionIds": [
        123,
        456998
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
    "msg": "操作成功",
    "english_msg": "Success"
}
```   
{{< /tab >}}

{{< tab "失败" >}}
```json
 {
    "status": 1,
    "msg": "RoleId 不可为空",
    "english_msg": "RoleId can't be empty"
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
