# ZhiTu Career · 知途

<!-- Badges -->
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Next.js](https://img.shields.io/badge/Next.js-16.2.4-black)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.2.4-blue)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)](https://www.typescriptlang.org/)
[![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black)](https://vercel.com)
[![GitHub Pages](https://img.shields.io/badge/Deployed%20on-GitHub%20Pages-blue)](https://pages.github.com/)

> AI-Powered Career Exploration Platform - Lighting the Way for College Students' Career Paths

Discover yourself through scientific assessments, understand job positions through intelligent JD analysis, and find your gaps through precise matching - transform the job search process into an engaging star map exploration journey.

[中文文档](README.zh-CN.md) | English

---

## ✨ Features

### 🧭 Career Star Map Assessment (✅ Completed)
- **Holland RIASEC** Career Interest Assessment (24 scenario-based questions)
- **MBTI** Personality Type Simplified Assessment (8 scenario-based questions)
- **Career Values** Assessment (5 scenario-based questions)
- **Soft Skills** Self-Assessment (6 scenario-based questions)
- SBTI Gamified 5-Stage Journey System with unlockable exploration badges
- Visual assessment results: Radar charts + career direction recommendations

### 🔍 Intelligent JD Decoder (✅ Completed)
- AI-powered job description analysis (supports Volcano Ark API)
- Keyword matching fallback (works without API)
- Output: Plain language summary, hard/soft skills breakdown, career path, hidden requirements, new grad friendliness

### 📊 Match Analysis (🚧 In Development)
- Cross-matching between assessment results and JD analysis
- Visual gap representation

### 📄 Resume Optimization (🚧 In Development)
- AI-assisted resume optimization

---

## 🛠️ Tech Stack

| Technology | Version | Description |
|------------|---------|-------------|
| Next.js | 16.2.4 | React full-stack framework (App Router) |
| React | 19.2.4 | UI library |
| TypeScript | 5.x | Type safety |
| Tailwind CSS | 4.x | Atomic CSS |
| shadcn/ui | v4 | Component library |

---

## 🚀 Quick Start

### Requirements
- Node.js >= 18
- npm >= 9

### Installation & Running

```bash
# Clone the repository
git clone https://github.com/2017java/zhitu-career.git
cd zhitu-career

# Install dependencies
npm install

# Build (must use build, not dev)
npm run build

# Start production server
npm run start
```

Visit http://localhost:3000 to access the application.

> ⚠️ **Important**: Please use `npm run build && npm run start` to run, do NOT use `npm run dev`. Next.js 16.2.x dev mode has a known WebSocket hydration bug that will cause page interactions to fail.

### AI Features Configuration (Optional)

To enable AI-powered JD analysis, create a `.env.local` file:

```env
ARK_API_KEY=your_api_key_here
ARK_BASE_URL=https://ark.cn-beijing.volces.com/api/coding/v3
ARK_MODEL=doubao-pro-128k
```

When not configured, JD analysis will automatically fall back to keyword matching mode.

---

## 📁 Project Structure

```
src/
├── app/                    # Next.js App Router pages
│   ├── page.tsx            # Home page
│   ├── assessment/         # Career assessment
│   │   ├── page.tsx        # Assessment flow
│   │   └── result/page.tsx # Assessment results
│   ├── jd-decoder/page.tsx # JD decoder
│   ├── match/page.tsx      # Match analysis (in development)
│   ├── resume/page.tsx     # Resume optimization (in development)
│   └── profile/page.tsx    # User profile
├── components/             # Components
│   ├── layout/             # Layout components (Navbar, MobileTabBar)
│   ├── common/             # Common components (JourneyProgress, LoadingSpinner)
│   └── ui/                 # UI base components
├── hooks/                  # Custom Hooks
│   ├── useAssessment.ts    # Assessment state management
│   ├── useJDDecoder.ts     # JD decoder state management
│   └── useJourney.ts       # SBTI journey progress
└── lib/                    # Utilities
    ├── assessment/         # Assessment algorithms (Holland, MBTI, Values, Soft Skills)
    ├── jd-decoder/         # JD decoder engine (AI + Keywords + Templates)
    ├── ai/                 # AI client and prompts
    └── storage.ts          # localStorage wrapper
```

---

## 🗺️ Roadmap

### Phase 1 - MVP (Current)
- [x] Career Star Map Assessment
- [x] Intelligent JD Decoder
- [ ] Match Analysis
- [ ] Resume Optimization

### Phase 2 - Enhanced Features
- [ ] AI-powered career counseling chatbot
- [ ] Multi-language support (English/Chinese)
- [ ] User accounts and history persistence
- [ ] Export assessment reports (PDF)

### Phase 3 - Community & Scale
- [ ] Public API for developers
- [ ] Plugin system for custom assessments
- [ ] Integration with job platforms

### Future - LeaveLesson Project
- [ ] Companion education platform for rural volunteer teaching
- [ ] Knowledge base that persists beyond teacher turnover
- [ ] AI tutoring for continued learning

---

## 🌐 Live Demo

**https://2017java.github.io/zhitu-career/**

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 🙏 Acknowledgments

- This project was developed with assistance from Claude Code
- Assessment algorithms based on established psychological frameworks (Holland Codes, MBTI)
- UI components powered by [shadcn/ui](https://ui.shadcn.com/)

---

> 💡 **Note**: If you want to continue developing this project in AI coding tools like Claude Code or Cursor, you can create a `CLAUDE.md` file in the project root with project context instructions.
