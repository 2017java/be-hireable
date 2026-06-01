# Contributing to ZhiTu Career

Thank you for considering contributing to ZhiTu Career! This document provides guidelines and instructions for contributing.

## 🎯 Project Vision

ZhiTu Career is an AI-powered career exploration platform that helps college students discover their career path through scientific assessments and intelligent job analysis. We believe everyone deserves access to quality career guidance.

## 🚀 How Can I Contribute?

### Reporting Bugs

Before creating bug reports:
- Check the [existing issues](https://github.com/2017java/zhitu-career/issues) to avoid duplicates
- Use the [bug report template](.github/ISSUE_TEMPLATE/bug_report.md) when creating new issues
- Include as much information as possible: OS, browser, steps to reproduce, screenshots

### Suggesting Features

We welcome feature suggestions! Please:
- Check the [roadmap](README.md#-roadmap) first
- Use the [feature request template](.github/ISSUE_TEMPLATE/feature_request.md)
- Explain how the feature would benefit users
- Consider alignment with the project's educational mission

### Pull Requests

1. **Fork the repository** and create your branch:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

2. **Follow the coding standards**:
   - TypeScript with strict mode
   - Use functional components with hooks
   - Follow existing code style (2-space indentation)

3. **Write meaningful commit messages**:
   ```bash
   git commit -m 'feat: add new assessment type'
   git commit -m 'fix: resolve JD decoder API timeout'
   git commit -m 'docs: update installation instructions'
   ```

4. **Push to your fork** and create a Pull Request:
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Fill out the PR template** with:
   - Clear description of changes
   - Link to related issues
   - Screenshots for UI changes
   - Testing instructions

## 📋 Development Setup

```bash
# Clone your fork
git clone https://github.com/your-username/zhitu-career.git
cd zhitu-career

# Add upstream remote
git remote add upstream https://github.com/2017java/zhitu-career.git

# Install dependencies
npm install

# Create .env.local for AI features (optional)
cp .env.example .env.local

# Start development
npm run dev
```

## 🎨 Code Standards

- **React Components**: Functional components with TypeScript
- **State Management**: React hooks (useState, useEffect, custom hooks)
- **Styling**: Tailwind CSS with shadcn/ui components
- **Testing**: Write tests for new features when applicable

## 📝 Commit Message Format

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting
- `refactor`: Code restructuring
- `test`: Adding tests
- `chore`: Maintenance

## 🔄 Keeping Your Fork Updated

```bash
# Fetch from upstream
git fetch upstream

# Merge upstream changes
git checkout main
git merge upstream/main

# Push to your origin
git push origin main
```

## 📜 License

By contributing, you agree that your contributions will be licensed under the MIT License.

## 🙏 Thank You!

Your contributions make open source thrive. Thank you for being part of the ZhiTu community!
