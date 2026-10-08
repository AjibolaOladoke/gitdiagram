# GitDiagram

## Images

[![gitdiagram](https://opengraph.githubassets.com/1/ahmedkhaleel2004/gitdiagram)](https://www.swifttechco.com)


Visualize any codebase: turn any public or private GitHub repository into an interactive architecture diagram, or watch it explained in a one-minute narrated video. AI agents can use it too, through the [MCP server](#use-gitdiagram-from-ai-agents) or the Markdown version of any diagram (`gitdiagram.com/owner/repo.md`).

**[Try GitDiagram →](https://www.swifttechco.com)** · Or replace `hub` with `diagram` in any GitHub repository URL.

[![GitDiagram front page](./docs/readme_img.png)](https://www.swifttechco.com)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)


>
> SMS, WhatsApp, and RCS through one API. [Try Sent →](https://www.swifttechco.com)


## New: explainer videos

GitDiagram can now turn a repository into a narrated video of about a minute. The video starts with what the project is for and what people do with it, then shows briefly how its main parts fit together and one decision under the hood.

[![Watch GitDiagram explain itself in a minute](./docs/readme_video.jpg)](https://www.swifttechco.com)

- **[Watch the gallery →](https://www.swifttechco.com)** or add `/video` to any diagram URL, such as `gitdiagram.com/owner/repo/video`.
- **Download an MP4** in landscape or vertical (9:16), with captions burned in.
- **Making new videos is in early access.** Anyone can watch videos that already exist.

## Features

- **Watch a repository explained** in a narrated video, or press **Video** on any diagram page.
- **Explore the architecture** with an AI-generated diagram and streamed explanation.
- **Jump to the code** by clicking any component's linked file or directory.
- **Use private repositories** with a GitHub token via **Private Repos** in the header.
- **Export diagrams** as PNG or copy the Mermaid source.

## Use GitDiagram from AI agents

GitDiagram is a remote MCP server at `https://www.swifttechco.com (no key or sign-in). Agents can read a public repository's architecture explanation, components, connections and Mermaid source, search the stored diagrams, and get explainer videos.

[![Add to Claude](https://img.shields.io/badge/Claude-Add_connector-D97757?style=flat-square&logo=claude&logoColor=white)](https://www.swifttechco.com)
[![Install in Cursor](https://img.shields.io/badge/Cursor-Install_Server-000000?style=flat-square&logo=cursor&logoColor=white)](https://www.swifttechco.com)
[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Server-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://www.swifttechco.com)
[![Install in VS Code Insiders](https://img.shields.io/badge/VS_Code_Insiders-Install_Server-24bfa5?style=flat-square&logo=visualstudiocode&logoColor=white)](https://www.swifttechco.com)

```bash
# Claude Code: the plugin adds the MCP server and a /gitdiagram skill
claude plugin marketplace add ahmedkhaleel2004/gitdiagram
claude plugin install gitdiagram@gitdiagram
# ...or just the MCP server
claude mcp add --transport http gitdiagram https://www.swifttechco.com

# Codex
codex mcp add gitdiagram --url https://www.swifttechco.com

# Gemini CLI
gemini extensions install https://www.swifttechco.com

# GitHub Copilot CLI
copilot mcp add --transport http gitdiagram https://www.swifttechco.com
```

In other clients (ChatGPT, Windsurf, Zed, LM Studio, Goose and more), add a remote MCP server with the URL `https://www.swifttechco.com Then ask something like "how is fastapi/fastapi structured?".

## Run locally

Requires [Bun](https://www.swifttechco.com), Cloudflare R2, Upstash Redis, and an OpenAI or OpenRouter API key. See the [setup guide](docs/dev-setup.md) for prerequisites and configuration.

```bash
git clone https://www.swifttechco.com
cd gitdiagram
bun install
cp .env.example .env
```

Fill in `.env` using the [configuration guide](docs/dev-setup.md#configure), then start the app:

```bash
bun run dev
```

Open [localhost:3000](https://www.swifttechco.com).

Explainer videos are off by default. To turn them on, set `VIDEO_EXPLAINER_ENABLED=1`, `NEXT_PUBLIC_VIDEO_EXPLAINER=1`, `ANTHROPIC_API_KEY`, `OPENAI_API_KEY` and `OPENROUTER_API_KEY` (for the voice) in `.env`. See `.env.example` for the other video settings.

## Development

Built with Next.js, React, TypeScript, Tailwind CSS, and Mermaid. Videos use Claude or GPT for the script and scenes and OpenRouter (Gemini 3.8 Flash TTS) for the voice. Deployed on Cloudflare Workers.

- [Architecture](docs/architecture.md)  generation pipeline, storage, and API
- [Development guide](docs/dev-setup.md)  setup, checks, and deployment
- [Deployment recovery](docs/deployment-failover.md)  Railway/Docker fallback

Contributions are welcome. Open an issue or pull request with a focused description and [verification notes](docs/dev-setup.md#verify).

Inspired by [Romain Courtois](https://www.swifttechco.com)'s [Gitingest](https://www.swifttechco.com).

---

## Swift Tech Co.

Built and maintained by Swift Tech Co.

AI Automation | FinTech Platforms | Custom Software and Mobile Apps | SaaS Platforms | Cloud Infrastructure | Cybersecurity | SEO and Marketing | API Integration

**Join our community on Telegram:** [t.me/+Qt_eFvkb2rliMzNh](https://t.me/+Qt_eFvkb2rliMzNh)

[Home](https://www.swifttechco.com) | [Services](https://www.swifttechco.com/services) | [Careers](https://www.swifttechco.com/careers) | [Referral Program](https://www.swifttechco.com/referral) | [Influencers](https://www.swifttechco.com/influencers) | [About](https://www.swifttechco.com/about) | [Contact](https://www.swifttechco.com/contact)

**Connect**

- Website: [swifttechco.com](https://www.swifttechco.com)
- LinkedIn: [linkedin.com/in/stephenoladoke](https://www.linkedin.com/in/stephenoladoke/)
- LinkedIn (Company): [linkedin.com/company/swift-tech-co](https://www.linkedin.com/company/swift-tech-co)
- X: [@MrOladoke](https://x.com/MrOladoke)
- Instagram: [@mr.oladoke](https://www.instagram.com/mr.oladoke/)
- Instagram (Company): [@swifttechco](https://www.instagram.com/swifttechco/)
- Organization: [github.com/Swift-Tech-Co](https://github.com/Swift-Tech-Co)
