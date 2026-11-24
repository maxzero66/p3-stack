# Upstream tracking

upstream: https://github.com/cursor/plugins
subtree: pstack/
pin: 9e278fe4d4ecd8bfe98b1b79bf4be662efb338cc
pin-date: 2026-11-23
pin-version: 0.15.48
synced-on: 2026-11-24
sync-target: 9e278fe4d4ecd8bfe98b1b79bf4be662efb338cc
sync-spec: docs/sync-spec-9e278fe.md

`pin` 取「上游 main 上最后一个动过 subtree 的 commit」，不取仓库 HEAD。同步进行中 `pin` 取各行「对齐到」的最小值，全部对齐后才前进到 `sync-target`。本轮已于 2026-11-24 对齐到 `9e278fe`（0.15.48）：批 1 为 statechart 修复与 `/reframe`，批 2 为 principle、unslop、technical-writing 瘦身，批 3 为 reflect 单文件化、多阶段计划砍成 5 步并删 `check-plan.mjs`、architect 砍成两段。默认模型与角色预算按既定策略跳过。
`scripts/upstream-diff.sh` 与 `scripts/parity-check.sh` 只读本文件：头部 `key: value` 加下面四张表（前三张是 spec §5.1 的固定表，第四张是 parity-check 的可选扩展）。状态取值：`ported`（已落地）、`pending`（已决定移植、未落地）、`gap`（有意缺口）、`p3-only`（p3 独有）。

## 映射

| 上游 | p3 | 对齐到 | 状态 | 备注 |
|---|---|---|---|---|
| skills/architect | skills/architect | 9e278fe | ported | 架构探索交给 arena，删 3 个 references |
| skills/arena | skills/arena | 9e278fe | ported | 只改默认模型，按策略跳过 |
| skills/automate-me | skills/automate-me | 9e278fe | ported | 只删 speed 措辞，p3 本无 |
| skills/benchmark-checklist | skills/benchmark-checklist | 9e278fe | ported | 只删 Opening a PR 引用；p3 保留该 playbook |
| skills/blast-radius | skills/blast-radius | 9e278fe | ported |  |
| skills/bro | skills/bro | 9e278fe | ported |  |
| skills/correct | skills/correct | 9e278fe | ported |  |
| skills/create-formal-verification-skill | skills/create-formal-verification-skill | 9e278fe | ported | 新技能 |
| skills/create-verification-skill | skills/create-verification-skill | 9e278fe | ported |  |
| skills/figure-it-out | skills/figure-it-out | 9e278fe | ported | 只删 speed 措辞，p3 本无 |
| skills/how | skills/how | 9e278fe | ported |  |
| skills/in-your-own-words | skills/in-your-own-words | 9e278fe | ported | 新技能 |
| skills/interrogate | skills/interrogate | 9e278fe | ported |  |
| skills/ketchup | skills/ketchup | 9e278fe | ported | 新技能 |
| skills/ketchup-video | skills/ketchup-video | 9e278fe | ported | 新技能 |
| skills/maintain-formal-verification-skill | skills/maintain-formal-verification-skill | 9e278fe | ported | 新技能 |
| skills/maintain-verification-skill | skills/maintain-verification-skill | 9e278fe | ported |  |
| skills/make-bot-ui | skills/make-bot-ui | 9e278fe | ported |  |
| skills/no-comments | skills/no-comments | 9e278fe | ported | 只删 speed 措辞，p3 本无 |
| skills/poteto-help | skills/p3-help | 9e278fe | ported | 改名；保留 Orchestrate close call，因为 p3 保留该 playbook |
| skills/poteto-mode | skills/p3-mode | 9e278fe | ported | 改名；T3 改写，orchestrate 与 worker.md 的处理见有意缺口 |
| skills/principle-attack-the-premise | skills/principle-attack-the-premise | 9e278fe | ported |  |
| skills/principle-boundary-discipline | skills/principle-boundary-discipline | 9e278fe | ported |  |
| skills/principle-build-the-lever | skills/principle-build-the-lever | 9e278fe | ported |  |
| skills/principle-encode-lessons-in-structure | skills/principle-encode-lessons-in-structure | 9e278fe | ported |  |
| skills/principle-exhaust-the-design-space | skills/principle-exhaust-the-design-space | 9e278fe | ported |  |
| skills/principle-experience-first | skills/principle-experience-first | 9e278fe | ported |  |
| skills/principle-explain-the-number | skills/principle-explain-the-number | 9e278fe | ported |  |
| skills/principle-fix-root-causes | skills/principle-fix-root-causes | 9e278fe | ported |  |
| skills/principle-foundational-thinking | skills/principle-foundational-thinking | 9e278fe | ported |  |
| skills/principle-guard-the-context-window | skills/principle-guard-the-context-window | 9e278fe | ported | description 保留 delegated tasks 用词 |
| skills/principle-laziness-protocol | skills/principle-laziness-protocol | 9e278fe | ported |  |
| skills/principle-make-operations-idempotent | skills/principle-make-operations-idempotent | 9e278fe | ported |  |
| skills/principle-migrate-callers-then-delete-legacy-apis | skills/principle-migrate-callers-then-delete-legacy-apis | 9e278fe | ported |  |
| skills/principle-minimize-reader-load | skills/principle-minimize-reader-load | 9e278fe | ported |  |
| skills/principle-model-the-domain | skills/principle-model-the-domain | 9e278fe | ported |  |
| skills/principle-never-block-on-the-human | skills/principle-never-block-on-the-human | 9e278fe | ported |  |
| skills/principle-outcome-oriented-execution | skills/principle-outcome-oriented-execution | 9e278fe | ported |  |
| skills/principle-prove-it-works | skills/principle-prove-it-works | 9e278fe | ported |  |
| skills/principle-redesign-from-first-principles | skills/principle-redesign-from-first-principles | 9e278fe | ported |  |
| skills/principle-separate-before-serializing-shared-state | skills/principle-separate-before-serializing-shared-state | 9e278fe | ported |  |
| skills/principle-sequence-verifiable-units | skills/principle-sequence-verifiable-units | 9e278fe | ported |  |
| skills/principle-subtract-before-you-add | skills/principle-subtract-before-you-add | 9e278fe | ported |  |
| skills/principle-test-behavior-not-implementation | skills/principle-test-behavior-not-implementation | 9e278fe | ported |  |
| skills/principle-type-system-discipline | skills/principle-type-system-discipline | 9e278fe | ported |  |
| skills/recall | skills/recall | 9e278fe | ported | 只删 speed 措辞，p3 本无 |
| skills/reframe | skills/reframe | 9e278fe | ported | 新技能 |
| skills/reflect | skills/reflect | 9e278fe | ported | 单文件、无子 agent；改读 t3_thread_read |
| skills/setup-pstack | skills/setup-p3 | 9e278fe | ported | 改名；角色退役跟进，默认模型与预算档位按策略跳过 |
| skills/sharpen | skills/sharpen | 9e278fe | ported | 新技能 |
| skills/show-me-your-work | skills/show-me-your-work | 9e278fe | ported | 改成 another vendor，p3 的 family 语义已等价 |
| skills/statechart | skills/statechart | 9e278fe | ported | 新技能 |
| skills/swarm | skills/swarm | 9e278fe | ported | 只删 speed 措辞，p3 本无 |
| skills/tdd | skills/tdd | 9e278fe | ported |  |
| skills/teach | skills/teach | 9e278fe | ported |  |
| skills/technical-writing | skills/technical-writing | 9e278fe | ported |  |
| skills/typescript-best-practices | skills/typescript-best-practices | 9e278fe | ported | 保留 p3 去掉的 paths: frontmatter 字段 |
| skills/unslop | skills/unslop | 9e278fe | ported |  |
| skills/why | skills/why | 9e278fe | ported |  |
| agents/poteto-agent.md | agents/p3-agent.md | 9e278fe | ported | 改名；只加 model 行，按默认模型策略跳过 |
| agents/comment-sicko.md | agents/comment-sicko.md | 9e278fe | ported | |
| README.md | README.md | 9e278fe | ported | p3 README 已重写，只摘技能表语义 |

## 有意缺口与忽略路径

| 上游路径（支持 glob） | 处理 | 理由 |
|---|---|---|
| .cursor-plugin/** | ignore | Cursor 清单，p3 靠 install.sh 软链 |
| plugin.json | ignore | Agent Plugins 根清单，p3 无插件清单 |
| docs/harness/** | ignore | Claude Code 适配说明，p3 面向 T3 Code |
| docs/guide/** | ignore | D5=A：本轮不带指南 |
| automations/** | ignore | 作者个人自动化，p3 从未带 |
| skills/poteto-mode/scripts/watch-pr/** | ignore | 由 watch_pull_request 取代 |
| skills/poteto-mode/scripts/orch/** | ignore | 上游已删除，p3 从未带 |
| skills/poteto-mode/scripts/worktree-audit.sh | ignore | 由 git worktree list --porcelain 与 gh 取代 |
| skills/poteto-mode/playbooks/orchestrate.md | note | 上游 9e278fe 删除；p3 保留为 p3 专属，因为台账与心跳把 T3 的 delegate/watch/schedule 组合成跨天程序 |
| skills/poteto-mode/playbooks/**（仅 Origin forge 分支） | note | 上游 playbook 里的 Origin forge 分支已删，p3 只保留 gh；这是正文缺口，不是文件缺口，不进忽略表 |
| pstack/**（默认模型内容） | note | 2026-11-16 max 定：不跟随上游默认模型换代（fable / opus / gemini），p3 角色模型由 setup-p3 按 orchestrator_capabilities 生成；其家族/vendor 语义、预算按步移动、defaults 标记一并跳过。见 docs/sync-spec-bf0c7cd.md §2.2 |

`install.sh` 是 p3 独有的安装方式：用户级多目标，把 `skills/*` 软链进 `~/.agents/skills` 与各 Claude 配置家目录的 `skills/`，同名外来条目跳过、不覆盖（`--replace <name>` 显式接管）。上游靠 `/add-plugin` 与 `.cursor-plugin/` 清单安装，没有对应脚本，所以不进映射表。

## 白名单

| 判据 | 路径 | 理由 |
|---|---|---|
| P4 schedule | skills/p3-mode/playbooks/visual-parity.md | p3 改成事件唤醒，不再用定时 |
| P2 | skills/p3-mode/playbooks/orchestrate.md | 上游 9e278fe 已删除，p3 保留为 p3 专属 |
| P2 | skills/p3-mode/worker.md | 上游 9e278fe 新增；规则并入 agents/p3-agent.md，p3 不单独建文件 |
| P4 preview | skills/p3-help/SKILL.md | p3-help 没有 control-ui/cli 对应句；B3 改写时复核 |
| P5 | agents/p3-agent.md | T3 改写最深，B3 重写首段 |
| P5 | skills/make-bot-ui/SKILL.md | T3 改写最深（preview_*/device_* 取代 control-ui） |
| P5 | skills/p3-mode/playbooks/babysit.md | T3 改写最深（watch_pull_request 事件唤醒） |
| P5 | skills/p3-mode/playbooks/worktree-cleanup.md | T3 改写最深（git worktree/gh/t3_thread_search 取代审计脚本） |
| P5 | skills/setup-p3/SKILL.md | T3 改写最深（角色表与 providerInstanceId 写法） |
| P5 | skills/p3-mode/playbooks/opening-a-pr.md | T3 改写最深（link_pull_request 只登记、delegated children 不 watch） |
| P6 | skills/setup-p3/SKILL.md | T3 侧有意加 disable-model-invocation |
| P8 | agents/p3-agent.md | 基线已超出 |
| P8 | skills/figure-it-out/SKILL.md | 基线已超出 |
| P8 | skills/p3-mode/playbooks/pause-safely.md | 基线已超出 |
| P8 | skills/show-me-your-work/SKILL.md | 基线已超出 |
| P8 | skills/ketchup-video/SKILL.md | D3=B：HTML 页 + preview_recording 录制步骤需写明 |
| P8 | skills/p3-mode/playbooks/worktree-cleanup.md | +2 行：git worktree/gh/t3_thread_search 取代审计脚本 |
| P8 | skills/statechart/SKILL.md | +1 行：`<skill dir>` 自解析；同一行补上原生 Windows 运行方式 |
| P8 | skills/statechart/references/render.md | +1 行：T3 下用图片语法或 html_render 展示 SVG |
| P8 | skills/p3-mode/SKILL.md | T3 改写最深（Subagents 的角色与 option 解析规则） |
| P8 | skills/p3-mode/playbooks/babysit.md | T3 改写最深（watch_pull_request 事件唤醒） |
| P8 | skills/p3-mode/playbooks/opening-a-pr.md | T3 改写最深（link_pull_request 与 worker 不 watch） |

## 逐字搬运

| 路径（p3 侧，支持 glob） | 理由 |
|---|---|
| skills/principle-attack-the-premise/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-encode-lessons-in-structure/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-exhaust-the-design-space/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-explain-the-number/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-fix-root-causes/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-laziness-protocol/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-make-operations-idempotent/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-migrate-callers-then-delete-legacy-apis/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-minimize-reader-load/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-model-the-domain/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-never-block-on-the-human/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-redesign-from-first-principles/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-subtract-before-you-add/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-test-behavior-not-implementation/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-type-system-discipline/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/correct/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/technical-writing/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/unslop/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/typescript-best-practices/references/patterns.md | B1 三方合并后与上游逐字相同 |
| skills/principle-build-the-lever/SKILL.md | B1 三方合并后与上游逐字相同 |
| skills/principle-boundary-discipline/SKILL.md | 与上游 9e278fe 逐字相同 |
| skills/principle-foundational-thinking/SKILL.md | 与上游 9e278fe 逐字相同 |
| skills/principle-prove-it-works/SKILL.md | 与上游 9e278fe 逐字相同 |
| skills/principle-separate-before-serializing-shared-state/SKILL.md | 与上游 9e278fe 逐字相同 |
| skills/principle-sequence-verifiable-units/SKILL.md | 与上游 9e278fe 逐字相同 |
| skills/in-your-own-words/SKILL.md | 新技能，与上游逐字相同 |
| skills/reframe/SKILL.md | 新技能，与上游 9e278fe 逐字相同 |
| skills/sharpen/SKILL.md | 新技能，与上游逐字相同 |
| skills/statechart/scripts/** | D6=A：整目录原样搬 |
