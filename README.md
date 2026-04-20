# TechStack 🔍

> **Technology Stack Detective** - Auto-Detect and Document Project Dependencies

[![npm](https://img.shields.io/npm/v/techstack.svg)](https://www.npmjs.com/package/techstack)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue.svg)](https://www.typescriptlang.org/)

---

## 🎯 What is TechStack?

TechStack automatically detects and documents the technology stack of any project. It analyzes source code, configuration files, and dependencies to create comprehensive technology reports.

### Why TechStack?

| Feature | Benefit |
|---------|---------|
| **Auto-Detection** | No manual configuration needed |
| **Multi-Language** | Supports 50+ programming languages |
| **Deep Analysis** | Detects frameworks, libraries, and tools |
| **Visual Reports** | Generate dependency graphs |
| **CI/CD Integration** | Add to your build pipeline |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      TechStack                              │
├─────────────────────────────────────────────────────────────┤
│  ┌────────────┐    ┌────────────┐    ┌────────────────┐   │
│  │   File     │───▶│  Analyzer  │───▶│    Detector    │   │
│  │   Scanner  │    │   Engine   │    │    Engine      │   │
│  └────────────┘    └────────────┘    └────────┬───────┘   │
│                                                  │           │
│                                                  ▼           │
│  ┌─────────────────────────────────────────────────────┐  │
│  │                  Results Engine                       │  │
│  │  Languages  │  Frameworks  │  Dependencies  │  Tools  │  │
│  └─────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
```

---

## ✨ Features

- **Language Detection** - Identify 50+ programming languages
- **Framework Detection** - React, Vue, Angular, Django, Rails, etc.
- **Dependency Analysis** - package.json, requirements.txt, Cargo.toml
- **Config Detection** - ESLint, Prettier, TypeScript, etc.
- **Tool Detection** - Git, Docker, Kubernetes, etc.
- **Visual Reports** - Dependency graphs and charts
- **Export Options** - JSON, Markdown, HTML, PDF

---

## 🚀 Quick Start

### Installation

```bash
npm install -g techstack
# or
yarn global add techstack
```

### Basic Usage

```bash
# Scan current directory
techstack scan

# Scan specific directory
techstack scan /path/to/project

# Scan and output JSON
techstack scan --format json
```

---

## 📖 Usage Examples

### CLI Usage

```bash
# Scan project
techstack scan ./my-project

# Output formats
techstack scan --format markdown    # Markdown report
techstack scan --format html         # HTML report  
techstack scan --format json         # JSON output
techstack scan --format dot         # GraphViz DOT

# Generate visualization
techstack visualize --output graph.png

# CI mode (non-interactive)
techstack scan --ci --format json
```

### Programmatic Usage

```typescript
import { TechStack, ProjectAnalyzer } from 'techstack';

const analyzer = new ProjectAnalyzer();
const result = await analyzer.analyze('/path/to/project');

console.log('Languages:', result.languages);
console.log('Frameworks:', result.frameworks);
console.log('Dependencies:', result.dependencies);
```

---

## ⚙️ Configuration

```json
{
  "techstack": {
    "exclude": ["node_modules", ".git"],
    "depth": 3,
    "includeDevDeps": true,
    "detectTools": true
  }
}
```

---

## 🔧 API Reference

| Class | Description |
|-------|-------------|
| `ProjectAnalyzer` | Main analysis class |
| `LanguageDetector` | Language identification |
| `FrameworkDetector` | Framework detection |
| `DependencyResolver` | Dependency analysis |

---

## 🤝 Contributing

Contributions welcome!

---

## 📄 License

MIT License
