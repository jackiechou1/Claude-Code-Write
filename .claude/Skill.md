---
name: gudai-skill
description: 古代权谋短篇小说创作技能包。执行大纲、人物、目录、章节的专业创作，基于古代权谋创作法则和严谨的写作风格生成高质量短篇内容。
---

# 古代权谋小说创作 Skill

[技能说明]
专业的古代权谋短篇小说创作技能包，覆盖故事构思、人物塑造、章节规划、正文写作全流程。根据不同创作阶段，调取对应的创作资源并生成符合古代权谋规范的小说内容。

[文件结构]
./claude/skills/gudai-skill/
├── SKILL.md                 # 本文件（技能包核心配置）
├── outline-method.md        # 大纲创作方法论（含人物塑造指导）
├── output-style.md          # 写作风格（含章节创作方法）
├── examples/
│   ├── outline-example.md   # 大纲示例
│   ├── character-example.md # 人物示例
│   └── chapter-example.md   # 章节示例
├── templates/
│   ├── outline-template.md  # 大纲文档格式模板
│   ├── character-template.md# 人物小传格式模板
│   ├── chapter-index-template.md # 章节目录格式模板
│   └── chapter-template.md  # 章节正文格式模板

[核心能力]
- **创作阶段理解**：识别当前处于大纲、人物、目录还是章节创作阶段
- **资源整合**：读取模板、方法论、风格、示例等多维度资源
- **专业创作**：基于资源和上下文创作符合古代权谋规范的小说内容
- **风格把控**：确保创作内容符合古代权谋的文白相济风格
- **模板遵循**：严格按照模板格式生成文档结构
- **上下文理解**：理解已有文档内容，确保创作连贯性

[执行流程]
第一步：理解创作需求
    识别当前创作阶段：
    - 如果在讨论故事大纲或outline.md不存在 -> 大纲创作阶段
    - 如果在讨论人物或刚执行/character -> 人物创作阶段
    - 如果在讨论章节规划或刚执行/catalog -> 目录创作阶段
    - 如果在讨论章节正文或刚执行/write -> 章节创作阶段
    

第二步：读取创作资源
    **大纲创作阶段**：
    1. 读取 templates/outline-template.md (文档格式模板)
    2. 读取 outline-method.md (古代权谋大纲创作方法论，含人物塑造指导)
    3. 读取 output-style.md (古代权谋写作风格)
    4. 读取 examples/outline-example.md (古代权谋大纲示例)
    5. 从对话历史获取用户回答的Q1-Q3 (核心创意、核心冲突、故事调性)

    **人物创作阶段**：
    1. 读取 outline.md (了解故事背景和设定)
    2. 读取 templates/character-template.md (人物小传格式模板)    
    3. 读取 outline-method.md (获取人物塑造指导部分)    
    4. 读取 output-style.md (古代权谋写作风格)    
    5. 读取 examples/character-example.md (人物示例)    
    6. 从对话历史获取用户关于角色的具体要求（如：核心人设、动机、阵营等）


   **目录创作阶段**：    
1. 读取 outline.md (获取故事大纲的起承转合结构)    
2. 读取所有已生成的人物小传 (了解关键角色)    
3. 读取 templates/chapter-index-template.md (章节目录格式模板)    
4. 读取 output-style.md (古代权谋写作风格)    
5. 结合大纲情节，自动生成章节标题和各章概要

   **章节创作阶段**：    
1. 读取 outline.md (获取故事大纲，明确本章所属阶段)    
2. 读取 chapter-index.md (获取章节目录，定位当前章节及其概要)    
3. 读取所有相关的人物小传 (获取本章出场人物的性格、动机)   
4. 读取 templates/chapter-template.md (章节正文格式模板)    
5. 读取 outline-method.md (获取权谋设计、场景描写技巧)   
6. 读取 output-style.md (古代权谋写作风格)    
7. 读取 examples/chapter-example.md (章节示例)    
8. 


第三步：生成与交付   
 1. 根据所处阶段和读取的资源，调用 **[核心能力]** 中的 **专业创作**。   
 2. 严格遵循 **模板遵循** 和 **风格把控** 原则，确保产出内容的专业性和一致性。    
 3. 生成符合规范的 .md 文档内容，或在对话中直接回应，交付给用户。   
 4. 保持 **上下文理解**，在创作完成后，智能引导用户进入下一个创作阶段（例如：大纲创作完成后，询问“是否需要我为您创建核心人物？）