# 知途 · ZhiTu Career

<!-- 徽章 -->
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Next.js](https://img.shields.io/badge/Next.js-16.2.4-black)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.2.4-blue)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)](https://www.typescriptlang.org/)
[![Vercel部署](https://img.shields.io/badge/Deployed%20on-Vercel-black)](https://vercel.com)
[![GitHub Pages部署](https://img.shields.io/badge/Deployed%20on-GitHub%20Pages-blue)](https://pages.github.com/)

> AI 驱动的职业探索平台，为大学生点亮职业方向的灯

通过科学测评认清自我，通过 JD 智能解读读懂岗位，通过精准匹配找到差距——将求职过程变成一场有趣的星图探索之旅。

中文 | [English](README.md)

---

## ✨ 功能特性

### 🧭 职业星图测评 (✅ 已完成)
- **Holland RIASEC** 职业兴趣测评（24道场景题）
- **MBTI** 性格类型简化测评（8道场景题）
- **职业价值观**测评（5道场景题）
- **软技能**自评（6道场景题）
- SBTI 游戏化 5 阶段旅程系统，解锁探索徽章
- 测评结果可视化：雷达图 + 职业方向推荐

### 🔍 JD 智能解读 (✅ 已完成)
- AI 驱动的岗位分析（支持火山方舟 API）
- 关键词匹配降级兜底（无需 API 也可使用）
- 输出：白话概括、硬/软技能拆解、职业路径、隐性要求、应届友好度

### 📊 匹配分析 (🚧 开发中)
- 测评结果与 JD 解读结果交叉匹配
- 差距可视化展示

### 📄 简历优化 (🚧 开发中)
- AI 辅助简历优化

---

## 🛠️ 技术栈

| 技术 | 版本 | 说明 |
|------|------|------|
| Next.js | 16.2.4 | React 全栈框架（App Router） |
| React | 19.2.4 | UI 库 |
| TypeScript | 5.x | 类型安全 |
| Tailwind CSS | 4.x | 原子化 CSS |
| shadcn/ui | v4 | 组件库 |

---

## 🚀 快速开始

### 环境要求
- Node.js >= 18
- npm >= 9

### 安装与运行

```bash
# 克隆仓库
git clone https://github.com/2017java/zhitu-career.git
cd zhitu-career

# 安装依赖
npm install

# 构建（必须用 build，不要用 dev）
npm run build

# 启动生产服务器
npm run start
```

打开 http://localhost:3000 即可访问。

> ⚠️ **重要**：请使用 `npm run build && npm run start` 运行，不要使用 `npm run dev`。Next.js 16.2.x 的 dev 模式存在已知的 WebSocket hydration bug，会导致页面交互失效。

### AI 功能配置（可选）

如需启用 AI 驱动的 JD 解读，创建 `.env.local` 文件：

```env
ARK_API_KEY=your_api_key_here
ARK_BASE_URL=https://ark.cn-beijing.volces.com/api/coding/v3
ARK_MODEL=doubao-pro-128k
```

不配置时，JD 解读会自动降级为关键词匹配模式。

---

## 📁 项目结构

```
src/
├── app/                    # Next.js App Router 页面
│   ├── page.tsx            # 首页
│   ├── assessment/         # 职业测评
│   │   ├── page.tsx        # 测评流程
│   │   └── result/page.tsx # 测评结果
│   ├── jd-decoder/page.tsx # JD 解读
│   ├── match/page.tsx      # 匹配分析（开发中）
│   ├── resume/page.tsx     # 简历优化（开发中）
│   └── profile/page.tsx    # 个人中心
├── components/             # 组件
│   ├── layout/             # 布局组件（Navbar、MobileTabBar）
│   ├── common/             # 通用组件（JourneyProgress、LoadingSpinner）
│   └── ui/                 # UI 基础组件
├── hooks/                  # 自定义 Hooks
│   ├── useAssessment.ts    # 测评状态管理
│   ├── useJDDecoder.ts     # JD 解读状态管理
│   └── useJourney.ts       # SBTI 旅程进度
└── lib/                    # 工具库
    ├── assessment/         # 测评算法（Holland、MBTI、价值观、软技能）
    ├── jd-decoder/         # JD 解读引擎（AI + 关键词 + 模板）
    ├── ai/                 # AI 客户端与提示词
    └── storage.ts          # localStorage 封装
```

---

## 🗺️ 项目路线图

### 第一阶段 - MVP (当前)
- [x] 职业星图测评
- [x] JD 智能解读
- [ ] 匹配分析
- [ ] 简历优化

### 第二阶段 - 增强功能
- [ ] AI 职业咨询对话机器人
- [ ] 多语言支持（中文/英文）
- [ ] 用户账户与历史记录
- [ ] 导出测评报告（PDF）

### 第三阶段 - 社区与扩展
- [ ] 开放 API 供开发者使用
- [ ] 插件系统支持自定义测评
- [ ] 与招聘平台集成

### 未来规划 - 留课项目
- [ ] 支教场景配套教育平台
- [ ] 知识库沉淀机制（教师流动，知识留存）
- [ ] AI 辅导继续学习

---

## 🌐 在线访问

**https://2017java.github.io/zhitu-career/**

---

## 📄 开源许可

本项目采用 [MIT 许可证](LICENSE)。

---

## 🤝 贡献指南

欢迎贡献！请随时提交 Pull Request。对于重大更改，请先开启 Issue 讨论您想要改变的内容。

1. Fork 本仓库
2. 创建您的功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交您的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

---

## 🙏 致谢

- 本项目在 Claude Code 的辅助下开发完成
- 测评算法基于成熟的心理学理论框架（霍兰德职业兴趣理论、MBTI 性格类型）
- UI 组件由 [shadcn/ui](https://ui.shadcn.com/) 提供支持

---

> 💡 **提示**：如需在 Claude Code / Cursor 等 AI 编码工具中继续开发本项目，可在项目根目录创建 `CLAUDE.md` 文件，添加项目上下文说明即可。
