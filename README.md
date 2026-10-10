<div align="center">
  <img src="https://raw.githubusercontent.com/finderxpro/FinderX/main/assest/finderx-banner.png" alt="FinderX radar and network banner" width="100%" />
</div>

<h1 align="center">FinderX</h1>

<p align="center"><strong>Advanced Network Recon Suite for Termux</strong><br />Network scanning · CDN research · DNS · Subdomains · Ports</p>

<p align="center"><em>Built for Android users running Termux. Use only on systems and networks you own or are explicitly authorized to test.</em></p>

## App preview

<p align="center">
  <img src="https://raw.githubusercontent.com/finderxpro/FinderX/main/assest/Screenshot_2026_1010_103228.png" alt="FinderX main menu running in a Termux terminal" width="720" />
</p>

## About FinderX

FinderX is a Python-based terminal suite for Android and Termux. It brings network scanning, response analysis, CDN/provider research, DNS utilities, reverse lookups, port checks, and subdomain discovery into one interactive interface.

FinderX is intended for authorized testing and network research. Results can vary with the phone, mobile or Wi-Fi connection, target responses, and availability or rate limits of third-party data sources.

## Features

- **Network Scanner** — scan selected IPs or authorized network ranges and review live responses.
- **Import & Scan** — import target lists and choose which target types to scan.
- **Provider CIDR Tools** — browse and synchronize provider and CDN address ranges.
- **Response Analyzer** — inspect HTTP responses, redirects, and page details.
- **CDN & Reverse Lookup** — investigate content-delivery and reverse-IP information.
- **Port Scanner** — check selected ports on authorized targets.
- **DNS Utilities** — perform DNS lookups and use resolver and DNS archive tools.
- **Subdomain Finder** — discover subdomains through supported public sources.
- **History & Saved Scans** — review saved results and supported scan checkpoints.

## Install on Termux

Install the official Termux app, open it, connect to the internet, and paste this one-time command:

```bash
pkg update -y && pkg install -y python curl && curl -fL --retry 3 "https://raw.githubusercontent.com/finderxpro/FinderX/main/FinderX.py" -o "$HOME/FinderX.py" && python "$HOME/FinderX.py" --self-test && mkdir -p "$PREFIX/bin" && printf '%s\n' '#!/system/bin/sh' 'exec python "$HOME/FinderX/FinderX.py" "$@"' > "$PREFIX/bin/finderx" && chmod +x "$PREFIX/bin/finderx" && finderx
```

The first setup requires an internet connection. FinderX attempts to install its Python dependencies in a private virtual environment. The command runs the built-in self-test, creates the `finderx` shortcut, and starts the app.

### Start FinderX later

```bash
finderx
```

### Update FinderX

```bash
curl -fL --retry 3 "https://raw.githubusercontent.com/finderxpro/FinderX/main/FinderX.py" -o "$HOME/FinderX.py" && python "$HOME/FinderX.py" --self-test
```

After updating, start it again with `finderx`.

## Compatibility

- Designed for **Termux on Android**; it is not a Windows or desktop Linux release.
- Termux and Python 3.8 or later are required. First-time setup and dependency installation require internet access.
- Android battery and background-process management may interrupt long scans. Keep Termux open during long-running work and use supported save/resume features.
- Mobile-data changes, DNS behavior, remote timeouts, and provider rate limits can affect results.
- The distributed Python file is encoded/obfuscated to discourage casual reading. It is **not encrypted** and does not prevent determined reverse engineering.

## Responsible use

Scan only systems and networks that you own or are explicitly authorized to test. Do not scan third-party hosts or address ranges without permission. Follow applicable laws, provider terms, and your organization's rules. You are responsible for selecting targets and handling scan results safely.

## Project information

Suggested GitHub repository description:

> Termux-based network reconnaissance and CDN research toolkit for authorized testing.

Suggested topics: `termux`, `android`, `python`, `network-recon`, `dns`, `cdn`.

---

<p align="center"><sub>FinderX · Termux / Android · Authorized use only</sub></p>
