---
title: 前言
weight: 1
---
<small>更新日期: 2021-09-30</small>

### 整体说明
1. 代码组成：本系统采用前端和服务器端分离架构开发，代码库分离；
2. 部署：本系统采用前端和服务器端在研发阶段分开单独部署，交付不同客户时有根据需要有可能集合为一个整体后部署；
3. 域名：前端系统和服务器端系统在研发阶段分别使用不同域名；交付不同客户时根据需要可能采用同一个域名，也有可能采用不同域名；每家客户的域名不同；
4. 域名端口后到第一段路径要求：不要使用 api 或 ws 开始
    ```
    不可以: https://{domain}:{port}/api/yyyyy 
    不可以: https://{domain}:{port}/apixxxx/yyyyy;
    ```
5. 协议： 根据不同客户需求，系统可能使用 https 协议，也可能使用 http 协议；
5. 端口： 采用https协议时若采用默认443端口可省略；采用http协议时若采用默认80端口可省略；
6. 域名配置：前端系统采用的域名和端口须告知服务器端工程师，提前在服务器端安全控制体系中配置；
7. 报文体格式：无特殊说明，服务器端返回给客户端的报文体(http body)为json格式；
1. 用户密码： 客户端不得保存用户密码；
1. 前端调试时，建议使用修改调试代码所在电脑的hosts文件方式，调试时在浏览器地址栏中直接访问hosts中配置的域名；

#### 向服务器端发送数据中的通用参数
{{< include file="/_includes/include_request_body_common.md"  options="linenos=table,hl_lines=0-6,linenostart=3">}}

### 返回数据中的通用参数

{{< include file="/_includes/include_response_body_common.md">}}
