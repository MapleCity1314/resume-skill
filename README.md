<h1 align="center">📄 Resume Skill Suite</h1>

<p align="center">
  <strong>一套专为 Claude Code 设计的简历优化 AI 技能包</strong><br/>
  A modular AI skill suite for resume optimization, powered by Claude Code
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-Skill_Suite-blueviolet?style=flat-square&logo=anthropic" alt="Claude Code"/>
  <img src="https://img.shields.io/badge/Language-中文%20%2F%20EN-orange?style=flat-square" alt="Language"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/Coverage-15%2B_Industries-blue?style=flat-square" alt="Industries"/>
</p>

---

## 简介 · What is this?

**Resume Skill Suite** 是一套运行在 [Claude Code](https://claude.ai/code) 上的结构化 AI 技能包，帮助各行业求职者用招聘官视角优化简历，**可感知地提升面试邀请率**。

涵盖 15+ 职业方向（前端 / 后端 / AI / 运营 / 广告 / 设计 / 产品 / 销售 / HR / 财务……），提供从整体诊断到逐模块精写的全流程支持。

---

## 技能模块 · Skills

| 技能 | 触发场景 | 核心能力 |
|------|---------|---------|
| 🔍 **resume-editor** | "帮我看看简历" / "resume review" | 整体诊断评分 · 全流程写作引导 · 文件生成 |
| 💼 **resume-experience** | "工作经历怎么写" / "实习经历太平了" | STAR 公式改写 · 行业化量化表达 |
| 🚀 **resume-project** | "项目经历没亮点" / "case 经历怎么写" | 项目→技能视角转换 · 贡献度提炼 |
| 🛠️ **resume-skills** | "技能栏怎么写" / "技术栈怎么排列" | 岗位适配排序 · 深度层次结构 |
| ✍️ **resume-summary** | "自我评价写什么" / "个人优势怎么写" | 删废话 · JD 定制化总结生成 |

---

## 快速使用 · Quick Start

### 1. 安装技能包

```bash
# 克隆到 Claude Code 技能目录
git clone https://github.com/MapleCity1314/resume-skill.git
```

在 Claude Code 中加载技能后，直接用自然语言触发：

```
帮我看看我的简历，目标岗位是前端开发，应届生
```

```
resume review — I'm applying for a product manager role
```

### 2. 工作流

```
用户输入简历 / 描述需求
       ↓
resume-editor 诊断评分 + 确认需求
       ↓
按需路由到专项技能
  ├── resume-experience  →  工作 / 实习经历改写
  ├── resume-project     →  项目 / 案例经历优化
  ├── resume-skills      →  技能模块结构化
  └── resume-summary     →  自我评价精简重写
```

---

## 评分体系 · Scoring System

诊断报告使用 5 维加权评分（满分 10 分）：

| 维度 | 权重 | 评分要点 |
|------|------|---------|
| 内容相关性 | **30%** | 经历与目标岗位的匹配程度 |
| 量化程度 | **25%** | 数字密度 + 可验证成果 |
| 结构清晰度 | **20%** | 板块完整 · 比例合理 · 逻辑清晰 |
| 表达专业度 | **15%** | 行业术语准确 · 语言凝练 |
| 视觉格式 | **10%** | 排版整洁 · 无乱码错字 |

---

## 六条铁律 · Six Rules

> 贯穿所有技能的核心写作原则

1. **量化一切** — 有数字写数字；无数字写规模（人数 / 预算 / 用户量）
2. **突出贡献** — 「主导」>「负责」>「参与」>「协助」
3. **对准 JD** — 投每家前按 JD 调整关键词顺序
4. **删除废话** — 「积极主动」「责任心强」无事实支撑一律删
5. **格式 PDF** — 永远用 PDF 投递，Word 会乱版
6. **一个方向** — 全简历围绕一个求职方向，不让 HR 猜你要做什么

---

## 知识库 · References

| 文件 | 内容 |
|------|------|
| `resume-editor/references/star-method.md` | STAR 公式完整指南 + 20+ 行业改写案例 |
| `resume-editor/references/field-guides.md` | 15+ 职业方向关键词词库 + 量化指标示例 |
| `resume-editor/references/common-mistakes.md` | 50+ 高频简历错误速查 + 修复方案 |

---

## 适用职业 · Industries

```
技术类    前端 · 后端 · 全栈 · AI/ML · 移动端 · DevOps
产品运营  产品经理 · 运营 · 增长 · 用户研究
市场商务  市场营销 · 广告 · 品牌 · 销售 · 商务拓展
设计创意  UI/UX · 视觉设计 · 内容创作
职能支持  HR · 财务 · 法务 · 行政
```

---

## 许可证 · License

[MIT License](LICENSE) © 2026 [MapleCity1314](https://github.com/MapleCity1314)
