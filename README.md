# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 11117ssm足球赛会管理系统

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Kp48e9EtU?p=18)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

足球赛会管理系统工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。足球赛会管理系统的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、用户管理实体图如图4-3所示：

![](/md/blog.014.png)

图4-3用户管理实体图

2、赛事盛况管理实体图如图4-4所示：

![](/md/blog.015.png)

`  `图4-4赛事盛况管理实体图

3、球星介绍管理实体图如图4-5所示：

![](/md/blog.016.png)

`   `图4-5球星介绍管理实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 baomingxinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|200|default NULL|
|zhanghao|varchar|200|default NULL|
|xingming|varchar|200|default NULL|
|xingbie|varchar|200|default NULL|
|lianxishouji|varchar|200|default NULL|
|zhaopian|varchar|200|default NULL|
|bisaibianhao|varchar|200|default NULL|


表4-2 qiuduijieshao表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|200|default NULL|
|qiuduimingcheng|varchar|200|default NULL|
|qiuduijieshao|varchar|200|default NULL|
|zhaopian|varchar|200|default NULL|

表4-3：qiuxingjieshao表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|200|default NULL|
|mingzi|varchar|200|default NULL|
|xingbie|varchar|200|default NULL|
|chushengriqi|varchar|200|default NULL|
|fazhanlicheng|varchar|200|default NULL|
|jiatingbeijing|varchar|200|default NULL|
|zhongdashijian|varchar|200|default NULL|
|huojiang|varchar|200|default NULL|
|zhaopian|varchar|200|default NULL|


表4-4：saishishengkuang表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|200|default NULL|
|tupian|varchar|200|default NULL|
|cansaiqiuyuan|varchar|200|default NULL|
|saishi|varchar|200|default NULL|
|bifen|varchar|200|default NULL|
|bisaixijie|varchar|200|default NULL|
|bisaishijian|varchar|200|default NULL|

表4-5：yonghu表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|200|default NULL|
|zhanghao|varchar|200|default NULL|
|mima|varchar|200|default NULL|
|xingming|varchar|200|default NULL|
|xingbie|varchar|200|default NULL|
|lianxishouji|varchar|200|default NULL|
|lianxiyouxiang|varchar|200|default NULL|
|zhaopian|varchar|200|default NULL|





# 5统详细设计
## 5.1前台首页功能模块
足球赛会管理系统，在系统首页可以查看首页、球队介绍、球星介绍、线下足球赛、论坛信息、个人中心、后台管理、在线客服等内容，如图5-1所示。

![](/md/blog.017.png)

图5-1前台首页功能界面图



`    `用户登录、用户注册，在注册页面可以填写账号、密码、姓名、联系手机、联系邮箱等信息进行注册、登录，如图5-2所示。

![](/md/blog.018.png)

![](/md/blog.019.png)

图5-2用户注册、用户登录界面图

论坛中心，在论坛中心页面通过查看标题、类型、内容等信息进行发布帖子，如图5-3所示。在球星介绍页面通过查看名字、性别、出生日期、发展历程、家庭背景、重大事件、获奖 、照片等信息进行提交操作，如图5-4所示。

![](/md/blog.020.png)

图5-3论坛中心界面图

![](/md/blog.021.png)

图5-4球星介绍界面图

## 5.2管理员功能模块
管理员登录，在登录页面填写用户名、密码等信息进行登录，如图5-5所示。

![](/md/blog.022.png)

图5-5管理员登录界面图

管理员登录进入足球赛会管理系统可以获取个人中心、用户管理、球队介绍管理、球星介绍管理、赛事盛况管理、线下足球赛管理、报名信息管理、系统公告管理、论坛交流、系统管理等信息。

用户管理，在用户管理页面中可以通过获取账号、密码、姓名、性别、联系手机、联系邮箱、照片等内容进行修改、删除，如图5-6所示。还可以根据需要对球队介绍管理进行删除、修改等详细操作，如图5-7所示。

![](/md/blog.023.png)

图5-6用户管理界面图

![](/md/blog.024.png)

图5-7球队介绍管理界面图

球星介绍管理，在球星介绍管理页面中可以获取名字、性别、出生日期、发展历程、家庭背景、重大事件、获奖 、照片等信息，并可根据需要对已有球星介绍管理进行查看、修改或删除等操作，如图5-8所示。

![](/md/blog.025.png)

图5-8球星介绍管理界面图

赛事盛况管理，在赛事盛况管理页面中可以获取图片、参赛球员、赛事、比分、比赛细节、比赛时间等信息，并可根据需要对已有赛事盛况管理进行查看、修改或删除等详细操作，如图5-9所示。

![](/md/blog.026.png)

图5-9赛事盛况管理界面图

线下足球赛管理，在线下足球赛管理页面中可以获取图片、比赛编号、地点、人数、人均费用、时间、备注等内容，并且根据需要对已有线下足球赛管理进行查看，修改或删除等详细操作，如图5-10所示。

![](/md/blog.027.png)

图5-10线下足球赛管理界面图

报名信息管理，在报名信息管理页面中可以查看账号、姓名、性别、联系手机、照片、比赛编号、用户id等内容，并且根据需要对已有报名信息管理进行查看，修改或删除等详细操作，如图5-11所示。

![](/md/blog.028.png)

图5-11报名信息管理界面图

系统公告管理，在系统公告管理页面中可以获取图片、标题、内容等信息，并且根据需要对已有系统公告管理进行查看、修改或删除等详细操作，如图5-12所示。

![](/md/blog.029.png)

图5-12系统公告管理界面图





## 5.3用户功能模块
用户登录进入足球赛会管理系统可以获取个人中心、线下足球赛管理、报名信息管理等内容。如图5-13所示。

![](/md/blog.030.png)

图5-13用户功能界面图

线下足球赛管理，在线下足球赛管理页面中可以获取图片、比赛编号、地点、人数、人均费用、时间、备注等信息，并且根据需要对已有线下足球赛管理进行查看、报名等其他详细操作，如图5-14所示。

![](/md/blog.031.png)

图5-14线下足球赛管理界面图

报名信息管理，在报名信息管理页面中可以获取账号、姓名、性别、联系手机、照片、比赛编号、用户id等信息，并且根据需要对已有报名信息管理进行查看、修改等其他详细操作，如图5-15所示。

![](/md/blog.031.png)

图5-15报名信息管理界面图













