---
title: 获取自己拥有的菜单树
weight: 100
# GeekdocHidden: true
---

<small>更新日期: 2021-11-30</small>

#### 基本参数
1. url : https://{domain}:{port}/api/staff-permission/my-menu-tree
2. http method : POST

#### 请求数据
遵守[鉴权机制](/auth/)
{{< tabs "uniqueid_request" >}}
{{< tab "参数" >}} 

|  参数名称   |  类型 |  示例 |  描述 |
|  ----  | ----  | ----  | ----  |

{{< /tab >}}
{{< tab "样例" >}}



body： 

```json
 
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
            "EnglishName": "Home",
            "PermissionType": 1,
            "MenuIcon": "layui-icon-set",
            "Children": [
                {
                    "Id": 2,
                    "ParentId": 1,
                    "ChineseName": "主页",
                    "EnglishName": "Home",
                    "MenuURL": "/",
                    "PermissionType": 2
                }
            ]
        },
        {
            "Id": 3,
            "ParentId": -1,
            "ChineseName": "项目",
            "EnglishName": "Project",
            "PermissionType": 1,
            "Children": [
                {
                    "Id": 4,
                    "ParentId": 3,
                    "ChineseName": "项目登录",
                    "EnglishName": "Project Login",
                    "MenuURL": "/",
                    "PermissionType": 1,
                    "Children": [
                        {
                            "Id": 5,
                            "ParentId": 4,
                            "ChineseName": "项目登录",
                            "EnglishName": "Project Login",
                            "MenuURL": "app/content/projectLogin",
                            "PermissionType": 2
                        }
                    ]
                },
                {
                    "Id": 6,
                    "ParentId": 3,
                    "ChineseName": "项目列表",
                    "EnglishName": "Project List",
                    "MenuURL": "app/content/projectList",
                    "PermissionType": 2
                },
                {
                    "Id": 7,
                    "ParentId": 3,
                    "ChineseName": "项目设置",
                    "EnglishName": "Project Setup",
                    "PermissionType": 2,
                    "Children": [
                        {
                            "Id": 8,
                            "ParentId": 7,
                            "ChineseName": "项目参数",
                            "EnglishName": "Project Parameter",
                            "MenuURL": "app/content/paramter",
                            "PermissionType": 2
                        },
                        {
                            "Id": 9,
                            "ParentId": 7,
                            "ChineseName": "导入数据",
                            "EnglishName": "Import Data",
                            "MenuURL": "app/content/import",
                            "PermissionType": 2
                        }
                    ]
                },
                {
                    "Id": 10,
                    "ParentId": 3,
                    "ChineseName": "项目计划",
                    "EnglishName": "Project Plan",
                    "MenuURL": "/",
                    "PermissionType": 1,
                    "Children": [
                        {
                            "Id": 11,
                            "ParentId": 10,
                            "ChineseName": "甘特图",
                            "EnglishName": "Gantt Chart",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 12,
                            "ParentId": 10,
                            "ChineseName": "资源配置",
                            "EnglishName": "Resource Allocation",
                            "MenuURL": "/",
                            "PermissionType": 2
                        }
                    ]
                }
            ]
        },
        {
            "Id": 13,
            "ParentId": -1,
            "ChineseName": "生产",
            "EnglishName": "Fabrication",
            "MenuURL": "/",
            "PermissionType": 1,
            "Children": [
                {
                    "Id": 14,
                    "ParentId": 13,
                    "ChineseName": "基础数据",
                    "EnglishName": "Drawing Data",
                    "MenuURL": "/",
                    "PermissionType": 2,
                    "Children": [
                        {
                            "Id": 17,
                            "ParentId": 14,
                            "ChineseName": "管道数据",
                            "EnglishName": "Piping Data",
                            "MenuURL": "component/table/pipeline",
                            "PermissionType": 2
                        },
                        {
                            "Id": 18,
                            "ParentId": 14,
                            "ChineseName": "结构数据",
                            "EnglishName": "Structural Data",
                            "MenuURL": "/",
                            "PermissionType": 2
                        }
                    ]
                },
                {
                    "Id": 15,
                    "ParentId": 13,
                    "ChineseName": "图纸下发",
                    "EnglishName": "Batch Issue",
                    "MenuURL": "/",
                    "PermissionType": 2,
                    "Children": [
                        {
                            "Id": 19,
                            "ParentId": 15,
                            "ChineseName": "材料匹配",
                            "EnglishName": "Material Allocation",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 20,
                            "ParentId": 15,
                            "ChineseName": "工作包",
                            "EnglishName": "Work Package",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 21,
                            "ParentId": 15,
                            "ChineseName": "创建批次",
                            "EnglishName": "Create Batches",
                            "MenuURL": "/",
                            "PermissionType": 2
                        }
                    ]
                },
                {
                    "Id": 16,
                    "ParentId": 13,
                    "ChineseName": "进度报告",
                    "EnglishName": "Progress Report",
                    "MenuURL": "/",
                    "PermissionType": 2,
                    "Children": [
                        {
                            "Id": 22,
                            "ParentId": 16,
                            "ChineseName": "批次报告",
                            "EnglishName": "Batch Report",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 23,
                            "ParentId": 16,
                            "ChineseName": "WBS报告",
                            "EnglishName": "WBS Report",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 24,
                            "ParentId": 16,
                            "ChineseName": "工作包报告",
                            "EnglishName": "WBS Report",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 25,
                            "ParentId": 16,
                            "ChineseName": "分包商报告",
                            "EnglishName": "Subcontractor Report",
                            "MenuURL": "/",
                            "PermissionType": 2
                        }
                    ]
                }
            ]
        },
        {
            "Id": 26,
            "ParentId": -1,
            "ChineseName": "权限",
            "EnglishName": "Permission",
            "MenuURL": "/",
            "PermissionType": 1,
            "Children": [
                {
                    "Id": 27,
                    "ParentId": 26,
                    "ChineseName": "权限管理",
                    "EnglishName": "Permission Management",
                    "MenuURL": "/",
                    "PermissionType": 1,
                    "Children": [
                        {
                            "Id": 28,
                            "ParentId": 27,
                            "ChineseName": "用户管理",
                            "EnglishName": "Users",
                            "MenuURL": "user/user/Users",
                            "PermissionType": 2
                        },
                        {
                            "Id": 29,
                            "ParentId": 27,
                            "ChineseName": "角色管理",
                            "EnglishName": "Roles",
                            "MenuURL": "user/administrators/list",
                            "PermissionType": 2
                        },
                        {
                            "Id": 30,
                            "ParentId": 27,
                            "ChineseName": "权限分配",
                            "EnglishName": "Permission Assignment",
                            "MenuURL": "user/administrators/role",
                            "PermissionType": 2
                        },
                        {
                            "Id": 31,
                            "ParentId": 27,
                            "ChineseName": "项目用户",
                            "EnglishName": "Project Users",
                            "MenuURL": "set/user/projectList",
                            "PermissionType": 2
                        }
                    ]
                }
            ]
        },
        {
            "Id": 32,
            "ParentId": -1,
            "ChineseName": "设置",
            "EnglishName": "Setting",
            "PermissionType": 1,
            "Children": [
                {
                    "Id": 33,
                    "ParentId": 32,
                    "ChineseName": "系统设置",
                    "EnglishName": "System Setting",
                    "PermissionType": 1,
                    "Children": [
                        {
                            "Id": 34,
                            "ParentId": 33,
                            "ChineseName": "网站设置",
                            "EnglishName": "Website Setting",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 35,
                            "ParentId": 33,
                            "ChineseName": "邮件服务",
                            "EnglishName": "Email Service",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 36,
                            "ParentId": 33,
                            "ChineseName": "PDA设置",
                            "EnglishName": "PDA Setting",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 37,
                            "ParentId": 33,
                            "ChineseName": "TBC",
                            "EnglishName": "TBC",
                            "MenuURL": "/",
                            "PermissionType": 2
                        },
                        {
                            "Id": 38,
                            "ParentId": 33,
                            "ChineseName": "字典管理",
                            "EnglishName": "Dictionary Management",
                            "MenuURL": "set/user/list",
                            "PermissionType": 2
                        }
                    ]
                },
                {
                    "Id": 39,
                    "ParentId": 32,
                    "ChineseName": "菜单配置",
                    "EnglishName": "Menu Setting",
                    "MenuURL": "menu",
                    "PermissionType": 2
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
    "msg": "查询我的菜单失败",
    "english_msg": "Failed"
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
|  MenuURL  |  string  | - | app/pro/xxx  | 菜单路径  |
|  MenuIcon  |  string  | - | layui-icon-set  | 菜单的图标  |
|  Children  |  数组  | - | [{}]  | 子级权限数组  |



#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
