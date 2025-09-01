# 🚀 Vibe Chatmodes - Clean Code Detectors for GitHub Copilot

> Transform your vibe-coded chaos into clean, maintainable code with laser-focused GitHub Copilot chatmodes

## 🎯 What is this?

A collection of specialized GitHub Copilot chatmodes designed to detect and fix common "vibe coding" issues. Each chatmode is focused on a single problem, providing precise detection and ready-to-implement fixes.

### The Problem with Vibe Coding

When developers use AI to generate code quickly without understanding it deeply, several anti-patterns emerge:
- 📋 **Copy-paste everywhere** - Same logic duplicated across files
- 🏔️ **Callback hell** - Deep nesting and pyramid of doom
- 🗑️ **Dead code graveyards** - Commented out code from ancient times
- 🎲 **Error handling roulette** - Empty catch blocks, swallowed errors
- 🔢 **Magic numbers** - `if (count > 17)` with no explanation
- 🍝 **Import spaghetti** - Circular dependencies and tangled imports
- 🎭 **Inconsistent patterns** - Mix of callbacks, promises, and async/await
- ❓ **Mystery names** - Variables named `data`, `temp`, `stuff`

## 📦 Available Chatmodes

| Chatmode | Description | Severity Levels |
|----------|-------------|-----------------|
| `detector-dead-code` | Finds commented blocks, unreachable code, unused exports | Critical/High/Medium |
| `detector-deep-callback` | Detects callback hell and deep nesting patterns | Critical/High/Medium |
| `detector-duplications` | Identifies copy-paste code and semantic duplicates | Critical/High/Medium |
| `detector-error-handling` | Exposes empty catches and missing error handling | Critical/High/Medium |
| `detector-hard-coded-values` | Finds magic numbers and hardcoded strings | Critical/High/Medium |
| `detector-import-spaghetti` | Detects circular dependencies and import chaos | Critical/High/Medium |
| `detector-inconsistent-patterns` | Finds mixed coding patterns and styles | Critical/High/Medium |
| `detector-variable-names` | Identifies generic and meaningless variable names | Critical/High/Medium |

## 🚀 Installation

### Option 1: VS Code (Recommended)
1. Clone this repository or download the chatmodes
2. Copy the desired `.chatmode.md` files to your workspace's `.github/chatmodes` directory
3. In VS Code, open the Chat view and select your chatmode from the dropdown

### Option 2: User Profile
Store chatmodes in your VS Code user profile for use across all projects:
1. Open VS Code Command Palette (`Cmd/Ctrl + Shift + P`)
2. Run "Chat: Configure Chat Modes..."
3. Copy the chatmode content into a new file

## 📖 Usage

### Basic Usage
1. Select a detector chatmode from the dropdown in GitHub Copilot Chat
2. Ask it to analyze your codebase:
   ```
   Analyze this codebase for issues
   ```
3. Review the detailed findings with severity levels
4. Copy the provided fixes directly into your code

### Example Workflow

```bash
# 1. Select "detector-duplications" chatmode
# 2. In chat: "Find duplicate code in my services folder"
# 3. Copilot responds with:

ISSUE FOUND: Exact Duplicate
Severity: HIGH
Locations: 
  - userService.js:10-25 (16 lines)
  - productService.js:40-55 (16 lines)
Impact: 32 lines redundant

FIXED CODE:
[Ready-to-use refactored code]

IMPLEMENTATION:
1. Create shared utility function
2. Update imports in affected files
3. Remove duplicated code
4. Run tests
```

## 🎯 Features

### For Each Detection:
- **Exact Location**: `file.js:line-range`
- **Severity Classification**: Critical/High/Medium
- **Working Fix Code**: Ready to copy-paste
- **Implementation Steps**: Numbered, clear instructions
- **Metrics**: Lines saved, complexity reduction
- **Benefits**: Quantified improvements

### Smart Detection:
- Complete codebase coverage tracking
- Context-aware analysis
- Business logic understanding
- Safe removal procedures
- Verification steps included

## 🔧 Creating Custom Chatmodes

Each chatmode follows this structure:

```markdown
---
description: 'Brief description of what this detector finds'
tools: ['search', 'codebase', 'filesystem', 'usages']
---

# Chatmode Title

You are a [specialist type] who detects [problem]...

## Mission
[Clear mission statement]

## Detection Rules
- **MUST show exact location** (file:line)
- **MUST provide working fix code**
- [Additional rules...]

[Rest of chatmode content...]
```

**Remember**: Good code is not about writing fast, it's about writing code that lasts 🎯

Created by [Tomer Shahar](https://github.com/tomer-shahar)
