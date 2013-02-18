# ◇ JavaScript公用组件库

##一、现有模块目录

* [base-v1](http://misc.360buyimg.com/lib/js/2012/base-v1.js)
  * pageConfig.*  ====>
  * login         ====>
  * regist        ====>
  * cookie        ====>
  * addToFavorite ====>
  * CookieUtil    ====>
  * search        ====>
* [lib-v1](http://misc.360buyimg.com/lib/js/2012/lib-v1.js)
  * JSON              ====> 
  * livequery         ====> 
  * query             ====> 
  * cookie            ====> 
  * utility           ====> 
  * jmsajax           ====> 
  * trimpath          ====> 
  * getJSONP          ====> 
  * Jdorpdown         ====> 
  * Jtab              ====> 
  * Jlazyload         ====> 
  * Jtimer            ====> 
  * Jslider           ====> 
  * pagination        ====> 
  * jdThickbox        ====> 
  * jdMarquee         ====> 
  * login             ====> 
  * friend            ====> 
  * jdCalcul          ====> 
  * mlazyload         ====> 
  * getrecent         ====> 
  * jdModelCallCenter ====> 
  * autoLocation      ====> 
  * doAttention       ====> 
  * category          ====> 
  * UC                ====> 
  * MCART             ====> 
  * search            ====> 
  * InitSidebar       ====> 
  * InitContrast      ====>  

##二、更合理的组件架构

![ Arch](https://f.cloud.github.com/assets/458894/148785/d2178152-7511-11e2-866b-2d65237e8155.png)

###1. 模块加载「Loader」
优先级最高，页面脚本入口
> Require.js

###2. 全局核心函数「Core」
全局共用函数，所有方法注册到pageConfig命名空间上
>pageConfig, login, regist, cookie, addToFavorite

###3. 第三方类库「Lib」
插件核心依赖类库
> jQuery1.2.6

###4. 组件「Component」
* jQuery plugin `依赖于jQuery插件`

  > livequery, cookie, jmsajax, getJSONP, Jdorpdown, Jtab, Jlazyload, Jtimer, Jslider, pagination, jdThickbox, jdMarquee, login, jdCalcul
* common `不依赖第三方类库的共用模块`

  > JSON, query, utility, trimpath, friend, mlazyload,

###5. 功能模块「Module」
页面级的共用模块，通常很多页面需要调用, 由固定人员维护
> getrecent, jdModelCallCenter, autoLocation, doAttention, category, UC, MCART, search, InitSidebar, InitContrast

