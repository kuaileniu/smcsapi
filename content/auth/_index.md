---
title: 鉴权机制
weight: 2
geekdocCollapseSection: true
# geekdocHidden: true
---
<small>更新日期: 2022-04-20</small>

### 无需鉴权接口

 不需要通过鉴权就能调用的接口有下列，其它接口都需要在http header 或 url中携带access-token。
> - 1. [获取t](/auth/get_t) ;
> - 2. [生成验证码图片](/auth/captcha)
> - 3. [用户登录](/auth/login);
> - 4. [刷新令牌](/auth/refresh-token);

### 服务器端获取 access-token 的优先顺序
{{< columns >}}
{{< mermaid class="text-center" >}}
graph LR
   A[Http Header] --未取到--> URL  --未取到--> Form表单;
   
{{< /mermaid >}}
<--->
{{< /columns >}}

### 鉴权流程

> 1. 若http method 为 POST，每次调用服务器端业务接口时，除报文(在body中)主体外需要在http head中携带 access-token(来自于[用户登录](/auth/login));
> 2. 若http method 为 GET，每次调用服务器端业务接口时，需要在url后拼接access-token(来自于[用户登录](/auth/login));
{{< tabs "uniqueid" >}}
{{< tab "POST" >}} 
{{< include file="/_includes/include-headers.md">}}
 

</br> </br> 
body：
```json
    {
        "key_1":"val_1",
        ......
        "key_n":"val_n"
    }
```    
{{< /tab >}}

{{< tab "GET" >}} 
- https://{domain}:{port}/xxxx/xxxx?access-token=浏览器中存储的access-token值&key_1=val_1 </br>
- https://{domain}:{port}/xxxx/xxxx?access-token= onAJTtFs6wS1Le5KqGXs7FxfdAWby0l73l4GCXRmZWEa1lmAVLadHt7IW4LOOzdOQgfcRRXxo3KrmNoFbZtOMwTOtSS5e5iqlLb%2Bg7BhPGwvN49%2F1vWdGQa4xVM90eU%2Bz7AgRmyxLIPM58T4qpeafY4gZPmiM5SXsp%2BSo4Gb2svwf3iRRnR7Ss158iH1B1OQU9XtCDnZ5XYSbeCdod4xb%2FKbjO92HUAfEr7kcDjuTvo%3D &key_1=val_1 
{{< /tab >}}

{{< /tabs >}}

> 3. 若系统返回http code为401，则使用 [刷新令牌](/auth/refresh-token)  接口刷新 access-token和refresh_token;
> 4. 若调用 [刷新令牌](/auth/refresh-token) 返回http code为401则需调用 [用户登录](/auth/login) 获取access-token 和 refresh-token;
> 5. 若系统返回http code为401，则需要使用refresh-token(来自于[用户登录](/auth/login))调用
> 6. 保存或更新 访问令牌(access-token) 和 刷新令牌(refresh-token)到客户端或浏览器。
> 7. 重新发起调用服务器端业务接口;



#### 鉴权流程图：

{{< columns >}}
{{< mermaid class="text-center" >}}
graph TD
    开始-->从客户端或浏览器取出访问令牌{从客户端或浏览器取出访问令牌};
    从客户端或浏览器取出访问令牌--成功取出---->调用服务器端业务接口;
    从客户端或浏览器取出访问令牌----未取出---->用户登录;
    调用服务器端业务接口 -- POST 方式 Header with access-token ----> 服务器端{服务器端};
    调用服务器端业务接口 -- GET 方式 uri with access-token ----> 服务器端;
    服务器端--返回 http code 为200---->业务数据 ----> 结束;
    服务器端--返回 http code 为401---->调用刷新令牌接口{调用刷新令牌接口};
    调用刷新令牌接口 --返回 http code 为200 ----> 更新访问令牌和刷新令牌 ----> 调用服务器端业务接口;
    调用刷新令牌接口 -- 返回 http code 为401 ----> 用户登录{用户登录};
    用户登录 --成功----> 更新访问令牌和刷新令牌;
    用户登录 --失败----> 用户登录;
{{< /mermaid >}}

{{< /columns >}}