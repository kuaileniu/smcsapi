---
title: 获取自己拥有的权限(含菜单)树
weight: 200
# GeekdocHidden: true
---

<small>更新日期: 2021-11-30</small>

权限说明：此处的权限包含菜单、目录、按钮；
#### 基本参数
1. url : https://{domain}:{port}/api/staff-permission/my-permission-tree
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
                    "PermissionType": 2,
                    "Children": [
                        {
                            "Id": 40,
                            "ParentId": 6,
                            "ChineseName": "新建",
                            "PermissionType": 3
                        },
                        {
                            "Id": 41,
                            "ParentId": 6,
                            "ChineseName": "批量编辑",
                            "PermissionType": 3
                        },
                        {
                            "Id": 42,
                            "ParentId": 6,
                            "ChineseName": "导出",
                            "PermissionType": 3
                        },
                        {
                            "Id": 43,
                            "ParentId": 6,
                            "ChineseName": "编辑",
                            "PermissionType": 3
                        },
                        {
                            "Id": 44,
                            "ParentId": 6,
                            "ChineseName": "删除",
                            "PermissionType": 3
                        }
                    ]
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
                            "PermissionType": 2,
                            "Children": [
                                {
                                    "Id": 45,
                                    "ParentId": 8,
                                    "ChineseName": "业主/客户",
                                    "EnglishName": "Clients",
                                    "MenuURL": "app/content/paramterList.html?tab=1",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 46,
                                    "ParentId": 8,
                                    "ChineseName": "分包商",
                                    "EnglishName": "Subcontractor",
                                    "MenuURL": "app/content/paramterList.html?tab=2",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 67,
                                            "ParentId": 46,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 68,
                                            "ParentId": 46,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 69,
                                            "ParentId": 46,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 70,
                                            "ParentId": 46,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 71,
                                            "ParentId": 46,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 47,
                                    "ParentId": 8,
                                    "ChineseName": "车间/工厂",
                                    "EnglishName": "Workshop",
                                    "MenuURL": "app/content/paramterList.html?tab=3",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 72,
                                            "ParentId": 47,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 73,
                                            "ParentId": 47,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 74,
                                            "ParentId": 47,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 75,
                                            "ParentId": 47,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 76,
                                            "ParentId": 47,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 48,
                                    "ParentId": 8,
                                    "ChineseName": "优先级",
                                    "EnglishName": "Priority",
                                    "MenuURL": "app/content/paramterList.html?tab=4",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 77,
                                            "ParentId": 48,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 78,
                                            "ParentId": 48,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 79,
                                            "ParentId": 48,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 80,
                                            "ParentId": 48,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 81,
                                            "ParentId": 48,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 49,
                                    "ParentId": 8,
                                    "ChineseName": "批次组",
                                    "EnglishName": "Batch Group",
                                    "MenuURL": "app/content/paramterList.html?tab=5",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 82,
                                            "ParentId": 49,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 83,
                                            "ParentId": 49,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 84,
                                            "ParentId": 49,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 85,
                                            "ParentId": 49,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 86,
                                            "ParentId": 49,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 50,
                                    "ParentId": 8,
                                    "ChineseName": "发货组",
                                    "EnglishName": "Delivery Group",
                                    "MenuURL": "app/content/paramterList.html?tab=6",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 87,
                                            "ParentId": 50,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 88,
                                            "ParentId": 50,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 89,
                                            "ParentId": 50,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 90,
                                            "ParentId": 50,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 91,
                                            "ParentId": 50,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 51,
                                    "ParentId": 8,
                                    "ChineseName": "其他",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 92,
                                            "ParentId": 51,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 93,
                                            "ParentId": 51,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 94,
                                            "ParentId": 51,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 95,
                                            "ParentId": 51,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 96,
                                            "ParentId": 51,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                }
                            ]
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
                            "PermissionType": 2,
                            "Children": [
                                {
                                    "Id": 97,
                                    "ParentId": 17,
                                    "ChineseName": "图纸/数据",
                                    "MenuURL": "component/table/eruipArea.html?tab=1",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 98,
                                    "ParentId": 17,
                                    "ChineseName": "设备区域",
                                    "EnglishName": "Plant Area",
                                    "MenuURL": "component/table/eruipArea.html?tab=2",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 99,
                                    "ParentId": 17,
                                    "ChineseName": "分区/单位",
                                    "EnglishName": "Area",
                                    "MenuURL": "component/table/eruipArea.html?tab=3",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 106,
                                            "ParentId": 99,
                                            "ChineseName": "新建",
                                            "PermissionType": 3,
                                            "Children": [
                                                {
                                                    "Id": 141,
                                                    "ParentId": 106,
                                                    "ChineseName": "新建",
                                                    "PermissionType": 3
                                                },
                                                {
                                                    "Id": 142,
                                                    "ParentId": 106,
                                                    "ChineseName": "批量编辑",
                                                    "PermissionType": 3
                                                },
                                                {
                                                    "Id": 143,
                                                    "ParentId": 106,
                                                    "ChineseName": "导出",
                                                    "PermissionType": 3
                                                },
                                                {
                                                    "Id": 144,
                                                    "ParentId": 106,
                                                    "ChineseName": "编辑",
                                                    "PermissionType": 3
                                                },
                                                {
                                                    "Id": 145,
                                                    "ParentId": 106,
                                                    "ChineseName": "删除",
                                                    "PermissionType": 3
                                                }
                                            ]
                                        },
                                        {
                                            "Id": 107,
                                            "ParentId": 99,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 108,
                                            "ParentId": 99,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 109,
                                            "ParentId": 99,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 110,
                                            "ParentId": 99,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 100,
                                    "ParentId": 17,
                                    "ChineseName": "介质",
                                    "EnglishName": "Service",
                                    "MenuURL": "component/table/eruipArea.html?tab=4",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 111,
                                            "ParentId": 100,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 112,
                                            "ParentId": 100,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 113,
                                            "ParentId": 100,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 114,
                                            "ParentId": 100,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 115,
                                            "ParentId": 100,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 101,
                                    "ParentId": 17,
                                    "ChineseName": "管线",
                                    "EnglishName": "Line",
                                    "MenuURL": "component/table/eruipArea.html?tab=5",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 116,
                                            "ParentId": 101,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 117,
                                            "ParentId": 101,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 118,
                                            "ParentId": 101,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 119,
                                            "ParentId": 101,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 120,
                                            "ParentId": 101,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 102,
                                    "ParentId": 17,
                                    "ChineseName": "单线",
                                    "EnglishName": "Isometric",
                                    "MenuURL": "component/table/Isometrics",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 121,
                                            "ParentId": 102,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 122,
                                            "ParentId": 102,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 123,
                                            "ParentId": 102,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 124,
                                            "ParentId": 102,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 125,
                                            "ParentId": 102,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 103,
                                    "ParentId": 17,
                                    "ChineseName": "管段",
                                    "EnglishName": "Spool",
                                    "MenuURL": "component/table/Spools",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 126,
                                            "ParentId": 103,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 127,
                                            "ParentId": 103,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 128,
                                            "ParentId": 103,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 129,
                                            "ParentId": 103,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 130,
                                            "ParentId": 103,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 104,
                                    "ParentId": 17,
                                    "ChineseName": "组件",
                                    "EnglishName": "Component",
                                    "MenuURL": "component/table/Components",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 131,
                                            "ParentId": 104,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 132,
                                            "ParentId": 104,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 133,
                                            "ParentId": 104,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 134,
                                            "ParentId": 104,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 135,
                                            "ParentId": 104,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                },
                                {
                                    "Id": 105,
                                    "ParentId": 17,
                                    "ChineseName": "焊接",
                                    "EnglishName": "Weld",
                                    "MenuURL": "component/table/Welds",
                                    "PermissionType": 3,
                                    "Children": [
                                        {
                                            "Id": 136,
                                            "ParentId": 105,
                                            "ChineseName": "新建",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 137,
                                            "ParentId": 105,
                                            "ChineseName": "批量编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 138,
                                            "ParentId": 105,
                                            "ChineseName": "导出",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 139,
                                            "ParentId": 105,
                                            "ChineseName": "编辑",
                                            "PermissionType": 3
                                        },
                                        {
                                            "Id": 140,
                                            "ParentId": 105,
                                            "ChineseName": "删除",
                                            "PermissionType": 3
                                        }
                                    ]
                                }
                            ]
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
                            "PermissionType": 2,
                            "Children": [
                                {
                                    "Id": 55,
                                    "ParentId": 28,
                                    "ChineseName": "新建",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 56,
                                    "ParentId": 28,
                                    "ChineseName": "批量编辑",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 57,
                                    "ParentId": 28,
                                    "ChineseName": "导出",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 58,
                                    "ParentId": 28,
                                    "ChineseName": "导入",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 59,
                                    "ParentId": 28,
                                    "ChineseName": "编辑",
                                    "PermissionType": 3
                                }
                            ]
                        },
                        {
                            "Id": 29,
                            "ParentId": 27,
                            "ChineseName": "角色管理",
                            "EnglishName": "Roles",
                            "MenuURL": "user/administrators/list",
                            "PermissionType": 2,
                            "Children": [
                                {
                                    "Id": 60,
                                    "ParentId": 29,
                                    "ChineseName": "新建角色",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 61,
                                    "ParentId": 29,
                                    "ChineseName": "编辑角色",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 62,
                                    "ParentId": 29,
                                    "ChineseName": "删除角色",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 63,
                                    "ParentId": 29,
                                    "ChineseName": "添加用户",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 64,
                                    "ParentId": 29,
                                    "ChineseName": "删除用户",
                                    "PermissionType": 3
                                }
                            ]
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
                            "PermissionType": 2,
                            "Children": [
                                {
                                    "Id": 65,
                                    "ParentId": 31,
                                    "ChineseName": "添加用户项目",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 66,
                                    "ParentId": 31,
                                    "ChineseName": "删除用户项目",
                                    "PermissionType": 3
                                }
                            ]
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
                            "PermissionType": 2,
                            "Children": [
                                {
                                    "Id": 52,
                                    "ParentId": 38,
                                    "ChineseName": "添加",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 53,
                                    "ParentId": 38,
                                    "ChineseName": "删除",
                                    "PermissionType": 3
                                },
                                {
                                    "Id": 54,
                                    "ParentId": 38,
                                    "ChineseName": "修改",
                                    "PermissionType": 3
                                }
                            ]
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
    "msg": "查询我的权限失败",
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
|  Children  |  数组  | - | [{}]  | 子级权限数组  |



#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

#### 服务器端返回客户端数据中的通用参数

{{< include file="/_includes/include_response_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}
