# 果冻影院：萌趣电影票务系统

## 项目简介
果冻影院是一个基于 Vue.js、Express 和 MySQL 构建的电影票务系统。它为用户提供了一个轻松、愉快的在线购票体验，并通过简洁高效的后台管理系统帮助管理员更好地管理电影信息和订单数据。整个系统涵盖了前端展示、后台管理及 API 接口服务，适用于学习与电影票务类网站的开发。

## 项目目录
├── film # 前端页面项目
├── film_admin # 后台管理系统
├── film_api # API接口项目
├── db_film.sql # 数据库初始化文件

## 环境要求
- **Node.js**：建议使用 LTS 版本
- **MySQL**：用于数据存储与管理

## 数据库配置

### 创建数据库
确保 MySQL 已启动并连接，执行以下命令来创建数据库：

```sql
CREATE DATABASE film_db;


导入数据
通过 db_film.sql 文件初始化数据库：
mysql -u root -p film_db < db_film.sql

# 项目启动

## 1. 启动 API 接口
进入 `film_api` 目录，使用 `nodemon` 启动后端接口：

```bash
cd film_api
nodemon app.js


## 启动前端页面
进入 `film` 目录，启动前端项目：

```bash
cd film
npm start

## 启动后台管理系统
进入 `film_admin` 目录，启动后台管理系统：

```bash
cd film_admin
npm start

项目访问
前端页面：访问 http://localhost:8080 以查看电影售票页面。可以切换到移动设备视图，查看适配的移动端页面。
后台管理系统：访问 http://localhost:8081 进入后台管理登录界面。默认账户：admin，密码：admin。
API 接口服务：接口服务运行在 3000 端口，处理前端和后台系统之间的数据交互。







