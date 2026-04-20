# CLAUDE.md - Vihara Medical

You are my ruthless mentor. Don't sugarcoat anything. If my idea is weak, call it trash and tell me why.

## Project Overview

**Vihara Medical** is a hospital/medical practice management system. Built on Frappe Framework.

| Attribute | Value |
|-----------|-------|
| **App Name** | vihara_medical |
| **Platform Type** | Medical Practice Management |
| **Owner** | Brother-in-law |
| **IT Admin** | Rajesh |
| **Deadline** | TBD |
| **Staging** | TBD |

## Business Context

<!-- TODO: Add business context after requirements discussion -->

## Core DocTypes

<!-- TODO: Define DocTypes based on requirements -->

### Masters
| DocType | Purpose |
|---------|---------|
| `Vihara Settings` | Single DocType for app configuration |

### Patients
| DocType | Purpose |
|---------|---------|
| TBD | TBD |

### Appointments
| DocType | Purpose |
|---------|---------|
| TBD | TBD |

### Billing
| DocType | Purpose |
|---------|---------|
| TBD | TBD |

## Tech Stack

- **Backend**: Frappe Framework (Python)
- **Frontend**: Frappe UI + Custom web pages
- **Database**: MariaDB
- **Payments**: TBD

## Development Setup

### Prerequisites
- Frappe Bench installed
- Python 3.10+
- Node.js 18+
- MariaDB 10.6+

### Local Development
```bash
# Clone into bench apps folder
cd ~/frappe-bench/apps
git clone https://github.com/Simbotix/vihara_medical.git

# Install app
cd ~/frappe-bench
bench get-app vihara_medical
bench --site your-site.localhost install-app vihara_medical

# Start development
bench start
```

### Using Codespaces
1. Open repo in GitHub Codespaces
2. Devcontainer auto-configures Frappe environment
3. Run `bench start` to begin development

## Environment Variables

Copy `.env.example` to `.env` and configure:

```bash
# Site Configuration
SITE_NAME=vihara.localhost
ADMIN_PASSWORD=
```

## File Structure

```
vihara_medical/
├── vihara_medical/
│   ├── __init__.py
│   ├── hooks.py
│   ├── modules.txt
│   ├── patches.txt
│   ├── vihara_medical/                # Module folder
│   │   ├── doctype/
│   │   └── report/
│   ├── api/                           # Whitelisted APIs
│   │   └── __init__.py
│   ├── public/
│   │   ├── css/vihara_medical.css
│   │   └── js/vihara_medical.js
│   ├── templates/
│   │   ├── pages/
│   │   └── includes/
│   └── www/
├── requirements/                      # Requirements docs
│   └── REQUIREMENTS.md
├── .devcontainer/
├── .env.example
├── CLAUDE.md
├── LICENSE
├── pyproject.toml
├── README.md
├── requirements.txt
└── setup.py
```

## Coding Standards

1. **DocType naming**: Prefix with `Vihara ` (e.g., `Vihara Patient`)
2. **Field naming**: snake_case
3. **Python**: Follow Frappe conventions, use type hints
4. **JavaScript**: Use Frappe's JS patterns
5. **Tests**: Write tests for critical business logic

## Developer

- **Name**: Rajesh Medampudi
- **Email**: rajesh@simbotix.com
- **Company**: Simbotix (One Person Company)

## qq — Knowledge Base Search

All searchable knowledge (~47k vectors, 8 collections) lives in Qdrant on Cozystack. `qq` is the only CLI.

### Commands

```bash
qq "keyword phrase"                   # fast keyword search, ~0.5-7s
qq -c <collection> "term"             # scope to one collection
qq -k 10 "topic"                      # top 10 results (default 5)
qq -l                                 # list all collections + vector counts
qq --semantic "fuzzy question"        # semantic search via fastembed, ~1-2s
```

### Which collection to search

| Question about… | Collection | Example |
|-----------------|-----------|---------|
| Cozystack, K8s, deployment, DNS, Caddy, Hetzner, servers | `infrastructure` | `qq -c infrastructure "cozystack ingress"` |
| Architecture, playbooks, operations, how-tos | `docs` | `qq -c docs "backup procedure"` |
| AppZ / SystemZ / BotZ pricing, Founding Member bundles | `pricing` | `qq -c pricing "founding member"` |
| Business strategy, customers, product specs, websites, marketing | `simbotix` | `qq -c simbotix "target customer"` |
| Blog posts, social content, publishing pipeline, AWS consulting content | `personal-social` | `qq -c personal-social "bitcoin"` |
| Katena, GRK workspace, Frappe client deployments | `grk-infra` | `qq -c grk-infra "katena dns"` |
| Career pivot, job search, skills development | `career-transition` | `qq -c career-transition "interview"` |
| Main project CLAUDE.md business context | `deployment-server` | `qq -c deployment-server "focus"` |
| Unknown / cross-cutting | *no `-c`* | `qq "rajesh medampudi"` |

### Reindex from source (when docs change)

```bash
qdrant-sync                           # incremental, hash-based skip unchanged
qdrant-sync -c <name>                 # reindex one collection
qdrant-sync --full                    # delete + rebuild all
```

**Rule: Always `qq` first before grep/explore/Agent for knowledge-base lookups.**
