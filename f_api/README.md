电影管理系统 API
项目概述
这是一个基于 Express 框架的电影管理系统后端接口，提供电影信息的增删改查（CRUD）功能。项目与 MySQL 数据库进行交互，支持管理员操作电影数据和用户管理。

项目目录结构
csharp
复制代码
|-- .gitignore          # Git 忽略的文件
|-- app.js              # 启动文件
|-- package.json        # 项目描述文件，包含依赖及启动配置
|-- README.md           # 项目介绍文件
|-- bin/                # 存放可执行文件
|   |-- www             # 项目启动文件
|-- db/                 # 数据库连接配置文件
|   |-- db.js           # 数据库连接及配置
|-- public/             # 静态资源文件夹
|   |-- images/         # 存放项目图片资源
|       |-- admin/      # 管理员图片
|       |-- avatar/     # 用户头像
|       |-- movie/      # 电影海报
|-- routes/             # 路由文件
|   |-- index.js        # 路由配置文件
|-- util/               # 工具库
|   |-- util.js         # 工具函数
|-- views/              # 视图文件夹
|   |-- error.ejs       # 错误页面
|   |-- index.ejs       # 首页视图
启动前准备
1. 安装 MySQL
确保已经安装并运行 MySQL 数据库，使用以下命令创建数据库并导入数据。

2. 导入数据库
执行以下步骤来准备数据库：

创建一个新的数据库 db_film：

sql
复制代码
CREATE DATABASE db_film;
导入数据库结构和数据文件：
下载并导入 db_film.sql 文件，或者可以选择根据自己的需求手动创建表结构和数据。

3. 配置数据库连接
修改 db/db.js 文件中的数据库配置，确保数据库连接信息正确：

js
复制代码
module.exports = {
  host: 'localhost',
  user: 'root',        // 数据库用户名
  password: '',        // 数据库密码
  database: 'db_film'  // 数据库名称
};
启动项目
在项目根目录下，执行以下命令来安装所需的依赖：

bash
复制代码
npm install  # 安装项目依赖
使用 nodemon 启动项目：

bash
复制代码
nodemon app.js  # 启动服务器
访问项目
在浏览器中访问 http://localhost:3000/，如果看到 Express 默认启动页面，说明项目已经成功启动。

常见问题
无法连接数据库： 请检查 db/db.js 配置中的数据库用户名、密码和数据库名称是否正确。
端口被占用： 如果端口 3000 被占用，可以在 app.js 中修改端口号。