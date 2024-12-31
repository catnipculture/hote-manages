> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

​

后台：

1.登录：输入账号、密码，即可登录。

2.套房管理：可对房间房型进行管理。

3.入住管理：可对客户入住状态进行管理。

4.订单管理：对用户已提交的订单进行管理。

5.员工管理：对酒店员工进行管理。 6.评论管理：对用户评论进行管理。

前台：

1.登录：输入账号、密码，即可登录。

2.套房预订：用户可以通过浏览套房进行了解并在线预订。

3.酒店详情：用户可以查询酒店的政策与设施，以及网友评价。

4.订单中心：用户可以查询自己的订单信息。

5.个人信息：编辑修改个人信息

# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA;

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS;

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目

6.数据库：MySql5.7/8.0等版本均可；

# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：Spring Boot+ Mybatis +VUE

# 使用说明

1.使用Navicat或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件；

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目；

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq

源码地址：[http://www.codegym.top](http://www.codegym.top/)

其它问题请关注公众号：**IT小舟**,关注后发送消息即可，都会给您回复的。若没有及时回复请耐心等待，通常当天会有回复

# 运行截图

## 文档截图

![img](https://img-blog.csdnimg.cn/img_convert/da3b2a42b6abcba4ec7e228f703dd669.png)

![springboot221酒店管理系统1](https://img-blog.csdnimg.cn/img_convert/145c12e570e7898528baa6203e9f408b.png)

![springboot221酒店管理系统2](https://img-blog.csdnimg.cn/img_convert/b84114bf9ef43fcd961cb3671a0ff2c7.png)

![springboot221酒店管理系统3](https://img-blog.csdnimg.cn/img_convert/cb31bc770fa8e7be7463935bdb0981ae.png)

![springboot221酒店管理系统4](https://img-blog.csdnimg.cn/img_convert/a516011948ec4ee68df70d5f63ae0f21.png)

### 代码

```
    public Boolean deleteMenu(Integer menuId) {
        if (menuId == null) {
            throw new BizException("菜单ID不能为空");
        }
        MenuDO menuDO = menuMapper.selectById(menuId);
        if (menuDO == null) {
            throw new BizException("菜单不存在");
        }
        menuDO.setDataStatus(0);
        int res = menuMapper.updateById(menuDO);
        return res > 0;
    }

```
