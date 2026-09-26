<h1 align="center">Hi, I'm J. F. Zhang 👋</h1>

<p align="center">
  Geek · incurable tinkerer · dad of a lovely little girl
  <br>
  I take things apart until they tell me how they work — laptops, phone kernels, AI agents.
  <br>
  Lately: teaching software that already knows its craft to talk to AI, in ways people can trust.
  <br><br>
  极客，爱搞机，家有可爱小女一枚
  <br>
  喜欢把东西拆开，直到它说出自己是怎么运转的：笔记本、手机内核、AI Agent。
  <br>
  最近在做的事：让懂行的老软件学会和 AI 对话，并且让人放心。
</p>

<p align="center">
  <a href="https://blog.ferstar.org"><img src="https://img.shields.io/badge/Blog-blog.ferstar.org-24292f?style=flat-square&logo=hugo&logoColor=white" alt="Blog"></a>
  <a href="https://x.com/ferstar_org"><img src="https://img.shields.io/badge/X-@ferstar__org-24292f?style=flat-square&logo=x&logoColor=white" alt="X"></a>
  <a href="https://blog.ferstar.org/index.xml"><img src="https://img.shields.io/badge/RSS-subscribe-24292f?style=flat-square&logo=rss&logoColor=white" alt="RSS"></a>
</p>

## What I work on

- **Making existing software agent-ready** — exposing what a product already does well as task-level MCP tools that any agent can call, rather than building yet another agent. The domain assets stay the moat; the agent is interchangeable.
- **The trust layer** — identity carried through to the person behind the agent, permissions that never exceed theirs, audit trails, answers traceable to the source page, and human sign-off where it matters.
- **Agent execution security** — what an agent can read, run and send out, and how to enforce that at the OS boundary instead of trusting the vendor's promise.
- **Agent runtimes** — streaming lifecycles, tool-call recovery, loop guards, context compaction and MCP isolation, mostly in Rust.
- **Financial document systems** — a production platform for regulatory filings and annual reports that I owned for a long stretch: parsing, rule checks, and a Python stack modernized end to end. On top of it, I led the build of the AI-powered annual report platform an exchange launched for its listed issuers.
- **Linux & low-level fixes** — touchpad gestures, laptop ACPI quirks, phone kernels: when the hardware misbehaves, I go down to the driver.
- **Pragmatic Python tooling** — small tools that remove a daily annoyance and then get out of the way.

## Featured

**[RunSeal](https://github.com/runseal-labs/runseal)** · Rust  
An OS-native sandbox layer and stable execution protocol for AI agents. Policy-governed filesystem and network boundaries, structured audit events, and fail-closed behavior whenever a request can't be fully enforced. Windows is the reference backend; macOS and Linux are experimental.
→ [Why I built it · 做 RunSeal 的初衷](https://blog.ferstar.org/posts/local-first-agent-execution-boundary-runseal/)

**ZCode silent upload disclosure** · Sep 2026  
Found that an AI coding tool with 1M+ users was packing workspaces — including full `.git` history — encrypting them and uploading them to cloud storage, on by default with no way to turn it off. The disclosure led to the feature being removed, the client being open-sourced, and third-party security audits.
→ [扒一扒 ZCode 静默上传全量 Git 历史的骚操作](https://blog.ferstar.org/posts/zcode-silent-workspace-snapshot-upload/)

## Notes on agent engineering

- [为什么说“套壳 Agent 就能做 SaaS”是个荒谬的幻想](https://blog.ferstar.org/posts/the-illusion-of-agent-saas/) — why wrapping an agent isn't a product
- [Agent 死循环的分级治理阶梯（Warn → Block → Halt）](https://blog.ferstar.org/posts/agent-graded-loop-guard-warn-block-halt/) — graded loop guards instead of a hard kill
- [跨 Chunk 流式状态机的 DSML 抢救实录](https://blog.ferstar.org/posts/agent-dsml-tool-call-streaming-recovery/) — recovering tool calls the model emitted as text
- [Agent 长会话的两阶段预热与可回捞设计](https://blog.ferstar.org/posts/agent-context-compaction-two-pass-prefire/) — moving context compaction off the hot path
- [MCP 服务的启动隔离与平滑降级](https://blog.ferstar.org/posts/mcp-server-startup-isolation-and-graceful-degradation/) — optional plugins must never block the core session
- [消除桌面 Agent 输入框假死与流式卡顿](https://blog.ferstar.org/posts/desktop-agent-streaming-lifecycle-reconciliation/) — decoupling heavy IO from UI end states

## Latest from the blog

<!-- BLOG-POST-LIST:START -->
- [做 RunSeal 的初衷：别再让本地 Agent 裸奔跑命令了](https://blog.ferstar.org/posts/local-first-agent-execution-boundary-runseal/)
- [扒一扒 ZCode 静默上传全量 Git 历史的骚操作](https://blog.ferstar.org/posts/zcode-silent-workspace-snapshot-upload/)
- [从一堆 Agent 演示日志说起：为什么说‘套壳 Agent 就能做 SaaS’是个荒谬的幻想](https://blog.ferstar.org/posts/the-illusion-of-agent-saas/)
- [可选插件不能拖死核心会话：MCP 服务的启动隔离与平滑降级](https://blog.ferstar.org/posts/mcp-server-startup-isolation-and-graceful-degradation/)
- [解耦重型 IO 与 UI 终态：消除桌面 Agent 输入框假死与流式卡顿](https://blog.ferstar.org/posts/desktop-agent-streaming-lifecycle-reconciliation/)
<!-- BLOG-POST-LIST:END -->

## Linux & systems

| Project | What it is |
| --- | --- |
| [gestures](https://github.com/ferstar/gestures) · Rust · ⭐111 | The maintained fork of a libinput touchpad gesture tool, rebuilt around fast three-finger dragging on both X11 and Wayland. Now has several times the stars of upstream. [Write-up](https://blog.ferstar.org/en/posts/linux-touchpad-gestures-drag/) |
| [ideapad-laptop-tb](https://github.com/ferstar/ideapad-laptop-tb) · C · ⭐55 | Out-of-tree kernel module fixing lid-close "dead sleep" and Fn+F5/F6 shutdowns on 2024 ThinkBooks, shipped to users months before the fix reached mainline in 6.15.4. |
| [xiaomi_xaga_kernel](https://github.com/ferstar/xiaomi_xaga_kernel) · C · ⭐50 | Custom kernel for Redmi K50i / POCO X4 GT / Note 11T Pro, including an MGLRU backport. |
| [kernel_manifest](https://github.com/ferstar/kernel_manifest) · ⭐36 | Kernel build for Realme GT5 Pro (SM8650), forked 48 times. |

## Tools

- [check-requirements-txt](https://github.com/ferstar/check-requirements-txt) ⭐12 — pre-commit hook that catches packages missing from `requirements.txt` / `pyproject.toml`
- [pot-app-recognize-plugin-rapid-py](https://github.com/ferstar/pot-app-recognize-plugin-rapid-py) ⭐15 — offline RapidOCR plugin for Pot App
- [fast-context](https://github.com/ferstar/fast-context) ⭐24 — codebase context locator for coding agents: local chunk prefetch plus remote symbol reasoning
- [dsh-tool-ocr](https://github.com/ferstar/dsh-tool-ocr) — local OCR so text-only LLMs can read images

## Upstream contributions

- [esengine/DeepSeek-Reasonix](https://github.com/esengine/DeepSeek-Reasonix/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐35k) — Windows 11 session-switch freeze, prompt history, per-arch macOS builds
- [BYVoid/OpenCC](https://github.com/BYVoid/OpenCC/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐10k) — manylinux2014 wheels, macOS ARM64 CI
- [tiann/hapi](https://github.com/tiann/hapi/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐5k) — terminal quick keys, mobile input and teardown fixes
- [zurawiki/gptcommit](https://github.com/zurawiki/gptcommit/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐2.4k) — custom OpenAI-compatible API base URLs
- [h2non/filetype.py](https://github.com/h2non/filetype.py/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐775) — zstd and CDFV2 Word detection, file-like reader fixes

<p align="right"><sub><i>Code is cheap, let's talk.</i></sub></p>
