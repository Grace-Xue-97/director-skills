# 导演技能包（GitHub Ready）

本仓库用于后续影视 / AIGC 视频项目复用，包含两个独立 Skill：

| Skill | 显示名称 | 用途 |
|---|---|---|
| `director-performance` | 导演表演skill | 情绪曲线、可拍摄表演、动作连续性、声音、环境反馈 |
| `director-storyboard` | 导演分镜skill | QH 五段式影视提示词、空间锚点、镜头时间轴、连续性约束 |

## 目录

```text
director-skills/
├── README.md
├── manifest.json
└── skills/
    ├── director-performance/
    │   ├── SKILL.md
    │   └── agents/
    │       └── openai.yaml
    └── director-storyboard/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        ├── assets/
        │   └── prompt-template.md
        └── references/
            └── manor-original.md
```

## 调用入口

GitHub 仓库建立后，两个核心入口分别是：

```text
skills/director-performance/SKILL.md
skills/director-storyboard/SKILL.md
```

Raw URL 模板：

```text
https://raw.githubusercontent.com/<你的GitHub用户名>/<仓库名>/main/skills/director-performance/SKILL.md
https://raw.githubusercontent.com/<你的GitHub用户名>/<仓库名>/main/skills/director-storyboard/SKILL.md
```

## 建议用法

### 导演表演skill
适合：
- 情绪导演
- 人物表演强化
- 动作连续性
- 台词与口型 / 声音设计
- 环境反馈

### 导演分镜skill
适合：
- 视频分镜
- 镜头时间轴
- 场景与空间关系
- 参考素材绑定
- 镜头连续性修订

两者可以串联使用：先用 `director-performance` 处理人物情绪与表演，再用 `director-storyboard` 将结果落成可执行分镜。

## 原则

本整理版尽量保持两个原始 Skill 的核心规则与输出逻辑，只做 GitHub 化目录、命名和入口规范化；不把两个 Skill 合并成一个，以便后续按项目单独调用。
