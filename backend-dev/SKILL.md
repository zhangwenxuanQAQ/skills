---
name: frontend-dev
description: 前端代码开发时需要遵守如下规则
---

##使用场景
- 构建前端web页面
- 调整页面样式以及布局
- 前端调用后端接口

##技术栈
- React （开发框架）
- TypeScript （代码风格）
- Tailwind CSS 
- Antdesign （组件库）
- Zustand
- 其他有用的前端依赖

##文件结构
src/
├── assets/              # 资产文件，放svg，icon等静态文件
├── pages/       # 功能页面
│   ├── page1/          # 具体页面
│         |── hooks/    #  具体页面的react hooks
│         |── less/    #  具体页面的样式
├── lib/             # Utilities and configurations
├── hooks/           # 通用react hooks
├── theme/           # 主题（控制夜间/白天模式）
├── utils/          # 工具类
├── services/          # 调用后端服务
