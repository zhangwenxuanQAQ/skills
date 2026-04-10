---
name: file-upload
description: 知识库数据集文档上传功能前后端代码实现
---

## 使用场景
- 知识库详情页面-数据集文档上传
- 需要参考RAGFLOW项目的document_app.py代码中的upload接口以及FileService的上传文档逻辑， ragflow项目源码在本系统目录 F:\project\ragflow-0.24.0

## 技术栈
- Rustfs
- Ragflow

## 需要满足如下要求
1.扫描ragflow项目工程， 参考RAGFLOW项目的document_app.py代码中的upload接口以及FileService的上传文档逻辑。
2.上传时需要将文档上传到rustfs中，上传路径到文件系统的路径为： 知识库id/文件名称
3.如果文件目录中有相同文件则需要在文件名后面加（递增数字）： 比如上传文件test.docx,如果存在则需要修改为test_(1).docx, 如果存在test_(1).docx则修改为test_(2).docx。 以此类推
4.上传时需要从文件对象中解析出knowledgebase_document表所需要的字段（包括）
5.需要成功上传到rustfs中后再新增到knowledgebase_document表中，如果失败需要抛出异常信息
6.需要实现文档下载功能，界面上需要实现在线阅读文档
7

### 代码实现
1.在本项目的services/knowledgebase/document 目录下实现文档服务接口
2.在本项目的core/knowledgebase/document 目录下实现文档服务中复杂的处理逻辑 （可创建子目录）

### 硬性规定
1.需要完整扫描ragflow项目工程，理解文件上传的后端逻辑
2.不要影响本项目已有的其他功能代码
3.结合本项目代码风格以及已存在代码实现数据集文档上传功能
