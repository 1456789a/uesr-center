# uesr-center
用户中心后台
## 技术选型

前端：三件套 + React + 组件库 Ant Design + Umi + Ant Design Pro（现成的管理系统）

后端：

- java
- spring（依赖注入框架，帮助你管理 Java 对象，集成一些其他的内容）
- springmvc（web 框架，提供接口访问、restful接口等能力）
- mybatis（Java 操作数据库的框架，持久层框架，对 jdbc 的封装）
- mybatis-plus（对 mybatis 的增强，不用写 sql 也能实现增删改查）
- springboot（**快速启动** / 快速集成项目。不用自己管理 spring 配置，不用自己整合各种框架）
- junit 单元测试库
- mysql 数据库

### 自动生成器的使用

MyBatisX 插件，自动根据数据库生成：

- domain：实体对象
- mapper：操作数据库的对象
- mapper.xml：定义了 mapper 对象和数据库的关联，可以在里面自己写 SQL
- service：包含常用的增删改查
- serviceImpl：具体实现 service



## 前端框架介绍

### Ant Design Pro（Umi 框架）权限管理

- app.tsx：项目全局入口文件，定义了整个项目中使用的公共数据（比如用户信息）
- access.ts 控制用户的访问权限



获取初始状态流程：首次访问页面（刷新页面），进入 app.tsx，执行 getInitialState 方法，该方法的返回值就是全局可用的状态值。
