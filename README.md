# fjojo-skills

一组自用的 Claude / Agent 技能（Skills），挑了 9 个最通用的开源出来。

每个技能就是一个文件夹里的 `SKILL.md`——纯 Markdown，没有代码依赖，不联网也能读懂。放进支持 Skills 的 Agent 里（Claude Code、Claude Desktop、Codex 等）即可生效。

在线索引（应用场景与相互关系）：**https://fjojo.pro/skills/**

## 技能清单

| 技能 | 一句话 | 类型 |
| --- | --- | --- |
| [jojo](skills/jojo) | 常开行为底座：怎么说话（短句＋清晰解释＋要点加粗）、怎么干活（先找现成的、决策单一次拍板、一次交清） | 行为准则 |
| [html-style](skills/html-style) | 做页面前先定风格：18 个预设风格池、联网找参考站、出方案拍板后才产出 | 创意产线 |
| [shengtu](skills/shengtu) | 生图提示词优化：草稿重构为可直接复制的中英正负提示词，附成品案例 | 创意产线 |
| [reading](skills/reading) | 把一整本书做成「全面细致、美观易读、可视化可交互」的单文件 HTML 读书页；另含英文学术文献对照翻译线 | 阅读 |
| [xuanxing](skills/xuanxing) | 任务选型：按环节拆段，每段选「够用的最低价」模型，交付分段提示词＋成本预估 | 效率 |
| [jojo-daily](skills/jojo-daily) | 资讯处理流水线：链接进 → 3 分钟读完的结构化笔记出（总结／要点／即刻抓手四问／专名罗列） | 效率 |
| [exam-panorama](skills/exam-panorama) | 考试全景：联网核验考情，按七节模板把一门考试讲透（科目、题型、赋分、流程），只讲考试本体 | 备考 |
| [shenlun](skills/shenlun) | 申论全流程：读材料／审题干／写答案三支柱、采分点覆盖批改、大作文两轮阅卷、命题预判 | 备考 |
| [xingce](skills/xingce) | 行测速解：资料分析、数量关系、言语、判断逐题快解，默认「速解 → 答案 → 考点」三段输出 | 备考 |

## 怎么用

**Claude Code / Claude Desktop（本地技能目录）**

```bash
git clone https://github.com/FJOJO2728/skills.git
# 挑要用的技能，拷进你的技能目录（仓库名就是 skills，所以路径是 skills/skills/…）：
cp -r skills/skills/reading ~/.claude/skills/
# 全套一起装：
cp -r skills/skills/* ~/.claude/skills/
```

**手动使用**：直接用编辑器打开某个 `SKILL.md`，把内容粘进对话，或作为系统提示词的一部分。

**触发方式**：每个技能在 frontmatter 的 `description` 里写了自己的触发条件，Agent 会按描述自动调用；也可以直接说触发词（如「考试全景」「学术翻译」「行测」）。

## 设计取向

- **单文件、零依赖**：每个技能就是一个 `SKILL.md`，规则内联，不引用外部脚本。
- **先讲人话**：技能里的规则尽量写成可直接执行的动作，不写黑话。
- **可裁剪**：每份都是自足的，删掉不需要的段落不影响其余部分。

## 许可

MIT，随便用、随便改。见 [LICENSE](LICENSE)。

---

另：个人网站 <https://fjojo.pro> ｜ 技能索引 <https://fjojo.pro/skills/>
