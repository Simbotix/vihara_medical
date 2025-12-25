# Vihara Medical

Hospital and medical practice management system. Built on [Frappe Framework](https://frappeframework.com).

## Features

<!-- TODO: Add features based on requirements -->

- **Patient Management**: TBD
- **Appointments**: TBD
- **Billing**: TBD

## Quick Start

### Using GitHub Codespaces (Recommended)

1. Click **Code** → **Codespaces** → **Create codespace on main**
2. Wait for the container to build (~5 minutes first time)
3. Run `bench start` in the terminal
4. Open `http://localhost:8000` in browser
5. Login: `Administrator` / `admin`

### Local Development

```bash
# Prerequisites: Frappe Bench installed
cd ~/frappe-bench/apps
git clone https://github.com/Simbotix/vihara_medical.git

cd ~/frappe-bench
bench get-app vihara_medical
bench new-site vihara.localhost
bench --site vihara.localhost install-app vihara_medical
bench --site vihara.localhost set-config developer_mode 1
bench use vihara.localhost
bench start
```

## Configuration

Copy `.env.example` to `.env` and configure:

```bash
cp .env.example .env
```

## Documentation

- [CLAUDE.md](./CLAUDE.md) - Development guidelines and project context
- [requirements/](./requirements/) - Business requirements and discussions
- [Frappe Framework Docs](https://frappeframework.com/docs)

## License

MIT License - see [LICENSE](./LICENSE)

## Author

Rajesh Medampudi ([@medampudi](https://github.com/medampudi))
Simbotix - [simbotix.com](https://simbotix.com)
