# 公共资源

## 一、服务器

### 1. 账号

- 账号： 服务器ip
- 密码： Timevale#123

### 2. 常用Linux命令

- cd/history/unzip/ls/ll 。。。
- [linux命令大全](https://www.linuxcool.com/)

### 3. ssh软件

- Windows: [SSH工具](https://zhuanlan.zhihu.com/p/609376551)
- Mac:  [Tabby](https://github.com/Eugeny/tabby/releases/tag/v1.0.197)

## 二、组件库

> npm私有仓库公共账号： 
>
> - name：esigndesign
>
> - pwd：esigndesign123

### 1. 分支

| 序号 | 组件库名称         | 业务平台        | 历史分支                           | 最终分支                       | 线上预览地址                                                 | git地址                                                      |
| ---- | ------------------ | --------------- | ---------------------------------- | ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1    | esign-design-sign  | 场景平台h5      | origin/feature/seal-cjyy-v1.10.0.1 | feature/seal-cjyy              | [文档](https://design.tsign.cn/esign-design-web/vue-sign/#/common-modal) | [git](git@git.timevale.cn:front-common/esign-design-sign.git) |
|      |                    |                 |                                    |                                |                                                              |                                                              |
| 2    | esign-ui           | 场景平台pc      | origin/feature/seal-cjyy-v1.9.5    | feature/seal-cjyy              | [文档](https://test-static.tsign.cn/esign-ui/#/component/installation) | [git](git@git.timevale.cn:front-common/esign-ui.git)         |
|      |                    | 医疗平台pc & h5 | origin/project/hospital-mobile     | origin/project/hospital-mobile |                                                              |                                                              |
| 3    | esign-design-vue   |                 |                                    |                                | [文档](https://design.tsign.cn/esign-design-web/vue/components/affix-cn) | [git](git@git.timevale.cn:front-common/esign-design-vue.git) |
| 4    | Esign-design-react |                 |                                    |                                | [文档](https://design.tsign.cn/esign-design-web/components/esign-ui/table-cn/) | [git](git@git.timevale.cn:front-common/esign-design.git)     |
| 5    | 数政pc组件         | 数政pc          |                                    |                                | [文档](https://design.tsign.cn/esign-design-web/vue-gov/#/esign-biz-login) | [git](http://git.timevale.cn:8081/esign_gov/esign-design-gov) |
| 6    | 数政h5组件         | 数政h5          |                                    |                                | [文档](https://design.tsign.cn/esign-design-web/vue-mobile-gov/#/esign-biz-login) | [git](http://git.timevale.cn:8081/esign_gov/esign-design-mobile-gov) |

### 2. 如何发包

#### 2.1 esign-ui/mobile

```js
1. 进入mobile目录
2. 源代码组件  mobile/package
3. 记得修改 mobile/package.json中version版本
4. 打包：  yarn build:dist
5. npm  adduser --registry https://registry-npm.tsign.cn/
6. npm publish
```

#### 2.2 esign-ui/base

>注意： base的部分包打包后无效果，可能愿意是   业务 ---> biz ---> base    所以biz也要发包

```js
1. 进入base目录
2. 源代码组件  mobile/base
3. 记得修改 base/package.json中version版本
4. 打包：  yarn dist
5. npm  adduser --registry https://registry-npm.tsign.cn/
6. npm publish
```

#### 2.3 esign-ui/biz

```js
1. 进入biz目录
2. 源代码组件  mobile/biz
3. 记得修改 biz/package.json中version版本
4. 打包：  yarn dist
5. npm  adduser --registry https://registry-npm.tsign.cn/
6. npm publish
```

#### 2.4 esign-design-sign

>注意
>
>- 每个组件都是一个单包，都可以单独发包

```js
1. 进入目录
2. 源代码组件  packages
3. 记得修改 ’packages/xxx组件‘ 中version版本
4. 打包：  yarn build_mobile  单包名称            #说明： 单包名称--->packages/xxx/package.json/name	
5. npm  adduser --registry https://registry-npm.tsign.cn/
6. npm publish
```

## 三、前端开发规范

#### [1. 前端开发规范](https://frontend-standard.tsign.cn/#%E6%9C%89%E8%BF%87%E5%BF%A7%E8%99%91%E5%90%97)

#### [2. 插件化](https://frontend-standard.tsign.cn/plugin/about/)

#### [3. 低代码](https://frontend-standard.tsign.cn/lowcode/chart/)

## 四、前端加密算法

### 1. 对称加密算法：

- 说明：对称加密算法使用相同的密钥进行加密和解密，常见的对称加密算法有AES（Advanced Encryption Standard）和DES（Data Encryption Standard）等。前端可以使用`crypto`模块来实现对称加密算法。

### 2. 非对称加密算法：

- 说明：非对称加密算法使用一对密钥，即公钥和私钥，分别用于加密和解密。常见的非对称加密算法有RSA和ECC（Elliptic Curve Cryptography）等。前端可以使用`crypto`模块中的`subtle`属性来实现非对称加密。

### 3. 哈希算法

- 说明：哈希算法是将数据映射为固定长度的字符串，常用于数据完整性校验和密码存储等。常见的哈希算法有MD5、SHA-1和SHA-256等。前端可以使用`crypto`模块中的`createHash`方法来实现哈希算法。

### 4.散列算法：

- 说明：散列算法是一种可逆的、定长输出的加密算法，常用于密码保护。常见的散列算法有Bcrypt和Scrypt等。前端可以使用相应的JavaScript库来实现散列算法。

### 5. 国密算法加解密

- 说明：国密算法sm2、sm3和sm4的js版。 
- 传送门:  [sm-crypto](https://www.npmjs.com/package/sm-crypto)

### 6. 相关资料

- [cryptojs文档](https://cryptojs.gitbook.io/docs/)     [cryptojs npm文档](https://www.npmjs.com/package/crypto-js)

# 业务线

## 一、医疗

### 1. 服务器

#### 1.1 账号

- 账号： 服务器ip
- 密码： Timevale#123

#### 1.2 前端资源存放路径

- /usr/local/esign/apps/front

#### 1.3nginx配置文件

- /etc/nginx/conf.d

### 2. 前端应用详情

> gitlab组： [public_health](http://git.timevale.cn:8081/public_health)
>
> gitlab权限申请： [运维平台申请gitlabe组](http://ops.timevale.cn/#/workpad/new/gitlab)
>
> 账号： 17621603915   1111     手机号登录

| 序号 | 应用名称                                                     | 备注                                                         |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1    | [esign-user-platform](http://git.timevale.cn:8081/public_health/esign-user-platform) | 医疗电子签名管理平台  https://testhospital.tsign.cn          |
| 2    | [esign-hospital-operation](http://git.timevale.cn:8081/public_health/esign-hospital-operation) | 医疗电子签名运营管理平台   https://testhospital.tsign.cn/operation/login |
| 3    | [esign-hospital-ppm](http://git.timevale.cn:8081/public_health/esign-hospital-ppm) | 医疗电子签名个人业务中台  https://testhospital.tsign.cn/ppm/login |
| 4    | [esign-certification-h5](http://git.timevale.cn:8081/public_health/esign-certification-h5) | 医疗h5 https://testhospital.tsign.cn/h5/login                |
| 5    | [esign-hospital-tablets](http://git.timevale.cn:8081/public_health/esign-hospital-tablets) | 医疗手写板3.0APP                                             |
| 6    | [esign-hospital-wechat](http://git.timevale.cn:8081/public_health/esign-hospital-wechat) | 医疗医护微信小程序                                           |
| 7    | [esign-patient-wechat](http://git.timevale.cn:8081/public_health/esign-patient-wechat) | 医疗患者微信小程序                                           |
| 8    | [esign-hospital-localsign](http://git.timevale.cn:8081/public_health/esign-hospital-localsign) | 医疗本地签                                                   |
| 9    | [esign-hospital-jquery](http://git.timevale.cn:8081/public_health/esign-hospital-jquery) | 医疗jquery工程【完善用户信息、断网签、授权】                 |
| 10   | [ding-health-front](http://git.timevale.cn:8081/public_health/ding-health-front) | 钉签医疗版                                                   |
| 11   | [esign-health-front](http://git.timevale.cn:8081/public_health/esign-health-front) | 医疗2.0版本管理平台 & 医疗演示demo                           |
| 12   | [esign-hospital-template](http://git.timevale.cn:8081/public_health/esign-hospital-template) | 医疗模板【用于发起签署自定义模板】                           |
| 13   | [sign-health-front](http://git.timevale.cn:8081/public_health/sign-health-front) | 医疗2.0患者签                                                |

### 3. 核心业务流程

![image-20230717094847820](https://trial-cdn.esign.cn/upload/43e6ea14-c610-5ac3-897c-e9f11df2f570!!7-17.png)

## 二、数政

### 1. 服务器

#### 1.1 账号

- 账号： 服务器ip
- 密码： Timevale#123

#### 1.2 前端资源存放路径

- /usr/local/esign/apps/front    印章平台
- /usr/local/gap/apps/front       场景平台

#### 1.3 nginx配置文件

> 服务存放目录： /etc/nginx/conf.d

##### 1.3.1 antman

```bash
    location ^~ /antman/{
        proxy_pass http://ant-man/;
    }
    location ^~ /staticTwo/{
        proxy_pass http://ant-man/staticTwo/;
    }
```

##### 1.3.2 common

```bash
    location ^~/file-system/{
        proxy_pass http://filesystem-service-deploy;
    }
    location ^~ /lops/ {
        proxy_pass http://lops;
    }
    location @router {
        rewrite ^/local-sign/pc/* /local-sign/pc.html last;
        rewrite ^/local-sign/mobile/* /local-sign/mobile.html last;
        rewrite ^/local-sign/middle/* /local-sign/middle.html last;
        rewrite ^/local-sign-cjyy/pc/* /local-sign-front-cjyy/pc.html last;
        rewrite ^/local-sign-cjyy/mobile/* /local-sign-front-cjyy/mobile.html last;
        rewrite ^/local-sign-cjyy/middle/* /local-sign-front-cjyy/middle.html last;
    }
    location /front-lops {
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
            break;
        }
    }
```

##### 1.3.3 esign【印章平台】

```bash
# open-web 配置
location / {
    if ($request_filename ~* ^.*?.(html|htm)$)
    {
      add_header Cache-Control "no-cache, no-store";
    }
    root /usr/local/esign/apps/front/open/;
    index open.html open.htm;
    try_files $uri $uri/ /open.html;
    autoindex off;
}
    # 嵊里签PC配置
    location /appCenterSZ {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
        alias /usr/local/esign/apps/front/appCenterSZ;
        index index.html index.htm;
        try_files $uri $uri/ /appCenterSZ/index.html;
        autoindex off;
    }

    # 领章base配置
    location /realNameSealBase/ {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
         alias  /usr/local/esign/apps/front/realNameSealBase/;
         try_files $uri $uri/ /realNameSealBase/index.html;
        index index.html index.htm;
    }

    # baseh5配置
    location /baseh5/ {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
        alias  /usr/local/esign/apps/front/baseh5/;
        try_files $uri $uri/ /baseh5/index.html;
        index index.html index.htm;
    }

    location /manage {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
       try_files $uri $uri/ /manage/index.html;
        alias  /usr/local/esign/apps/front/manage;
        index index.html index.htm;
    }

     # 前端eform报表子应用集成nginx配置
    location /magic-micro-chart {
      if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
     	alias /usr/local/esign/apps/front/dist;
     	index index.htm index.html;
     	try_files $uri $uri/ /magic-micro-chart/index.html;
    }

    # 签署模板配置
    location /documents {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
        try_files $uri $uri/ /documents/index.html;
        alias  /usr/local/esign/apps/front/sealplatform-template-front;
        index index.html index.htm;
    }
      # 低代码集成页面
    location /formSign {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
        alias /usr/local/esign/apps/front/support-microfe-rheafront;
        index index.html index.htm;
        try_files $uri $uri/ /formSign/index.html;
        autoindex off;
    }
      # 本地签配置
    location /local-sign {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
        alias /usr/local/esign/apps/front/local-sign-front;
        try_files $uri $uri/ @router;
        index index.html index.htm;

    }

    location ^~ /magic-flow-middle {
        if ($request_filename ~* ^.*?.(html|htm)$) # 配置页面不缓存html 和htm结尾的文件
        {
          add_header Cache-Control "no-cache, no-store";
        }
        alias /usr/local/esign/apps/front/magic-flow-middle;
        index index.html index.htm;
        try_files $uri $uri/ /magic-flow-middle/index.html;
        autoindex off;

        break;
    }

    location /v1/lsc/ {
        proxy_pass        http://seal-deploy/v1/lsc/;
        proxy_redirect     off;
        proxy_set_header    X-Real-IP    $remote_addr;
        proxy_set_header    X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /v1/ {
        proxy_pass        http://open-deploy/v1/;
        proxy_redirect     off;
        proxy_set_header    X-Real-IP    $remote_addr;
        proxy_set_header    X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /signapi/ {
        proxy_pass       http://seal-deploy/;
        proxy_redirect     off;
        proxy_set_header    X-Real-IP    $remote_addr;
        proxy_set_header    X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /sc/ {
          proxy_pass                http://172.24.29.55:8094/;
          proxy_redirect          off;
          proxy_set_header        X-Real-IP       $remote_addr;
          proxy_set_header        X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    # 单点登录配置,没有单点登录可不配置
    location /v1/sso/analysisToken {
         proxy_pass            http://open-deploy/v1/sso/analysisToken;
         proxy_redirect          off;
         proxy_set_header        X-Real-IP       $remote_addr;
         proxy_set_header        X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    # v2版本接口nginx配置添加 add by v2.5.2
    location /v2/ {
       proxy_pass        http://open-deploy/v2/;
       proxy_redirect     off;
       proxy_set_header    X-Real-IP    $remote_addr;
       proxy_set_header    X-Forwarded-For $proxy_add_x_forwarded_for;

    }
```

##### 1.3.4 gap【场景平台】

```bash
    location /backmanagemain {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /documents-cjyy {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /innermain {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /local-sign-front {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /middletool {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /outerh5 {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /outermain {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /outerpc {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    location /rheafront {
        add_header Cache-Control "no-cache, no-store";
        index  index.html index.htm;
        if (!-e $request_filename) {
            rewrite ([^/]+)/?(.+) /$1/index.html;
        break;
        }
    }

    error_page 404 /404.html;
    location = /404.html {
        root /usr/local/esign/apps/front;
        internal;
    }
    location  /local-sign-cjyy {
        add_header Cache-Control "no-cache, no-store";
        alias /usr/local/esign/apps/front/local-sign-front-cjyy;
        try_files $uri $uri/ @router;
        index index.html index.htm;
    }

    location ^~/gapadmin/ {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' 'Content-Type';
        if ($request_method = 'OPTIONS') {
             return 204;
        }
        proxy_pass http://gap-deploy/gapadmin/;
    }
    location ^~/gapopen/ {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' 'Content-Type';
        if ($request_method = 'OPTIONS') {
            return 204;
        }
        proxy_pass http://gap-deploy/gapopen/;
    }
    location ^~/gappub/ {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' 'Content-Type';
        if ($request_method = 'OPTIONS') {
            return 204;
        }
        proxy_pass http://gap-deploy/gappub/;
    }
    location ^~/gapgov/ {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' 'Content-Type';
        if ($request_method = 'OPTIONS') {
            return 204;
        }
        proxy_pass http://gap-deploy/gapgov/;
    }
    location ^~/gapsign/ {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' '*';
        if ($request_method = 'OPTIONS') {
          return 204;
        }
        proxy_pass http://gap-deploy/gapsign/;
    }
    location ^~/signTemplate/ {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' 'Content-Type';
        if ($request_method = 'OPTIONS') {
            return 204;
        }
        proxy_pass http://gap-deploy/signTemplate/;
    }
    location ^~/rheaApi/{
        proxy_pass http://private-deploy/;
    }
    location ^~ /V1/{
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Credentials' 'true';
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
        add_header 'Access-Control-Allow-Headers' '*';
        if ($request_method = 'OPTIONS') {
           return 204;
        }
        proxy_pass http://gap-deploy/gapopen/V1/;
    }
     location ^~ /esignpro/{
            add_header 'Access-Control-Allow-Origin' '*';
            add_header 'Access-Control-Allow-Credentials' 'true';
            add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
            add_header 'Access-Control-Allow-Headers' '*';
            if ($request_method = 'OPTIONS') {
               return 204;
            }
            proxy_pass http://gap-deploy/gapopen/esignpro/;
     }
     location ^~ /gap/v1/ {
         add_header 'Access-Control-Allow-Origin' '*';
         add_header 'Access-Control-Allow-Credentials' 'true';
         add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
         add_header 'Access-Control-Allow-Headers' '*';
         if ($request_method = 'OPTIONS') {
             return 204;
         }
         proxy_pass http://gap-deploy/v1/;
     }

     location ^~ /version/v1/ {
         add_header 'Access-Control-Allow-Origin' '*';
         add_header 'Access-Control-Allow-Credentials' 'true';
         add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
         add_header 'Access-Control-Allow-Headers' '*';
         if ($request_method = 'OPTIONS') {
             return 204;
         }
         proxy_pass http://gap-deploy/version/v1/;
     }
     location ^~ /a/{
         add_header 'Access-Control-Allow-Origin' '*';
         add_header 'Access-Control-Allow-Credentials' 'true';
         add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE';
         add_header 'Access-Control-Allow-Headers' '*';
         if ($request_method = 'OPTIONS') {
             return 204;
         }
         proxy_pass http://gap-deploy/a/;
     }
```



### 2. 场景平台

#### 2.1 前端应用详情

> gitlab组：[gov_app_platform](http://git.timevale.cn:8081/gov_app_platform)
>
> gitlab权限申请： [运维平台申请gitlabe组](http://ops.timevale.cn/#/workpad/new/gitlab)

| 序号 | 应用名称                                                     | 分支                                                         | 备注                                           |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------------- |
| 1 *  | [unify-application-platform-outer-h5](http://git.timevale.cn:8081/gov_app_platform/unify-application-platform-outer-h5) | base/release/vx.x.x                                          | 公众侧H5                                       |
| 2 *  | [unify-application-platform-outer-pc](http://git.timevale.cn:8081/gov_app_platform/unify-application-platform-outer-pc) | base/release/vx.x.x                                          | 公众侧PC（可支持微应用项目-qiankun框架）       |
| 3 *  | [unify-application-platform-backmanage-main](http://git.timevale.cn:8081/gov_app_platform/unify-application-platform-backmanage-main) | base/release/vx.x.x                                          | 后台管理系统（可支持微应用项目-qiankun框架）   |
| 4 *  | [unify-application-platform-inner-main](http://git.timevale.cn:8081/gov_app_platform/unify-application-platform-inner-main) | base/release/vx.x.x                                          | 政务端（可支持微应用项目-qiankun框架）         |
| 5    | [unify-application-platform-outer-main](http://git.timevale.cn:8081/gov_app_platform/unify-application-platform-outer-main) | base/release/vx.x.x                                          | 公众平台门户页（可支持微应用项目-qiankun框架） |
| 6 *  | [local-sign-front](http://git.timevale.cn:8081/esign_gov/local-sign-front/tree/feature/seal-cjyy) | 主分支：feature/seal-cjyy，迭代分支：base/release/vx.x.x     | 本地签                                         |
| 7    | [template-front](http://git.timevale.cn:8081/saas-front/template-front_2.0/tree/feature/gov-seal-cjyy) | (主开发分支，副开发分支+版本号：feature/gov-seal-cjyy-v1.x.x ) | 模板                                           |

#### 2.2. 项目各个环境域名/账号/路由：   

1、测试/稳定环境： [test-signapp.tsign.cn](http://test-signapp.tsign.cn/)

​      测试APP：专有钉钉下载，https://www.dg-work.cn/download/，账号所属租户找后端绑定。

   2、模拟环境：[sml-signapp.tsign.cn](http://sml-signapp.tsign.cn/)

   3、预发环境：[pre-signapp.tsign.cn](http://pre-signapp.tsign.cn/) （浙政钉）

   链接路由：

   1、统一门户首页（暂时静态展示）：/outermain/

   2、公众侧H5页面：/outerh5/

   3、公众侧PC页面：/outerpc/ 

   4、政府侧PC页面：/innermain/ （可支持微应用项目-qiankun框架）

   5、后台管理系统：/backmanagemain/

   6、本地签(签署pc)：/local-sign/pc/sign?flowUuid=0230b88100b3496f9f606e89cb17fe97&accountId=594369d9cbe846df9f388d2d2e6b2ef1&organizeId=

   7、签署h5(签署h5)：sign/egov/sceneApp?flowUuid=0230b88100b3496f9f606e89cb17fe97&accountId=594369d9cbe846df9f388d2d2e6b2ef1&organizeId=

   8、模板控件(PC)：/documents/local/components/set/1a9b2b3db8a841499d2bec188a698ad5?owner=&templateHeaders=xx&apiType=signTemplate&templateTypes=1 



#### 2.3  发布平台对应应用

 1、统一门户首页（暂时静态展示）：http://devops.timevale.cn/app/new/1229

   2、公众侧H5（签署h5）页面：http://devops.timevale.cn/app/new/1387

   3、公众侧PC页面：http://devops.timevale.cn/app/new/1415

   4、政府侧PC页面：http://devops.timevale.cn/app/new/1230

   5、后台管理系统：http://devops.timevale.cn/app/new/1278

   6、本地签(签署pc)：http://devops.timevale.cn/app/new/1416

   7、模板控件(PC)：http://devops.timevale.cn/app/new/1503

#### 2.4 核心业务流程

![image-20230717095643176](https://trial-cdn.esign.cn/upload/e02ef21e-af5a-5e29-9af8-1b3b7360558b!!7-17.png)

##### 2.4.1 场景平台业务熟悉进度表

| 序号 | 平台       | 进度 | 备注 |
| ---- | ---------- | ---- | ---- |
| 1    | 一条主流程 | 100% |      |
| 2    | 管理平台   | 100% |      |
| 3    | 政务平台   | 100% |      |
| 4    | 公众平台   | 100% |      |
| 5    | open api   | 100% |      |
| 6    | 签署       | 100% |      |

#### 2.5 优化列表

| 序号 | 平台                      | 优化点         | 进度 | 备注                                                         |
| ---- | ------------------------- | -------------- | ---- | ------------------------------------------------------------ |
| 1    | 场景平台-模板项目         | 字体切换无效果 | 0    | 场景应用平台政务端-模板管理-新建模板-控件设置，对于控件字符-字体样式的修改，无实时渲染效果。 |
| 2    | 数政pc组件                | 登录组件       | 0    | 登录组件验证码登录，但是显示的是账号[文档](https://design.tsign.cn/esign-design-web/vue-gov/#/esign-biz-login)  [git](http://git.timevale.cn:8081/esign_gov/esign-design-mobile-gov) |
| 3    | 场景平台政务端+管理端登录 | 登录组件       | 0    | 政务端和管理端登录的时候验证码输入错误，点击登录，提示验证码错误后，会自动刷新图形验证码；公众端不会刷新图形验证码，是不是得保持统一好点  ---------  原因： 登录组件验证码登录没有刷新图形验证码的逻辑， this.$refs.loginRef.getGraphCode() |
| 4    | 场景平台                  | 登录组件       | 0    | 获取验证码优化：  是否添加短时间内重复发送验证码             |



### 3.印章平台

#### 3.1 相关资源

##### [3.11 新人指引](http://wiki.timevale.cn:8081/pages/viewpage.action?pageId=132744159)

##### [3.12 平台索引](http://wiki.timevale.cn:8081/pages/viewpage.action?pageId=147446211)

##### [3.13 git仓库和分支](http://wiki.timevale.cn:8081/pages/viewpage.action?pageId=128370613)

##### [3.14 环境部署、项目启动](http://wiki.timevale.cn:8081/pages/viewpage.action?pageId=145143451)

#### 3.2 核心业务流程

![image-20230717095304602](https://trial-cdn.esign.cn/upload/adec43ae-4f02-555f-9c55-1cfaf3e9b60e!!7-17.png)

##### 3.2.1 场景平台业务熟悉进度表

| 序号 | 平台       | 进度 | 备注 |
| ---- | ---------- | ---- | ---- |
| 1    | 一条主流程 | 100% |      |
| 2    | PC - 企业  | 100% |      |
| 3    | PC - 个人  | 100% |      |
| 4    | H5 - 企业  | 100% |      |
| 5    | H5 - 个人  | 100% |      |
| 6    | 监管端     | 100% |      |



## 三、数政1-N

### 1.负责事项

- 开发【流动性开发】 医疗、江西、海南、场景
- 方案评审、设计等相关
- 1-n前端开发同学个人成长
- 1-n扩展点挖掘【对接郁卿】

### 2. 1-n资源情况同步 -- 表格

### 3. 1-n安全扫描问题

### 4. 项目情况

### 5. 资源链接

1. [江西政务服务管理门户](http://ganfutong.jiangxi.gov.cn:30014/api-gateway/common-ucenter-server/oauth2/ssologin?redirectUrl=http://ganfutong.jiangxi.gov.cn:30014/jpaas/appcenter/appmenu/AppDetail?iid=49a701eed01a4508838bd2876831b644)
   1. 账号密码： jgyykf       Jgyykf@12345678

# 前端技能汇总

![前端-学习路线 (1)](https://s3.bmp.ovh/imgs/2023/07/17/21e5aba7171fa830.png)

