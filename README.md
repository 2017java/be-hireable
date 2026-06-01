# ZhiTu Career · 知途

> AI-Powered Career Exploration Platform - Lighting the Way for College Students' Career Paths

Discover yourself through scientific assessments, understand job positions through intelligent JD analysis, and find your gaps through precise matching - transform the job search process into an engaging star map exploration journey.

[中文文档](README.zh-CN.md) | English

---

## ✨ Features

### 🧭 Career Star Map Assessment
- **Holland RIASEC** Career Interest Assessment (24 scenario-based questions)
- **MBTI** Personality Type Simplified Assessment (8 scenario-based questions)
- **Career Values** Assessment (5 scenario-based questions)
- **Soft Skills** Self-Assessment (6 scenario-based questions)
- SBTI Gamified 5-Stage Journey System with unlockable exploration badges
- Visual assessment results: Radar charts + career direction recommendations

### 🔍 Intelligent JD Decoder
- AI-powered job description analysis (supports Volcano Ark API)
- Keyword matching fallback (works without API)
- Output: Plain language summary, hard/soft skills breakdown, career path, hidden requirements, new grad friendliness

### 📊 Match Analysis
- Cross-matching between assessment results and JD analysis
- Visual gap representation

### 📄 Resume Optimization
- AI-assisted resume optimization (in development)

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
│   ├── match/page.tsx      # Match analysis
│   ├── resume/page.tsx     # Resume optimization
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

## 🌐 Live Demo

**https://2017java.github.io/zhitu-career/**

---

## 📄 License

This project is licensed under a dual-license model:

### MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Apache License 2.0

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

### License Comparison

| Feature | MIT License | Apache 2.0 |
|---------|-------------|------------|
| **Permissiveness** | Very permissive | Permissive with patent protection |
| **Attribution** | Must include copyright notice | Must include copyright notice and NOTICE file |
| **Patent Rights** | Silent on patents | Explicit patent grant from contributors |
| **Trademark** | Silent | Explicitly prohibits trademark use without permission |
| **Modification Tracking** | Not required | Must state changes made to files |
| **Liability** | No warranty, no liability | No warranty, no liability |
| **Best For** | Simple projects, maximum freedom | Enterprise use, patent-sensitive projects |

**Why dual-license?** We offer both licenses to give users maximum flexibility. You may choose to use this project under either the MIT License or the Apache License 2.0, whichever better suits your needs.

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
