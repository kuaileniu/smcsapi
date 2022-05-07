## smcsdocs
静态文件和用户登录服务器端分开域名、分开部署
## 工具
- hugo-extendes_0.88.1 Mac版本 https://github.com/gohugoio/hugo/releases/download/v0.88.1/hugo_extended_0.88.1_macOS-64bit.tar.gz  windows 版本： https://github.com/gohugoio/hugo/releases/download/v0.88.1/hugo_extended_0.88.1_Windows-64bit.zip 
- 主题 hugo-geekdoc  v0.18.3  https://github.com/thegeeklab/hugo-geekdoc/releases/download/v0.18.3/hugo-geekdoc.tar.gz （此处是纯主题）
- 样例站点源文件  https://github.com/thegeeklab/hugo-geekdoc/archive/refs/tags/v0.18.3.zip （此代码下含 exampleSite）
- 在线样例 https://geekdocs.de/
- mermaid  https://mermaid-js.github.io/mermaid/#/
## 创建项目
> - 在git服务器端创建项目 smcsapi_src_202201
> - clone smcsapi_src_202201 到笔记本电脑
    > .gitignore中添加:

    ```
        .DS_Store 
        __MACOSX
        hugo
        hugo.exe
        resources
        public
    ```
> - 创建临时目录tmp123, copy hugo 到tmp123下
> - 进入临时目录tmp123，执行 hugo new site smcsdocs
> - copy smcsdocs/ 下所有文件到 smcsapi_src_202201/
> - 删除 smcsapi_src_202201/config.toml
> - 将 hugo copy 到smcsapi_src_202201/
> - copy hugo-geekdoc 到 smcsapi_src_202201/themes/hugo-geekdoc
> - copy https://github.com/thegeeklab/hugo-geekdoc/archive/refs/tags/v0.18.3.zip  解压后的 exampleSite/ 到 smcsapi_src_202201/ （替换全部相同的）
> - 默认折叠 # geekdocCollapseSection: true
## 调试
- cd smcsapi_src_202201
- hugo server
    > 浏览器地址栏 http://localhost:1313/ （根据提示，端口可能会变化）

## 发布
- cd smcsapi_src_202201
- hugo // 生成 smcsapi_src_202201/public 目录
- 将 public下文件 上传到web服务器  https://github.com/kuaileniu/smcsapi

## 演示 
- http://smcs.shxckt.com/views/
- http://smcs.shxckt.com/start/
## 前端部分
- 前端部署位置 2021-11-30前部署位置 https://github.com/kuaileniu/smcsdocs 的 prod分支
- 前端部署位置 2021-12-01后 计划部署位置 /mnt/smcsdev/smcsdocs_front
## 服务器端认证
- https://smcsdocsserver.zhsit.cn
- 源代码在 https://github.com/kuaileniu/smcsdocs_server
- 服务器端部署位置 /mnt/smcsdev/smcsdocs10001
- （本系统未采用）将静态文件编译成go源代码与服务器端代码一同编译成可执行文件，在服务器端认证 https://github.com/kuaileniu/smcsdocs_exe_202109
## 登录

https://smcsdocs.zhsit.cn/?username=smcs&password=smcs123456

http://localhost:1313/?username=smcs&password=smcs123456

http://localhost:1313/usage/getting-started/?r=1632414538124&username=smcs&password=smcs123456


http://local.zhsit.cn/?username=smcs&password=smcs123456