# TaskForceAI Unified Changelog

All notable changes across TaskForceAI platforms will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Platform Overview

- **Web Application** - Next.js 16 multi-agent AI orchestration platform
- **Desktop Application** - Tauri-based macOS desktop app
- **Mobile Application** - React Native/Expo iOS & Android app
- **CLI/TUI** - Go-based terminal interface with npm distribution
- **TypeScript SDK** - Official Node.js/TypeScript SDK
- **Python SDK** - Official Python SDK
- **REST API** - Developer API with tiered pricing

---

## [Unreleased]

### 🌐 Web Application

- Next.js 16 upgrade with stable Turbopack and React Compiler
- Enhanced multi-agent orchestration with real-time telemetry streaming
- Improved local-first architecture with Dexie.js offline storage
- Advanced security middleware with input sanitization and rate limiting
- Modern ChatGPT-style interface with skeleton loading states

### 🖥️ Desktop Application (Tauri)

- Pending

### ⌨️ CLI/TUI (Go)

- Fixed Linux global installs pulling the macOS binary by always building or copying the platform-specific executable during the postinstall step.

---

## [0.1.1] - 2025-11-04

### 🖥️ Desktop Application (Tauri)

#### Added

- Bundled Next.js standalone server with embedded SQLite database for offline-first desktop usage
- Updated Tauri bootstrap to spawn the bundled server and gracefully shut it down on exit
- Sparkle auto-update initialization now runs with env-configurable feed/public key values

#### Fixed

- Resolved Dexie initialization failures by ensuring the local database opens before performing operations
- Removed fragile pnpm symlink assumptions by copying missing dependencies (e.g., `semver`) into the standalone bundle
- Ensured desktop builds package a complete Prisma client and SQLite database

### 🖥️ Desktop Application (Tauri)

- macOS desktop shell with native window management
- Sparkle auto-update integration for seamless updates
- Native macOS app icon and asset preparation

### 📱 Mobile Application (React Native)

- Expo SDK 54 integration with React Native 0.81.5
- Offline-first architecture with SQLite storage
- Real-time sync capabilities with conflict resolution
- iOS and Android platform-specific optimizations

### ⌨️ CLI/TUI (Go)

- Terminal User Interface with Bubble Tea framework
- Self-updating mechanism with GitHub releases
- Cross-platform binary distribution
- Configuration management and history tracking

### 📚 SDKs

- **TypeScript SDK**: Full TypeScript support with comprehensive types
- **Python SDK**: Async/await support with httpx client
- **CLI npm package**: Automated build and distribution system

### 🔌 REST API

- Developer API with tiered pricing (STARTER/PRO/ENTERPRISE)
- Real-time usage tracking and rate limiting
- OpenAPI/Swagger documentation with client generation
- API key management with automated alerts

---

## [1.0.0] - 2025-11-03

### 🌐 Web Application

#### Added

- Multi-agent orchestration system with parallel execution (4 agents)
- React-based frontend with TypeScript and Next.js 16
- JWT authentication with NextAuth.js v5 (username/password + Google OAuth)
- Stripe payments integration with subscription management (Free/Pro tiers)
- Redis caching with automatic in-memory fallback
- Prisma ORM with PostgreSQL (Neon) database
- Comprehensive security middleware (CORS, rate limiting, input sanitization)
- Real-time agent progress visualization via Server-Sent Events
- Local-first architecture with IndexedDB offline storage
- PWA support with service worker and app manifest
- Developer dashboard at `/dashboard` for API key management
- Structured JSON logging with Sentry error tracking
- 26+ production best practices implemented

#### Security

- Bcrypt password hashing with salt rounds
- AES-256-GCM encryption for sensitive data
- Rate limiting: Free (3/30 days), Pro (2/hour)
- Input sanitization preventing XSS and injection attacks
- Environment variable validation with startup checks
- Security headers middleware (HSTS, CSP, etc.)

### 🖥️ Desktop Application (Tauri)

#### Added

- Cross-platform desktop application framework
- Native macOS window management
- Auto-update system with Sparkle integration
- Rust-based backend for performance
- Native file system access
- System tray integration

### 📱 Mobile Application (React Native)

#### Added

- React Native application with Expo SDK 54
- Cross-platform iOS and Android support
- Offline-first architecture with SQLite
- Real-time synchronization with conflict resolution
- Native biometric authentication support
- Push notification capabilities
- Responsive design with mobile-optimized UI

### ⌨️ CLI/TUI (Go)

#### Added

- Terminal User Interface with Bubble Tea framework
- Cross-platform binary distribution (macOS, Linux, Windows)
- Self-updating mechanism using GitHub releases
- Configuration file management
- Command history and search
- Model selection and switching
- Real-time streaming responses
- Copy-to-clipboard functionality

### 📚 SDKs

#### TypeScript SDK (v1.0.0)

- Official Node.js/TypeScript SDK
- Full TypeScript definitions
- Promise-based API with async/await support
- Error handling with custom exception types
- Streaming response support
- Comprehensive test coverage

#### Python SDK (v0.1.0)

- Official Python SDK with httpx client
- Async/await support for high performance
- Type hints with mypy compatibility
- Pydantic models for data validation
- Comprehensive test suite with pytest
- Support for Python 3.9+

#### CLI npm Package (v0.3.3)

- npm-based distribution for easy installation
- Automated build system with postinstall scripts
- Cross-platform binary bundling
- Version management and update notifications

### 🔌 REST API

#### Added

- RESTful API with OpenAPI 3.0 specification
- Developer API tiers: STARTER ($10/mo), PRO ($50/mo), ENTERPRISE (custom)
- API key management with creation, listing, and revocation
- Real-time usage tracking and rate limiting
- Webhook support for event notifications
- Comprehensive API documentation
- SDK generation from OpenAPI spec

#### API Endpoints

- `/api/v1/run` - Task execution endpoint
- `/api/v1/stream/[taskId]` - Real-time streaming
- `/api/v1/conversations` - Conversation management
- `/api/v1/developer/usage` - Usage statistics
- `/api/v1/developer/keys` - API key management
- `/api/v1/sync/*` - Real-time synchronization

---

## [0.1.0] - Initial Development

### 🌐 Web Application

#### Added

- Basic agent system with tool support
- SQLite database for conversation storage
- Simple web interface with React
- Vercel AI Gateway integration
- Basic authentication system

### ⌨️ CLI/TUI (Go)

#### Added

- Basic command-line interface
- Simple model selection
- Basic configuration management
- Terminal output formatting

### 📚 SDKs

#### Added

- Initial TypeScript SDK prototype
- Basic Python client implementation
- Simple API wrapper functionality

---

## Platform Version Matrix

| Platform        | Current Version | Package Name                 | Repository                  |
| --------------- | --------------- | ---------------------------- | --------------------------- |
| Web Application | 1.0.0           | `@taskforce/web`             | `apps/web/`                 |
| Desktop App     | 0.1.1           | `taskforceai-desktop`        | `apps/desktop/`             |
| Mobile App      | 0.1.0           | `taskforceai-mobile`         | `apps/mobile/`              |
| CLI/TUI (Go)    | -               | `github.com/TaskForceAI/tui` | `apps/tui/`                 |
| CLI npm Package | 0.3.3           | `taskforceai-cli`            | `packages/taskforceai-cli/` |
| TypeScript SDK  | 1.0.0           | `taskforceai-sdk`            | `packages/taskforceai-sdk/` |
| Python SDK      | 0.1.0           | `taskforceai`                | `packages/python-sdk/`      |
| Core Library    | 1.0.0           | `@taskforce/core`            | `packages/core/`            |

---

## Release Process

### Automated Releases

- **Web**: Deployed to Vercel on merge to `main`
- **Desktop**: Auto-built and released via GitHub Actions
- **Mobile**: Expo EAS builds with deployment to app stores
- **CLI**: Go binaries attached to GitHub releases
- **SDKs**: Published to npm/PyPI on version bump

### Version Coordination

- Major releases coordinated across all platforms
- Minor/patch releases independent per platform
- Breaking changes announced across all channels
- Migration guides provided for major updates

---

## Links

- **Main Website**: https://taskforceai.chat
- **Documentation**: https://docs.taskforceai.chat
- **GitHub Repository**: https://github.com/ClayWarren/taskforceai-hub
- **API Documentation**: https://taskforceai.chat/docs/api
- **Developer Dashboard**: https://taskforceai.chat/dashboard
- **Status Page**: https://status.taskforceai.chat

---

[Unreleased]: https://github.com/ClayWarren/taskforceai/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/ClayWarren/taskforceai/releases/tag/v1.0.0
[0.1.0]: https://github.com/ClayWarren/taskforceai/releases/tag/v0.1.0
