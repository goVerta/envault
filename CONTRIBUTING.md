# Contributing to envault

Thanks for your interest in making envault better! 🎉

---

## Getting Started

### Prerequisites

- Go 1.21 or higher
- Git
- A code editor

### Setup
```bash
# Clone the repo
git clone https://github.com/goverta/envault.git
cd envault

# Install dependencies
go mod download

# Run the project
go run main.go

# Run tests
go test ./...
```

---

## Project Structure
```
envault/
├── cmd/              # CLI commands
├── internal/         # Internal packages
│   ├── crypto/       # Encryption/decryption
│   ├── vault/        # Vault management
│   └── config/       # Configuration handling
├── pkg/              # Public packages
├── tests/            # Integration tests
└── main.go           # Entry point
```

---

## Development Guidelines

### Code Style

- Follow standard Go conventions
- Run `go fmt` before committing
- Use meaningful variable names
- Keep functions small and focused
- Write tests for new features

### Commit Messages

Use clear, descriptive commit messages:
```bash
# Good
git commit -m "Add multi-environment support"
git commit -m "Fix encryption key generation bug"

# Bad
git commit -m "stuff"
git commit -m "fixed it"
```

### Testing
```bash
# Run all tests
go test ./...

# Run with coverage
go test -cover ./...

# Run specific test
go test -run TestEncryption ./internal/crypto
```

Write tests for:
- New features
- Bug fixes
- Edge cases

---

## How to Contribute

### 1. Find Something to Work On

- Check [open issues](https://github.com/goverta/envault/issues)
- Look for `good first issue` labels
- Have an idea? Open an issue first to discuss

### 2. Fork & Create Branch
```bash
# Fork the repo on GitHub, then:
git clone https://github.com/YOUR_USERNAME/envault.git
cd envault
git checkout -b feature/your-feature-name
```

### 3. Make Your Changes

- Write clean, tested code
- Update documentation if needed
- Add tests for new functionality

### 4. Test Your Changes
```bash
# Run tests
go test ./...

# Build and test locally
go build -o envault
./envault init
./envault set TEST_KEY value
```

### 5. Submit Pull Request
```bash
git add .
git commit -m "Add your feature"
git push origin feature/your-feature-name
```

Then open a PR on GitHub with:
- Clear description of what you changed
- Why you made the change
- Any related issues (e.g., "Fixes #123")

---

## Pull Request Guidelines

### Before Submitting

- [ ] Code follows Go conventions
- [ ] Tests pass locally
- [ ] Added tests for new features
- [ ] Updated documentation
- [ ] No merge conflicts

### PR Description Template
```markdown
## What

Brief description of changes

## Why

Why this change is needed

## How

How you implemented it

## Testing

How you tested the changes

Fixes #(issue number)
```

---

## What to Contribute

### Good First Issues

- Documentation improvements
- Bug fixes
- Test coverage
- Error message improvements
- CLI help text

### Feature Ideas

- Import from existing .env files
- Key rotation
- Audit logging
- IDE plugins
- CI/CD integrations

### Not Sure?

Open an issue and ask! We're happy to help.

---

## Code of Conduct

**Be respectful. Be kind. Build cool stuff.**

- Be welcoming to newcomers
- Give constructive feedback
- Focus on what's best for the project
- Show empathy towards others

We don't tolerate harassment, trolling, or disrespectful behavior.

---

## Questions?

- Open an [issue](https://github.com/goverta/envault/issues)
- Email us at [verta.connect@gmail.com](mailto:verta.connect@gmail.com)
- DM us on [Instagram](https://instagram.com/go.verta)

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thanks for making envault better! 🚀**

<sub>Built with care by the goVerta team</sub>
