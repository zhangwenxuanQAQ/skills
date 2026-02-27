---
name: backend-dev
description: 后端代码开发是需要遵循（包括Restful API设计，数据库设计，逻辑代码生成）
---

##使用场景
- 创建RESTFUL API
- 设置数据库连接以及数据模型
- 数据库交互
- 实现用户管理以及登录认证
- 集成第三方服务等

##技术栈
- Python 3.10+
- Flask （后端框架）
- Peewee （数据库管理）
- Restful API
- Flasgger （Swagger 文档）
- Gunicorn 部署

##要求
1. API 设计
- 接口返回需要封装成统一json格式 （包含code , data , messages字段）
- 新增删除用POST，更新用PUT，查询用GET
- 需要验证所有入参
- 需要对接口进行流量限制（比如每分钟限制单用户多少次访问，可用slowapi）
- 需要设计统一的错误码
- 需要生成Swagger文档

2.数据库
- 项目启动时需要根据最新的数据库模型进行数据库结构更新（不需要抛异常）
- 需要使用连接池
- 新增删除更新需要使用事务

3. 必要要有README.md和CHANGELOG.md文件
- README.md 需要对项目进行描述
- CHANGELOG.md 需要对重要功能以及版本更新进行记录

##文件结构
├──app/  主应用包
    ├── database/           # 数据库管理（数据模型，数据库连接）
    ├── conf/           # 配置文件
    ├── services/           # 业务实现
    ├── utils/          # 工具包
    ├── api/          #  接口包
    ├── test/          # 单元测试和集成测试
├──server_run.py  开发环境入口
├──server_wsgi.py  生成环境入口
