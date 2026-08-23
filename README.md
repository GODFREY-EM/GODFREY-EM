# Godfrey E.M

> Systems engineer from Tanzania 🇹🇿 · Laravel devotee · I design, build, deploy **and operate** what I ship — on infrastructure I run myself.

I build systems worth talking about: multi-tenant platforms, payment rails, e-commerce at scale. Not tutorials, not clones-for-practice — software with paying users and real consequences, deployed to my own VPS, backed up on my terms, monitored while I sleep.

**Why:** technology adoption here doesn't stall because of frameworks — it stalls because nobody ships the boring operational half. My work is an argument that world-class systems can be built, hosted, and hardened *from* Tanzania, *for* Tanzania and the rest of Africa.

---

## In Production

| System | What it is | Where |
|---|---|---|
| [**Nazareth**](https://github.com/GODFREY-EM/nazareth) | Multi-tenant property-management SaaS — leases with two-party e-signature, rent invoicing, tenant portal, public listings. Tenancy isolation enforced in `LandlordScope`, which fails closed. Rent moves through Snippe straight to landlords; the platform never holds tenant money. | prod + staging |
| [**Parcelflow**](https://github.com/GODFREY-EM/parcelflow) | Logistics & parcel-tracking platform — multi-panel operations dashboard on **Laravel + Filament v5 + Livewire 4**, plus its marketing site | prod |
| [**Spectral-Store**](https://github.com/GODFREY-EM/Spectral-Store) | Bagisto-based storefront serving real customers — custom Tanzanian payment integrations, zero-downtime release pipeline (`releases/` + rollback), running current upstream v2.4.x | prod |
| Private client builds | Farm management & other commissioned systems | prod |

## How It Runs — the Half Most Repos Skip

One VPS, five systems, no hand-waving:

- **Staging → production** separation with per-app deploy scripts and atomic release directories
- **Push-to-deploy** via bare git remotes; rollbacks are a symlink flip, rehearsed before they're needed
- **Nightly database backups kept outside the app's scheduler** — if the application is broken, that is exactly when the backup must still run (14-day retention, restore-tested)
- Scheduled **health digests**: cron-driven checks shell out to composer/artisan and report drift before users do
- Least-privilege user accounts, SSH-key-only access, firewall discipline

## Security Engineering

Security isn't a checklist item — it shapes the architecture:

- [`security-advisories`](https://github.com/GODFREY-EM/security-advisories) — tracking PHP package vulnerabilities
- [`AIFD`](https://github.com/GODFREY-EM/AIFD) — AI-assisted fraud detection
- [`SECURE-CODING`](https://github.com/GODFREY-EM/SECURE-CODING) — secure development reference
- Patterns I practice: authorization that **fails closed**, thin admin panels that can see metadata but never tenant records, approval-gated onboarding, optional-but-first-class 2FA

## East African Payment Rails

Integrating what local businesses actually transact with:

[**M-Pesa**](https://github.com/GODFREY-EM/mpesa-payment-gateway) · [**ClickPesa**](https://github.com/GODFREY-EM/bagisto-clickpesa-payment-gateway) · [**AzamPay**](https://github.com/GODFREY-EM/azampay-payment-gateway) · **Snippe** — webhook verification, idempotency, reconciliation built in.

## Open Source

- **Swahili localization for [Bagisto](https://github.com/bagisto/bagisto)** — full framework translation (~9,800 lines across 19 files), upstreamed via [PR #11439](https://github.com/bagisto/bagisto/pull/11439); Kiswahili speakers deserve first-class software
- [`kill-ai-slop`](https://github.com/GODFREY-EM/kill-ai-slop) — an agent skill + field guide for stripping machine-generated visual tics from products

---

![PHP](https://img.shields.io/badge/PHP-8.3%2B-777BB4?logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-11%E2%86%9213-FF2D20?logo=laravel&logoColor=white)
![Filament](https://img.shields.io/badge/Filament-v5-F97316)
![Livewire](https://img.shields.io/badge/Livewire-4-FB50A0?logo=livewire&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-3%2F4-06B6D4?logo=tailwindcss&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-VPS-A81D33?logo=debian&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=GODFREY-EM&show_icons=true&theme=default&hide_border=true&count_private=true" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=GODFREY-EM&layout=compact&hide_border=true&langs_count=6" height="150" />
</p>

📫 **godfreymapunda112@gmail.com** — open to building systems worth talking about, security reviews, and payment-integration work across Africa.
