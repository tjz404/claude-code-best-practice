# claude-code-best-practice
从氛围编程（vibe coding）到智能体工程（agentic engineering）- 熟能生巧，Claude 更强（practice makes claude perfect）

![updated with Claude Code](https://img.shields.io/badge/updated_with_Claude_Code-v2.1.126%20(May%2002%2C%202026%203%3A17%20PM%20PKT)-white?style=flat&labelColor=555) <a href="https://github.com/shanraisshan/claude-code-best-practice/stargazers"><img src="https://img.shields.io/github/stars/shanraisshan/claude-code-best-practice?style=flat&label=%E2%98%85&labelColor=555&color=white" alt="GitHub Stars"></a><br>

[![Best Practice](!/tags/best-practice.svg)](best-practice/) [![Implemented](!/tags/implemented.svg)](implementation/) [![Orchestration Workflow](!/tags/orchestration-workflow.svg)](orchestration-workflow/orchestration-workflow.md) [![Claude](!/tags/claude.svg)](https://code.claude.com/docs) [![Boris](!/tags/boris-cherny.svg)](#-tips-and-tricks) [![Community](!/tags/community.svg)](#-subscribe) ![Click on these badges below to see the actual sources](!/tags/click-badges.svg)<br>
<img src="!/tags/a.svg" height="14"> = 智能体 (Agents) · <img src="!/tags/c.svg" height="14"> = 命令 (Commands) · <img src="!/tags/s.svg" height="14"> = 技能 (Skills)

<p align="center">
  <img src="!/claude-jumping.svg" alt="Claude Code mascot jumping" width="120" height="100"><br>
  <a href="https://github.com/trending"><img src="!/root/github-trending-day.svg" alt="GitHub Trending #1 Repository Of The Day"></a>
</p>

<p align="center">
  <img src="!/root/boris-slider.gif" alt="Boris Cherny on Claude Code" width="600"><br>
  Boris Cherny 在 X 上 (<a href="https://x.com/bcherny/status/2007179832300581177">推文 1</a> · <a href="https://x.com/bcherny/status/2017742741636321619">推文 2</a> · <a href="https://x.com/bcherny/status/2021699851499798911">推文 3</a>)
</p>

> [!TIP]
> 请访问 [**如何使用**](#如何使用) 部分，以充分利用本仓库。

## 🧠 核心概念 (CONCEPTS)

| 特性 | 位置 | 描述 |
|---------|----------|-------------|
| <img src="!/tags/a.svg" height="14"> [**子智能体 (Subagents)**](https://code.claude.com/docs/en/sub-agents) | `.claude/agents/<name>.md` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-subagents.md) [![Implemented](!/tags/implemented.svg)](implementation/claude-subagents-implementation.md) |
| <img src="!/tags/c.svg" height="14"> [**命令 (Commands)**](https://code.claude.com/docs/en/slash-commands) | `.claude/commands/<name>.md` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-commands.md) [![Implemented](!/tags/implemented.svg)](implementation/claude-commands-implementation.md) |
| <img src="!/tags/s.svg" height="14"> [**技能 (Skills)**](https://code.claude.com/docs/en/skills) | `.claude/skills/<name>/SKILL.md` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-skills.md) [![Implemented](!/tags/implemented.svg)](implementation/claude-skills-implementation.md) [官方技能](https://github.com/anthropics/skills/tree/main/skills) · [单体大仓库技能](reports/claude-skills-for-larger-mono-repos.md) |
| [**工作流 (Workflows)**](https://code.claude.com/docs/en/common-workflows) | [`.claude/commands/weather-orchestrator.md`](.claude/commands/weather-orchestrator.md) | [![Orchestration Workflow](!/tags/orchestration-workflow.svg)](orchestration-workflow/orchestration-workflow.md) |
| [**钩子 (Hooks)**](https://code.claude.com/docs/en/hooks) | `.claude/hooks/` | [![Best Practice](!/tags/best-practice.svg)](https://github.com/shanraisshan/claude-code-hooks) [![Implemented](!/tags/implemented.svg)](https://github.com/shanraisshan/claude-code-hooks) [指南](https://code.claude.com/docs/en/hooks-guide) |
| [**MCP 服务器**](https://code.claude.com/docs/en/mcp) | `.claude/settings.json`, `.mcp.json` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-mcp.md) [![Implemented](!/tags/implemented.svg)](.mcp.json) |
| [**插件 (Plugins)**](https://code.claude.com/docs/en/plugins) | 可分发包 | [应用市场](https://code.claude.com/docs/en/discover-plugins) · [创建市场](https://code.claude.com/docs/en/plugin-marketplaces) |
| [**设置 (Settings)**](https://code.claude.com/docs/en/settings) | `.claude/settings.json` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-settings.md) [![Implemented](!/tags/implemented.svg)](.claude/settings.json) [权限](https://code.claude.com/docs/en/permissions) · [模型配置](https://code.claude.com/docs/en/model-config) · [输出风格](https://code.claude.com/docs/en/output-styles) · [沙盒](https://code.claude.com/docs/en/sandboxing) · [快捷键](https://code.claude.com/docs/en/keybindings) · [自动模式配置](https://code.claude.com/docs/en/auto-mode-config) |
| [**状态栏 (Status Line)**](https://code.claude.com/docs/en/statusline) | `.claude/settings.json` | [![Best Practice](!/tags/best-practice.svg)](https://github.com/shanraisshan/claude-code-status-line) [![Implemented](!/tags/implemented.svg)](.claude/settings.json) |
| [**记忆 (Memory)**](https://code.claude.com/docs/en/memory) | `CLAUDE.md`, `.claude/rules/`, `~/.claude/rules/`, `~/.claude/projects/<project>/memory/` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-memory.md) [![Implemented](!/tags/implemented.svg)](CLAUDE.md) [自动记忆](https://code.claude.com/docs/en/memory) · [自动记忆深度解析](reports/claude-agent-memory.md) · [规则](https://code.claude.com/docs/en/memory#organize-rules-with-clauderules) |
| [**检查点 (Checkpointing)**](https://code.claude.com/docs/en/checkpointing) | 自动 (基于 git) |  |
| [**CLI 启动参数**](https://code.claude.com/docs/en/cli-reference) | `claude [flags]` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-cli-startup-flags.md) [交互模式](https://code.claude.com/docs/en/interactive-mode) · [环境变量](https://code.claude.com/docs/en/env-vars) |
| **AI 术语** | | [![Best Practice](!/tags/best-practice.svg)](https://github.com/shanraisshan/claude-code-codex-cursor-gemini/blob/main/reports/ai-terms.md) |
| [**最佳实践 (Best Practices)**](https://code.claude.com/docs/en/best-practices) | | [提示词工程](https://github.com/anthropics/prompt-eng-interactive-tutorial) · [扩展 Claude Code](https://code.claude.com/docs/en/features-overview) |

### 🔥 热门特性

| 特性 | 位置 | 描述 |
|---------|----------|-------------|
| [**极限审查 (Ultrareview)**](https://code.claude.com/docs/en/ultrareview) ![beta](!/tags/beta.svg) | `/ultrareview`, `claude ultrareview [target]` | [任务跟踪](https://code.claude.com/docs/en/ultrareview#track-a-running-review) |
| [**开发容器 (Devcontainers)**](https://code.claude.com/docs/en/devcontainer) | `.devcontainer/` |  |
| [**频道 (Channels)**](https://code.claude.com/docs/en/channels) ![beta](!/tags/beta.svg) | `--channels`, 基于插件 | [参考文档](https://code.claude.com/docs/en/channels-reference) |
| [**极限计划 (Ultraplan)**](https://code.claude.com/docs/en/ultraplan) ![beta](!/tags/beta.svg) | `/ultraplan` |  |
| [**无闪烁模式 (No Flicker Mode)**](https://code.claude.com/docs/en/fullscreen) ![beta](!/tags/beta.svg) | `/tui fullscreen`, `CLAUDE_CODE_NO_FLICKER=1` | [![Best Practice](!/tags/best-practice.svg)](https://x.com/bcherny/status/2039421575422980329) |
| [**自动模式 (Auto Mode)**](https://code.claude.com/docs/en/permission-modes#eliminate-prompts-with-auto-mode) ![beta](!/tags/beta.svg) | `--permission-mode auto`, `Shift+Tab` | [![Best Practice](!/tags/best-practice.svg)](https://x.com/claudeai/status/2036503582166393240) [博客](https://claude.com/blog/auto-mode) |
| [**强化/能量包 (Power-ups)**](best-practice/claude-power-ups.md) | `/powerup` | [![Best Practice](!/tags/best-practice.svg)](best-practice/claude-power-ups.md) |
| [**快速模式 (Fast Mode)**](https://code.claude.com/docs/en/fast-mode) ![beta](!/tags/beta.svg) | `/fast`, `"fastMode": true` |  |
| [**计算机控制 (Computer Use)**](https://code.claude.com/docs/en/computer-use) ![beta](!/tags/beta.svg) | `computer-use` MCP 服务器 | [桌面](https://code.claude.com/docs/en/desktop#let-claude-use-your-computer) |
| [**智能体 SDK (Agent SDK)**](https://code.claude.com/docs/en/agent-sdk/overview) | `npm` / `pip` 包 | [快速入门](https://code.claude.com/docs/en/agent-sdk/quickstart) · [示例](https://github.com/anthropics/claude-agent-sdk-demos) |
| [**Ralph Wiggum 循环**](https://github.com/anthropics/claude-code/tree/main/plugins/ralph-wiggum) | 插件 | [![Best Practice](!/tags/best-practice.svg)](https://github.com/ghuntley/how-to-ralph-wiggum) [![Implemented](!/tags/implemented.svg)](https://github.com/shanraisshan/ralph-wiggum-self-evolving-loop) |
| [**Chrome**](https://code.claude.com/docs/en/chrome) ![beta](!/tags/beta.svg) | `--chrome`, 扩展程序 | [![Best Practice](!/tags/best-practice.svg)](reports/claude-in-chrome-v-chrome-devtools-mcp.md) |
| [**Claude Code 网页版**](https://code.claude.com/docs/en/claude-code-on-the-web) ![beta](!/tags/beta.svg) | `claude.ai/code` | [惯例 (Routines)](https://code.claude.com/docs/en/routines) |
| [**Slack**](https://code.claude.com/docs/en/slack) | Slack 中的 `@Claude` |  |
| [**代码审查 (Code Review)**](https://code.claude.com/docs/en/code-review) ![beta](!/tags/beta.svg) | GitHub App (托管) | [![Best Practice](!/tags/best-practice.svg)](https://x.com/claudeai/status/2031088171262554195) [博客](https://claude.com/blog/code-review) |
| [**GitHub Actions**](https://code.claude.com/docs/en/github-actions) | `.github/workflows/` | [GitLab CI/CD](https://code.claude.com/docs/en/gitlab-ci-cd) |
| [**远程控制 (Remote Control)**](https://code.claude.com/docs/en/remote-control) | `/remote-control`, `/rc` | [![Best Practice](!/tags/best-practice.svg)](https://x.com/noahzweben/status/2032533699116355819) [无头模式 (Headless)](https://code.claude.com/docs/en/headless) |
| [**智能体团队 (Agent Teams)**](https://code.claude.com/docs/en/agent-teams) ![beta](!/tags/beta.svg) | 内置 (环境变量) | [![Best Practice](!/tags/best-practice.svg)](https://x.com/bcherny/status/2019472394696683904) [![Implemented](!/tags/implemented.svg)](implementation/claude-agent-teams-implementation.md) |
| [**定时任务 (Scheduled Tasks)**](https://code.claude.com/docs/en/scheduled-tasks) | `/loop`, `/schedule`, cron 工具 | [![Best Practice](!/tags/best-practice.svg)](https://x.com/bcherny/status/2030193932404150413) [![Implemented](!/tags/implemented.svg)](implementation/claude-scheduled-tasks-implementation.md) [桌面定时任务](https://code.claude.com/docs/en/desktop-scheduled-tasks) · [公告](https://x.com/noahzweben/status/2036129220959805859) |
| [**惯例 (Routines)**](https://code.claude.com/docs/en/routines) ![beta](!/tags/beta.svg) | `claude.ai/code/routines`, `/schedule` | [桌面任务](https://code.claude.com/docs/en/desktop-scheduled-tasks) |
| [**任务 (Tasks)**](reports/claude-global-vs-project-settings.md#tasks-system) | `/tasks`, `~/.claude/tasks/` | [![Best Practice](!/tags/best-practice.svg)](reports/claude-global-vs-project-settings.md) [极限审查跟踪](https://code.claude.com/docs/en/ultrareview#track-a-running-review) |
| [**语音听写 (Voice Dictation)**](https://code.claude.com/docs/en/voice-dictation) ![beta](!/tags/beta.svg) | `/voice` | [![Best Practice](!/tags/best-practice.svg)](https://x.com/trq212/status/2028628570692890800) |
| [**简化与批处理 (Simplify & Batch)**](https://code.claude.com/docs/en/skills#bundled-skills) | `/simplify`, `/batch` | [![Best Practice](!/tags/best-practice.svg)](https://x.com/bcherny/status/2027534984534544489) |
| [**Git 工作树 (Git Worktrees)**](https://code.claude.com/docs/en/common-workflows#run-parallel-claude-code-sessions-with-git-worktrees) | 内置, `EnterWorktree`/`ExitWorktree`, `isolation: "worktree"` | [![Best Practice](!/tags/best-practice.svg)](https://x.com/bcherny/status/2025007393290272904) |

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

<a id="orchestration-workflow"></a>

## <a href="orchestration-workflow/orchestration-workflow.md"><img src="!/tags/orchestration-workflow-hd.svg" alt="Orchestration Workflow"></a>

请参阅 [编排工作流 (orchestration-workflow)](orchestration-workflow/orchestration-workflow.md) 了解 <img src="!/tags/c.svg" height="14"> **命令** → <img src="!/tags/a.svg" height="14"> **智能体** → <img src="!/tags/s.svg" height="14"> **技能** 模式的具体实现细节。

<p align="center">
  <img src="orchestration-workflow/orchestration-workflow.svg" alt="Command Skill Agent Architecture Flow" width="100%">
</p>

<p align="center">
  <img src="orchestration-workflow/orchestration-workflow.gif" alt="Orchestration Workflow Demo" width="600">
</p>

![How to Use](!/tags/how-to-use.svg)

```bash
claude
/weather-orchestrator
```

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## ⚙️ 开发工作流 (DEVELOPMENT WORKFLOWS)

所有主要工作流都汇聚于相同的架构模式：**研究 (Research) → 计划 (Plan) → 执行 (Execute) → 审查 (Review) → 发布 (Ship)**

| 名称 | ★ | 工作流 | <img src="!/tags/a.svg" height="14"> | <img src="!/tags/c.svg" height="14"> | <img src="!/tags/s.svg" height="14"> |
|------|---|----------|---|---|---|
| [Superpowers](https://github.com/obra/superpowers) | 175k | <img src="https://img.shields.io/badge/brainstorming-ddf4ff" alt="brainstorming" align="middle"> → <img src="https://img.shields.io/badge/using--git--worktrees-ddf4ff" alt="using-git-worktrees" align="middle"> → <img src="https://img.shields.io/badge/writing--plans-ddf4ff" alt="writing-plans" align="middle"> → <img src="https://img.shields.io/badge/subagent--driven--development-ddf4ff" alt="subagent-driven-development" align="middle"> → <img src="https://img.shields.io/badge/test--driven--development-fff3b0" alt="test-driven-development" align="middle"> → <img src="https://img.shields.io/badge/requesting--code--review-fff3b0" alt="requesting-code-review" align="middle"> → <img src="https://img.shields.io/badge/finishing--a--development--branch-ddf4ff" alt="finishing-a-development-branch" align="middle"> | 5 | 3 | 14 |
| [Everything Claude Code](https://github.com/affaan-m/everything-claude-code) | 171k | <img src="https://img.shields.io/badge/%2Fecc:plan-ddf4ff" alt="/ecc:plan" align="middle"> → <img src="https://img.shields.io/badge/%2Ftdd-ddf4ff" alt="/tdd" align="middle"> → <img src="https://img.shields.io/badge/%2Fcode--review-ddf4ff" alt="/code-review" align="middle"> → <img src="https://img.shields.io/badge/%2Fsecurity--scan-ddf4ff" alt="/security-scan" align="middle"> → <img src="https://img.shields.io/badge/%2Fe2e-ddf4ff" alt="/e2e" align="middle"> → <img src="https://img.shields.io/badge/merge-ddf4ff" alt="merge" align="middle"> | 48 | 143 | 230 |
| [Spec Kit](https://github.com/github/spec-kit) | 92k | <img src="https://img.shields.io/badge/%2Fspeckit.constitution-ddf4ff" alt="/speckit.constitution" align="middle"> → <img src="https://img.shields.io/badge/%2Fspeckit.clarify-ddf4ff" alt="/speckit.clarify" align="middle"> → <img src="https://img.shields.io/badge/%2Fspeckit.specify-ddf4ff" alt="/speckit.specify" align="middle"> → <img src="https://img.shields.io/badge/%2Fspeckit.plan-ddf4ff" alt="/speckit.plan" align="middle"> → <img src="https://img.shields.io/badge/%2Fspeckit.tasks-ddf4ff" alt="/speckit.tasks" align="middle"> → <img src="https://img.shields.io/badge/%2Fspeckit.implement-ddf4ff" alt="/speckit.implement" align="middle"> | 0 | 9 | 0 |
| [gstack](https://github.com/garrytan/gstack) | 88k | <img src="https://img.shields.io/badge/%2Foffice--hours-ddf4ff" alt="/office-hours" align="middle"> → <img src="https://img.shields.io/badge/%2Fplan--ceo--review-ddf4ff" alt="/plan-ceo-review" align="middle"> → <img src="https://img.shields.io/badge/%2Fplan--eng--review-ddf4ff" alt="/plan-eng-review" align="middle"> → <img src="https://img.shields.io/badge/%2Fplan--design--review-ddf4ff" alt="/plan-design-review" align="middle"> → <img src="https://img.shields.io/badge/implement-ddf4ff" alt="implement" align="middle"> → <img src="https://img.shields.io/badge/%2Freview-ddf4ff" alt="/review" align="middle"> → <img src="https://img.shields.io/badge/%2Fqa-ddf4ff" alt="/qa" align="middle"> → <img src="https://img.shields.io/badge/%2Fship-ddf4ff" alt="/ship" align="middle"> → <img src="https://img.shields.io/badge/%2Fland--and--deploy-ddf4ff" alt="/land-and-deploy" align="middle"> | 0 | 0 | 43 |
| [Get Shit Done](https://github.com/gsd-build/get-shit-done) | 59k | <img src="https://img.shields.io/badge/%2Fgsd--new--project-ddf4ff" alt="/gsd-new-project" align="middle"> → <img src="https://img.shields.io/badge/%2Fgsd--discuss--phase-ddf4ff" alt="/gsd-discuss-phase" align="middle"> → <img src="https://img.shields.io/badge/%2Fgsd--plan--phase-ddf4ff" alt="/gsd-plan-phase" align="middle"> → <img src="https://img.shields.io/badge/%2Fgsd--execute--phase-ddf4ff" alt="/gsd-execute-phase" align="middle"> → <img src="https://img.shields.io/badge/%2Fgsd--verify--work-fff3b0" alt="/gsd-verify-work" align="middle"> → <img src="https://img.shields.io/badge/%2Fgsd--ship-ddf4ff" alt="/gsd-ship" align="middle"> → <img src="https://img.shields.io/badge/%2Fgsd--complete--milestone-ddf4ff" alt="/gsd-complete-milestone" align="middle"> | 33 | 65 | 0 |
| [Matt Pocock Skills](https://github.com/mattpocock/skills) | 51k | <img src="https://img.shields.io/badge/%2Fgrill--with--docs-ddf4ff" alt="/grill-with-docs" align="middle"> → <img src="https://img.shields.io/badge/%2Fto--prd-ddf4ff" alt="/to-prd" align="middle"> → <img src="https://img.shields.io/badge/%2Fto--issues-ddf4ff" alt="/to-issues" align="middle"> → <img src="https://img.shields.io/badge/%2Ftriage-ddf4ff" alt="/triage" align="middle"> → <img src="https://img.shields.io/badge/%2Ftdd-fff3b0" alt="/tdd" align="middle"> → <img src="https://img.shields.io/badge/%2Fdiagnose-fff3b0" alt="/diagnose" align="middle"> → <img src="https://img.shields.io/badge/%2Fimprove--codebase--architecture-ddf4ff" alt="/improve-codebase-architecture" align="middle"> → <img src="https://img.shields.io/badge/%2Fzoom--out-ddf4ff" alt="/zoom-out" align="middle"> | 0 | 0 | 22 |
| [BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD) | 46k | <img src="https://img.shields.io/badge/bmad--product--brief-ddf4ff" alt="bmad-product-brief" align="middle"> → <img src="https://img.shields.io/badge/bmad--create--prd-ddf4ff" alt="bmad-create-prd" align="middle"> → <img src="https://img.shields.io/badge/bmad--create--architecture-ddf4ff" alt="bmad-create-architecture" align="middle"> → <img src="https://img.shields.io/badge/bmad--create--epics--and--stories-ddf4ff" alt="bmad-create-epics-and-stories" align="middle"> → <img src="https://img.shields.io/badge/bmad--sprint--planning-ddf4ff" alt="bmad-sprint-planning" align="middle"> → <img src="https://img.shields.io/badge/bmad--create--story-fff3b0" alt="bmad-create-story" align="middle"> → <img src="https://img.shields.io/badge/bmad--dev--story-fff3b0" alt="bmad-dev-story" align="middle"> → <img src="https://img.shields.io/badge/bmad--code--review-fff3b0" alt="bmad-code-review" align="middle"> → <img src="https://img.shields.io/badge/bmad--retrospective-ddf4ff" alt="bmad-retrospective" align="middle"> | 0 | 0 | 40 |
| [OpenSpec](https://github.com/Fission-AI/OpenSpec) | 45k | <img src="https://img.shields.io/badge/%2Fopsx:propose-ddf4ff" alt="/opsx:propose" align="middle"> → <img src="https://img.shields.io/badge/%2Fopsx:apply-ddf4ff" alt="/opsx:apply" align="middle"> → <img src="https://img.shields.io/badge/%2Fopsx:archive-ddf4ff" alt="/opsx:archive" align="middle"> | 0 | 11 | 0 |
| [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) | 32k | <img src="https://img.shields.io/badge/%2Fdeep--interview-ddf4ff" alt="/deep-interview" align="middle"> → <img src="https://img.shields.io/badge/%2Fteam-ddf4ff" alt="/team" align="middle"> → <img src="https://img.shields.io/badge/team--plan-fff3b0" alt="team-plan" align="middle"> → <img src="https://img.shields.io/badge/team--prd-fff3b0" alt="team-prd" align="middle"> → <img src="https://img.shields.io/badge/team--exec-fff3b0" alt="team-exec" align="middle"> → <img src="https://img.shields.io/badge/team--verify-fff3b0" alt="team-verify" align="middle"> → <img src="https://img.shields.io/badge/team--fix-fff3b0" alt="team-fix" align="middle"> → <img src="https://img.shields.io/badge/%2Fralph-ddf4ff" alt="/ralph" align="middle"> → <img src="https://img.shields.io/badge/merge-ddf4ff" alt="merge" align="middle"> | 19 | 0 | 38 |
| [agent-skills](https://github.com/addyosmani/agent-skills) | 27k | <img src="https://img.shields.io/badge/%2Fspec-ddf4ff" alt="/spec" align="middle"> → <img src="https://img.shields.io/badge/%2Fplan-ddf4ff" alt="/plan" align="middle"> → <img src="https://img.shields.io/badge/%2Fbuild-ddf4ff" alt="/build" align="middle"> → <img src="https://img.shields.io/badge/%2Ftest-ddf4ff" alt="/test" align="middle"> → <img src="https://img.shields.io/badge/%2Freview-ddf4ff" alt="/review" align="middle"> → <img src="https://img.shields.io/badge/%2Fship-ddf4ff" alt="/ship" align="middle"> | 3 | 7 | 21 |
| [Compound Engineering](https://github.com/EveryInc/compound-engineering-plugin) | 16k | <img src="https://img.shields.io/badge/%2Fce--ideate-ddf4ff" alt="/ce-ideate" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--brainstorm-ddf4ff" alt="/ce-brainstorm" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--plan-ddf4ff" alt="/ce-plan" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--work-ddf4ff" alt="/ce-work" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--code--review-ddf4ff" alt="/ce-code-review" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--debug-fff3b0" alt="/ce-debug" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--optimize-fff3b0" alt="/ce-optimize" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--compound-ddf4ff" alt="/ce-compound" align="middle"> → <img src="https://img.shields.io/badge/%2Fce--compound--refresh-fff3b0" alt="/ce-compound-refresh" align="middle"> | 49 | 4 | 39 |
| [HumanLayer](https://github.com/humanlayer/humanlayer) | 11k | <img src="https://img.shields.io/badge/%2Fcreate__plan-ddf4ff" alt="/create_plan" align="middle"> → <img src="https://img.shields.io/badge/%2Fvalidate__plan-ddf4ff" alt="/validate_plan" align="middle"> → <img src="https://img.shields.io/badge/%2Fimplement__plan-ddf4ff" alt="/implement_plan" align="middle"> → <img src="https://img.shields.io/badge/%2Fiterate__plan-fff3b0" alt="/iterate_plan" align="middle"> → <img src="https://img.shields.io/badge/%2Flocal__review-ddf4ff" alt="/local_review" align="middle"> → <img src="https://img.shields.io/badge/%2Fcommit-ddf4ff" alt="/commit" align="middle"> | 6 | 27 | 0 |

> *注意：黄色标签表示子循环 —— 在父步骤中重复执行的步骤（例如按任务、按故事，或直到验证条件通过为止）。*

### 其他
- [跨模型 (Claude Code + Codex) 工作流](development-workflows/cross-model-workflow/cross-model-workflow.md) [![Implemented](!/tags/implemented.svg)](development-workflows/cross-model-workflow/cross-model-workflow.md)
- [RPI](development-workflows/rpi/rpi-workflow.md) [![Implemented](!/tags/implemented.svg)](development-workflows/rpi/rpi-workflow.md)
- [Ralph Wiggum 循环](https://www.youtube.com/watch?v=eAtvoGlpeRU) [![Implemented](!/tags/implemented.svg)](https://github.com/shanraisshan/ralph-wiggum-self-evolving-loop)
- [Andrej Karpathy (OpenAI 创始成员) 工作流](https://x.com/karpathy/status/2015883857489522876)
- [Peter Steinberger (OpenClaw 创始人) 工作流](https://youtu.be/8lF7HmQ_RgY?t=2582)
- Boris Cherny (Claude Code 创始人) 工作流 — [13 个技巧](tips/claude-boris-13-tips-03-jan-26.md) · [10 个技巧](tips/claude-boris-10-tips-01-feb-26.md) · [12 个技巧](tips/claude-boris-12-tips-12-feb-26.md) · [2 个技巧](tips/claude-boris-2-tips-25-mar-26.md) · [15 个技巧](tips/claude-boris-15-tips-30-mar-26.md) · [6 个技巧](tips/claude-boris-6-tips-16-apr-26.md) [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny)
- Thariq (Anthropic) 工作流 — [技能](tips/claude-thariq-tips-17-mar-26.md) · [会话管理](tips/claude-thariq-tips-16-apr-26.md) [![Thariq](!/tags/thariq.svg)](https://x.com/trq212)

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## 🧰 技能集合 (SKILL COLLECTIONS)

主要作为 `SKILL.md` 文件精选库的仓库（区别于上述完整的工作流方法论）。按星标数降序排列。

| 名称 | ★ | <img src="!/tags/s.svg" height="14"> |
|------|---|---|
| [anthropics/skills](https://github.com/anthropics/skills) | 127k | 17 |
| [mattpocock/skills](https://github.com/mattpocock/skills) | 51k | 18 |
| [wshobson/agents](https://github.com/wshobson/agents) | 35k | 152 |
| [agent-skills](https://github.com/addyosmani/agent-skills) | 27k | 21 |
| [scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) | 20k | 134 |
| [awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 20k | 930+ (精选列表) |

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## 💡 提示与技巧 (83)

🚫👶 = 不要当保姆 (do not babysit)

[提示词 (Prompting)](#tips-prompting) · [计划 (Planning)](#tips-planning) · [上下文 (Context)](#tips-context) · [会话 (Session)](#tips-session) · [CLAUDE.md + 规则](#tips-claudemd) · [智能体 (Agents)](#tips-agents) · [命令 (Commands)](#tips-commands) · [技能 (Skills)](#tips-skills) · [钩子 (Hooks)](#tips-hooks) · [工作流 (Workflows)](#tips-workflows) · [进阶 (Advanced)](#tips-workflows-advanced) · [Git / PR](#tips-git-pr) · [调试 (Debugging)](#tips-debugging) · [实用工具 (Utilities)](#tips-utilities) · [日常 (Daily)](#tips-daily)

![Community](!/tags/community.svg)

<a id="tips-prompting"></a>■ **提示词 (Prompting) (3)**

| 技巧 | 来源 |
|-----|--------|
| 挑战 Claude —— "针对这些更改盘问我，在我通过你的测试之前不要提交 PR。" 或 "向我证明这能起作用"，并让 Claude 比较 main 和你的分支的差异 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742752566632544) |
| 在进行了一个平庸的修复后 —— "结合你现在所知道的一切，放弃这个方案并实现一个优雅的解决方案" 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742752566632544) |
| Claude 能自行修复大多数 bug —— 粘贴 bug，说 "修复 (fix)"，不要微观管理它是怎么修的 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742750473720121) |

<a id="tips-planning"></a>■ **计划与规范 (Planning/Specs) (7)**

| 技巧 | 来源 |
|-----|--------|
| 始终从 [计划模式 (plan mode)](https://code.claude.com/docs/en/common-workflows) 开始 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179845336527000) |
| 从最小的规范或提示词开始，要求 Claude 使用 [AskUserQuestion](https://code.claude.com/docs/en/cli-reference) 工具对你进行采访，然后开启一个新会话来执行规范 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2005315275026260309) |
| 始终制定分阶段门控的计划，每个阶段都应包含多种测试 (单元、自动化、集成) | [![Dex](!/tags/community-dex.svg)](videos/claude-dex-mlops-community-24-mar-26.md) [![Video](!/tags/video.svg)](https://youtu.be/YwZR6tc7qYg?t=1032) |
| 将 PRD 分解为贯穿所有层 (DB + 服务 + UI) 的垂直切片 (曳光弹) —— AI 默认倾向于水平分阶段 (DB 阶段，然后 API 阶段，再然后前端阶段)，这会将端到端反馈延迟到最后一个阶段。源自《程序员修炼之道》 🚫👶 | [![Matt](!/tags/community-matt.svg)](videos/claude-matt-pocock-24-apr-26.md) [![Video](!/tags/video.svg)](https://youtu.be/-QFHIoCo-Ko) |
| 启动第二个 Claude 作为主任工程师来审查你的计划，或者使用 [跨模型工作流](development-workflows/cross-model-workflow/cross-model-workflow.md) 进行审查 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742745365057733) |
| 在移交工作之前，编写详细的规范并减少歧义 —— 你越具体，输出就越好 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742752566632544) |
| 原型 > PRD —— 构建 20-30 个版本而不是花时间写规范，构建成本很低，可以多尝试几次 | [![Boris](!/tags/boris-cherny.svg)](https://youtu.be/julbw1JuAz0?t=3630) [![Video](!/tags/video.svg)](https://youtu.be/julbw1JuAz0?t=3630) |

<a id="tips-context"></a>■ **上下文 (Context) (5)**

| 技巧 | 来源 |
|-----|--------|
| 在 1M 上下文模型上，上下文腐败会在 ~300-400k token 时发生 —— 对于智力敏感的工作，不要让会话超过这个限制 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| 迟钝区大约在 40% 上下文时出现 —— "到达这个点后，结果质量会下降"。新手指南："尽量保持在 40% 以下，如果达到 60%，考虑结束会话"。老手指南："积极保持在 30% 以下" —— 只有在简单任务时才推至 60%。切换任务时手动使用 [/compact](https://code.claude.com/docs/en/interactive-mode) 或 [/clear](https://code.claude.com/docs/en/cli-reference) 重置 | [![Dex](!/tags/community-dex.svg)](videos/claude-dex-mlops-community-24-mar-26.md) [![Video](!/tags/video.svg)](https://youtu.be/YwZR6tc7qYg?t=1541) |
| 回溯 > 纠正 —— 连按两次 Esc 或使用 [/rewind](https://code.claude.com/docs/en/checkpointing) 回到失败尝试之前，并带着你学到的东西重新提示，而不是将失败的尝试 + 纠正过程留在上下文中污染环境 🚫👶 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| 带有提示的 [/compact](https://code.claude.com/docs/en/interactive-mode)（例如：/compact focus on the auth refactor, drop the test debugging）优于让其自动压缩 —— 模型在自动压缩时由于上下文腐败处于智力最低点 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| 使用子智能体进行上下文管理 —— 问自己："我还需要再次使用这个工具的输出，还是只需要最终结论？" —— 20 次文件读取 + 12 次 grep + 3 次死胡同都留在子智能体的上下文中，只有最终报告返回给主会话 🚫👶 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |

<a id="tips-session"></a>■ **会话管理 (Session Management) (6)**

| 技巧 | 来源 |
|-----|--------|
| 每一轮对话都是一个分支点 —— Claude 结束一轮后，根据你需要保留多少现有上下文，在 Continue、/rewind、/clear、/compact 或 子智能体 (Subagent) 之间做出选择 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| 新任务 = 新会话 —— 相关任务（例如为刚构建的功能写文档）可以重用上下文以提高效率，但真正的新任务值得开启全新会话 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| 回溯之前使用 "summarize from here" 让 Claude 写一条交接信息 —— 就像上一代 Claude 写给未来自己的便签一样 | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| /compact vs /clear —— compact 是有损的但能保持势头 (任务中途，模糊细节可接受)；/clear + 简报 需要更多工作，但你能精确控制带入的内容 (高风险的下一步) | [![Thariq](!/tags/thariq.svg)](tips/claude-thariq-tips-16-apr-26.md) |
| 对于长时间运行的会话使用 recaps (总结) —— 关于 Claude 做了什么和接下来要做什么的简短摘要，在几分钟或几小时后返回时非常有用。可以在 /config 中禁用 | [![Boris](!/tags/boris-cherny.svg)](tips/claude-boris-6-tips-16-apr-26.md) |
| 使用 [/rename](https://code.claude.com/docs/en/cli-reference) 重命名重要会话（例如 [TODO - refactor task]）并稍后 [/resume](https://code.claude.com/docs/en/cli-reference) 恢复它们 —— 同时运行多个 Claude 实例时为每个实例打标签 | [![Cat](!/tags/cat-wu.svg)](https://every.to/podcast/how-to-use-claude-code-like-the-people-who-built-it) |

<a id="tips-claudemd"></a>■ **CLAUDE.md + .claude/rules (8)**

| 技巧 | 来源 |
|-----|--------|
| [CLAUDE.md](https://code.claude.com/docs/en/memory) 每个文件最好保持在 [200 行](https://code.claude.com/docs/en/memory#write-effective-instructions) 以下。[humanlayer 建议 60 行](https://www.humanlayer.dev/blog/writing-a-good-claude-md)（[即便如此也不能 100% 保证被遵循](https://www.reddit.com/r/ClaudeCode/comments/1qn9pb9/claudemd_says_must_use_agent_claude_ignores_it_80/)） | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179840848597422) [![Dex](!/tags/community-dex.svg)](https://www.humanlayer.dev/blog/writing-a-good-claude-md) |
| .claude/rules/*.md 会像 CLAUDE.md 一样自动加载到每个会话中 —— 添加 `paths:` YAML frontmatter，以便仅当 Claude 接触匹配 glob 路径的文件时才懒加载它们 | [![Claude](!/tags/claude.svg)](https://code.claude.com/docs/en/memory#organize-rules-with-clauderules) |
| 将特定领域的 CLAUDE.md 规则包裹在 [\<important if="..."\> 标签](https://www.hlyr.dev/blog/stop-claude-from-ignoring-your-claude-md) 中，以防止 Claude 在文件变长时忽略它们 | [![Dex](!/tags/community-dex.svg)](https://www.hlyr.dev/blog/stop-claude-from-ignoring-your-claude-md) |
| 对于单体大仓库，使用 [多个 CLAUDE.md](best-practice/claude-memory.md) —— 祖先 + 后代加载机制 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2016339448863355206) |
| 使用 [.claude/rules/](https://code.claude.com/docs/en/memory#organize-rules-with-clauderules) 拆分超长的指令 | [![Claude](!/tags/claude.svg)](https://code.claude.com/docs/en/memory#organize-rules-with-clauderules) |
| 任何开发者都应该能启动 Claude，说 "运行测试"，然后一次成功 —— 如果失败了，说明你的 CLAUDE.md 缺少必要的 setup/build/test 命令 | [![Dex](!/tags/community-dex.svg)](https://x.com/dexhorthy/status/2034713765401551053) |
| 保持代码库整洁并完成迁移 —— 迁移到一半的框架会使模型混淆，可能选错模式 | [![Boris](!/tags/boris-cherny.svg)](https://youtu.be/julbw1JuAz0?t=1112) [![Video](!/tags/video.svg)](https://youtu.be/julbw1JuAz0?t=1112) |
| 使用 [settings.json](best-practice/claude-settings.md) 来强制执行底层行为 (如 attribution, permissions, model) —— 当 `attribution.commit: ""` 是确定性行为时，不要在 CLAUDE.md 中写 "NEVER add Co-Authored-By" | [![davila7](!/tags/community-davila7.svg)](https://x.com/dani_avila7/status/2036182734310195550) |

<a id="tips-agents"></a><img src="!/tags/a.svg" height="14"> **智能体 (Agents) (4)**

| 技巧 | 来源 |
|-----|--------|
| 拥有针对特定功能的 [子智能体](https://code.claude.com/docs/en/sub-agents) (提供额外上下文) 和 [技能](https://code.claude.com/docs/en/skills) (渐进式披露)，而不是通用的 "QA" 或 "后端工程师" 角色 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179850139000872) |
| 说 "使用子智能体 (use subagents)" 来投入更多算力解决问题 —— 卸载任务以保持主上下文干净聚焦 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742755737555434) |
| 使用 [配合 tmux 的智能体团队](https://code.claude.com/docs/en/agent-teams) 和 [git 工作树](https://x.com/bcherny/status/2025007393290272904) 进行并行开发 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2025007393290272904) |
| 使用 [测试时计算 (test time compute)](https://code.claude.com/docs/en/sub-agents) —— 独立的上下文窗口能产生更好的结果；一个智能体可能引发 bug，而另一个 (同模型) 智能体可以发现它 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2031151689219321886) |

<a id="tips-commands"></a><img src="!/tags/c.svg" height="14"> **命令 (Commands) (3)**

| 技巧 | 来源 |
|-----|--------|
| 为你的工作流使用 [命令 (commands)](https://code.claude.com/docs/en/slash-commands) 而不是 [子智能体](https://code.claude.com/docs/en/sub-agents) | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179847949500714) |
| 为你每天多次执行的每个 "内循环 (inner loop)" 工作流使用 [斜杠命令](https://code.claude.com/docs/en/slash-commands) —— 节省重复提示的时间，命令存放在 .claude/commands/ 中并纳入 git 版本控制 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179847949500714) |
| 如果你每天做某事超过一次，把它变成 [技能](https://code.claude.com/docs/en/skills) 或 [命令](https://code.claude.com/docs/en/slash-commands) —— 构建 /techdebt, context-dump, 或 analytics 命令 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742748984742078) |

<a id="tips-skills"></a><img src="!/tags/s.svg" height="14"> **技能 (Skills) (9)**

| 技巧 | 来源 |
|-----|--------|
| 使用 [context: fork](https://code.claude.com/docs/en/skills) 在隔离的子智能体中运行技能 —— 主上下文只看到最终结果，看不到中间的工具调用。`agent` 字段允许你设置子智能体类型 | [![Lydia](!/tags/lydia.svg)](https://x.com/lydiahallie/status/2033603164398883042) |
| 对于单体大仓库，[在子文件夹中使用技能](reports/claude-skills-for-larger-mono-repos.md) | [![Claude](!/tags/claude.svg)](https://code.claude.com/docs/en/skills) |
| 技能是文件夹，而不是单个文件 —— 使用 references/, scripts/, examples/ 子目录进行 [渐进式披露 (progressive disclosure)](https://code.claude.com/docs/en/skills) | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 在每个技能中建立一个 Gotchas (避坑指南) 部分 —— 包含最高价值的信号，随时间记录 Claude 容易失败的点 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 技能的 description 字段是触发器，而不是摘要 —— 为模型编写它 ("什么时候我应该触发它？") | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 不要在技能中陈述显而易见的事情 —— 专注于那些能把 Claude 推出其默认行为的东西 🚫👶 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 不要在技能中对 Claude 进行强行约束 —— 给出目标和约束，而不是规定性的按部就班指令 🚫👶 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 在技能中包含脚本和库，以便 Claude 进行组合，而不是让它从头重建样板代码 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 在 SKILL.md 中嵌入 `!command` 以将动态的 shell 输出注入提示词 —— Claude 在调用时运行它，模型只看到结果 | [![Lydia](!/tags/lydia.svg)](https://x.com/lydiahallie/status/2034337963820327017) |

<a id="tips-hooks"></a>■ **钩子 (Hooks) (5)**

| 技巧 | 来源 |
|-----|--------|
| 在技能中使用 [按需钩子](https://code.claude.com/docs/en/skills) —— 例如 `/careful` 阻止破坏性命令，`/freeze` 阻止对某目录外的编辑 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 使用 PreToolUse 钩子 [衡量技能使用情况](https://code.claude.com/docs/en/skills)，以找出最受欢迎或未被充分触发的技能 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 使用 [PostToolUse 钩子](https://code.claude.com/docs/en/hooks) 自动格式化代码 —— Claude 生成格式良好的代码，钩子处理最后 10% 以避免 CI 失败 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179852047335529) |
| 通过钩子将 [权限请求](https://code.claude.com/docs/en/hooks) 路由给 Opus 模型 —— 让它扫描恶意攻击并自动批准安全的请求 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742755737555434) |
| 使用 [Stop 钩子](https://code.claude.com/docs/en/hooks) 提示 Claude 在一轮结束时继续进行或验证其工作 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2021701059253874861) |

<a id="tips-workflows"></a>■ **工作流 (Workflows) (5)**

| 技巧 | 来源 |
|-----|--------|
| 使用 [/model](https://code.claude.com/docs/en/model-config) 选择模型和推理，[/context](https://code.claude.com/docs/en/interactive-mode) 查看上下文使用率，[/usage](https://code.claude.com/docs/en/costs) 检查额度，[/extra-usage](https://code.claude.com/docs/en/interactive-mode) 配置超额计费，[/config](https://code.claude.com/docs/en/settings) 配置设置 —— 使用 Opus 进行计划模式，Sonnet 负责编写代码，取两者之长 | [![Cat](!/tags/cat-wu.svg)](https://x.com/_catwu/status/1955694117264261609) |
| 在 [/config](https://code.claude.com/docs/en/settings) 中始终开启 [思考模式 (thinking mode)](https://code.claude.com/docs/en/model-config) 为 true (以查看推理过程)，并将 [输出风格 (Output Style)](https://code.claude.com/docs/en/output-styles) 设置为 Explanatory (以看到带有 ★ Insight 框的详细输出)，从而更好地理解 Claude 的决策 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179838864666847) |
| 在提示词中使用 `ultrathink` 关键字进行 [高强度推理](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking#tips-and-best-practices) | [![Claude](!/tags/claude.svg)](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking#tips-and-best-practices) |
| `/focus` 模式隐藏所有中间工作过程，仅显示最终结果 —— 信任模型运行正确的命令，直接查看成果即可 (使用 /focus 切换) | [![Boris](!/tags/boris-cherny.svg)](tips/claude-boris-6-tips-16-apr-26.md) |
| 通过 Opus 4.7 的自适应思考来调节投入程度 —— low 为速度快且 token 少，max 提供最大智能度 (滑块范围：low · medium · high · xhigh · max) | [![Boris](!/tags/boris-cherny.svg)](tips/claude-boris-6-tips-16-apr-26.md) |

<a id="tips-workflows-advanced"></a>■ **进阶工作流 (Workflows Advanced) (9)**

| 技巧 | 来源 |
|-----|--------|
| 大量使用 ASCII 图表来理解你的架构 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742759218794768) |
| 使用 [/loop](https://code.claude.com/docs/en/scheduled-tasks) 进行本地定期监控 (最多 7 天) · 使用 [/schedule](https://code.claude.com/docs/en/routines) 设置即使机器关闭也能运行的云端定时任务 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2038454341884154269) |
| 使用 [Ralph Wiggum 插件](https://github.com/shanraisshan/ralph-wiggum-self-evolving-loop) 执行长时间运行的自主任务 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179858435281082) |
| 在 [/permissions](https://code.claude.com/docs/en/permissions) 中使用通配符语法 (如 `Bash(npm run *)`, `Edit(/docs/**)`) 而不是 `dangerously-skip-permissions` | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2007179854077407667) |
| 使用 [/sandbox](https://code.claude.com/docs/en/sandboxing) 通过文件和网络隔离来减少权限提示 —— 内部统计减少了 84% | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2021700506465579443) [![Cat](!/tags/cat-wu.svg)](https://creatoreconomy.so/p/inside-claude-code-how-an-ai-native-actually-works-cat-wu) |
| 投入时间开发 [产品验证 (product verification)](https://code.claude.com/docs/en/skills) 技能 (如 signup-flow-driver, checkout-verifier) —— 值得花一周时间去完善 | [![Thariq](!/tags/thariq.svg)](https://x.com/trq212/status/2033949937936085378) |
| 使用 [自动模式 (auto mode)](https://code.claude.com/docs/en/permission-modes#eliminate-prompts-with-auto-mode) 替代 `dangerously-skip-permissions` —— 这是一个基于模型的分类器，决定每个命令是否安全并自动批准，遇到风险则暂停并询问。按 `Shift+Tab` 循环切换 Ask → Plan → Auto 模式 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](tips/claude-boris-6-tips-16-apr-26.md) |
| 使用 `/less-permission-prompts` 技能扫描会话历史中频繁提示的安全 bash/MCP 命令，然后获取建议的白名单以粘贴到 [设置](best-practice/claude-settings.md) 中 | [![Boris](!/tags/boris-cherny.svg)](tips/claude-boris-6-tips-16-apr-26.md) |
| 构建一个 `/go` 技能来：(1) 通过 bash/浏览器/电脑控制进行端到端测试 (2) 运行 `/simplify` (3) 提交 PR —— 这样当你回来时，你就知道代码是可以工作的 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](tips/claude-boris-6-tips-16-apr-26.md) |

<a id="tips-git-pr"></a>■ **Git / PR (5)**

| 技巧 | 来源 |
|-----|--------|
| 保持 PR 短小且专注 —— [中位数 (p50) 118 行](tips/claude-boris-2-tips-25-mar-26.md) (一天内处理 141 个 PR，涉及 45K 行代码)，每个 PR 只包含一个功能，更容易审查和还原 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2038552880018538749) |
| 始终使用 [squash merge](tips/claude-boris-2-tips-25-mar-26.md) 合并 PR —— 保持干净的线性历史，每个功能一个提交，易于执行 git revert 和 git bisect | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2038552880018538749) |
| 频繁提交 —— 尽量做到每小时至少提交一次，任务一完成就立即提交 | ![Shayan](!/tags/community-shayan.svg) |
| 在同事的 PR 上@ [@claude](https://github.com/apps/claude) 以自动生成针对重复出现的审查反馈的 lint 规则 —— 让你自己从代码审查中自动化解脱出来 🚫👶 | [![Boris](!/tags/boris-cherny.svg)](https://youtu.be/julbw1JuAz0?t=2715) [![Video](!/tags/video.svg)](https://youtu.be/julbw1JuAz0?t=2715) |
| 使用 [/code-review](https://code.claude.com/docs/en/code-review) 进行多智能体 PR 分析 —— 在合并之前捕获 bug、安全漏洞和退化 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2031089411820228645) |

<a id="tips-debugging"></a>■ **调试 (Debugging) (6)**

| 技巧 | 来源 |
|-----|--------|
| 养成习惯：每当你遇到任何问题卡住时，截图并与 Claude 分享 | ![Shayan](!/tags/community-shayan.svg) |
| 使用 mcp ([Claude in Chrome](https://code.claude.com/docs/en/chrome), [Playwright](https://github.com/microsoft/playwright-mcp), [Chrome DevTools](https://developer.chrome.com/blog/chrome-devtools-mcp)) 让 claude 自己能看到 chrome 控制台日志 | [![Claude](!/tags/claude.svg)](https://code.claude.com/docs/en/chrome) |
| 为了更好地调试，总是让 claude 将终端（你想要查看日志的那个终端）作为后台任务运行 | ![Shayan](!/tags/community-shayan.svg) |
| 使用 [/doctor](https://code.claude.com/docs/en/cli-reference) 来诊断安装、身份验证和配置问题 | ![Shayan](!/tags/community-shayan.svg) |
| 使用 [跨模型 (cross-model)](development-workflows/cross-model-workflow/cross-model-workflow.md) 进行 QA —— 例如使用 [Codex](https://github.com/shanraisshan/codex-cli-best-practice) 进行计划和实现审查 | ![Shayan](!/tags/community-shayan.svg) |
| 智能体式搜索 (glob + grep) 优于 RAG —— Claude Code 曾尝试过向量数据库并放弃了，因为代码容易失去同步且权限很复杂 | [![Boris](!/tags/boris-cherny.svg)](https://youtu.be/julbw1JuAz0?t=3095) [![Video](!/tags/video.svg)](https://youtu.be/julbw1JuAz0?t=3095) |

<a id="tips-utilities"></a>■ **实用工具 (Utilities) (5)**

| 技巧 | 来源 |
|-----|--------|
| 使用 [iTerm](https://iterm2.com/)/[Ghostty](https://ghostty.org/)/[tmux](https://github.com/tmux/tmux) 终端替代 IDE ([VS Code](https://code.visualstudio.com/)/[Cursor](https://www.cursor.com/)) | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2017742753971769626) |
| 使用 [/voice](https://code.claude.com/docs/en/voice-dictation) 或 [Wispr Flow](https://wisprflow.ai) 进行语音提示 (提高 10 倍生产力) | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2038454362226467112) |
| 使用 [claude-code-hooks](https://github.com/shanraisshan/claude-code-hooks) 获取 claude 反馈 | ![Shayan](!/tags/community-shayan.svg) |
| 使用 [状态栏](https://github.com/shanraisshan/claude-code-status-line) 获取上下文感知能力并实现快速压缩 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2021700784019452195) ![Shayan](!/tags/community-shayan.svg) |
| 探索 [settings.json](best-practice/claude-settings.md) 中的功能，如 [计划目录 (Plans Directory)](best-practice/claude-settings.md#plans-directory)、[加载动画动词 (Spinner Verbs)](best-practice/claude-settings.md#display--ux)，以获得个性化体验 | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny/status/2021701145023197516) |

<a id="tips-daily"></a>■ **日常 (Daily) (2)**

| 技巧 | 来源 |
|-----|--------|
| 每天 [更新](https://code.claude.com/docs/en/setup) Claude Code | ![Shayan](!/tags/community-shayan.svg) |
| 每天早上的第一件事就是阅读 [更新日志 (changelog)](https://github.com/anthropics/claude-code/blob/main/CHANGELOG.md) | ![Shayan](!/tags/community-shayan.svg) |

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## 🎬 视频 / 播客 (VIDEOS / PODCASTS)

| 视频 / 播客 | 来源 | YouTube |
|-----------------|--------|---------|
| From Vibe Coding to Agentic Engineering (Andrej) \| 02 May 2026 \| AI Engineer | [![Andrej](!/tags/community.svg)](https://x.com/karpathy) | [YouTube](https://www.youtube.com/watch?v=96jN2OCOfLs) |
| Full Walkthrough: Workflow for AI Coding (Matt) \| 24 Apr 2026 \| Matt Pocock | [![Matt](!/tags/community-matt.svg)](https://x.com/mattpocockuk) | [YouTube](https://youtu.be/-QFHIoCo-Ko) |
| Everything We Got Wrong About Research-Plan-Implement (Dex) \| 24 Mar 2026 \| MLOps Community | [![Dex](!/tags/community-dex.svg)](https://x.com/daborhyde) | [YouTube](https://youtu.be/YwZR6tc7qYg) |
| Building Claude Code with Boris Cherny (Boris) \| 04 Mar 2026 \| The Pragmatic Engineer | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny) | [YouTube](https://youtu.be/julbw1JuAz0) |
| Head of Claude Code: What happens after coding is solved (Boris) \| 19 Feb 2026 \| Lenny's Podcast | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny) | [YouTube](https://youtu.be/We7BZVKbCVw) |
| Inside Claude Code With Its Creator Boris Cherny (Boris) \| 17 Feb 2026 \| Y Combinator | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny) | [YouTube](https://youtu.be/PQU9o_5rHC4) |
| Boris Cherny (Creator of Claude Code) On What Grew His Career (Boris) \| 15 Dec 2025 \| Ryan Peterman | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny) | [YouTube](https://youtu.be/AmdLVWMdjOk) |
| The Secrets of Claude Code From the Engineers Who Built It (Cat) \| 29 Oct 2025 \| Every | [![Boris](!/tags/boris-cherny.svg)](https://x.com/bcherny) | [YouTube](https://youtu.be/IDSAMqip6ms) |

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## 🔔 订阅 (SUBSCRIBE)

| 平台 | 账号 / 板块 | 标签 |
|--------|------|-------|
| ![Reddit](https://img.shields.io/badge/-FF4500?style=flat&logo=reddit&logoColor=white) | [r/ClaudeAI](https://www.reddit.com/r/ClaudeAI/), [r/ClaudeCode](https://www.reddit.com/r/ClaudeCode/), [r/Anthropic](https://www.reddit.com/r/Anthropic/) | ![Boris + Team](!/tags/claude.svg) |
| ![X](https://img.shields.io/badge/-000?style=flat&logo=x&logoColor=white) | [Claude](https://x.com/claudeai), [Claude Devs](https://x.com/ClaudeDevs), [Anthropic](https://x.com/AnthropicAI), [Boris](https://x.com/bcherny), [Thariq](https://x.com/trq212), [Cat](https://x.com/_catwu), [Lydia](https://x.com/lydiahallie), [Noah](https://x.com/noahzweben), [Anthony](https://x.com/amorriscode), [Alex](https://x.com/alexalbert__), [Kenneth](https://x.com/neilhtennek) | ![Boris + Team](!/tags/claude.svg) |
| ![X](https://img.shields.io/badge/-000?style=flat&logo=x&logoColor=white) | [Jesse Kriss](https://x.com/obra) ([Superpowers](https://github.com/obra/superpowers)), [Affaan Mustafa](https://x.com/affaanmustafa) ([ECC](https://github.com/affaan-m/everything-claude-code)), [Garry Tan](https://x.com/garrytan) ([gstack](https://github.com/garrytan/gstack)), [Dex Horthy](https://x.com/dexhorthy) ([HumanLayer](https://github.com/humanlayer/humanlayer)), [Kieran Klaassen](https://x.com/kieranklaassen) ([Compound Eng](https://github.com/EveryInc/compound-engineering-plugin)), [Tabish Gilani](https://x.com/0xTab) ([OpenSpec](https://github.com/Fission-AI/OpenSpec)), [Brian McAdams](https://x.com/BMadCode) ([BMAD](https://github.com/bmad-code-org/BMAD-METHOD)), [Lex Christopherson](https://x.com/official_taches) ([GSD](https://github.com/gsd-build/get-shit-done)), [Matt Pocock](https://x.com/mattpocockuk) ([Skills](https://github.com/mattpocock/skills)), [Dani Avila](https://x.com/dani_avila7) ([CC Templates](https://github.com/davila7/claude-code-templates)), [Dan Shipper](https://x.com/danshipper) ([Every](https://every.to/)), [Andrej Karpathy](https://x.com/karpathy) ([AutoResearch](https://x.com/karpathy/status/2015883857489522876)), [Peter Steinberger](https://x.com/steipete) ([OpenClaw](https://x.com/openclaw)), [Sigrid Jin](https://x.com/realsigridjin) ([claw-code](https://github.com/ultraworkers/claw-code)), [Yeachan Heo](https://x.com/bellman_ych) ([oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode)) | ![Community](!/tags/community.svg) |
| ![YouTube](https://img.shields.io/badge/-F00?style=flat&logo=youtube&logoColor=white) | [Anthropic](https://www.youtube.com/@anthropic-ai) | ![Boris + Team](!/tags/claude.svg) |
| ![YouTube](https://img.shields.io/badge/-F00?style=flat&logo=youtube&logoColor=white) | [Lenny's Podcast](https://www.youtube.com/@LennysPodcast), [Y Combinator](https://www.youtube.com/@ycombinator), [The Pragmatic Engineer](https://www.youtube.com/@pragmaticengineer), [Ryan Peterman](https://www.youtube.com/@ryanlpeterman), [Every](https://www.youtube.com/@every_media), [MLOps Community](https://www.youtube.com/@MLOps) | ![Community](!/tags/community.svg) |

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## ☠️ 初创公司 / 商业产品 (STARTUPS / BUSINESSES)

| Claude 特性 | 替代的商业产品 |
|-|-|
|[**代码审查 (Code Review)**](https://code.claude.com/docs/en/code-review)|[Greptile](https://greptile.com), [CodeRabbit](https://coderabbit.ai), [Devin Review](https://devin.ai), [OpenDiff](https://opendiff.com), [Cursor BugBot](https://bugbot.dev)|
|[**语音听写 (Voice Dictation)**](https://code.claude.com/docs/en/voice-dictation)|[Wispr Flow](https://wisprflow.ai), [SuperWhisper](https://superwhisper.com/)|
|[**远程控制 (Remote Control)**](https://code.claude.com/docs/en/remote-control)|[OpenClaw](https://openclaw.ai/)
|[**Claude in Chrome**](https://code.claude.com/docs/en/chrome)|[Playwright MCP](https://github.com/microsoft/playwright-mcp), [Chrome DevTools MCP](https://developer.chrome.com/blog/chrome-devtools-mcp)|
|[**电脑控制 (Computer Use)**](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use)|[OpenAI CUA](https://openai.com/index/computer-using-agent/)|
|[**Cowork**](https://claude.com/blog/cowork-research-preview)|[ChatGPT Agent](https://openai.com/chatgpt/agent/), [Perplexity Computer](https://www.perplexity.ai/computer/), [Manus](https://manus.im)|
|[**任务 (Tasks)**](https://x.com/trq212/status/2014480496013803643)|[Beads](https://github.com/steveyegge/beads)
|[**计划模式 (Plan Mode)**](https://code.claude.com/docs/en/common-workflows)|[Agent OS](https://github.com/buildermethods/agent-os)|
|[**设计 (Design)**](https://claude.com/design)|[Figma](https://figma.com), [Framer](https://framer.com), [Sketch](https://sketch.com), [v0](https://v0.dev)|
|[**智能体 SDK (Agent SDK)**](https://code.claude.com/docs/en/agent-sdk/overview)|[LangChain](https://langchain.com), [LangGraph](https://www.langchain.com/langgraph), [CrewAI](https://www.crewai.com), [AutoGen](https://github.com/microsoft/autogen), [OpenAI Assistants API](https://platform.openai.com/docs/assistants/overview)|
|[**技能 / 插件 (Skills / Plugins)**](https://code.claude.com/docs/en/plugins)|基于 AI 包装的 YC 初创公司 ([reddit 讨论](https://reddit.com/r/ClaudeAI/comments/1r6bh4d/claude_code_skills_are_basically_yc_ai_startup/))|

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

<a id="billion-dollar-questions"></a>
![Billion-Dollar Questions](!/tags/billion-dollar-questions.svg)

*如果你有答案，请通过 shanraisshan@gmail.com 告诉我*

**记忆与指令 (4)**

1. 你究竟应该在 CLAUDE.md 中放些什么 —— 又该省去什么？
2. 如果你已经有了一个 CLAUDE.md，那么还需要单独的 constitution.md 或 rules.md 吗？
3. 你应该多久更新一次 CLAUDE.md，又怎么知道它什么时候已经过时了？
4. 为什么即使 CLAUDE.md 中的指令全大写标明 MUST (必须)，Claude 仍然会忽略它们？ ([reddit](https://reddit.com/r/ClaudeCode/comments/1qn9pb9/claudemd_says_must_use_agent_claude_ignores_it_80/))

**智能体、技能与工作流 (6)**

1. 什么时候该用命令、智能体，或者技能 —— 又在什么时候原始的 Claude Code 就是最好的选择？
2. 随着模型的进步，你应该多久更新一次你的智能体、命令和工作流？
3. 你应该使用通用型的子智能体还是特定功能/特定角色的智能体？赋予子智能体详细的"人设"是否能提高质量？对于研究/视觉类任务，"完美的人设提示词"是什么样的？
4. 你应该依赖 Claude Code 内置的计划模式，还是构建自己的计划命令/智能体来强制执行团队的特定工作流？
5. 如果你有一个私人技能 (例如具有你的编码风格的 `/implement`)，你如何整合社区技能 (如 `/simplify`) 而不产生冲突 —— 且当它们产生分歧时，谁说了算？
6. 我们达到那个阶段了吗：我们能否将现有的代码库转换为规范，删除代码，然后让 AI 仅凭这些规范就重新生成完全相同的代码？

**规范与文档 (3)**

1. 你仓库中的每个功能都应该有一个作为 Markdown 文件的规范吗？
2. 你需要多久更新一次规范，以避免在实现新功能时它们过时？
3. 在实现新功能时，你如何处理对其他功能规范产生的连锁反应？

### 🤔 [代码还重要吗？](https://github.com/shanraisshan/agentic-engineering)

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## 📊 研究报告 (REPORTS)

<p align="center">
  <a href="reports/claude-agent-sdk-vs-cli-system-prompts.md"><img src="https://img.shields.io/badge/Agent_SDK_vs_CLI-555?style=for-the-badge" alt="Agent SDK vs CLI"></a>
  <a href="reports/claude-in-chrome-v-chrome-devtools-mcp.md"><img src="https://img.shields.io/badge/Browser_Automation_MCP-555?style=for-the-badge" alt="Browser Automation MCP"></a>
  <a href="reports/claude-global-vs-project-settings.md"><img src="https://img.shields.io/badge/Global_vs_Project_Settings-555?style=for-the-badge" alt="Global vs Project Settings"></a>
  <a href="reports/claude-skills-for-larger-mono-repos.md"><img src="https://img.shields.io/badge/Skills_in_Monorepos-555?style=for-the-badge" alt="Skills in Monorepos"></a>
  <br>
  <a href="reports/claude-agent-memory.md"><img src="https://img.shields.io/badge/Agent_Memory-555?style=for-the-badge" alt="Agent Memory"></a>
  <a href="reports/claude-advanced-tool-use.md"><img src="https://img.shields.io/badge/Advanced_Tool_Use-555?style=for-the-badge" alt="Advanced Tool Use"></a>
  <a href="reports/claude-usage-and-rate-limits.md"><img src="https://img.shields.io/badge/Usage_&_Rate_Limits-555?style=for-the-badge" alt="Usage & Rate Limits"></a>
  <a href="reports/claude-agent-command-skill.md"><img src="https://img.shields.io/badge/Agents_vs_Commands_vs_Skills-555?style=for-the-badge" alt="Agents vs Commands vs Skills"></a>
  <br>
  <a href="reports/llm-day-to-day-degradation.md"><img src="https://img.shields.io/badge/LLM_Degradation-555?style=for-the-badge" alt="LLM Degradation"></a>
  <a href="reports/why-harness-is-important.md"><img src="https://img.shields.io/badge/Why_Harness_is_Important-555?style=for-the-badge" alt="Why Harness is Important"></a>
  <a href="reports/claude-spinner-verbs-and-tips.md"><img src="https://img.shields.io/badge/Spinner_Verbs_&_Tips-555?style=for-the-badge" alt="Spinner Verbs & Tips"></a>
</p>

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

<a id="how-to-use"></a>

## 🚀 <img src="!/tags/how-to-use-hd.svg" alt="How to Use">

按照以下步骤充分利用本仓库：

1. **将本仓库当作一门课程来读，而不是单纯的工作流或技能库。** 它首先是参考资料；你在后面再运行它们。
2. **不要把 Claude 当作聊天机器人使用。** 学习基础原语 —— 智能体 (agents)、命令 (commands)、技能 (skills)、钩子 (hooks) —— 并将它们组装成你自己的工作流。
3. **运行 [`/weather-orchestrator`](orchestration-workflow/orchestration-workflow.md)** 来查看完整的 命令 → 智能体 → 技能 流程。将其作为从计划到发布的任何开发工作流的模板。
4. **工作时注意听自定义钩子的声音。** 它们的实现位于专用的 [Claude Code Hooks 仓库](https://github.com/shanraisshan/claude-code-hooks) 中；其他模式（如 [智能体团队](implementation/claude-agent-teams-implementation.md)）的实现包含在本仓库的 `implementation/` 目录下。
5. **从 [🔥 热门特性](#-hot) 子表中学习高级主题及其实现** —— 例如，[Ralph Wiggum 自我进化循环](https://github.com/shanraisshan/ralph-wiggum-self-evolving-loop) 是一个完整的工作仓库，你可以克隆它来查看这一模式端到端的运作。
6. **在你自己的项目中，向 Claude 提供 [提示与技巧](#-tips-and-tricks-83) 部分**，并让它提出修改建议 —— 尤其是如何重构你的 `CLAUDE.md`。每一个技巧都来源于 Claude 团队或社区。
7. **在 [订阅部分](#-subscribe) 订阅 Reddit 和 YouTube 频道**，以跟进社区最新动态。

**🎬 视频**

<a href="https://www.youtube.com/watch?v=AkAhkalkRY4"><img src="!/thumbnail/video-1.png" alt="Watch on YouTube" width="300"></a>

**📊 演讲**

<a href="https://github.com/shanraisshan/claude-code-best-practice/tree/main/presentation/2026-04-25-gdg-kolachi-cli-claude-code-gemini"><img src="!/thumbnail/presentation-1.png" alt="Claude Code & Gemini CLI — GDG Kolachi" width="300"></a>

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

<p align="center">
  <a href="https://github.com/trending?since=monthly"><img src="!/root/github-trending.png" alt="GitHub Trending" width="1200"></a><br>
  ✨2026 年 3 月 Github 趋势榜✨
</p>

## ⭐ Star 历史

[![Star History Chart](https://api.star-history.com/svg?repos=shanraisshan/claude-code-best-practice&type=Date&v=2)](https://star-history.com/#shanraisshan/claude-code-best-practice&Date)

<a href="https://github.com/shanraisshan/claude-code-best-practice/stargazers"><img src="https://img.shields.io/github/stars/shanraisshan/claude-code-best-practice?style=flat&label=%E2%98%85&labelColor=555&color=white" alt="GitHub Stars" align="center"></a> stars and counting

## 📦 其他仓库

<table>
<tr>
<td align="center" width="140">
  <a href="https://github.com/shanraisshan/claude-code-hooks"><img src="!/claude-speaking.svg" alt="Claude Code Hooks" width="64" height="64"></a><br>
  <a href="https://github.com/shanraisshan/claude-code-hooks"><strong>Claude Code<br>Hooks</strong></a>
</td>
<td align="center" width="140">
  <a href="https://github.com/shanraisshan/codex-cli-best-practice"><img src="!/codex-jumping.svg" alt="Codex CLI Best Practice" width="64" height="64"></a><br>
  <a href="https://github.com/shanraisshan/codex-cli-best-practice"><strong>Codex CLI<br>最佳实践</strong></a>
</td>
<td align="center" width="140">
  <a href="https://github.com/shanraisshan/codex-cli-hooks"><img src="!/codex-speaking.svg" alt="Codex CLI Hooks" width="64" height="64"></a><br>
  <a href="https://github.com/shanraisshan/codex-cli-hooks"><strong>Codex CLI<br>Hooks</strong></a>
</td>
<td align="center" width="140">
  <a href="https://github.com/shanraisshan/gemini-cli-best-practice"><img src="!/gemini-jumping.svg" alt="Gemini CLI Best Practice" width="64" height="64"></a><br>
  <a href="https://github.com/shanraisshan/gemini-cli-best-practice"><strong>Gemini CLI<br>最佳实践</strong></a>
</td>
<td align="center" width="140">
  <a href="https://github.com/shanraisshan/gemini-cli-hooks"><img src="!/gemini-speaking.svg" alt="Gemini CLI Hooks" width="64" height="64"></a><br>
  <a href="https://github.com/shanraisshan/gemini-cli-hooks"><strong>Gemini CLI<br>Hooks</strong></a>
</td>
</tr>
</table>

## 🛠️ 开发者

![Developed by](!/tags/developed-by.svg)

> | # | 工作流 | 描述 |
> |---|----------|-------------|
> | 1 | /workflows:development-workflows | 通过并行研究所有 10 个工作流仓库，更新开发工作流表格和跨工作流分析报告 |
> | 2 | /workflows:skill-collections | 通过并行研究所有 5 个技能集合仓库，更新技能集合表格 |
> | 3 | /workflows:best-practice:workflow-concepts | 使用最新的 Claude Code 特性和概念更新 README 的 CONCEPTS 部分 |
> | 4 | /workflows:best-practice:workflow-claude-settings | 跟踪 Claude Code 设置报告的更改，并找出需要更新的内容 |
> | 5 | /workflows:best-practice:workflow-claude-subagents | 跟踪 Claude Code 子智能体报告的更改，并找出需要更新的内容 |
> | 6 | /workflows:best-practice:workflow-claude-commands | 跟踪 Claude Code 命令报告的更改，并找出需要更新的内容 |
> | 7 | /workflows:best-practice:workflow-claude-skills | 跟踪 Claude Code 技能报告的更改，并找出需要更新的内容 |

## 🎁 附加内容

[![Claude for OSS](!/tags/claude-for-oss.svg)](https://claude.com/contact-sales/claude-for-oss)
[![Claude Community Ambassador](!/tags/claude-community-ambassador.svg)](https://claude.com/community/ambassadors)
[![Claude Certified Architect](!/tags/claude-certified-architect.svg)](https://anthropic.skilljar.com/claude-certified-architect-foundations-access-request)
[![Anthropic Academy](!/tags/anthropic-academy.svg)](https://anthropic.skilljar.com/)
[![Join Claude Pakistan community on WhatsApp](!/tags/whatsapp-claude-pakistan.svg)](https://chat.whatsapp.com/BDUV2stIS0c7X5uY7RY6nS)

<p align="center">
  <img src="!/claude-jumping.svg" alt="section divider" width="60" height="50">
</p>

## 💖 <img src="!/tags/sponsor-heart.svg" width="22" height="22" align="center"> 赞助我的工作

如果你喜欢我的工作，请请我喝杯奶茶 (doodh patti) 🍵 

<a href="https://buy.polar.sh/polar_cl_R6wjUESl8RiJD0iVaTyStBUV6WNuYvDmLJ0si1XXj4C"><img src="!/tags/polar.svg" alt="Polar" width="40" height="40" align="center"></a> <a href="https://buy.polar.sh/polar_cl_R6wjUESl8RiJD0iVaTyStBUV6WNuYvDmLJ0si1XXj4C"><strong>Polar</strong></a>
