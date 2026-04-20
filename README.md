# TechStack 🔍

> **Technology Stack Detective** - Auto-Detect and Document Project Dependencies

[![npm](https://img.shields.io/npm/v/techstack.svg)](https://www.npmjs.com/package/techstack)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue.svg)](https://www.typescriptlang.org/)
[![Node](https://img.shields.io/badge/Node-18+-green.svg)](https://nodejs.org/)

---

## 🎯 What is TechStack?

TechStack automatically detects and documents the technology stack of any project. It analyzes source code, configuration files, and dependencies to create comprehensive technology reports with zero configuration required.

### Why TechStack?

| Feature | Benefit |
|---------|---------|
| **Zero Config** | Works out of the box |
| **Multi-Language** | Supports 50+ programming languages |
| **Deep Analysis** | Detects frameworks, libraries, and tools |
| **Visual Reports** | Generate dependency graphs |
| **CI/CD Ready** | Add to your build pipeline |
| **Fast** | Parallel processing for speed |

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                         TechStack                                   │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌──────────────────────────────────────────────────────────────┐  │
│  │                      File Scanner                            │  │
│  │  ┌────────┐  ┌────────┐  ┌────────┐  ┌────────┐       │  │
│  │  │ Source │  │ Config │  │ Build  │  │  Meta  │       │  │
│  │  │ Files  │  │  Files │  │ Files  │  │  Files │       │  │
│  │  └────┬───┘  └────┬───┘  └────┬───┘  └────┬───┘       │  │
│  └───────┼────────────┼────────────┼────────────┼────────────┘  │
│          │            │            │            │                │
│          └────────────┴─────┬──────┴────────────┘                │
│                             │                                      │
│                             ▼                                      │
│  ┌──────────────────────────────────────────────────────────────┐  │
│  │                    Analyzer Engine                            │  │
│  │  ┌────────────┐  ┌────────────┐  ┌────────────────────┐   │  │
│  │  │  Language  │  │ Framework  │  │   Dependency       │   │  │
│  │  │  Detector  │  │  Detector  │  │    Resolver       │   │  │
│  │  └────────────┘  └────────────┘  └────────────────────┘   │  │
│  └──────────────────────────────────────────────────────────────┘  │
│                             │                                      │
│                             ▼                                      │
│  ┌──────────────────────────────────────────────────────────────┐  │
│  │                     Results Engine                            │  │
│  │  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────────┐  │  │
│  │  │Languages  │ │Frameworks│ │Dependencies│ │   Tools     │  │  │
│  │  │  (50+)   │ │  (100+)  │ │  (All)   │ │   (50+)      │  │  │
│  │  └──────────┘ └──────────┘ └──────────┘ └──────────────┘  │  │
│  └──────────────────────────────────────────────────────────────┘  │
│                                                                      │
│                             │                                      │
│                             ▼                                      │
│  ┌──────────────────────────────────────────────────────────────┐  │
│  │                     Report Generator                          │  │
│  │  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐      │  │
│  │  │  JSON   │  │ Markdown │  │  HTML   │  │   DOT   │      │  │
│  │  └─────────┘  └─────────┘  └─────────┘  └─────────┘      │  │
│  └──────────────────────────────────────────────────────────────┘  │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### Component Overview

| Component | Responsibility |
|-----------|----------------|
| **File Scanner** | Discovers relevant files in project |
| **Language Detector** | Identifies programming languages |
| **Framework Detector** | Detects frameworks and libraries |
| **Dependency Resolver** | Analyzes package dependencies |
| **Tool Detector** | Identifies development tools |
| **Report Generator** | Creates formatted output |

---

## ✨ Features

### Core Features

| Feature | Description |
|---------|-------------|
| **Language Detection** | Identifies 50+ programming languages |
| **Framework Detection** | React, Vue, Angular, Django, Rails, Next.js, Nuxt, etc. |
| **Dependency Analysis** | package.json, requirements.txt, Cargo.toml, go.mod, etc. |
| **Config Detection** | ESLint, Prettier, TypeScript, Babel, Webpack, etc. |
| **Tool Detection** | Git, Docker, Kubernetes, npm, yarn, etc. |
| **Build File Analysis** | Dockerfile, docker-compose.yml, Makefile, etc. |
| **Database Detection** | Identifies database configurations |

### Advanced Features

| Feature | Description |
|---------|-------------|
| **Dependency Graph** | Visualize dependency relationships |
| **Version Tracking** | Track library versions |
| **Vulnerability Check** | Flag known vulnerable dependencies |
| **License Detection** | Identify licensing requirements |
| **Outdated Detection** | Flag outdated dependencies |
| **Custom Rules** | Define your own detection rules |
| **CI/CD Integration** | GitHub Actions, GitLab CI, Jenkins |

---

## 🚀 Quick Start

### Installation

```bash
# Using npm
npm install -g techstack

# Using yarn
yarn global add techstack

# Using pnpm
pnpm global add techstack
```

### Verify Installation

```bash
techstack --version
# Should output: techstack v1.0.0
```

### Basic Usage

```bash
# Scan current directory
techstack scan

# Scan specific directory
techstack scan /path/to/project

# Scan with verbose output
techstack scan --verbose

# Scan and save results
techstack scan --output report.json
```

---

## 📖 Usage Examples

### Example 1: Basic Project Scan

```bash
# Navigate to project
cd my-project

# Run scan
techstack scan

# Output:
# 🔍 Scanning my-project...
# ✅ Scan complete!
#
# Languages:
#   - TypeScript (87%)
#   - HTML (8%)
#   - CSS (5%)
#
# Frameworks:
#   - React 18.2.0
#   - Next.js 13.4.0
#
# Dependencies:
#   - react (18.2.0)
#   - next (13.4.0)
#   - typescript (5.1.0)
```

### Example 2: Generate Visual Report

```bash
# Generate HTML report
techstack scan --format html --output techstack-report.html

# Generate Markdown documentation
techstack scan --format markdown --output TECHSTACK.md

# Generate JSON for automation
techstack scan --format json --output analysis.json
```

### Example 3: CI/CD Integration

```yaml
# GitHub Actions
name: TechStack Analysis
on: [push, pull_request]

jobs:
  analyze:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Node
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      - name: Install TechStack
        run: npm install -g techstack
      - name: Run Analysis
        run: techstack scan --ci --format json > techstack-report.json
      - name: Upload Report
        uses: actions/upload-artifact@v3
        with:
          name: techstack-report
          path: techstack-report.json
```

### Example 4: Programmatic Usage

```typescript
import { TechStack, ProjectAnalyzer, AnalysisOptions } from 'techstack';

async function analyzeProject() {
  // Configure analysis
  const options: AnalysisOptions = {
    exclude: ['node_modules', '.git', 'dist'],
    includeDevDeps: true,
    detectTools: true,
    detectDatabases: true,
    detectContainers: true,
    depth: 5,
  };

  // Create analyzer
  const analyzer = new ProjectAnalyzer(options);

  // Analyze project
  const result = await analyzer.analyze('/path/to/project');

  // Access results
  console.log('Languages:', result.languages);
  console.log('Frameworks:', result.frameworks);
  console.log('Dependencies:', result.dependencies);
  console.log('Tools:', result.tools);
  console.log('Databases:', result.databases);
  console.log('Containers:', result.containers);

  return result;
}

// Generate custom report
async function generateReport() {
  const analyzer = new ProjectAnalyzer();
  const result = await analyzer.analyze('./my-project');

  // Get summary
  const summary = result.getSummary();
  console.log(`
    Project: ${summary.name}
    Languages: ${summary.languageCount}
    Frameworks: ${summary.frameworkCount}
    Dependencies: ${summary.dependencyCount}
    Files Scanned: ${summary.fileCount}
  `);

  // Export to different formats
  await result.export('json', 'report.json');
  await result.export('markdown', 'report.md');
  await result.export('html', 'report.html');
}
```

### Example 5: Custom Detection Rules

```typescript
import { TechStack, DetectionRule } from 'techstack';

// Define custom rule
const customRule: DetectionRule = {
  name: 'my-custom-tool',
  patterns: [
    { file: 'my-tool.config.js', type: 'config' },
    { file: 'my-tool.json', type: 'package' },
  ],
  detect: (files) => {
    const configFile = files.find(f => f.name === 'my-tool.config.js');
    if (configFile) {
      return {
        name: 'My Custom Tool',
        version: extractVersion(configFile.content),
        confidence: 'high',
      };
    }
    return null;
  },
};

// Create TechStack with custom rules
const techstack = new TechStack({
  customRules: [customRule],
});

const result = await techstack.analyze('./project');
```

### Example 6: Dependency Visualization

```typescript
import { TechStack, DependencyGraph } from 'techstack';

async function visualizeDependencies() {
  const techstack = new TechStack();
  const result = await techstack.analyze('./my-project');

  // Generate dependency graph
  const graph = new DependencyGraph(result.dependencies);

  // Export as DOT (GraphViz)
  const dot = graph.toDOT();
  await writeFile('dependencies.dot', dot);

  // Generate PNG
  await graph.render('png', 'dependencies.png');

  // Generate interactive HTML
  await graph.render('html', 'dependencies.html');
}
```

---

## ⚙️ Configuration

### Configuration File (techstack.config.json)

```json
{
  "techstack": {
    "exclude": [
      "node_modules",
      ".git",
      "dist",
      "build",
      ".next",
      "coverage"
    ],
    "includePatterns": [
      "**/*.{ts,tsx,js,jsx,json}"
    ],
    "excludePatterns": [
      "**/*.test.{ts,js}",
      "**/*.spec.{ts,js}"
    ],
    "depth": 5,
    "parallel": true,
    "maxWorkers": 4,
    "includeDevDeps": true,
    "detectTools": true,
    "detectDatabases": true,
    "detectContainers": true,
    "checkVulnerabilities": false,
    "checkLicenses": false,
    "checkOutdated": false
  }
}
```

### CLI Options

| Option | Short | Description | Default |
|--------|-------|-------------|---------|
| `--scan <path>` | `-s` | Path to scan | `.` |
| `--output <file>` | `-o` | Output file | - |
| `--format <type>` | `-f` | Output format | `json` |
| `--exclude <globs>` | `-e` | Exclude patterns | `node_modules,.git` |
| `--depth <n>` | `-d` | Scan depth | `5` |
| `--verbose` | `-v` | Verbose output | `false` |
| `--ci` | - | CI mode (non-interactive) | `false` |
| `--config <file>` | `-c` | Config file path | - |
| `--help` | `-h` | Show help | - |
| `--version` | `-V` | Show version | - |

### Environment Variables

| Variable | Description |
|----------|-------------|
| `TECHSTACK_CONFIG` | Path to config file |
| `TECHSTACK_EXCLUDE` | Default exclude patterns |
| `TECHSTACK_WORKERS` | Number of parallel workers |

---

## 📊 Supported Technologies

### Programming Languages (50+)

| Language | Extensions | Detection Method |
|----------|------------|-----------------|
| JavaScript | `.js`, `.jsx`, `.mjs` | File patterns |
| TypeScript | `.ts`, `.tsx` | File patterns |
| Python | `.py` | File patterns |
| Java | `.java` | File patterns |
| C# | `.cs` | File patterns |
| Go | `.go` | File patterns |
| Rust | `.rs` | File patterns |
| Ruby | `.rb` | File patterns |
| PHP | `.php` | File patterns |
| Swift | `.swift` | File patterns |
| Kotlin | `.kt`, `.kts` | File patterns |
| Scala | `.scala` | File patterns |
| C++ | `.cpp`, `.hpp` | File patterns |
| C | `.c`, `.h` | File patterns |
| HTML | `.html`, `.htm` | File patterns |
| CSS | `.css`, `.scss`, `.sass` | File patterns |
| SQL | `.sql` | File patterns |
| Shell | `.sh`, `.bash` | File patterns |
| PowerShell | `.ps1` | File patterns |
| R | `.r`, `.R` | File patterns |
| MATLAB | `.m` | File patterns |
| Julia | `.jl` | File patterns |
| Lua | `.lua` | File patterns |
| Haskell | `.hs` | File patterns |
| Elixir | `.ex`, `.exs` | File patterns |
| Clojure | `.clj` | File patterns |
| F# | `.fs`, `.fsx` | File patterns |
| Dart | `.dart` | File patterns |
| Groovy | `.groovy` | File patterns |
| Perl | `.pl`, `.pm` | File patterns |
| Scala | `.scala` | File patterns |
| Objective-C | `.m`, `.mm` | File patterns |
| Zig | `.zig` | File patterns |
| Nim | `.nim` | File patterns |
| Crystal | `.cr` | File patterns |
| V | `.v` | File patterns |
| Odin | `.odin` | File patterns |
| Gleam | `.gleam` | File patterns |
| Rescript | `.res`, `.resi` | File patterns |
| Lean | `.lean` | File patterns |
| Agda | `.agda` | File patterns |
| Idris | `.idr` | File patterns |
| Coq | `.v` | File patterns |
| OCaml | `.ml`, `.mli` | File patterns |
| Scheme | `.scm`, `.ss` | File patterns |
| Racket | `.rkt` | File patterns |
| Fortran | `.f`, `.f90` | File patterns |
| COBOL | `.cbl`, `.cob` | File patterns |
| Pascal | `.pas` | File patterns |
| Prolog | `.pl` | File patterns |

### Frameworks (100+)

**Frontend:**
- React, Vue, Angular, Svelte, Solid, Qwik
- Next.js, Nuxt, Remix, Astro
- Gatsby, Jekyll, Hugo
- jQuery, Backbone, Ember
- TailwindCSS, Bootstrap, Material UI, Chakra UI

**Backend:**
- Express, Fastify, NestJS, Koa
- Django, Flask, FastAPI, Pyramid
- Rails, Sinatra, Hanami
- Spring, Spring Boot, Quarkus
- Laravel, Symfony, CakePHP
- ASP.NET, ASP.NET Core
- Echo, Gin, Fiber (Go)
- Axum, Actix-web (Rust)

**Mobile:**
- React Native, Flutter, Ionic, NativeScript
- SwiftUI, Jetpack Compose

**Desktop:**
- Electron, Tauri, NW.js
- GTK, Qt, wxWidgets

**Data/ML:**
- TensorFlow, PyTorch, Keras
- Pandas, NumPy, Scikit-learn
- Apache Spark, Hadoop

### Package Managers

| Manager | Files |
|---------|-------|
| npm | `package.json`, `package-lock.json` |
| yarn | `yarn.lock` |
| pnpm | `pnpm-lock.yaml` |
| bun | `bun.lockb` |
| pip | `requirements.txt`, `Pipfile` |
| Poetry | `poetry.lock` |
| Cargo | `Cargo.toml`, `Cargo.lock` |
| Go | `go.mod`, `go.sum` |
| Maven | `pom.xml` |
| Gradle | `build.gradle`, `build.gradle.kts` |
| Bundler | `Gemfile`, `Gemfile.lock` |
| Composer | `composer.json`, `composer.lock` |
| NuGet | `packages.config`, `*.csproj` |
| CocoaPods | `Podfile`, `Podfile.lock` |
| Swift Package Manager | `Package.swift` |

### Databases

| Database | Detection |
|----------|-----------|
| PostgreSQL | Config files |
| MySQL | Config files |
| MongoDB | Config files |
| Redis | Config files |
| SQLite | File patterns |
| Oracle | Config files |
| SQL Server | Config files |
| Cassandra | Config files |
| Neo4j | Config files |
| InfluxDB | Config files |

### Containers

| Tool | Detection |
|------|-----------|
| Docker | `Dockerfile`, `docker-compose.yml` |
| Kubernetes | `*.yaml`, `*.yml` |
| Helm | `Chart.yaml` |
| Terraform | `*.tf` |
| Vagrant | `Vagrantfile` |
| Podman | `Containerfile` |

---

## 📋 Output Formats

### JSON Output

```json
{
  "project": {
    "name": "my-project",
    "path": "/path/to/project",
    "scannedAt": "2024-01-15T10:30:00Z"
  },
  "languages": [
    { "name": "TypeScript", "percentage": 85, "files": 120 },
    { "name": "HTML", "percentage": 10, "files": 15 },
    { "name": "CSS", "percentage": 5, "files": 8 }
  ],
  "frameworks": [
    { "name": "React", "version": "18.2.0" },
    { "name": "Next.js", "version": "13.4.0" }
  ],
  "dependencies": [
    { "name": "react", "version": "18.2.0", "type": "production" },
    { "name": "typescript", "version": "5.1.0", "type": "development" }
  ],
  "tools": [
    { "name": "Git", "detected": true },
    { "name": "ESLint", "detected": true },
    { "name": "Prettier", "detected": true }
  ],
  "summary": {
    "totalFiles": 143,
    "totalDependencies": 45,
    "totalLanguages": 3,
    "totalFrameworks": 2
  }
}
```

### Markdown Output

```markdown
# TechStack Report: my-project

## Languages
| Language | Percentage | Files |
|----------|------------|-------|
| TypeScript | 85% | 120 |
| HTML | 10% | 15 |
| CSS | 5% | 8 |

## Frameworks
- **React** 18.2.0
- **Next.js** 13.4.0

## Dependencies

### Production
- react@18.2.0
- next@13.4.0

### Development
- typescript@5.1.0
- eslint@8.45.0
- prettier@3.0.0
```

---

## 🔧 API Reference

### Classes

| Class | Description |
|-------|-------------|
| `TechStack` | Main entry point |
| `ProjectAnalyzer` | Analyzes projects |
| `LanguageDetector` | Detects languages |
| `FrameworkDetector` | Detects frameworks |
| `DependencyResolver` | Resolves dependencies |
| `ToolDetector` | Detects tools |
| `DatabaseDetector` | Detects databases |
| `ContainerDetector` | Detects containers |
| `DependencyGraph` | Generates graphs |
| `ReportGenerator` | Creates reports |

### Methods

```typescript
// TechStack
const techstack = new TechStack(config);
const result = await techstack.analyze(path);

// ProjectAnalyzer
const analyzer = new ProjectAnalyzer(options);
const result = await analyzer.analyze(path);
const result = await analyzer.analyzeMultiple(paths);

// Detection Results
result.languages;       // Language[]
result.frameworks;      // Framework[]
result.dependencies;    // Dependency[]
result.tools;           // Tool[]
result.databases;        // Database[]
result.containers;      // Container[]

// Export
await result.export(format, outputPath);
const json = result.toJSON();
const markdown = result.toMarkdown();
const html = result.toHTML();
```

---

## 🐛 Troubleshooting

### Common Issues

#### Issue: Scan Takes Too Long

**Solution:**
1. Increase workers
2. Exclude unnecessary directories
3. Reduce depth

```bash
techstack scan --exclude "node_modules,dist,build" --depth 3 --workers 8
```

#### Issue: Missing Dependencies

**Solution:**
1. Ensure package files are in project root
2. Check for nested monorepos
3. Verify file permissions

#### Issue: Incorrect Language Detection

**Solution:**
1. Check file extensions
2. Verify shebang lines
3. Review custom rules

---

## 🤝 Contributing

Contributions welcome! See CONTRIBUTING.md for guidelines.

### Development Setup

```bash
git clone https://github.com/moggan1337/techstack.git
cd techstack
npm install
npm run build
npm test
```

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file.

---

**Built with ❤️ by [moggan1337](https://github.com/moggan1337)**
