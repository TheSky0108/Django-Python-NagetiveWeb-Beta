# Django-Pyhton-NagetiveWeb-Beta
基于Django2.0.6和Python3.5.3类似于知乎问答社区平台

## 主要功能：
- 文章发布、编辑、点赞、点怼、标注标签、分类、评论、收藏、打赏、举报、二维码分享
- 专题发布、编辑、点赞、点怼、标注标签、分类、评论、收藏、打赏、举报、二维码分享
- 支持文章、专题、点名的标题和全文内容搜索，需要手动选择搜索板块。
- 支持文章、专题按照推荐度、关注度、热度、发布时间排序。
- 支持用户注册、用户头像设置、更改，用户基本信息录入、编辑功能。
- 支持用户主页显示功能：发布的文章、发布的专题、评论过的文章专题、赞过的文章专题、收藏的文章、关注的专题、围观的点名、关注的用户、粉丝
- 评论功能：支持评论文章、专题、评论。
- 点赞/怼功能：支持文章、专题、评论的点赞/怼功能。
- 侧边栏3个区域：功能区，分类区，推荐用户区，后期加入热点标签云功能。
- 支持用户登录信息加密功能，通过AES加密实现，秘钥和偏移参数可在admin 后台设置。
- 支持`Redis`缓存，支持缓存自动刷新，支持设定在admin后台设置刷新延迟时长。
- 后期加入关注的专题更新或者收到评论回复和点名时候通过预留邮箱提醒。

## 安装
使用pip安装必要第三方库：  

`asn1crypto      0.24.0` 
`Django          2.0.6`  
`django-appconf  1.0.2`  
`django-ckeditor 5.6.1`  
`django-imagekit 4.0.2`  
`django-redis    4.10.0` 
`image           1.5.24` 
`oscrypto        0.19.1` 
`pip             19.0.3`
`sqlparse        0.3.0` 
`uWSGI           2.0.18`

### 配置
配置都是在`setting.py`中.部分配置迁移到了后台配置中。

`bin`目录是在`linux`环境中使用`Nginx`+`Gunicorn`+`virtualenv`+`supervisor`来部署的脚本和`Nginx`配置文件.可以参考我的文章:

>[使用Nginx+Gunicorn+virtualenv+supervisor来部署django项目](https://www.lylinux.org/%E4%BD%BF%E7%94%A8nginxgunicornvirtualenvsupervisor%E6%9D%A5%E9%83%A8%E7%BD%B2django%E9%A1%B9%E7%9B%AE.html)

有详细的部署介绍.


## 运行
 先生成测试sqlite
    python manage.py makemigrations
    python manage.py migrate
 创建超级用户
    python manage.py createsuperuser
 收集静态文件
    python manage.py collectstatic
 再runserver
    python manage.py runserver 0:8000

 浏览器打开: http://127.0.0.1:8000/  就可以看到效果了。

 有任何问题欢迎提Issue,或者将问题描述发送至我邮箱 `616604060@qq.com`.我会尽快解答.推荐提交Issue方式.  
 
 ---
 ## 致大家🙋‍♀️🙋‍♂️
 感谢大家不吝留下一颗小星星  
🙏🙏🙏
