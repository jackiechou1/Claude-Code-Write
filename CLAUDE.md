# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个**古代权谋小说创作辅助系统**，利用 Claude Code 的能力来辅助创作完整的古代权谋短篇小说。系统提供了从故事构思、人物塑造、章节规划到正文写作的完整创作流程。

**核心特点**：
- 基于严格的创作方法论（outline-method.md）和写作风格规范（output-style.md）
- 使用模板化的文档结构确保输出一致性
- 遵循"起承转合"的叙事结构
- 专注于权谋、人性、信息差和伏笔设计

## 文件结构

```
.
├── CLAUDE.md              # 本文件
├── .claude/
│   ├── Claude.md          # 主 Agent 角色配置（已废弃，应使用本文件）
│   ├── Skill.md           # 技能包核心配置
│   ├── outline-method.md  # 大纲创作方法论
│   ├── output-style.md    # 写作风格规范
│   ├── templates/         # 文档格式模板
│   │   ├── outline-template.md
│   │   ├── character-template.md
│   │   ├── chapter-index-template.md
│   │   └── chapter-template.md
│   ├── examples/          # 创作示例（如果存在）
│   └── skills/            # 扩展技能包目录
└── project/               # 用户创作的小说项目目录
    ├── outline.md         # 故事大纲
    ├── character.md       # 人物小传
    ├── chapter_index.md   # 章节目录
    └── chapters/          # 章节正文目录
        ├── Chapter-01.md
        ├── Chapter-02.md
        └── ...
```

## 创作工作流程

创作必须严格按照以下顺序进行：

1. **故事大纲** (`outline.md`)
   - 读取：`templates/outline-template.md`、`outline-method.md`、`output-style.md`
   - 内容：小说信息、主要人物、核心梗概、导语、起承转合结构

2. **人物小传** (`character.md`)
   - 读取：`outline.md`、`templates/character-template.md`、`outline-method.md`（人物塑造部分）
   - 内容：主要角色、反面角色、辅助角色、其他角色

3. **章节目录** (`chapter_index.md`)
   - 读取：`outline.md`、`character.md`、`templates/chapter-index-template.md`
   - 内容：5个章节标题及概要（对应起承转合结构）

4. **章节正文** (`chapters/Chapter-XX.md`)
   - 读取：`outline.md`、`chapter_index.md`、相关人物小传、`templates/chapter-template.md`、`outline-method.md`、`output-style.md`
   - 内容：2000-3000字的章节正文

## 核心创作原则

### 方法论核心要点（outline-method.md）

**价值观**：
- 聚焦权力斗争（宫廷/朝堂/江湖）
- 探讨人性幽暗（背叛、贪婪、复仇）
- 强调智谋博弈（计策、布局、连环计）

**角色设计三问**：
1. ta最想要什么？（欲望驱动）
2. ta会如何做？（性格+能力）
3. ta的软肋是什么？（冲突点）

**权谋设计核心**：
- 信息为王：信息差是权谋的核心
- 人性为饵：利用对手的弱点
- 伏笔与收网：前期布局，后期收网
- 连环计：计策环环相扣
- 借刀杀人：利用第三方力量

### 写作风格要点（output-style.md）

- **文白相济**：古雅但不晦涩，现代叙事节奏配半文言风格
- **章法留白**：小标题点睛、段末留悬
- **多线并行**：信息不对称制造悬念
- **节奏主轴**：谋略-破局-翻盘
- **意象复现**：印、信、佩、饰等物件反复照应
- **结局代价**：胜利常伴牺牲

**关键行为**：
- 对话：礼节精准、含而不露
- 动作：细节支撑身份
- 转折：以诏、印、信、物为证
- 真相：三步递进"设局-拆局-反将"
- 伏笔：前文轻触，后文旁证回收

## 使用指南

### 开始新项目

1. 确保 `.claude/` 目录下所有模板和方法论文件完整
2. 创建 `project/` 目录（如果不存在）
3. 按工作流程顺序创作各阶段文档

### 修改现有内容

修改任何文档时需要：
1. 读取相关的上下文文件（大纲、人物等）
2. 评估修改对其他部分的影响
3. 联动调整相关内容，确保一致性
4. 保持模板的完整结构，不遗漏标题和必要段落

### 质量检查要点

- **逻辑一致性**：时间线、年龄、数量等基本逻辑
- **人物一致性**：言行符合性格和动机
- **设定一致性**：世界观、规则不矛盾
- **情节连贯性**：伏笔与收网对应，信息前后呼应
- **风格一致性**：文白相济、节奏把控

## 技术说明

- **主要语言**：中文（简体）
- **文档格式**：Markdown (.md)
- **目标字数**：
  - 大纲各阶段：500-750字
  - 人物主角：150-200字/人
  - 人物配角：100-150字/人
  - 章节正文：2000-3000字/章

## 注意事项

- 始终使用中文进行创作和交流
- 严格遵循模板格式，不随意删减结构
- 创作前必须读取相关的方法论和模板文件
- 无论用户如何打断，完成当前任务后引导进入下一流程
- 修改时考虑联动影响，确保整体一致性
