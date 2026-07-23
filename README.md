# tourismshare
在线旅游记忆管理系统 旅游管理系统 计算机毕业设计

所有源码均本人开发，项目是前后端分离的，所有的项目都具备了完整的业务逻辑，不仅仅局限于基础的增删改查（CRUD）操作，系统亮点众多。

本文注重于计算机毕业设计选题指导，列出题目均有源码， 大家可以去【公众号】(毕业终点站)获取或者加我【qq】(2112698948)提意见(别忘记Star哟)。备注：git

声明：仅用于学习使用，请勿用于任何商业行为！

1.系统非商用，非开源，非无偿。

2.由本人开发，如需源码，请联系以下方式，qq:2112698948。

3.项目有很多，并未全部上传，如果未找到想要的，可直接咨询。

<font style="color:rgb(17, 124, 238);">🎈</font><font style="color:rgb(17, 124, 238);">系统亮点：腾讯地图API，协同过滤算法，可分享链接到扣扣、微博，中国地图，Echarts图形化分析，WebSocket及时通讯；</font>

# <font style="color:rgb(72, 179, 120);">一.系统开发工具与环境搭建</font>
## <font style="color:rgb(38, 38, 38);">1.系统设计开发工具</font>
<font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">后端使用Java编程语言的Spring boot框架</font><font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">项目架构：B/S架构</font><font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">运行环境：win10/win11、jdk17</font>

<font style="color:rgb(38, 38, 38);"></font>



<font style="color:rgb(38, 38, 38);"></font><font style="color:rgb(72, 179, 120);">前端：</font><font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">技术：框架Vue.js；UI库：ElementUI；   
</font><font style="color:rgb(38, 38, 38);">开发工具：Visual Studio Code；</font>

---

<font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(72, 179, 120);">后端:</font><font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">技术：Java语言、mybatis plus、Spring boot框架；   
</font><font style="color:rgb(38, 38, 38);">开发工具：IDEA 2024版本；</font>

---

<font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(72, 179, 120);">数据库：</font><font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">数据库：mysql5.7/8.0 </font><font style="color:rgb(38, 38, 38);">  
</font><font style="color:rgb(38, 38, 38);">数据库工具：Navicat12版本；</font>

---

# <font style="color:rgb(72, 179, 120);">二.系统功能需求分析</font>
在线旅行记忆分享系统分为管理员和用户两大模块，管理员可通过系统标签管理分类标签，可通过数据图形化分析查看景点分布、综合统计，管理用户信息，查看用户的行程，维护景点信息和美食信息，管理系统的广告轮播图封面，及时处理用户反馈，话题管理可推荐热门话题，审核用户发布的话题。用户可以注册登录系统，系统使用协同过滤算法推荐热门景点信息，供用户查看，记忆空间用于存储、编辑个人旅行经历，分享照片、视频等内容，话题交流方便用户参与讨论、分享见解，用户可定制行程，进行打卡，打卡成功后，会自动点亮地图，好友申请和聊天功能支持用户与志同道合的朋友互动交流，反馈申请便于用户提交建议与问题。

根据系统模块分为：
用户管理模块：普通用户用到的主要有注册、登录、查看和修改个人信息、改密码这些功能。管理员则包括查用户信息，对用户信息进行增删改查操作。
景点管理模块：普通用户能浏览景点，查看景点信息详情。按分类筛选、搜索、收藏，还能打卡。管理员对景点信息做增、删、改、查，以及数据维护。
美食管理模块：普通用户可以浏览景点的美食信息。管理员是录入、修改、删除和查询美食信息。
行程管理模块：普通用户能创建、查看、修改、删除行程，还可以把景点加到行程里。用户可以根据自己的出行时间和旅游目标自己规划行程。系统会通过地图点亮的方式展示旅游足迹。管理员可管理行程，查看行程明细信息，可对不合规的行程进行删除。
记忆分享模块：普通用户可以用它创建记忆空间、关联旅行故事、上传旅行图片、编辑分享内容，还能查看个人的旅行记录，支持添加记忆空间的成员，为成员设置权限。用户可以把旅行中的见闻、感受和照片整理保存下来，实现旅行经历的数字化记录和展示。浏览用户的旅行故事，可通过旅行故事添加其他用户为好友，进行在线交流。
互动交流模块：普通用户可以围绕景点、美食和旅行经历发话题、参与讨论、点赞互动，可进行关注话题的作者。管理员是管理话题、评论、监管互动内容，以及处理违规信息。
推荐与统计模块：普通用户能看到景点推荐、热门内容展示和个性化内容参考等。系统会根据景点热度、标签信息或用户兴趣，给用户推荐相应的旅游内容，帮用户更高效地找到感兴趣的信息。管理员包括景点浏览量、收藏量、点赞量、打卡量的统计，以及相关业务数据分析。
反馈管理模块：普通用户可以提交对平台的建议。管理员可通过反馈管理及时处理用户意见和系统问题。
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660203052-134308f9-539d-4e50-b277-975fad7bd570.png)

# <font style="color:rgb(72, 179, 120);">三.系统实现（部分截图）</font>
## 3.1 用户
### 3.1.1 首页
![](https://cdn.nlark.com/yuque/0/2025/jpeg/45326128/1761660209852-423c7253-3fa6-45ad-a349-7650d4b38538.jpeg)

### 3.1.2 景点列表
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660216256-30b88d6b-ca8b-4394-bbbf-9935eea5b235.png)

### 3.1.3景点详情
![](https://cdn.nlark.com/yuque/0/2025/jpeg/45326128/1761660218537-edffe2e3-daaf-43f0-babc-6074db739b9c.jpeg)

### 3.1.4 旅行故事
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660220811-6e8d375f-7f95-4f57-9a2b-c34695ea408b.png)

### 3.1.5故事详情
![](https://cdn.nlark.com/yuque/0/2025/jpeg/45326128/1761660223562-abf6e7f3-1308-47a1-bcc5-80115e99326f.jpeg)

### 3.1.6 话题交流
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660226550-1d6e7235-1540-4220-b6f8-4b41c15b2999.png)

### 3.1.7 话题详情
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660229009-bb4ff5c5-1828-4609-a178-5208602e945d.png)

### 3.1.8 去过的省份
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660232400-f4da8b6d-4453-4ba2-9e5e-3bec386c16a2.png)

### 3.1.9 好友申请
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660234482-cb3a25d3-1353-49b1-a311-624ce4a07531.png)

### 3.1.10 好友聊天
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660237102-479a4538-a72b-4e69-813f-4b8f69fde347.png)

### 3.1.11 定制行程
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660239652-811f0215-b499-4e37-849a-0d8a4dfc6496.png)

### 3.1.12 行程明细
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660245483-eab52e4b-46ab-4260-b02f-1dbeaf6b24d8.png)

### 3.1.13 线路图
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660248414-c5d7f82c-8dac-414c-8099-deea18258396.png)

### 3.1.14 个人中心
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660250221-2dadff41-7079-4e29-9e5e-3a88f63e0f93.png)

### 3.1.15 我的游记打卡
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660253988-6673d41b-b335-4d54-96ec-74901e3c379d.png)

### 3.1.16 我的记忆空间
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660256788-480087e8-3996-49aa-a70d-d390394f37c9.png)

## 3.2 管理员
### 3.2.1 用户信息
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660259271-6f0fb8e2-0c79-4804-896e-25d667bfb3a5.png)

### 3.2.2 话题信息
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660263434-97d37c5f-b7b3-4203-9480-e8cabb16338a.png)

### 3.2.3 话题综合分析
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660267019-fb39b637-da37-4e6f-aa7e-015c5a6c2f95.png)

### 3.2.4 反馈信息
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660270312-dcdf25df-996c-4cec-b941-ea5a6b4e02d8.png)

### 3.2.5 景点信息
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660272764-ba7d3cf7-1d52-4d1b-9d40-2a8897dfbb4d.png)

### 3.2.6景点打卡
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660274991-f2f2230d-3390-4006-a705-eb5c7dc57917.png)

### 3.2.7 美食
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660290586-085e364e-d39b-481b-ab78-bfe331af25ef.png)

### 3.2.8 景点统计
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660293540-3eb6198c-ae32-4c9c-b609-dd98c4c15fd7.png)

### 3.2.9 行程
### ![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660297056-48239760-416c-4986-b63b-8b28108bb7b2.png)
### 3.2.10 综合统计
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660302136-e3434371-34e3-4bee-a43f-09cf07ec005a.png)

### 3.2.11 系统标签
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660304918-12dde591-4a99-4e15-9c8e-80e6a6962206.png)

# <font style="color:rgb(72, 179, 120);">四、系统代码结构截图</font>
## <font style="color:rgb(38, 38, 38);">4.1 前端</font>
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660307530-ca053825-cbdf-4ca8-a979-c2cb49879232.png)

## 4.2后端
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660309777-dcc9e85a-6848-4a33-8b78-9b3d74211aa7.png)

## 4.3 数据库
![](https://cdn.nlark.com/yuque/0/2025/png/45326128/1761660311629-c609201d-87da-4f97-b122-7d5bc48b122b.png)

# <font style="color:rgb(72, 179, 120);">五.</font><font style="color:rgb(26, 173, 25);">系统代码结构截图</font>
<font style="color:rgb(0, 0, 0);">1.系统非商用，非开源，非无偿。</font>

<font style="color:rgb(0, 0, 0);">2.由本人开发，非简单增删改查操作，业务逻辑完整。</font>

<font style="color:rgb(0, 0, 0);">3.项目有很多，并未全部上传，如果未找到想要的，可直接咨询。</font>

