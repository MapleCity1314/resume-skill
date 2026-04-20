<h1 align="center">📄 Resume Skill Suite</h1>

<p align="center">
  <strong>一套专为 Claude Code 设计的端到端求职 AI 技能包</strong><br/>
  A modular AI skill suite for end-to-end job seeking, powered by Claude Code
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-Skill_Suite-blueviolet?style=flat-square&logo=anthropic" alt="Claude Code"/>
  <img src="https://img.shields.io/badge/Skills-9_Modules-blue?style=flat-square" alt="Skills"/>
  <img src="https://img.shields.io/badge/Language-中文%20%2F%20EN-orange?style=flat-square" alt="Language"/>
  <img src="https://img.shields.io/badge/Industries-15%2B-green?style=flat-square" alt="Industries"/>
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square" alt="License"/>
</p>

---

## 简介 · What is this?

**Resume Skill Suite** 是一套运行在 [Claude Code](https://claude.ai/code) 上的结构化 AI 技能包，覆盖从**简历诊断 → JD 对齐 → 内容改写 → ATS 适配 → 文件导出 → 打招呼语 → 面试衔接**的完整求职链路。

涵盖 15+ 职业方向，无论你是应届生、职场人、转行者还是海归，均有对应的场景指导。

---

## 端到端工作流

```
          你的简历
              ↓
    ┌── resume-editor ──────────┐
    │  整体诊断 / 评分 / 写作引导  │
    └──────────────┬────────────┘
                   │ 路由到专项 skill
      ┌────────────┼─────────────────────────────┐
      ↓            ↓            ↓                 ↓
resume-jd-match  resume-     resume-          resume-
  JD 对齐分析   experience  project          skills
                 工作经历改写  项目经历改写     技能模块优化
      ↓            ↓            ↓                 ↓
  resume-ats   resume-summary              resume-interview-bridge
  ATS 兼容检查  自我评价改写                  面试衔接预测
      ↓
resume-file-export        resume-cover-letter
   导出 PDF/Markdown          BOSS 打招呼语 / 私信
```

---

## 技能模块 · Skills

### 核心模块

| 技能 | 触发场景 | 核心能力 |
|------|---------|---------|
| 🔍 **resume-editor** | "帮我看看简历" / "resume review" | 整体诊断评分 · 职业阶段加权 · 全流程写作引导 · 急用模式 |
| 📋 **resume-jd-match** | "对一下 JD" / "岗位匹配度" | JD 拆解 · 关键词提取 · 差距清单 · 改写路由 |
| 💼 **resume-experience** | "工作经历怎么写" / "实习太平了" | STAR 改写 · 15+ 行业示例 · 升职/轮岗/短实习场景 |
| 🚀 **resume-project** | "项目经历没亮点" / "case 怎么写" | 开源/内部/UX 项目 · 多人协作归因 · 教程升级 |
| 🛠️ **resume-skills** | "技能怎么写" / "技术栈怎么排" | 前端/后端/AI/数据/移动端/DevOps · 深度层次结构 |
| ✍️ **resume-summary** | "自我评价怎么写" / "个人优势" | 删废话 · JD 定制 · 海归/Gap/转行场景 · Highlights 格式 |

### 专项辅助模块

| 技能 | 触发场景 | 核心能力 |
|------|---------|---------|
| 🖨️ **resume-file-export** | "导出 PDF" / "生成简历文件" | Markdown/HTML 双路径 · pandoc/Typora/VSCode 三种方法 |
| 🎯 **resume-interview-bridge** | "会被问什么" / "帮我准备面试" | 追问预测 · STAR 预答框架 · 自陷语句警示 |
| ✉️ **resume-cover-letter** | "BOSS 打招呼" / "脉脉私信" | BOSS/脉脉/领英三渠道 · 内推话术 |
| 🔐 **resume-ats** | "外企投递" / "ATS 能过吗" | 格式红线检查 · 关键词密度 · 中英双语注意点（外企专用） |

---

## 快速使用 · Quick Start

### 1. 安装技能包

```bash
npx skills add MapleCity1314/resume-skill
```

在 Claude Code 中加载技能目录，然后用自然语言触发：

```
帮我看看我的简历，目标岗位是前端开发，应届生
```
```
对一下这个 JD，我想看看我的匹配度
```
```
这段实习经历太平了，帮我改写一下
```
```
BOSS 打招呼语怎么写，我要投数据分析岗
```

### 2. 典型使用场景

**场景 A：从零写简历**
> 「帮我从零写简历，我是 23 届应届生，投运营岗」
> → `resume-editor` Mode B 引导 → 各专项 skill 深度改写

**场景 B：有简历想优化**
> 粘贴简历 → `resume-editor` 诊断评分 → 按报告逐项用专项 skill 改写

**场景 C：已有简历 + 目标 JD**
> 粘贴简历 + JD → `resume-jd-match` 对齐分析 → 差距清单 → 专项 skill 改写

**场景 D：明天就要投**
> 「明天就要投了，时间紧」→ `resume-editor` Mode D 急用模式 → 20 分钟必改清单

**场景 E：投外企**
> 简历 + JD → `resume-ats` ATS 检查 → `resume-jd-match` 关键词对齐

---

## 知识库 · References

| 文件 | 内容 |
|------|------|
| `resume-editor/references/star-method.md` | STAR 公式完整指南 + 20+ 行业改写案例 |
| `resume-editor/references/field-guides.md` | 15+ 职业方向关键词词库 + 量化指标（含 DevOps/AI 应用/安全/测试） |
| `resume-editor/references/common-mistakes.md` | 50+ 高频简历错误速查 + 修复方案 |
| `resume-editor/references/career-stage-weights.md` | 应届/初职/成长/资深/转行 五阶段评分加权指引 |
| `resume-editor/references/ats-guide.md` | ATS 系统解析原理 + 格式红线 + 关键词密度指南（外企专用） |

---

## 评分体系 · Scoring

5 维加权评分（满分 10 分），**按职业阶段调整权重**：

| 维度 | 应届生 | 初职期 | 成长期 | 资深期 |
|------|------|------|------|------|
| 内容相关性 | 持平 | 持平 | ↑上调 | ↑最重要 |
| 量化程度 | ↓下调 | 持平 | ↑上调 | ↑上调 |
| 结构清晰度 | ↑上调 | 持平 | 持平 | ↓下调 |
| 表达专业度 | 持平 | 持平 | 持平 | 持平 |
| 视觉格式 | ↑上调 | 持平 | ↓下调 | ↓最低 |

---

## 六条铁律 · Six Rules

贯穿所有技能的核心写作原则：

1. **量化一切** — 有数字写数字；无数字写规模（人数 / 预算 / 用户量）
2. **突出贡献** — 「主导」>「负责」>「参与」>「协助」
3. **对准 JD** — 投每家前按 JD 调整关键词顺序（用 `resume-jd-match`）
4. **删除废话** — 「积极主动」「责任心强」无事实支撑一律删
5. **格式 PDF** — 永远用 PDF 投递，Word 会乱版
6. **一个方向** — 全简历围绕一个求职方向，不让 HR 猜你要做什么

---

## 适用职业 · Industries

```
技术类    前端 · 后端 · 全栈 · AI/ML · 移动端 · DevOps · 安全 · 测试
数据类    数据分析 · 数据工程 · BI
产品运营  产品经理 · 运营（用户/内容/活动/社群）· 增长
市场商务  市场营销 · 广告 · 品牌 · 销售 · 商务拓展 · 公关传媒
设计创意  UI/UX · 视觉设计 · 内容创作
职能支持  HR · 财务 · 法务 · 审计 · 供应链 · 教师/教育培训
```

---

## 许可证 · License

[MIT License](LICENSE) © 2026 [MapleCity1314](https://github.com/MapleCity1314)
