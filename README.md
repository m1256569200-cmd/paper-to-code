# 📄 paper-to-code

**Turn any paper into running code. 丢进论文链接，拿出可运行代码 — *paper-to-code is all you need.***

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Skill](https://img.shields.io/badge/skill-Claude%20Code%20%7C%20Cursor%20%7C%20Copilot-blue)

## ✨ What it does

Share an arXiv link, a PDF, or pasted text — your agent reads the method section, extracts the core algorithm, and writes **runnable code where every block cites its equation** (`# Eq. 3 (§3.2)`). You also get a paper↔code map and an honest fidelity note.

```
you: "implement the core idea of https://arxiv.org/abs/...."
agent: 📐 blueprint → 💻 faithful implementation → ✅/⚠️/❓ fidelity note
```

## 📦 Install

```bash
# Claude Code
mkdir -p ~/.claude/skills/paper-to-code && cp SKILL.md ~/.claude/skills/paper-to-code/

# Cursor (project-level)
mkdir -p .cursor/skills/paper-to-code && cp SKILL.md .cursor/skills/paper-to-code/
```

## 🎯 How it works

1. **📖 Reads** the paper — method, equations, pseudocode, hyperparameters
2. **📐 Extracts** a blueprint: algorithm steps, I/O shapes, key equations
3. **💻 Implements** clean code mirroring the paper's structure, cited line-by-line
4. **🔍 Reports fidelity** — what's faithful, what's simplified, what's ambiguous

## 🧭 Honesty rules

- Never claims to reproduce the paper's numbers without running the eval
- Flags every simplification and ambiguity instead of silently guessing
- Points you to official code when it exists

---

## 🇨🇳 中文介绍

**论文 → 可运行代码。** 把 arXiv 链接/PDF 丢给 agent，它读懂方法部分，写出**每一行都能对应到论文公式**的代码实现。

- 📖 先读论文：方法、公式、伪代码、超参数
- 📐 提炼蓝图：算法步骤、输入输出、关键方程编号
- 💻 忠实实现：代码结构对齐论文结构，注释标注公式出处
- 🔍 诚实报告：哪些忠实、哪些简化、哪些论文里没讲清

适合：想快速复现/学习论文的 AI 爱好者、学生、研究员。

## 📄 License

MIT
