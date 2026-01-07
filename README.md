# TaskForceAI

**TaskForceAI** is a multi-agent orchestration platform that emulates the behavior of Grok 4 Heavy but is model-agnostic. It is a production-ready system.

## 🌟 Ecosystem

This repository serves as the central hub for the TaskForceAI ecosystem. While the core platform is currently private, we maintain several open-source components:

### 🖥️ Client Applications

- **[TaskForceAI TUI](https://github.com/ClayWarren/taskforceai-tui)**
  A powerful terminal user interface for managing agents, conversations, and workflows directly from your command line. Built with Go and Bubble Tea.

  ```bash
  # Install via Homebrew (macOS)
  brew tap ClayWarren/taskforceai
  brew install taskforceai-cli

  # Install via npm (Cross-platform)
  npm install -g taskforceai-cli
  ```

### 📚 Software Development Kits (SDKs)

- **[Python SDK](https://github.com/ClayWarren/taskforceai-sdk-python)**
  Async-first Python client with type hints, Pydantic models, and built-in support for streaming responses.

  ```bash
  pip install taskforceai
  ```

- **[TypeScript SDK](https://github.com/ClayWarren/taskforceai-sdk-typescript)**
  Type-safe client for Node.js and browsers with streaming support, automatic retries, and full IDE autocomplete.

  ```bash
  npm install taskforceai-sdk
  ```
### 🍺 Package Distribution

* **[Homebrew Tap](https://github.com/ClayWarren/homebrew-taskforceai)**

Official Homebrew tap for installing and managing TaskForceAI CLI releases on macOS.

```bash
brew tap ClayWarren/taskforceai
brew install taskforceai-cli
```

## 📖 Documentation

- **[Official Documentation](https://docs.taskforceai.chat)** - Comprehensive guides, API references, and tutorials.
- **[REST API Reference](https://taskforceai.chat/docs/api)** - Detailed API endpoints and usage.

## 🛤️ Roadmap & Changelog

See [CHANGELOG.md](./CHANGELOG.md) for a unified history of updates across all platforms (Web, Desktop, Mobile, CLI, and SDKs).

## 🤝 Support

- **Issues**: Please file issues in the specific repository (e.g., TUI, SDKs) or reach out via our [support channels](https://taskforceai.chat/support).
- **Discussions**: Join the community on [GitHub Discussions](https://github.com/claywarren/taskforceai/discussions).

## 📄 License

Individual components are licensed under their respective licenses (mostly MIT). See specific repositories for details.

- In addition to the developer suite, TaskForceAI has:
- Apps: React Native Expo mobile (ios/android), Typescript/Tailwind CSS Tanstack Start web, and Rust Tauri desktop (macOS/Linux/Windows).
- Our Go server hosts the core package (Go), and connects to the multiple clients, services.
- Agent Tools: Web Search, Code Execution, Files.
- Everything publicly offered can be accessed from the main company site (Nextjs).
- Deployed on Vercel. Uses Vercel AI Gateway, Vercel Blob installers, Redis cache, Inngest background jobs, Stripe. 
- Databases: Postgres for web, SQLite for mobile, desktop, cli. 
- Web also uses fusejs for local search, dexiejs (indexedDB) for local storage.
- Many more details behind the scenes...
