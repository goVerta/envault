# envault

<div align="center">

### Encrypted secrets. Zero paranoia.

> 🚧 **Shipping soon** - Building in public

[![Go](https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat&logo=go&logoColor=white)](https://go.dev)
[![MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Alpha-orange?style=flat)](https://github.com/verta/envault)

</div>

---

## The Problem

Your `.env` file is a security nightmare. One accidental commit away from disaster.

Sharing secrets via Slack? Even worse.

## The Solution
```bash
envault init                           # Setup encrypted vault
envault set API_KEY sk_live_dangerous  # Encrypted instantly
envault push                           # Safe to commit
envault run -- npm start               # Just works
```

Git-safe encrypted environment variables. One command to sync with your team.

---

## Why

| Old Way | envault Way |
|---------|-------------|
| Copy `.env.example` | `envault init` |
| Slack secrets around | `git pull` |
| Pray you didn't commit | `git push` (encrypted) |
| Different `.env` files | One source of truth |
| Secrets in 5 places | One vault |

---

## Features

- **AES-256 encryption** - Industry standard
- **Git-friendly** - Encrypted vault, safe to commit
- **Multi-environment** - dev, staging, production
- **Zero dependencies** - Single 5MB binary
- **Team sync** - Git-based collaboration
- **Works everywhere** - Any language, any framework

---

## Quick Start
```bash
# Install (coming soon)
go install github.com/verta/envault@latest

# Setup in your project
cd your-project
envault init

# Add secrets
envault set DATABASE_URL postgres://prod.db/app
envault set STRIPE_KEY sk_live_xyz
envault set NODE_ENV production

# Generate .env for local dev
envault local

# Run with environment variables
envault run -- npm start
envault run --env staging -- npm test

# Sync with team
envault push  # Commit encrypted vault
envault pull  # Pull latest changes
```

---

## How It Works
```
1. Variables encrypted with AES-256-GCM
2. Vault committed to git (.envault/*.enc)
3. Team shares encryption key once (via 1Password, etc.)
4. Everyone syncs via normal git workflow
```

**Local-first.** Works offline. No servers. No accounts. No monthly fees.

---

## Roadmap
```
[████████░░░░░░] 50% to v0.1.0

✅  Encryption engine
✅  Core CLI structure  
🚧  Multi-environment
🚧  Git integration
📋  Team workflows
📋  CI/CD docs
```

**Want it now?** Star the repo. We'll notify you when v0.1 ships.

---

## Philosophy

**Secrets should be boring.** Set once, forget forever.

**Git is your sync layer.** No servers, no accounts, no BS.

**Local-first.** Works offline, always.

**Zero config.** Just works.

---

## FAQ

**Q: Why not just use git-crypt?**  
A: git-crypt encrypts entire files. envault gives you per-variable control, environments, and better DX.

**Q: What about 1Password/Doppler/Infisical?**  
A: Great tools, but they cost money and require servers. envault is free, offline, and git-based.

**Q: How do I share the encryption key?**  
A: Via 1Password, secure email, or in person. Key setup is one-time per developer.

**Q: Is this production ready?**  
A: Not yet. Soon. Star the repo for updates.

---

## Coming Soon

- `envault import` - Migrate from existing .env files
- `envault rotate` - Key rotation
- `envault audit` - Change history
- IDE plugins (VSCode, JetBrains)
- CI/CD integration guides

---

## Contributing

We're building in public. Jump in:
```bash
git clone https://github.com/verta/envault
cd envault
go run main.go
```

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## License

MIT © [Verta](https://github.com/goverta)

We build tools that don't waste your time.

---

<div align="center">

**Connect**  
[Instagram](https://instagram.com/go.verta) • [GitHub](https://github.com/goverta) • [Email](mailto:verta.connect@gmail.com)

<sub>Built with care by the Verta team</sub>

</div>
