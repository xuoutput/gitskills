# gitskills
Creating a new branch is quick & simple.
add merge

wandan  zhe
## this is markdown format


## install yarn and parcel
instead of using npm and webpack

> although parcel is easy to use, webpack is need to learn.
> a gitbook about webpack 
> [深入浅出 Webpack](http://webpack.wuhaolin.cn/)

## PWA?


## webpack+es6+vue2


## pat lintcode leetcode

## using hexo

> fail to put the blog on git, still 404

## git command


## 可以写个关于chrome插件的博客水一下

##  in the middle

## tomorrow is a good day

## github desktop false

## 刷题

## 刷题前的准备

## 完善markdown语法文章

## 开始刷题PAT

## nodejs es6

## vue2

## python

## vue基础回顾了一遍

## vue-router and vuex

## vue 进阶

## vue demo

## vue-cli 跑一下例子 

## vueCnodeJS是个好例子

## 视频知识

## potplayer修改 这个有个单独的madvr文件

## vuex 分离 es5 常量
actions只有commit到mutations上  mutations才是改变state的唯一途径

## mongoDB & koa2

## vue2+koa2+mongodb

## ubuntu 梅花

## 抢红包

## 跨

## ikcamp

## 水

## koa2 & koa-router & bodyparamer

## zeal API大全

## tmux

## 课表

## js & tmux

## vue-svg-icon & 

## 刷题PAT

## 离散数学好烦啊

## 高软&多媒体

## 人工智障AI

## vue+koa2+mongodb

## successful run vue-blog

## 整理vue-blog

## 整理vue-blog所有用到依赖

##  fastclick font-awnsome simplemde marked highlight.js mongoose md5 moment lru-cache require-dir

## 看懂代码吧 

## node模块 http fs quertString url 

## 复习js

## 准备resume

## 中期资料

## 完善工程实践啊

## js 高程 5章

## 工程实践登录

## hexo blog维护下

## IT service

## jwt

## 6

## cnode

## 下了一堆cnode

## tensorflow

## blue

## flex真好用

## 用vue axios显示数据

## pagination

## vuex复习

## beforeRouteUpdate

## 分页问题是因为page用了函数里面的 没有改动vue对象的page,而axios的是vue对象的page 所以 一直出问题,现在好了 就剩下loading效果

## loading完成 完成首页tab分类

## 昨天一直没哟请求成功是因为我的下拉框value写成valut了  然后报错的err信息再network 的preview中可以看到  不要到时候catch一个err  具体点到

## 关于vuejs社区没哟修改主题的API接口,可以利用原来查看主题详情来判断  里面有个loginname  显示有没有编辑和删除按钮,然后点击编辑跳转到 新建主题页面,把原来的主题内容get过来 填入 这不就达到了  修改, 之后在post过去,只不过即使在body中带了 topic_id 还是会新建一个topic,这个有问题 .评论丢了

## 还是借用cnode的编辑接口样式呗 同理设置个删除的

## 新建了一个删除主题的api 然后做了个confirm

## 完成主题详情页的评论的以及对评论的回复,对修改和删除评论 以及评论的嵌套展示,点赞完成 就是变色提醒没做

## 收藏主题 也没开始

## 主题收藏用到 3个api 一个加入一个取消收藏,还有一个是本用户详情中有collect_topics  .每次比较本用户收藏的主题中和当前主题id是否一致

## 如何保证异步和同步顺序  当然vuex可以

## AI报告 离散作业

## 将API接口单独抽离出来

## 回顾一下koa的使用 找到一个MOCK API 工具 淘宝的RAP2

## 完全没搞明白RAP2这个接口工具怎么get post到一个interface

## 浙江执御

## AI captcha

## vue koa2中router restfull接口

## 成功用mongoose连上mongodb并且可以使用post来传入数据并存入. 有要注意各是 find和findone区别,前者返回对象数组,后者就是一个对象,并且后者doc一条,若是用doc.username会造成对null对象使用无效property的错误. 直接用if(doc)来判断callback中这条记录是否存在于数据库中.

## save完后 并不能返回所需要的数据data 用了await也不行 应该哪里有问题

## 首先还是先findone,这个和写入的值+save不冲突,所以分开写好了,其次是callback, 当然先要await,然后callback中不要写返回值, 拿出去写就没问题了 正常返回

```
    postSignout: async (name, pwd) => {
        let data 

        //  先find下 有没有 还是用findone好了,没找到就报错,找到了else. 这里报错原因找到了,见下面doc.name
        var user =  await User.findOne({username: name}, function (err, doc) {
            if (err) {
                return console.error(err)
            } 
            // 首先是null没找到哦啊, 这样才能存入新的
            console.log('doc='+doc)
        })
        console.log('user='+user);
        console.log('name='+name);
        console.log('pwd='+pwd);
        if (!user) {
            var userInfo = new User({
                username: name,
                password: pwd
            })                           
            // doc.save(function (err, doc) {  同理用了doc报错哦,而且存的是userInfo而不是doc
            await userInfo.save(function (err, userInfo) {
                if (err) {return console.err(err)}
                //  问题 写是肯定写入数据库了 但就是 设置一个返回值 没有返回  应该是异步操作的问题,访问数据库慢啊
                // 把return放出去就可以正常返回了
                // return data = {
                //     status: 1,
                //     data: {
                //         success: true
                //     }                        
                // } 
            })                
            return data = {
                status: 1,
                data: {
                    success: true
                }                        
            } 
        } else {
            return data = {
                status: 0,
                data: {
                    success: false                
                }
            }
        }
       

    } 
```


## 完成用户的signout和signin还差 完善信息和改密码

## 完成了修改密码的post

## 完成vue-cnode的build 用了nginx, tensorboard更新使用配套的TensorFlow1.3+ 用pip3 install --upgrade tensorflow

## 前端面经初步整理

## 算法

## 做一个可视化数据结构??  AI数据分析 个人博客

## 终于完成shell_sort

## 凉 express+mongodb做restfull接口

## linux ubuntu上安装软件3种方法

## 转投linux上编程

## linux命令 export 

## 多媒体复习完 linux第二章完

## 做个思维导图吧

## 离散

## javascript shell vim
## javascript数据结构

## js第3章整理

## js 4 5章

## js 整理 剑指offer

## js 第6章

## js整理到第6章

## js 整理到第6章继承

## 面试tradeshift 和 zoom
## 碧格网 大禹? 麦科田
## madcaptian 意向
## ts bigone
## cico qiniu 看完HTML http 跨域 web安全

## css
## css看完 继续js  其中csstab用input radio name + checked display:none
## ts 论文过程



## es6 nodejs 

## es6 let const 块级作用域 set map 函数 箭头函数 |  promise class
## es6 js6 OO和继承

## js 第7章
[How to implement a PL](http://lisperator.net/pltut/)
## js 13事件,nodejs
## qiniu
## parser
## compiler
## nodejs n-blog
## n-blog
## 差部署
## discrete
## js刷题 Go
## go
## 刷完题 然后接着搞 先搭好环境
## 房价 Array & Object的扩展 es6
## es6 module ubuntu 18.04安装
## ubuntu18.04放弃了
## manjaro
## pacmam
## 7  
## hb
## vsc shotcuts
## git
## css git 剩余
## css  chapter1-3
## 文档
## xiaolongxia css
## css3  bianyi
## 最后的棒棒
## bb
## vsc  生门
## 导论
## 结题文档
## discrete
## compile 8 discrete 6
## 概率
## 培训
## ll
## kde
##  图解git learninggitbranch
## 离散考完  KDE基本有些掌握, git的 learninggitbranch
## kde配置好
## 编译
## 编译看完
## 搜狗拼音搞定
