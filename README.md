# envault

<div align="center">

### Encrypted secrets. Zero paranoia. Maximum flow.

> 🚧 **Shipping soon** — built in public, fueled by caffeine & chaos

[![Go](https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat\&logo=go\&logoColor=white)](https://go.dev)
[![MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Alpha-orange?style=flat)](https://github.com/goverta/envault)

</div>

---

## The Problem

`.env` files age like milk.
One misplaced commit, one “quick push”, and you’ve accidentally speed-ran a security breach.

Sharing secrets on Slack? That’s basically leaving them on a public billboard.

---

## The Solution

```bash
envault init                           # Create secure vault
envault set API_KEY sk_live_dangerous  # Encrypt on the spot
envault push                           # Safe to commit
envault run -- npm start               # Auto-loads decrypted vars
```

Git-safe encrypted environment variables with zero drama.
One command and your whole team is synced.

---

## Why envault?

| The Old Way                    | The envault Way        |
| ------------------------------ | ---------------------- |
| Copy `.env.example`            | `envault init`         |
| Pass secrets in Slack          | `git pull`             |
| Pray you didn't commit secrets | `git push` (encrypted) |
| Different `.env` everywhere    | One vault, same truth  |
| Secrets scattered everywhere   | One secure home        |

---

## Features

* **AES-256-GCM encryption** — modern, rock-solid cryptography
* **Git-friendly** — commit the vault without a mini heart attack
* **Multi-environment** — dev, staging, prod
* **Zero dependencies** — a single tiny binary
* **Team sync** — works with your existing Git workflow
* **Works anywhere** — language-agnostic, framework-agnostic
* **Offline-first** — no servers, no logins, no monthly fees

---

## Quick Start

```bash
# Install (coming soon)
go install github.com/goverta/envault@latest

# Initialize a project
cd your-project
envault init

# Add secrets
envault set DATABASE_URL postgres://prod.db/app
envault set STRIPE_KEY sk_live_xyz
envault set NODE_ENV production

# Generate local .env
envault local

# Run your app with injected variables
envault run -- npm start
envault run --env staging -- npm test

# Sync with your team using git
envault push
envault pull
```

---

## How It Works

```
1. Secrets encrypted using AES-256-GCM
2. Encrypted vault stored in git under .envault/
3. Team shares one encryption key (once)
4. Everyone stays synced through normal git pushes/pulls
```

Local-first, minimalistic, developer-centric.
No dashboards. No vendor lock-in. No SaaS bills.

---

## Roadmap

```
[████████░░░░░░] 50% → v0.1.0

✔️  Encryption engine
✔️  Core CLI
🚧  Multi-environment support
🚧  Git integration
📋  Team workflows
📋  CI/CD usage docs
```

Want early access? Smash that ⭐ on the repo.

---

## Philosophy

Secrets should not be exciting.
They should sit quietly in a vault doing their job.

Git is the best sync system you already use — envault simply teaches it a new trick.

Everything local. Everything simple. Everything fast.

---

## FAQ

**Q: Why not git-crypt?**
A: git-crypt encrypts *files*. envault encrypts *variables*, handles environments, and delivers way better DX.

**Q: Why not 1Password/Doppler/Infisical?**
A: Amazing tools — but they require servers, accounts, and money. envault is free, offline, and built around Git.

**Q: How do I share the key?**
A: Pass it once through something secure (1Password, SMS over VPN, carrier pigeon—your call).

**Q: Production-ready?**
A: Not yet. Progress is rapid though. Follow the repo for updates.

---

## Coming Soon

* `envault import` — slurp existing `.env` files
* `envault rotate` — painless key rotation
* `envault audit` — change history
* VSCode / JetBrains extensions
* CI/CD guides for GitHub Actions, GitLab, Jenkins, etc.

---

## Contributing

Building in public → contributions welcome.

```bash
git clone https://github.com/goverta/envault
cd envault
go run main.go
```

Check out `CONTRIBUTING.md` for guidelines.

---

## License

MIT © [goVerta](https://github.com/goverta)

We build tools that stay out of your way and out of your nightmares.

---

<div align="center">

**Connect**
[Instagram](https://instagram.com/go.verta) • [GitHub](https://github.com/goverta) • [Email](mailto:verta.connect@gmail.com)

<sub>Crafted with care by the goVerta team</sub>

</div>
