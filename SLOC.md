# Source Lines of Code (SLOC) Statistics

This document provides statistics on the source lines of code (SLOC) for the clice project.

**Last Updated:** 2026-02-14

## Overall Summary

Total project statistics (excluding build artifacts, dependencies, and generated files):

| Metric | Count |
|--------|-------|
| **Total Files** | 265 |
| **Total Code Lines** | 32,754 |
| **Blank Lines** | 8,441 |
| **Comment Lines** | 4,121 |
| **Total Lines** | 45,316 |

## By Language

| Language | Files | Blank | Comment | Code | % of Code |
|----------|-------|-------|---------|------|-----------|
| C++ | 96 | 4,066 | 2,500 | 17,707 | 54.1% |
| C/C++ Header | 109 | 2,298 | 1,431 | 6,203 | 18.9% |
| YAML | 15 | 1,541 | 12 | 5,239 | 16.0% |
| Python | 9 | 201 | 15 | 1,323 | 4.0% |
| TypeScript | 9 | 89 | 14 | 523 | 1.6% |
| Pascal | 1 | 2 | 2 | 438 | 1.3% |
| Lua | 3 | 63 | 11 | 386 | 1.2% |
| CMake | 4 | 66 | 12 | 374 | 1.1% |
| TOML | 8 | 38 | 54 | 225 | 0.7% |
| Flatbuffers | 1 | 22 | 0 | 81 | 0.2% |
| Bourne Shell | 3 | 12 | 3 | 59 | 0.2% |
| CSS | 1 | 17 | 55 | 58 | 0.2% |
| JavaScript | 2 | 6 | 7 | 40 | 0.1% |
| Rust | 1 | 6 | 1 | 37 | 0.1% |
| PowerShell | 1 | 6 | 0 | 33 | 0.1% |
| Bourne Again Shell | 1 | 8 | 4 | 25 | 0.1% |
| DOS Batch | 1 | 0 | 0 | 3 | 0.0% |
| **Total** | **265** | **8,441** | **4,121** | **32,754** | **100%** |

## By Component

### Main Source Code (`src/`)

| Language | Files | Blank | Comment | Code |
|----------|-------|-------|---------|------|
| C++ | 48 | 2,370 | 1,663 | 10,828 |
| Pascal | 1 | 2 | 2 | 438 |
| C/C++ Header | 3 | 92 | 36 | 213 |
| **Total** | **52** | **2,464** | **1,701** | **11,479** |

### Headers (`include/`)

| Language | Files | Blank | Comment | Code |
|----------|-------|-------|---------|------|
| C/C++ Header | 105 | 2,203 | 1,393 | 5,984 |
| Flatbuffers | 1 | 22 | 0 | 81 |
| **Total** | **106** | **2,225** | **1,393** | **6,065** |

### Tests (`tests/`)

| Language | Files | Blank | Comment | Code |
|----------|-------|-------|---------|------|
| C++ | 47 | 1,682 | 828 | 6,840 |
| Python | 5 | 78 | 1 | 385 |
| TOML | 2 | 3 | 2 | 14 |
| **Total** | **54** | **1,763** | **831** | **7,239** |

### Editor Extensions (`editors/`)

| Language | Files | Blank | Comment | Code |
|----------|-------|-------|---------|------|
| YAML | 1 | 1,081 | 0 | 3,292 |
| TypeScript | 6 | 81 | 7 | 438 |
| JavaScript | 2 | 6 | 7 | 40 |
| Rust | 1 | 6 | 1 | 37 |
| TOML | 3 | 3 | 0 | 27 |
| Lua | 2 | 6 | 3 | 26 |
| **Total** | **15** | **1,183** | **18** | **3,860** |

## Key Insights

- **Core C++ Implementation**: The project consists of approximately 17,707 lines of C++ source code and 6,203 lines of C++ headers, totaling **23,910 lines** of C++ code (73% of the codebase).

- **Test Coverage**: The test suite contains 7,239 lines of code (22% of the total), primarily in C++ (6,840 lines) with Python test infrastructure (385 lines).

- **Editor Support**: Multi-editor support is provided through 3,860 lines of code across VSCode (TypeScript), Zed (YAML), and Neovim (Lua) extensions.

- **Build System**: The project uses CMake (374 lines) for its build system.

- **Documentation**: Comprehensive bilingual documentation (English/Chinese) is maintained using VitePress.

- **Code Quality**: The codebase maintains a healthy comment-to-code ratio of approximately 12.6% (4,121 comments for 32,754 lines of code).

## How These Statistics Were Generated

These statistics were generated using [cloc](https://github.com/AlDanial/cloc) (Count Lines of Code) version 1.98:

```bash
cloc . --exclude-dir=build,node_modules,.git,.vscode,dist,out,third_party --exclude-ext=json,lock,md
```

To regenerate these statistics:

1. Install cloc:
   ```bash
   # Ubuntu/Debian
   sudo apt-get install cloc
   
   # macOS
   brew install cloc
   
   # Other systems: see https://github.com/AlDanial/cloc
   ```

2. Run from the project root:
   ```bash
   cloc . --exclude-dir=build,node_modules,.git,.vscode,dist,out,third_party --exclude-ext=json,lock,md
   ```

## Notes

- Build artifacts, dependencies (node_modules), and generated files are excluded from the count
- JSON, lock files, and markdown documentation are excluded to focus on source code
- The YAML count is high due to the Zed editor extension configuration
