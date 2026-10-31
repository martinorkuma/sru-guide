# SRU Soldier Guide

An unofficial, mobile-friendly resource guide for Army Reserve Soldiers
arriving at the Soldier Recovery Unit (SRU) at Fort Hood.

**Live site:** https://martinorkuma.github.io/sru-guide/

> **Disclaimer:** This is not an official Army, USARC, or SRU product.
> Official guidance and the Soldier's chain of command take precedence.

## Content rules

All content must follow these rules before it is pushed:

- Use official office phone numbers only. No personal cell numbers.
- Describe roles, not people. No names, rosters, or unit-internal details.
- No PII, and no forms or anything that collects user data.
- Link to official sources (TRICARE, IPPS-A, MyArmyBenefits) instead of copying policy text.
- No Army logos or insignia.
- Verify every phone number and address before publishing.

## Project structure

```
docs/                  # site pages (one .md file per page)
docs/assets/extra.css  # custom Army Reserve colors
zensical.toml          # site name, navigation, theme
requirements.txt       # pinned Zensical version
.github/workflows/     # automatic build and deploy to GitHub Pages
```

## Editing locally

Requires Python 3 and Bash.

```bash
git clone https://github.com/martinorkuma/sru-guide.git
cd sru-guide
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
zensical serve        # preview at http://localhost:8000
```

## Adding a page

1. Create `docs/<page-name>.md`.
2. Add it to `nav` in `zensical.toml`. Every entry ends with a comma.
3. Run `zensical build` and confirm there are no errors.
4. Commit and push to `main`. The site deploys automatically in about a minute.

## Deployment

Every push to `main` runs `.github/workflows/deploy.yml`, which builds the
site and publishes it to GitHub Pages. Check the **Actions** tab if a
change doesn't appear. A red run means the build failed, and the log
shows why.

## Maintenance

- Review one page per month and update its "Last reviewed" date.
- Before a PCS or ETS, transfer the repo or add a successor as a collaborator.

## Maintainer

SFC Martin Orkuma (WTSP Support Coordinator, SRU Fort Hood). Contact via email martin.t.orkuma.mil@army.mil
