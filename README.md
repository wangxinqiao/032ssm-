# 032ssm企业人事管理系统

## 介绍
企业人事管理系统，可以实现简单的企业内部的管理.

源码获取：[ **点此获取** ](http://www.shuyue.fun/index.php?type=productinfo&id=133)

## 软件功能
主要有管理员、人事专员、员工三种角色。
> 管理员功能：登录、分发工资、管理其他角色账号  
> 员工功能：注册、登录、打卡、查看工资、请假  
> 人事专员：登录、查看员工信息列表、查看(编辑)考勤情况、请假审批

## 使用说明
1.  `management.sql` 为数据库文件,请将数据库文件导入,或以代码方式加载进mysql数据库中,如果内容为空,请务必在`user_login`表种添加一个 `userType`=0 的用户,此用户为 `超级管理员` .
2.  `out/artifacts/management_war2` 文件夹内为导出的war文件,存放在tomcat即可在只启动tomcat时也可以使用.
3.  运行成功后，在浏览器中输入地址：http://localhost:8080/userLogin/login 使用管理员账号登录，管理员账号: `admin` 密码: `admin`，人事专员账号：renshi  密码：renshi 普通用户：a  密码：a

### 关于数据库配置
`management/ src / main / resources / applicationContext.xml` 此文件为spring配置文件,下面部分代码为数据库连接部分,请将这四个内容改为自己机器所对应的信息即可
~~~Java
<bean id="dataSource" class="com.mchange.v2.c3p0.ComboPooledDataSource">
        <property name="driverClass" value="com.mysql.jdbc.Driver"/>
        <property name="jdbcUrl" value="jdbc:mysql://localhost:3306/management"/>
        <property name="user" value="root"/>
        <property name="password" value="root"/>
</bean>
~~~

## 软件版本
- 系统版本:  
    > Windows10 
- 软件环境:  
    > IDEA/Eclipse  
> Tomcat 8.0以上  
> Mysql 5.0以上，推荐5.7； 注：8.0不可使用；  

## 运行截图
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221508_eb6b5563_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221522_bed4c5db_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221532_acac7c84_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221543_9fa67939_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221553_2c42fee7_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221604_e6fb805c_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221614_cb16210d_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221625_9dec06ae_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0315/221633_b6252d04_863230.png "屏幕截图.png")
