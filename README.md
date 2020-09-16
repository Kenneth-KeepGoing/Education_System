
# 使用技术
IOC容器：Spring

Web框架：SpringMVC

ORM框架：Mybatis

数据库:：Mysql

安全框架：Shiro

日志：log4j

前端框架：Bootstrap 、 jQuery 、 JSP

开发平台：Intellij IDEA 2020.1

项目管理工具：Maven

# 功能模块介绍

项目目录结构

    └───src
        ├───main
        │   ├───java
        │   │   └───com
        │   │       └───system
        │   │           ├───controller
        │   │           │   │   AdminController.java
        │   │           │   │   LoginController.java
        │   │           │   │   RestPasswordController.java
        │   │           │   │   StudentController.java
        │   │           │   │   TeacherController.java
        │   │           │   │
        │   │           │   └───converter
        │   │           │           CustomDateConverter.java
        │   │           │
        │   │           ├───exception
        │   │           │       CustomException.java
        │   │           │       CustomExceptionResolver.java
        │   │           │
        │   │           ├───mapper
        │   │           │       CollegeMapper.java
        │   │           │       CollegeMapper.xml
        │   │           │       CourseMapper.java
        │   │           │       CourseMapper.xml
        │   │           │       CourseMapperCustom.java
        │   │           │       CourseMapperCustom.xml
        │   │           │       RoleMapper.java
        │   │           │       RoleMapper.xml
        │   │           │       SelectedcourseMapper.java
        │   │           │       SelectedcourseMapper.xml
        │   │           │       StudentMapper.java
        │   │           │       StudentMapper.xml
        │   │           │       StudentMapperCustom.java
        │   │           │       StudentMapperCustom.xml
        │   │           │       TeacherMapper.java
        │   │           │       TeacherMapper.xml
        │   │           │       TeacherMapperCustom.java
        │   │           │       TeacherMapperCustom.xml
        │   │           │       UserloginMapper.java
        │   │           │       UserloginMapper.xml
        │   │           │       UserloginMapperCustom.java
        │   │           │       UserloginMapperCustom.xml
        │   │           │
        │   │           ├───po
        │   │           │       College.java
        │   │           │       CollegeCustom.java
        │   │           │       CollegeExample.java
        │   │           │       Course.java
        │   │           │       CourseCustom.java
        │   │           │       CourseExample.java
        │   │           │       PagingVO.java
        │   │           │       Role.java
        │   │           │       RoleExample.java
        │   │           │       Selectedcourse.java
        │   │           │       SelectedCourseCustom.java
        │   │           │       SelectedcourseExample.java
        │   │           │       Student.java
        │   │           │       StudentCustom.java
        │   │           │       StudentExample.java
        │   │           │       Teacher.java
        │   │           │       TeacherCustom.java
        │   │           │       TeacherExample.java
        │   │           │       Userlogin.java
        │   │           │       UserloginCustom.java
        │   │           │       UserloginExample.java
        │   │           │
        │   │           ├───realm
        │   │           │       LoginRealm.java
        │   │           │
        │   │           └───service
        │   │               │   CollegeService.java
        │   │               │   CourseService.java
        │   │               │   RoleService.java
        │   │               │   SelectedCourseService.java
        │   │               │   StudentService.java
        │   │               │   TeacherService.java
        │   │               │   UserloginService.java
        │   │               │
        │   │               └───impl
        │   │                       CollegeServiceImpl.java
        │   │                       CourseServiceImpl.java
        │   │                       RoleServiceImpl.java
        │   │                       SelectedCourseServiceImpl.java
        │   │                       StudentServiceImpl.java
        │   │                       TeacherServiceImpl.java
        │   │                       UserloginServiceImpl.java
        │   │
        │   ├───resources
        │   │   │   log4j.properties
        │   │   │   mysql.properties
        │   │   │
        │   │   ├───mybatis
        │   │   │       mybatis.cfg.xml
        │   │   │
        │   │   └───spring
        │   │           applicationContext-dao.xml
        │   │           applicationContext-service.xml
        │   │           applicationContext-shiro.xml
        │   │           applicationContext-trsaction.xml
        │   │           springmvc.xml
        │   │
        │   └───webapp
        │       │   login.jsp
        │       │
        │       ├───css
        │       │       bootstrap-theme.css
        │       │       bootstrap-theme.min.css
        │       │       bootstrap.css
        │       │       bootstrap.min.css
        │       │
        │       ├───fonts
        │       │       glyphicons-halflings-regular.eot
        │       │       glyphicons-halflings-regular.svg
        │       │       glyphicons-halflings-regular.ttf
        │       │       glyphicons-halflings-regular.woff
        │       │       glyphicons-halflings-regular.woff2
        │       │
        │       ├───images
        │       │       a.jpg
        │       │
        │       ├───js
        │       │       bootstrap.js
        │       │       bootstrap.min.js
        │       │       jquery-3.2.1.min.js
        │       │       npm.js
        │       │
        │       └───WEB-INF
        │           │   web.xml
        │           │
        │           └───jsp
        │               │   error.jsp
        │               │   success.jsp
        │               │
        │               ├───admin
        │               │       addCourse.jsp
        │               │       addStudent.jsp
        │               │       addTeacher.jsp
        │               │       editCourse.jsp
        │               │       editStudent.jsp
        │               │       editTeacher.jsp
        │               │       menu.jsp
        │               │       passwordRest.jsp
        │               │       showCourse.jsp
        │               │       showStudent.jsp
        │               │       showTeacher.jsp
        │               │       top.jsp
        │               │       userPasswordRest.jsp
        │               │
        │               ├───student
        │               │       menu.jsp
        │               │       overCourse.jsp
        │               │       passwordRest.jsp
        │               │       selectCourse.jsp
        │               │       showCourse.jsp
        │               │       top.jsp
        │               │
        │               └───teacher
        │                       mark.jsp
        │                       menu.jsp
        │                       passwordRest.jsp
        │                       showCourse.jsp
        │                       showGrade.jsp
        │                       top.jsp
        │
        └───test
            └───java
                └───com
                    └───system
                        ├───mapper
                        │       CourseMapperCustomTest.java
                        │       StudentMapperCustomTest.java
                        │       StudentMapperTest.java
                        │       TeacherMapperCustomTest.java
                        │       UserloginMapperCustomTest.java
                        │
                        └───service
                            └───impl
                                    CourseServiceImplTest.java
                                    SelectedCourseServiceImplTest.java
                                    StudentServiceImplTest.java
                                    TeacherServiceImplTest.java
                                    UserloginServiceImplTest.java
    
    
 
### 1、登录模块功能
使用Shiro权限管理框架，实现登录验证和登录信息的储存，根据不同的登录账户，分发权限角色，对不同页面url进行角色设置
![image](http://imgsrc.baidu.com/forum/pic/item/5a8d9e1c8701a18b1ea553e4942f07082938fead.jpg)
### 2、管理员模块功能
管理员可对 教师信息、学生信息、课程信息 进行 增删改查 操作，管理员账户，可以重置非管理员账户的密码
* 课程管理：当课程已经有学生选课成功时，将不能删除
* 学生管理：添加学生信息时，其信息也会添加到登录表中
* 教师管理：同上
* 账户密码重置：
* 修改密码：
![image](http://imgsrc.baidu.com/forum/pic/item/96499412c8fcc3ce82d37e989845d688d53f20e7.jpg)
![image](http://imgsrc.baidu.com/forum/pic/item/e8829bfd5266d0165ce22a839d2bd40734fa357f.jpg)
![image](http://imgsrc.baidu.com/forum/pic/item/004a5ef082025aafccfdca60f1edab64024f1a23.jpg)
### 3、教师模块功能
教师登陆后，可以获取其，教授的课程列表，并可以给已经选择该课程的同学打分，无法对已经给完分的同学进行二次操作
* 我的课程
* 修改密码
![image](http://imgsrc.baidu.com/forum/pic/item/db884fd9f2d3572c8f662b778013632763d0c36b.jpg)
![image](http://imgsrc.baidu.com/forum/pic/item/7e08dedeb48f8c549e49728430292df5e1fe7f58.jpg)
![image](http://imgsrc.baidu.com/forum/pic/item/7c6d7482b2b7d0a2eb88b336c1ef76094a369ab6.jpg)
### 4、学生模块功能
学生登录后，根据学生信息，获取其已经选择的课程，和已经修完的课程
* 所有课程: 在这里选修课程，选好后，将会自动跳转到已选课程选项
* 已选课程: 这里显示的是，还没修完的课程，也就是老师还没给成绩，由于还没有给成绩，所以这里可以进行退课操作
* 已修课程: 显示已经修完，老师已经给成绩的课程
* 修改密码:
![image](http://imgsrc.baidu.com/forum/pic/item/8f86a0b1cb1349541f345ecf5c4e9258d0094ac8.jpg)
![image](http://imgsrc.baidu.com/forum/pic/item/4f0822b30f2442a7871a4b0edb43ad4bd01302da.jpg)
![image](http://imgsrc.baidu.com/forum/pic/item/821ad6f2b21193136cb8481b6f380cd790238d78.jpg)
