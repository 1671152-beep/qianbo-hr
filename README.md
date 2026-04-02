# OpenClaw HR 系统

## 项目概述

OpenClaw HR 是为千播公司定制的企业级人力资源管理系统，涵盖制度流程、预算成本、人事管理的全流程数字化解决方案。

## 快速开始

```bash
# 克隆项目
git clone https://github.com/openclaw/openclaw-hr.git
cd openclaw-hr

# 启动服务
docker-compose up -d

# 访问系统
http://localhost:8080
```

## 项目结构

```
openclaw-hr/
├── README.md              # 项目说明
├── docs/                  # 文档
├── policies/              # 15项制度文件
├── budget/                # 预算数字模型
├── src/                   # 源代码
└── docker-compose.yml     # 部署配置
```

## 制度文件清单 (15项)

### 核心流程制度
1. 报销流程制度
2. 费用申请流程制度
3. 账号使用流程制度
4. 出差流程制度
5. 人事扩编流程制度
6. 设备管理流程制度

### 补充流程制度
7. 招聘与入职流程制度
8. 考勤与休假流程制度
9. 薪酬福利管理制度
10. 绩效考核流程制度
11. 培训管理流程制度
12. 离职交接流程制度
13. 合同管理流程制度
14. 信息安全与保密制度
15. 固定资产管理制度

## 预算模型

- 4大中心预算体系
- 月度/年度预算编制
- 预算执行跟踪
- 成本分析报表
- 预警预测系统

## 技术栈

- 前端: Vue3 + Element Plus
- 后端: Node.js / Python
- 数据库: MySQL + Redis
- 部署: Docker

## 许可证

MIT License
