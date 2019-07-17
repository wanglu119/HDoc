## 使用说明

>**设置hosts**
>
>>`/etc/hosts`添加如下域名配置:
>>
>>```
>>106.13.62.131  frontend.gitlab
>>
>>```
>>
>>
>
>**注册帐号**
>
>>```
>>http://frontend.gitlab:8080/
>>```
>>
>>![](./images/auth_client_1.png)
>>
>>![](./images/auth_client_2.png)
>>
>>登录获取token
>>
>>![](./images/auth_client_3.png)
>>
>>
>>
>>
>
>**下载，配置client**
>
>>```
>>https://github.com/wanglu119/HDoc/tree/master/auth_ngrok
>>
>>wget https://raw.githubusercontent.com/wanglu119/HDoc/master/auth_ngrok/ngrok_new_client
>>
>>添加执行权限:
>>chmod +x ngrok_new_client
>>
>>
>>```
>>
>>创建配置文件:
>>
>>```
>>在ngrok_new_client同级目录下，创建
>>config/ngrok.cfg
>>配置文件内容:
>>server_addr: "frontend.gitlab:3443"
>>trust_host_root_certs: false
>>auth_token: "xxxx"
>>```
>>
>>
>
>**启动client**
>
>>启动参数:
>>
>>```
>>./ngrok_new_client -h
>>
>>Usage of bin/ngrok_new_client:
>>  -cpath string
>>        client config path, default ./config/ngrok.cfg (default "./config/ngrok.cfg")
>>```
>>
>>启动client后，在登录`http://frontend.gitlab:8080/`可以创建，穿透通道
>>
>>![](./images/auth_client_4.png)
>>
>>
>
>





























































































