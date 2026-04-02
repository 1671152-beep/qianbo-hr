# OpenClaw HR 系统 - 快速启动指南

## 🚀 项目已创建完成

### 1. 交互式WEB系统
**位置**：`src/index.html`

**功能**：
- 📊 数据看板（KPI卡片、图表可视化）
- 💰 预算管理（实时调整、自动计算）
- 🏢 组织架构（可视化展示）
- 📋 制度文件（15项制度）
- 📈 成本分析（盈亏平衡、人效分析）
- 📥 Excel导出（一键生成报表）

**启动方式**：
```bash
# 本地浏览器打开
open /root/.openclaw/workspace/openclaw-hr/src/index.html

# 或启动本地服务器
cd /root/.openclaw/workspace/openclaw-hr/src
python3 -m http.server 8080
# 访问 http://localhost:8080
```

### 2. Excel模板生成器
**位置**：`src/excel-generator.html`

**功能**：
- 实时调整预算数据
- 自动生成带公式的Excel
- 盈亏状态实时计算

### 3. 预算数字模型
**位置**：`budget/成本预算数字模型.md`

**内容**：
- 4大中心预算体系
- 盈亏平衡分析
- 人效分析
- 优化建议

### 4. 制度文件（15项）
**位置**：`policies/*.md`

---

## 📁 项目结构

```
openclaw-hr/
├── README.md                    # 项目总览
├── docs/
│   ├── 系统架构文档.md           # 技术架构
│   └── 飞书文档导入指南.md       # 飞书导入说明
├── policies/                    # 15项制度文件
│   ├── 01-报销流程制度.md
│   ├── 02-费用申请流程制度.md
│   ├── ...
│   └── 15-固定资产管理制度.md
├── budget/                      # 预算模型
│   ├── 成本预算数字模型.md
│   └── 预算明细表.csv
└── src/                         # WEB源代码
    ├── index.html              # 主系统
    └── excel-generator.html    # Excel生成器
```

---

## 🎯 核心功能演示

### 预算管理
- 点击"预算管理"标签
- 修改任意输入框数值
- 下方合计自动更新
- 点击"导出Excel"下载报表

### 成本分析
- 盈亏平衡点自动计算
- 费销比实时显示
- 超支预警提示

### 组织架构
- 可视化展示4大中心
- 点击中心查看详情
- 显示编制和预算数据

---

## 📊 关键数据（4月预算）

| 指标 | 数值 | 状态 |
|------|------|------|
| 总编制 | 23人 | - |
| 月度总预算 | ¥357,150 | - |
| 销售指标 | ¥319,500 | - |
| 费销比 | 111.8% | 🔴 亏损 |
| 盈亏平衡 | ¥430,000 | 需+34.6% |

---

## 🔧 自定义配置

### 修改预算数据
编辑 `src/index.html` 中的 `centers` 数据对象。

### 添加新制度
在 `policies` 数组中添加新条目。

### 调整图表
在 `initCharts()` 方法中修改 Chart.js 配置。

---

## 📱 部署建议

### 方案1：内部服务器
```bash
# 复制到Nginx目录
cp -r src/* /var/www/html/openclaw-hr/
```

### 方案2：静态托管
- GitHub Pages
- 阿里云OSS
- 腾讯云COS
- Vercel/Netlify

### 方案3：Docker部署
```dockerfile
FROM nginx:alpine
COPY src /usr/share/nginx/html
EXPOSE 80
```

---

## 📞 支持与反馈

如有问题或需求调整，随时联系。

---

**创建时间**：2026-04-01  
**系统版本**：v1.0
