<h1 align="center">Hi, I'm Jeff Zhang 👋</h1>

<p align="center">
  Geek · incurable tinkerer · dad of a lovely little girl
  <br>
  I take things apart until they tell me how they work — laptops, phone kernels, AI agents.
  <br>
  Lately: turning proven software into trusted tools for AI agents — keeping the craft in the product and permissions on a leash.

</p>

<p align="center">
  <a href="https://blog.ferstar.org/en/"><img src="https://img.shields.io/badge/Blog-blog.ferstar.org-24292f?style=flat-square&logo=hugo&logoColor=white" alt="Blog"></a>
  <a href="https://x.com/ferstar_org"><img src="https://img.shields.io/badge/X-@ferstar__org-24292f?style=flat-square&logo=x&logoColor=white" alt="X"></a>
  <a href="https://blog.ferstar.org/en/index.xml"><img src="https://img.shields.io/badge/RSS-subscribe-24292f?style=flat-square&logo=rss&logoColor=white" alt="RSS"></a>
</p>

## What I work on

- **Agent execution boundaries & attribution** — OS-native sandboxing, end-to-end human identity, capped permissions, verifiable citations, and audit trails instead of trusting a vendor's prompt.
- **Agent-ready software & runtimes** — exposing proven domain tools via MCP so expertise stays in the product, backed by Rust runtimes with streaming recovery, graded loop guards, and fault isolation.
- **Financial document systems** — production infrastructure for regulatory filings and listed-company annual reports: deep document parsing, rule checks, and exchange-scale AI authoring workflows.
- **Linux graphics, input & kernels** — zero-copy GPU encoding pipelines (NVENC / VAAPI DMA-BUF), Wayland/X11 capture, touchpad gestures, laptop ACPI quirks, and phone kernels: when hardware or the stack misbehaves, I go down to the driver.
- **Pragmatic Python tooling** — small, sharp tools that remove a daily annoyance and get out of the way.

## Featured

**[RunSeal](https://github.com/runseal-labs/runseal)** · Rust  
An OS-native sandbox layer and stable execution protocol for AI agents: policy-governed filesystem and network boundaries, structured audit events, and fail-closed behavior whenever a request can't be fully enforced. Windows is the reference backend; macOS and Linux are experimental.  
→ [Why I built it](https://blog.ferstar.org/en/posts/local-first-agent-execution-boundary-runseal/)

**ZCode silent upload disclosure** · Sep 2026  
Found that an AI coding tool was silently packing users' open workspaces — including full `.git` history — encrypting and uploading them to cloud storage by default with no kill switch. The write-up drew 1.6M+ views on X and led to the upload pipeline being removed, the client being open-sourced, and third-party assessments.  
→ [How ZCode silently uploaded full Git history](https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/)

**[SealDesk](https://github.com/runseal-labs/sealdesk)** · Rust  
A RustDesk fork built on the tailcat transport: scan a QR code and connect, zero config, P2P first with DERP fallback. Early alpha, Linux x64 for now.  
→ [Rebuilding RustDesk on tailcat for zero-config QR connections](https://blog.ferstar.org/en/posts/yet-another-remote-desktop-application-sealdesk/)

## Notes on agent engineering

- [The illusion of Agent SaaS](https://blog.ferstar.org/en/posts/the-illusion-of-agent-saas/) — why wrapping an agent isn't a product
- [Graded loop guards for agents (Warn → Block → Halt)](https://blog.ferstar.org/en/posts/agent-graded-loop-guard-warn-block-halt/) — graded loop guards instead of a hard kill
- [Cross-chunk streaming recovery for DSML tool calls](https://blog.ferstar.org/en/posts/agent-dsml-tool-call-streaming-recovery/) — recovering tool calls the model emitted as text

## Latest from the blog

<!-- BLOG-POST-LIST:START -->
- [Strata 0.2.7.1 on GB10 Benchmark and SPEC_COST Ablation](https://blog.ferstar.org/en/posts/strata-gb10-sm121-benchmark-optimization/)
- [RTX 4090 D Tensor Unlock: What Can Quantized MoE Inference Gain?](https://blog.ferstar.org/en/posts/tensor-unlock-quantized-moe/)
- [RTX 4090 D Unlock Measurements: Doubled Tensor Throughput and a Strata Retest](https://blog.ferstar.org/en/posts/rtx4090d-gpu-unlock-strata-benchmark/)
- [Driving an Electron Desktop App Through UIA: A Windows-MCP Field Test](https://blog.ferstar.org/en/posts/ai-agent-drives-electron-app-windows-mcp-uia/)
- [I Rebuilt RustDesk with tailcat for Scan-to-Connect Remote Desktop](https://blog.ferstar.org/en/posts/yet-another-remote-desktop-application-sealdesk/)
<!-- BLOG-POST-LIST:END -->

## Linux & systems

| Project | What it is |
| --- | --- |
| [uu-remote-linux](https://github.com/VallierDev/uu-remote-linux/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) · Rust · ⭐859 | Unofficial Linux host for NetEase UU Remote (core contributor). Built the in-process A/V pipeline replacing `ffmpeg` subprocesses: native NVENC (XShm + 4:4:4), zero-copy VAAPI/DMA-BUF (DRI3 & Portal), XDamage delta capture, live encoder hot-swap, and KDE Wayland privacy blanking. |
| [gestures](https://github.com/ferstar/gestures) · Rust · ⭐111 | Maintained fork of a libinput touchpad gesture tool, rebuilt around low-latency three-finger dragging on both X11 and Wayland. Now has several times the stars of upstream. [Write-up](https://blog.ferstar.org/en/posts/linux-touchpad-gestures-drag/) |
| [ideapad-laptop-tb](https://github.com/ferstar/ideapad-laptop-tb) · C · ⭐55 · archived | Out-of-tree kernel module fixing lid-close "dead sleep" and Fn+F5/F6 shutdowns on 2024 ThinkBooks, shipped to users months before the fix reached mainline in 6.15.4. |
| [xiaomi_xaga_kernel](https://github.com/ferstar/xiaomi_xaga_kernel) · C · ⭐54 | Custom kernel for Redmi K50i / POCO X4 GT / Note 11T Pro, including an MGLRU backport. |
| [kernel_manifest](https://github.com/ferstar/kernel_manifest) · ⭐37 | Kernel build for Realme GT5 Pro (SM8650), forked 48 times. |

## Tools

- [fast-context](https://github.com/ferstar/fast-context) ⭐24 — codebase context locator for coding agents: local chunk prefetch plus remote symbol reasoning
- [dsh-tool-runseal](https://github.com/runseal-labs/dsh-tool-runseal) — RunSeal sandbox provider for DeepSeek Harness (`dsh`), bringing OS-native policy-enforced command execution across Windows, macOS, and Linux
- [pot-app-recognize-plugin-rapid-py](https://github.com/ferstar/pot-app-recognize-plugin-rapid-py) ⭐15 — offline RapidOCR plugin for Pot App
- [check-requirements-txt](https://github.com/ferstar/check-requirements-txt) ⭐12 — pre-commit hook that catches packages missing from `requirements.txt` / `pyproject.toml`

## Upstream contributions

- [Niko1221/Strata](https://github.com/Niko1221/Strata/releases/tag/v0.2.7) (⭐45k) — ARM64 / NVIDIA DGX Spark (GB10) engine support
- [esengine/DeepSeek-Reasonix](https://github.com/esengine/DeepSeek-Reasonix/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐36k) — Windows 11 session-switch freeze, prompt history, per-arch macOS builds
- [BYVoid/OpenCC](https://github.com/BYVoid/OpenCC/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐10k) — manylinux2014 wheels, macOS ARM64 CI
- [tiann/hapi](https://github.com/tiann/hapi/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐5k) — terminal quick keys, mobile input and teardown fixes
- [zurawiki/gptcommit](https://github.com/zurawiki/gptcommit/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐2.4k) — custom OpenAI-compatible API base URLs
- [h2non/filetype.py](https://github.com/h2non/filetype.py/pulls?q=is%3Apr+author%3Aferstar+is%3Amerged) (⭐779) — zstd and CDFV2 Word detection, file-like reader fixes

<p align="right"><sub><i>Code is cheap, let's talk.</i></sub></p>
