# 知途 · ZhiTu Career

> AI 驱动的职业探索平台，为大学生点亮职业方向的灯

通过科学测评认清自我，通过 JD 智能解读读懂岗位，通过精准匹配找到差距——将求职过程变成一场有趣的星图探索之旅。

中文 | [English](README.md)

---

## ✨ 功能特性

### 🧭 职业星图测评
- **Holland RIASEC** 职业兴趣测评（24道场景题）
- **MBTI** 性格类型简化测评（8道场景题）
- **职业价值观**测评（5道场景题）
- **软技能**自评（6道场景题）
- SBTI 游戏化 5 阶段旅程系统，解锁探索徽章
- 测评结果可视化：雷达图 + 职业方向推荐

### 🔍 JD 智能解读
- AI 驱动的岗位分析（支持火山方舟 API）
- 关键词匹配降级兜底（无需 API 也可使用）
- 输出：白话概括、硬/软技能拆解、职业路径、隐性要求、应届友好度

### 📊 匹配分析
- 测评结果与 JD 解读结果交叉匹配
- 差距可视化展示

### 📄 简历优化
- AI 辅助简历优化（开发中）

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
│   ├── match/page.tsx      # 匹配分析
│   ├── resume/page.tsx     # 简历优化
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

## 🌐 在线访问

**https://2017java.github.io/zhitu-career/**

---

## 📄 开源许可

本项目采用双许可模式：

### MIT 许可证

特此免费授予任何获得本软件及相关文档文件（以下简称"软件"）的人
不受限制地处理本软件的权利，包括但不限于使用、复制、修改、合并、
发布、分发、再许可和/或销售软件副本的权利，并允许获得本软件的
人在遵守以下条件的前提下这样做：

上述版权声明和本许可声明应包含在本软件的所有副本或实质性部分中。

本软件按"原样"提供，不提供任何形式的明示或暗示担保，包括但不限于
对适销性、特定用途适用性和非侵权性的担保。在任何情况下，作者或
版权持有人均不对任何索赔、损害或其他责任负责，无论是在合同诉讼、
侵权行为或其他方面，由软件或软件的使用或其他交易引起或与之相关。

### Apache 许可证 2.0

根据 Apache 许可证 2.0 版（以下简称"许可证"）获得许可；
除非遵守许可证，否则您不得使用此文件。
您可以在以下网址获取许可证副本：

    http://www.apache.org/licenses/LICENSE-2.0

除非适用法律要求或书面同意，否则根据许可证分发的软件
按"原样"分发，不提供任何明示或暗示的担保或条件。
请参阅许可证以了解管理权限和限制的特定语言。

### 许可证对比说明

| 特性 | MIT 许可证 | Apache 2.0 许可证 |
|------|------------|-------------------|
| **宽松程度** | 非常宽松 | 宽松，但包含专利保护 |
| **署名要求** | 必须保留版权声明 | 必须保留版权声明和 NOTICE 文件 |
| **专利授权** | 未提及专利 | 明确的专利授权条款 |
| **商标使用** | 未提及 | 明确禁止未经许可使用商标 |
| **修改声明** | 无需声明修改 | 必须声明对文件的修改 |
| **责任限制** | 无担保，无责任 | 无担保，无责任 |
| **适用场景** | 简单项目，追求最大自由度 | 企业使用，涉及专利敏感的项目 |

**为什么选择双许可？** 我们提供两种许可证，让用户拥有最大的灵活性。您可以根据自己的需求选择使用 MIT 许可证或 Apache 2.0 许可证。

### MIT vs Apache 2.0 详细区别

#### 1. **专利保护**
- **MIT**：未明确提及专利授权。这意味着如果代码贡献者拥有相关专利，理论上可能在未来主张专利权。
- **Apache 2.0**：包含明确的专利授权条款。贡献者自动授予用户永久、免费、不可撤销的专利许可，防止"专利陷阱"。

#### 2. **商标使用**
- **MIT**：未涉及商标问题。
- **Apache 2.0**：明确禁止未经许可使用项目商标，保护项目品牌。

#### 3. **修改声明**
- **MIT**：不要求声明对代码的修改。
- **Apache 2.0**：要求声明对文件的修改，有助于追踪代码演变。

#### 4. **法律严谨性**
- **MIT**：文本简短（约 20 行），表述简洁，法律术语较少。
- **Apache 2.0**：文本详细（约 200 行），法律条款更全面，在法庭上更具可执行性。

#### 5. **企业友好度**
- **MIT**：适合个人开发者、小型项目，追求代码传播最大化。
- **Apache 2.0**：更受大型企业青睐，因为专利保护条款让法务部门更放心。

#### 6. **兼容性**
- **MIT**：与 GPL、BSD、Apache 等大多数许可证兼容。
- **Apache 2.0**：与 GPL v3 兼容，但与 GPL v2 不兼容（因为专利条款）。

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
