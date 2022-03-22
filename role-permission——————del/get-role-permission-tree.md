---
title: 根据角色获取权限(含未被分配的权限)
weight: 100
# GeekdocHidden: true
---

<small>更新日期: 2021-11-26</small>

权限说明：此处的权限包含菜单、目录、按钮；
#### 基本参数
1. url : https://{domain}:{port}/api/role-permission/get-role-permission-tree
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |
|  RoleId  | number  | 143083874570001  | 角色ID |

{{< /tab >}}
{{< tab "样例" >}}



body： 

```json
{
    "RoleId":143083874570001
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
            "Id": 1,
            "ParentId": -1,
            "ChineseName": "主页",
            "PermissionType": 1,
            "MenuIcon": "layui-icon-set",
            "LAY_CHECKED": false,
            "Children": [
                {
                    "Id": 2,
                    "ParentId": 1,
                    "ChineseName": "主页",
                    "MenuURL": "/",
                    "PermissionType": 2,
                    "LAY_CHECKED": false
                }
            ]
        },
        {
            "Id": 3,
            "ParentId": -1,
            "ChineseName": "项目",
            "PermissionType": 1,
            "LAY_CHECKED": false,
            "Children": [
                {
                    "Id": 4,
                    "ParentId": 3,
                    "ChineseName": "项目登录",
                    "PermissionType": 1,
                    "LAY_CHECKED": false,
                    "Children": [
                        {
                            "Id": 5,
                            "ParentId": 4,
                            "ChineseName": "项目登录",
                            "MenuURL": "app/content/projectLogin",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 6,
                            "ParentId": 4,
                            "ChineseName": "项目列表",
                            "MenuURL": "app/content/projectList",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 7,
                            "ParentId": 4,
                            "ChineseName": "项目设置",
                            "MenuURL": "system/authorities",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 8,
                            "ParentId": 4,
                            "ChineseName": "项目参数",
                            "MenuURL": "app/content/paramter",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 9,
                            "ParentId": 4,
                            "ChineseName": "导入数据",
                            "MenuURL": "app/content/import",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        }
                    ]
                },
                {
                    "Id": 10,
                    "ParentId": 3,
                    "ChineseName": "项目计划",
                    "PermissionType": 1,
                    "LAY_CHECKED": false,
                    "Children": [
                        {
                            "Id": 11,
                            "ParentId": 10,
                            "ChineseName": "甘特图",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 12,
                            "ParentId": 10,
                            "ChineseName": "资源配置",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        }
                    ]
                }
            ]
        },
        {
            "Id": 13,
            "ParentId": -1,
            "ChineseName": "生产",
            "PermissionType": 1,
            "LAY_CHECKED": false,
            "Children": [
                {
                    "Id": 14,
                    "ParentId": 13,
                    "ChineseName": "基础数据",
                    "PermissionType": 2,
                    "LAY_CHECKED": false,
                    "Children": [
                        {
                            "Id": 17,
                            "ParentId": 14,
                            "ChineseName": "管道数据",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 18,
                            "ParentId": 14,
                            "ChineseName": "结构数据",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        }
                    ]
                },
                {
                    "Id": 15,
                    "ParentId": 13,
                    "ChineseName": "图纸下发",
                    "PermissionType": 2,
                    "LAY_CHECKED": false,
                    "Children": [
                        {
                            "Id": 19,
                            "ParentId": 15,
                            "ChineseName": "材料匹配",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 20,
                            "ParentId": 15,
                            "ChineseName": "工作包",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 21,
                            "ParentId": 15,
                            "ChineseName": "创建批次",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        }
                    ]
                },
                {
                    "Id": 16,
                    "ParentId": 13,
                    "ChineseName": "进度报告",
                    "PermissionType": 2,
                    "LAY_CHECKED": false,
                    "Children": [
                        {
                            "Id": 22,
                            "ParentId": 16,
                            "ChineseName": "批次报告",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 23,
                            "ParentId": 16,
                            "ChineseName": "WBS报告",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 24,
                            "ParentId": 16,
                            "ChineseName": "工作包报告",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 25,
                            "ParentId": 16,
                            "ChineseName": "分包商报告",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        }
                    ]
                }
            ]
        },
        {
            "Id": 26,
            "ParentId": -1,
            "ChineseName": "权限",
            "PermissionType": 1,
            "LAY_CHECKED": false,
            "Children": [
                {
                    "Id": 27,
                    "ParentId": 26,
                    "ChineseName": "权限管理",
                    "PermissionType": 1,
                    "LAY_CHECKED": false,
                    "Children": [
                        {
                            "Id": 28,
                            "ParentId": 27,
                            "ChineseName": "用户管理",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 29,
                            "ParentId": 27,
                            "ChineseName": "角色管理",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 30,
                            "ParentId": 27,
                            "ChineseName": "权限分配",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        },
                        {
                            "Id": 31,
                            "ParentId": 27,
                            "ChineseName": "用户项目",
                            "PermissionType": 2,
                            "LAY_CHECKED": false
                        }
                    ]
                }
            ]
        }
    ]
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
|  Id  | number  | 是  | 2109300032090001  | 权限的id  |
|  ParentId  | number  | - | -1  | 父级权限id  |
|  ChineseName  |  string  | - | 主页  | 权限的中文名称  |
|  EnglishName  |  string  | - | xxx  | 英文名  |
|  PermissionType  |  number  | - | 1  | 权限类型，1为目录，2为菜单，3为按钮  |
|  LAY_CHECKED  |  boolean  | - | true  | true表示有此权限，false表示无此权限  |
|  MenuURL  |  string  | - | app/pro/xxx  | 菜单路径  |
|  MenuIcon  |  string  | - | layui-icon-set  | 菜单的图标  |
|  Children  |  数组  | - | [{}]  | 子级权限数组  |



#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
