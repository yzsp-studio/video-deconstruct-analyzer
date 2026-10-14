<div align="center">

# 🎬 video-deconstruct-analyzer

## 拆一条 AI 视频：30 字定性 + 8 维分析 + 最少段数提示词
## One AI video in: 8-dimension teardown plus the fewest prompts that cover it

📮 **商务合作 / Business：wow.vip@foxmail.com**
🎬 **抖音 / Douyin：[v.douyin.com/07EjIDGVErY](https://v.douyin.com/07EjIDGVErY/)**

</div>

---

## 🇨🇳 中文

这是面向 Hub 工具链优化的 AI 视频深度拆解技能：先用元信息拿到时长、宽高比例、横竖屏方向和媒体类型，语义读取成功且够细就直接分析，超时、失败、太笼统或动作细节不足时必须转入高密度关键帧分支。抽帧密度有硬标准——15 秒内至少 10–12 帧，16–30 秒至少 16–20 帧，31–60 秒按每 1.5–2 秒至少 1 帧，快动作和转场密集提高到每秒 1 帧，并且拼图格数不得小于实际帧数。关键帧拼图必须放到画布，Markdown 报告用 sourceNodeIds 挂回证据链，报告按元信息、一句话定性、八维度分析、剧情时间线、提示词、统一负面词、拆解理由和自检结果组织。最后按「每条尽量 15 秒、条数尽量少」输出中文时间戳分镜提示词，理论段数等于时长除以 15 向上取整。

### ✨ 能做什么

- 先读时长、比例、分辨率与媒体类型；语义太粗就切高密度关键帧分支，15 秒少于 10 帧判不合格
- 八维度拆解：角色、场景、剧情、镜头、光影、风格、节奏、声音，未选维度一行带过
- 关键帧拼图必须上画布，Markdown 报告用 sourceNodeIds 建立可追溯证据链，对话只做摘要
- 提示词按 ceil(时长/15) 最少段数输出：15 秒 1 条、30 秒 2 条、45 秒 3 条、60 秒 4 条
- 每条写成 0-3、3-6、6-9、9-12、12-15 秒时间戳分镜，标明时长与画幅，镜头用中文术语
- 多条提示词之间补衔接点：尾帧角色位置、动作、光影与镜头状态；句末附全片统一负面词

### 📦 包含的技能

- `video-deconstruct-analyzer` —— 见 [`video-deconstruct-analyzer/SKILL.md`](video-deconstruct-analyzer/SKILL.md)

### 🚀 安装

```bash
git clone https://github.com/yzsp-studio/video-deconstruct-analyzer.git
cp -r video-deconstruct-analyzer/* "$DSH_HOME/skills/"
```

> 技能是**纯文本说明**（`SKILL.md` + `references/`），零依赖、零 API key，用你当前 agent 的会话额度。

---

## 🇬🇧 English

This skill does deep AI-video teardown optimized for the Hub toolchain: it first reads metadata for duration, aspect ratio, orientation, and media type, proceeds straight to analysis when semantic reading is successful and detailed enough, and must switch to the high-density keyframe branch when that read times out, fails, stays vague, or lacks action detail. Frame density has hard standards: at least 10-12 keyframes for 0-15s, at least 16-20 for 16-30s, one frame per 1.5-2 seconds for 31-60s, and one frame per second for fast action or transition-heavy footage, with tile capacity never below the actual frame count. Keyframe mosaics must go onto the canvas and the Markdown report links back through sourceNodeIds, structured as metadata, a one-sentence characterization, eight-dimension analysis, story timeline, prompts, unified negative terms, the reasoning behind the split, and a self-check. It finishes with Chinese timestamp storyboard prompts written as few and as close to 15 seconds each as possible, where the theoretical segment count is duration divided by 15, rounded up.

### ✨ What it does

- Reads duration, ratio, resolution, and media type first; coarse semantics trigger the dense-keyframe branch, and under 10 frames for 15s fails the check
- Eight-dimension teardown covering character, scene, story, camera, lighting, style, rhythm, and sound, with unchosen dimensions given one line
- Keyframe mosaics go on the canvas and the Markdown report builds a traceable evidence chain via sourceNodeIds, while chat stays a summary
- Prompt count follows the minimum of duration divided by 15, rounded up: 1 for 15s, 2 for 30s, 3 for 45s, 4 for 60s
- Each prompt uses 0-3, 3-6, 6-9, 9-12, and 12-15 second timestamp beats with duration and aspect ratio stated and Chinese camera terminology
- Multi-prompt sets include handoff notes for tail-frame character position, action, lighting, and camera state, plus unified negative terms for the whole film

### 📦 Skills included

- `video-deconstruct-analyzer` — [`video-deconstruct-analyzer/SKILL.md`](video-deconstruct-analyzer/SKILL.md)

### 🚀 Install

```bash
git clone https://github.com/yzsp-studio/video-deconstruct-analyzer.git
cp -r video-deconstruct-analyzer/* "$DSH_HOME/skills/"
```

> Skills are **plain-text instructions** (`SKILL.md` + `references/`). Zero dependencies, no API keys — they run on your agent's existing session quota.

---

## 📮 联系 / Contact

| | |
|---|---|
| 🎬 **抖音 / Douyin** | [https://v.douyin.com/07EjIDGVErY/](https://v.douyin.com/07EjIDGVErY/) |
| 📮 **商务合作 / Business** | **wow.vip@foxmail.com** |
| 🐙 **GitHub** | [https://github.com/yzsp-ai](https://github.com/yzsp-ai) |
| 💖 **打赏 / Support** | [afdian.com/a/yzsp-ai](https://afdian.com/a/yzsp-ai) |

## 📄 License

[MIT](LICENSE) · © 2026 [yzsp-ai](https://github.com/yzsp-ai)
