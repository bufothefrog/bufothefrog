IT systems engineer in the Los Angeles area, working on identity, endpoints, security and automation at a managed service provider, mostly for healthcare organizations.

#### Talks

- **Building with AI: A Developer's Approach for Non-Developers** (Sep 2026) - Git, testing, CI and deployment for people building software with AI. [Slides](https://claude.ai/artifact/5AhKvMy3YaY2sdyZKgudAS)
- **GenUI frameworks**, with a live demo (Aug 2026) - [Slides](https://docs.google.com/presentation/d/1Xsd678W7tFS6GpaNDXmD3CIdyCsXiH19_z19bV4201Q/view)
- **OpenClaw 101: Practical AI, Smarter Workflows, and Secure Setup** (Apr 2026) - running an open-source AI agent gateway, real workflows, and a least-privilege setup with an honest look at the risks. [Slides](https://docs.google.com/presentation/d/1Ui1Z-cc1liHRLHrVYAq5BrjnRuPb_b-ZswdCmv6NkeE/view)
- **Multi-agent AI coding workflows** (Oct 2025) - [repo](https://github.com/bufothefrog/multi-agent-coding)

#### Projects

- **[bufoindex.com](https://bufoindex.com)** ([source](https://github.com/bufothefrog/bufoindex)) - personal-finance calculators: a paycheck allocator, a Monte Carlo retirement model and a tax-aware portfolio rebalancer. Next.js, TypeScript, Vitest, CI on every push.
- **Homelab** (private repo) - Docker Compose stacks on a TrueNAS server, managed entirely from git:
  - **Deploys:** every commit runs CI (secrets check, Compose and Caddy validation, ShellCheck, OpenTofu validate). Only passing commits reach a `deploy` branch, which the server pulls on a schedule, redeploying just the changed stacks and rolling a stack back to its last good commit if it fails to come up.
  - **Secrets:** SOPS with age, encrypted in git and decrypted only at deploy time.
  - **DNS and TLS:** zones managed as code with OpenTofu (encrypted state); Caddy issues certificates over DNS-01.
  - **Access, updates, backups:** NetBird mesh VPN instead of open ports; Renovate with pinned image digests; rclone backups to cloud storage.
