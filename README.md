# desktop-girlfriend-video-prompt

桌面 AI 女友视频提示词 Skill —— 根据用户需求，设计可直接交给生视频模型的中文提示词。成片呈现为一段全屏桌面录屏：桌面 OS UI 是画面框架，成年女主在桌面壁纸场景中通过镜头与用户互动；用户仅以画外音存在，绝不出镜。

## 功能特点

- **先确认后生成**：首次创作指令先输出"制作确认单"（桌面系统 / 参考图预留 / 成片规格 / 人物互动 / 字幕 UI），确认后才产出完整提示词
- **单一桌面系统**：macOS / Windows / 自定义三选一，不混入另一系统 UI
- **一镜到底时间轴**：精确到时间码的连续镜头编排，含服装/位置、动作、台词、聆听反应、音效、微表情
- **可选字幕 UI**：启用后固定在屏幕左侧中部，仅含字幕文字、样式及颜色、音频波形动效；不使用任何图标、头像、按钮或具象说话者标记，并提供后期覆盖 cue sheet 保证中文准确
- **微表情方法论**：每个情绪转折用 1–3 个可观察的面部细节描述，拒绝"生气""心软"等抽象词
- **参考图分组**：人物 / 桌面 UI / 场景 / 服装四类参考图分开声明锁定范围，防止错误继承

## 目录结构

```text
desktop-girlfriend-video-prompt/
├── SKILL.md                        # 主规则：确认单、创作模式、生成要求、自检
├── agents/
│   └── openai.yaml                 # Agent 界面配置
└── references/
    ├── configuration.md            # 配置字段表、主题路由、时长预算
    ├── micro-expressions.md        # 微表情参考与情绪组合
    ├── output-format.md            # 输出格式：主提示词、时间轴、cue sheet
    └── quality-checklist.md        # 交付前质量自检清单
```

## 安装（WorkBuddy）

```bash
git clone https://github.com/renhairong/desktop-girlfriend-video-prompt.git \
  ~/.workbuddy/skills/desktop-girlfriend-video-prompt
```

重开会话后，用自然语言触发即可，例如：

> 为我设计一段桌面 AI 女友互动视频提示词，并包含时间轴、字幕 cue sheet 和负面约束。

## 内容边界

- 女主必须是**成年角色**，无幼态化表达
- 男主（用户）仅画外音，不出镜、不出现任何可识别元素
- 默认只写提示词与制作说明；生视频工具调用与参考图上传需用户明确授权

## License

MIT
