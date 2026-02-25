# 🎬 n8n Production Workflows

**Battle-tested n8n workflow templates for AI-powered content automation.**

A collection of production-grade n8n workflow JSON files, featuring the YouTube Illustrated Story Factory — an end-to-end automated pipeline that generates illustrated video content from story prompts.

![n8n](https://img.shields.io/badge/n8n-Workflows-EA4B71?logo=n8n&logoColor=white)
![Automation](https://img.shields.io/badge/AI-Automation-blueviolet)
![Production](https://img.shields.io/badge/Status-Production-green)

---

## ✨ What's Inside

### 🎥 YouTube Illustrated Story Factory
Fully automated video content creation pipeline with three production iterations:

- **v3** — Core story-to-video pipeline
- **v4** — Improved generation and rendering
- **v5** — Latest iteration with refined orchestration

### 🔧 Modular Subflows

| Subflow | Purpose |
|---------|---------|
| 🗣️ **Voice** | AI voice generation for narration |
| 🎨 **Image Generation** | Illustrated scene creation |
| 🎬 **Render** | Video frame rendering |
| 🧵 **Stitch** | Final video assembly |
| 🔗 **URL Clearing** | Asset URL management |

## 🏗️ Architecture

```
Story Prompt
     │
     ▼
┌─────────────────────────────────────┐
│        Story Factory (n8n)          │
│                                     │
│  ┌─────────┐  ┌──────────────────┐  │
│  │  Voice   │  │ Image Generation │  │
│  │ Subflow  │  │    Subflow       │  │
│  └────┬─────┘  └───────┬─────────┘  │
│       │                │            │
│  ┌────▼────────────────▼─────────┐  │
│  │       Render Subflow          │  │
│  └──────────────┬────────────────┘  │
│                 │                   │
│  ┌──────────────▼────────────────┐  │
│  │       Stitch Subflow          │  │
│  └───────────────────────────────┘  │
└─────────────────────────────────────┘
     │
     ▼
  Final Video
```

## 🚀 Usage

1. Import any `.json` file into your n8n instance
2. Configure credentials (API keys for AI services)
3. Activate the workflow

```bash
# Clone the collection
git clone https://github.com/gaganthakur04/n8n-production-workflows.git

# Import via n8n CLI
n8n import:workflow --input=<workflow-file>.json
```

## 📂 Workflow Files

```
n8n-production-workflows/
├── story-factory-v3.json
├── story-factory-v4.json
├── story-factory-v5.json
└── subflows/
    ├── voice.json
    ├── render.json
    ├── stitch.json
    ├── image-generation.json
    └── url-clearing.json
```

## 💡 Why This Matters

These aren't toy workflows. They represent **production orchestration patterns** — multi-step AI pipelines with error handling, modular subflows, and iterative refinement across three major versions.

## 👤 Author

**Gagan Thakur** — 15 years in enterprise AI, ex-Microsoft, ex-Nuance. Applying enterprise engineering rigor to AI automation.

## 📄 License

MIT
