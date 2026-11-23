# Contributing to CLIProxy Dashboard

First off, thank you for considering contributing to CLIProxy Dashboard! 🎉

## 📋 Table of Contents
- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Style Guidelines](#style-guidelines)
- [Commit Messages](#commit-messages)

## 📜 Code of Conduct

This project adheres to a Code of Conduct. By participating, you are expected to uphold this code. Please be respectful and constructive in all interactions.

## 🚀 Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/cliProxyAPI-Dashboard.git
   cd cliProxyAPI-Dashboard
   ```
3. **Add upstream remote**:
   ```bash
   git remote add upstream https://github.com/0xAstroAlpha/cliProxyAPI-Dashboard.git
   ```
4. **Create a branch** for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## 💡 How Can I Contribute?

### 🐛 Reporting Bugs
- Check if the bug has already been reported in [Issues](https://github.com/0xAstroAlpha/cliProxyAPI-Dashboard/issues)
- Use the bug report template
- Include as much detail as possible

### ✨ Suggesting Features
- Use the feature request template
- Explain the use case clearly
- Consider how others might use this feature

### 🔧 Pull Requests
1. Make sure your code follows our style guidelines
2. Update documentation if needed
3. Add tests for new functionality
4. Make sure all tests pass
5. Submit a PR using the template

## 🛠️ Development Setup

For a documentation-only task, use the [offline swarm-ready checks](SWARM_READY.md#offline-setup-and-verification); no server, browser session, or provider account is needed.

### Prerequisites
- Go version declared in [go.mod](go.mod) (1.24.0 for this source)
- The Dashboard frontend is tracked as [`static/management.html`](static/management.html); this checkout has no Node package manifest or install step for it.
- Docker (optional, for containerized testing)

### Running Locally
```bash
# Install dependencies
go mod download

# Copy example config
cp config.example.yaml config.yaml

# Run the server
go run cmd/server/main.go

# Access dashboard at http://localhost:8317/management.html
```

### Running Tests
```bash
go test ./...
```

## 🎨 Style Guidelines

### Go Code
- Follow standard Go formatting (`gofmt`)
- Use meaningful variable and function names
- Add comments for exported functions
- Keep functions focused and small

### HTML/CSS/JavaScript
- Use consistent indentation (2 spaces)
- Follow existing patterns in the codebase
- Keep JavaScript modular
- Use semantic HTML

## 📝 Commit Messages

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
type(scope): description

[optional body]
[optional footer]
```

### Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples:
```
feat(dashboard): add export accounts bundle feature
fix(auth): resolve token refresh race condition
docs(readme): update installation instructions
```

## 🙏 Thank You!

Your contributions make this project better for everyone. We appreciate your time and effort! ❤️

---

**Questions?** Feel free to open an issue or reach out on [Facebook](https://www.facebook.com/lehuyducanh/).
