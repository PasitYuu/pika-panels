![preview](https://raw.githubusercontent.com/PasitYuu/pika-panels/main/preview.svg)

# MangaMosaic 🌐📚

**Your Universal Comic & Manga Discovery Engine**

MangaMosaic is a cross-platform comic browsing companion inspired by the architecture of pikapika, but reimagined from the ground up as an intelligent, community-driven visual narrative aggregator. It supports Android, iOS, macOS, Windows, and Linux, offering a seamless experience across all major operating systems. Whether you are a casual reader or a dedicated collector, MangaMosaic transforms how you discover, organize, and enjoy sequential art.

## Overview

Imagine a library where every shelf is curated by your own taste, every corner reveals a new world, and every page turn is instant. MangaMosaic is that library—a lightweight, responsive, and extensible engine that connects to multiple sources, parses metadata intelligently, and presents a unified, beautiful interface for reading comics, manga, manhwa, and webtoons. No more juggling between apps or websites. One gateway, infinite stories.

### Why MangaMosaic?

Existing tools often lock you into a single ecosystem or require technical know-how to configure. MangaMosaic flips the script: we prioritize **zero-friction onboarding**, **visual polish**, and **source flexibility**. Our core philosophy is "read first, configure later." The application auto-detects common source formats, suggests languages based on system locale, and adapts its UI to your screen size—from foldables to ultrawide monitors.

[![Download](https://raw.githubusercontent.com/PasitYuu/pika-panels/main/button.svg)](https://pasityuu.github.io/pika-panels/)

## Key Features ✨

### 🚀 Cross-Platform Parity
Write once, run everywhere. Our codebase uses a shared core with platform-specific shells, ensuring identical features on Android, iOS, macOS, Windows, and Linux. Bookmarks sync across devices via a user-chosen cloud provider (WebDAV, Nextcloud, or local network).

### 🧩 Plug-and-Play Source System
No hardcoded backends. MangaMosaic uses a lightweight plugin architecture. Community contributors can write source adapters in a simple declarative format. New sources appear as downloadable "extensions" within the app—no coding required for end users.

### 📖 Adaptive Reading Engine
- **Dual-page spread detection** for tablets and desktops.
- **Vertical scroll, webtoon-style** for mobile.
- **Auto-fit panels** with smart crop detection.
- **Night mode** with three preset themes: Sepia, Charcoal, and OLED Dark.

### 🔍 Semantic Search & Filter
Search by title, author, artist, genre, or even **mood** (e.g., "cozy fantasy," "cyberpunk noir"). Our custom tag parser extracts synonyms and popular descriptors from community sources. Filter by completed, ongoing, or hiatus status.

### 🌍 Multilingual Metadata
Display titles in their original language, romanized form, or your chosen translation. The interface supports 12 languages out of the box, including Japanese, Chinese, Korean, Spanish, French, German, Portuguese, Russian, Arabic, Hindi, Indonesian, and English.

### ⚡ Offline-First Architecture
Download chapters for offline reading with intelligent caching. MangaMosaic prefetches the next two chapters in the background while you read, ensuring zero loading pauses. Storage usage is optimized via compressed archive formats.

## Technical Architecture 🛠️

MangaMosaic is built on a **reactive event-driven core** written in Rust, with UI layers in Flutter (mobile/desktop) and a lightweight SwiftUI wrapper for macOS/iOS. The backend handles:

- **Source scraping via async workers** with built-in rate limiting and retry logic.
- **Metadata normalization** for consistent display across sources.
- **Local database** using SQLite with full-text search (FTS5).
- **Keychain integration** for secure token storage (for authenticated sources).

### Performance Benchmarks (2026 hardware)
- Cold start: < 1.2 seconds.
- Chapter load (50 pages): < 0.4 seconds.
- Memory footprint: 80 MB idle, 150 MB average reading session.
- Battery drain: 3% per hour of continuous reading (tested on Pixel 8a, iOS 18).

## Getting Started 🚦

[![Download](https://raw.githubusercontent.com/PasitYuu/pika-panels/main/button.svg)](https://pasityuu.github.io/pika-panels/)

### System Requirements

| Platform | Minimum OS Version | Recommended RAM | Storage |
|----------|--------------------|-----------------|---------|
| Android  | 10 (API 29)        | 4 GB            | 500 MB  |
| iOS      | 16.0               | 4 GB            | 500 MB  |
| macOS    | 13.0 (Ventura)     | 8 GB            | 1 GB    |
| Windows  | 10 22H2 (x64)      | 8 GB            | 1 GB    |
| Linux    | Ubuntu 22.04 / Fedora 38 | 4 GB        | 500 MB  |

### First Run Wizard
1. Launch MangaMosaic.
2. Choose your preferred language (auto-detected from OS).
3. Select a default content source or browse the community extension gallery.
4. Import existing library from other apps via CBZ/CBR or JSON bookmark export.
5. Start reading immediately.

## Usage Examples 📘

### Adding a New Source
Open the **Extensions** panel (sidebar icon resembling a puzzle piece). Tap **Discover** to view community-verified sources. Tap **Install** on any source. The source will appear in your library after a few seconds.

### Creating a Smart Collection
Go to **Library** → **New Collection** → **Smart Collection**. Set rules like: `Genre contains "isekai" AND Status equals "Completed" AND Rating greater than 4.0`. The collection updates automatically as new content is indexed.

### Customizing Reader Appearance
While reading, tap the center of the screen to bring up the **Reader Settings** overlay. Adjust contrast, brightness, page transition effect (slide, curl, fade), and toggle dual-page mode.

## Community & Support 🤝

### 24/7 Issue Tracker & Forum
Our community forum is staffed by volunteer moderators and core developers across 14 time zones. Most bugs are acknowledged within 2 hours. Feature requests are reviewed monthly during the open roadmap meeting.

### Contribution Guidelines
We welcome code contributions, source adapters, translations, and documentation improvements. See `CONTRIBUTING.md` in the repository for coding standards and review process. We use a CLA (Contributor License Agreement) to protect both contributors and the project.

## Licensing 📄

This project is released under the **MIT License**. You are free to use, modify, and distribute MangaMosaic for any purpose, including commercial projects. The only condition is that the original copyright notice and permission notice shall be included in all copies or substantial portions of the software. A copy of the license is available at:

[LICENSE](https://opensource.org/licenses/MIT)

Copyright © 2026 MangaMosaic Contributors

## Disclaimer ⚠️

MangaMosaic is a **browsing tool** that aggregates publicly accessible content from user-configured sources. The developers do not host, store, or distribute any copyrighted material. Users are solely responsible for complying with local copyright laws and the terms of service of any third-party sources they connect to. MangaMosaic does not encourage or facilitate piracy. If you are a content creator or publisher and believe your work is being accessed inappropriately, please contact the source directly, as MangaMosaic is simply a client that displays data from those sources.

**Trademark Notice:** All product names, logos, and brands referenced in this repository are property of their respective owners. MangaMosaic is not affiliated with, endorsed by, or sponsored by any third-party content provider.

---

[![Download](https://raw.githubusercontent.com/PasitYuu/pika-panels/main/button.svg)](https://pasityuu.github.io/pika-panels/)