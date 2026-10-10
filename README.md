<div align="center">
  <img src="assets/finderx-icon.png" alt="FinderX icon" width="112" />
  <h1>FinderX</h1>
  <p><strong>Advanced Network Recon &amp; CDN Hunter for Termux</strong></p>
  <p>Terminal-based network discovery and diagnostics for Android users.</p>
  <img src="assets/finderx-banner.png" alt="FinderX Theme" width="100%" />
</div>

<p align="center">
  <img src="https://github.com/finderxpro/FinderX/blob/main/assest/finderx-banner.png" alt="Platform: Termux and Android" />
  <img src="https://github.com/finderxpro/FinderX/blob/main/assest/finderx-icon.png" alt="Language: Python" />
  <img src="https://github.com/finderxpro/FinderX/blob/main/assest/finderx-terminal.png" alt="Authorized testing only" />
</p>

> **Authorization required:** Only scan systems and networks that you own or have explicit permission to test.

## App preview

The image below is a real FinderX terminal screenshot supplied by the project owner.

<p align="center">
  <img src="assets/finderx-terminal.png" alt="FinderX main menu running in a Termux-style terminal" width="720" />
</p>

## What is FinderX?

FinderX is a Python-based terminal toolkit designed to run in **Termux on Android**. It brings network scanning, response analysis, provider/CDN research, DNS utilities, reverse lookups, port checks, and subdomain discovery into one interactive interface.

FinderX is intended for authorized testing and network research. Results depend on the device, connection, target responses, and availability or limits of third-party data sources.

## Quick install — Termux

Install the official Termux app first. Open Termux, connect to the internet, then paste this one-time setup command:

```bash
pkg update -y && pkg install -y python curl && curl -fL --retry 3 "https://raw.githubusercontent.com/finderxpro/FinderX/main/FinderX.py" -o "$HOME/FinderX.py" && python "$HOME/FinderX.py" --self-test && mkdir -p "$PREFIX/bin" && printf '%s\n' '#!/system/bin/sh' 'exec python "$HOME/FinderX/FinderX.py" "$@"' > "$PREFIX/bin/finderx" && chmod +x "$PREFIX/bin/finderx" && finderx
```

The first run needs an internet connection. FinderX attempts to set up its required Python packages in a private virtual environment. The command runs the built-in self-test, creates the `finderx` shortcut, and starts the app.

### Launch FinderX later

```bash
finderx
```

### Update FinderX

```bash
curl -fL --retry 3 "https://raw.githubusercontent.com/finderxpro/FinderX/main/FinderX.py" -o "$HOME/FinderX.py" && python "$HOME/FinderX.py" --self-test
```

After updating, launch it with `finderx`.

## Features

- **Network Scanner** — scan selected IPs or authorized network ranges and review live responses.
- **Provider CIDR Tools** — browse and synchronize provider/CDN range data.
- **Response Analyzer** — inspect HTTP responses, redirects, and page details.
- **CDN & Reverse Lookup Tools** — investigate CDN/content-delivery and reverse-IP information.
- **Port Scanner** — check selected ports on authorized targets.
- **DNS Tools** — DNS lookup, resolver utilities, and DNS archive features.
- **Subdomain Finder** — discover subdomains through supported public sources.
- **Import & Scan** — import supported lists and select the target types to scan.
- **History & Saved Scans** — revisit saved results and continue supported scan workflows.

Some data sources may rate-limit requests or change availability. A result is an aid to investigation, not a guarantee that a host, provider, or service is present or absent.

## Screenshots

- `assets/finderx-terminal.png` — real FinderX main-menu screenshot.
- `assets/finderx-banner.png` — original README brand illustration.
- `assets/finderx-icon.png` — FinderX radar/network icon.

To add more real screenshots, place them in `assets/` and reference them in Markdown, for example:

```markdown
![Live scan dashboard](assets/finderx-scan.png)
```

Use screenshots with sample or non-sensitive targets. Hide private addresses, customer data, API tokens, and other sensitive details before publishing.

## Compatibility notes

- FinderX is intended for **Termux on Android**, not Windows or desktop Linux.
- Termux and Python must be installed. The first setup and dependency installation need internet access.
- Android may stop or restrict long-running background processes. Keep the app in the foreground for long scans and use FinderX's supported save/resume options.
- Network changes, DNS behavior, mobile-data conditions, remote timeouts, and provider rate limits can affect results.
- The distributed Python file is encoded/obfuscated to discourage casual reading. It is **not encrypted** and does not prevent determined reverse engineering.

## Responsible use

Use FinderX only on your own systems or within a clearly authorized assessment scope. Do not use it to scan third-party networks, services, or address ranges without permission. Follow applicable laws, provider terms, and your organization's rules. You are responsible for selecting targets and handling scan results safely.

## About this repository

Suggested GitHub **About** description:

> Termux-based network reconnaissance and CDN research toolkit for authorized testing.

Suggested repository topics: `termux`, `android`, `python`, `network-recon`, `dns`, `cdn`.

---

<p align="center"><sub>FinderX · Termux / Android · Use responsibly and only with authorization.</sub></p>
