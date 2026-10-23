# wechat-human-writing

微信公众号"活人感"专业写作 Skill。让 AI 写的公众号文章摆脱厚重的"模型腔"和"报告腔"，读起来像一个有见识、有温度的具体的人在认真说话。

本 Skill 在 [KKKKhazix/human-writing](https://github.com/KKKKhazix/human-writing) 的行文功底（材料纪律、去模型腔禁令、中文韵律）之上，叠加了一套公众号专属工作流：三维确认、黄金3秒开篇、每 300-400 字配图建议、三类 CTA 引导与完整排版规范。

## 核心特性

- **三维确认工作流**：输入新题目时，先确认目标读者、文章风格、CTA 引导三个维度（各含 A/B/C/D 选项），绝不跳过直接开写。
- **材料纪律**：非虚构长文动笔前至少清点五件具体材料，宁短勿假，杜绝车轱辘话凑字数。
- **黄金3秒开篇**：严禁 AI 套话，从具体场景、痛点或反直觉现象切入。
- **成稿禁令**：禁止翻案腔、提示性冒号、破折号、商业黑话、模型腔路标词，附检查脚本。
- **专业排版与配图**：小标题与加粗规范、每 300-400 字一条【配图建议】（画面/色调/构图三要素）、封面图建议。
- **三类 CTA 写法**：评论区互动、朋友圈转发、收藏关注，各有具体规则与示例。

## 目录结构

```
wechat-human-writing/
├── SKILL.md                      # 主入口：标准工作流 + 硬性规范
├── references/
│   ├── forum-prose.md            # 活人感行文功底（来自 human-writing）
│   ├── reality.md                # 现实写作的事实边界（来自 human-writing）
│   ├── fiction.md                # 虚构创作规则（来自 human-writing）
│   ├── formats.md                # 特殊形式处理（来自 human-writing）
│   ├── revision.md               # 改稿规则（来自 human-writing）
│   ├── wechat-format.md          # 公众号排版与配图规范（新增）
│   └── cta-guide.md              # 三类 CTA 写法（新增）
├── scripts/
│   └── check_prose.py            # 成稿禁令检查脚本（来自 human-writing）
└── dist/
    └── wechat-lite.md            # 蒸馏版，可直接粘贴给任意聊天产品
```

## 使用方式

### WorkBuddy / Claude 等 Agent 环境

将本目录放入 `~/.workbuddy/skills/`（用户级）或项目 `.workbuddy/skills/`（项目级），然后直接说"帮我写一篇公众号文章，题目是……"，Agent 会自动加载本 Skill 并走三维确认工作流。

### 不支持 Skill 的聊天产品

打开 `dist/wechat-lite.md`，把整段内容粘贴到对话里，跟在写作需求后面即可。

### 检查脚本

```bash
python3 scripts/check_prose.py 你的稿件.md
```

脚本检查成稿硬禁令（翻案腔、破折号、提示性冒号、黑话等），输出违禁项位置。修改直到禁用项清零。

## 写作工作流

1. **三维确认**：读者 / 风格 / CTA，逐项选定，绝不跳过。
2. **材料清点**：五件具体材料起步，不够就研究、追问或写短。
3. **正文创作**：黄金3秒开篇，每段带来新东西，判断从正面下。
4. **排版与配图**：小标题 + 加粗 + 每 300-400 字【配图建议】。
5. **CTA 落笔**：按确认方向写一两句，从正文长出来。
6. **改稿自查**：跑检查脚本，禁用项清零。
7. **交稿**：标题候选 + 正文（含配图建议）+ CTA + 封面图建议。

## 致谢与许可

- 行文规则体系改编自 [KKKKhazix/human-writing](https://github.com/KKKKhazix/human-writing)（MIT License）。
- 公众号工作流、排版配图规范与 CTA 写法为本 Skill 新增。
- 本仓库同样以 MIT License 发布，见 [LICENSE](LICENSE)。
