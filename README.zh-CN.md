# Adaptive Study Tutor｜大学课程导师

一个把“提前备课、诊断式讲课、严格验收掌握程度”合并到一起的自适应学习技能，适合高数、物理、电路、编程、工程和期末复习等课程。

## 三种能力

- **PREP 备课**：整理教材、老师 PPT 和考试范围，产出知识路线、例题、检查点、易错点；需要时制作并核验教学 PPT。
- **TEACH 讲课**：先确认你卡在哪一步，再用直觉、正式定义、推导和练习逐层讲清楚；根据你的回答动态调整难度和题量。
- **MASTERY 验收**：用第一性原理、费曼复述、苏格拉底追问、刻意练习和陌生迁移题，区分“听懂了”和“能够独立使用”。

你不需要手动选择模式。说“提前备课”“开始上课”“严格检查我是否真正掌握”，技能会自动切换。讲课按完整知识单元和自然停顿组织，不强行限制为固定几分钟。

## 连续上课

长期学科分支负责保存课程账本，临时新聊天负责一节课的课堂工作。每章、每个大知识单元或临时课堂结束时，技能会生成详细交接状态卡，记录教材位置、已掌握和薄弱点、典型错误、用过的例题，以及下一节课的开场回忆题和主讲路线。

完整格式见 [`references/continuity.md`](references/continuity.md)。

## 安装

```bash
npx skills add shitiwen/adaptive-study-tutor --skill adaptive-study-tutor --global
```

也可以直接下载：

```bash
git clone https://github.com/shitiwen/adaptive-study-tutor.git
```

详细英文说明见 [`README.md`](README.md)，许可证见 [`LICENSE`](LICENSE)。
