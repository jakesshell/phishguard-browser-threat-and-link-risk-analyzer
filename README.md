# PhishGuard Browser Threat & Link Risk Analyzer

PhishGuard is a defensive Chrome and Edge browser extension that automatically scans webpages for phishing risk, shows browser warning banners, scores suspicious URLs, and gives users a clear risk report.

It was upgraded from the original `Browser-Phishing-Risk-Analyzer` into a polished browser security portfolio project with automatic page scanning, a custom neon shield icon, explainable risk findings, scan history, JSON report export, and Manifest V3 extension support.

## Project Preview

<p>
  <img src="screenshots/auto-warning-banner.png" alt="PhishGuard automatic high-risk warning banner" width="100%">
</p>

## Overview

PhishGuard is designed to feel like a lightweight browser security tool for students, staff, teachers, and support teams.

When a webpage loads, PhishGuard checks the URL and visible page signals in the background. If the page looks suspicious, it can show a warning banner directly on the page. The user can then click the PhishGuard extension icon to view the full risk report.

## What It Does

PhishGuard can:

- Automatically scan the current webpage
- Show a warning banner on risky pages
- Change the browser extension badge based on risk level
- Scan the current tab manually
- Scan a pasted URL manually
- Score phishing risk from 0 to 100
- Explain why a URL looks suspicious
- Review basic page signals like forms, password fields, and login wording
- Save recent scan history
- Export a JSON risk report
- Support classroom-safe phishing awareness demonstrations

## Automatic Protection Behavior

PhishGuard runs automatically when a page loads.

Automatic behavior includes:

- Current-page URL analysis
- Page signal collection
- Extension badge status
- Green `OK` badge for low-risk pages
- Yellow `!` badge for watch-level pages
- Red `!!` badge for high-risk pages
- On-page warning banner for watch-level and high-risk pages
- Full report available by clicking the extension icon

The popup remains the detailed review panel. The banner gives the user an immediate warning without requiring them to manually open the extension first.

## Install / Load The Extension Locally In Chrome

PhishGuard must be loaded into Chrome before it can scan pages.

This GitHub version is installed locally using Chrome Developer Mode. It is not installed from the Chrome Web Store yet.

1. Open Chrome.
2. Go to:

```text
chrome://extensions
```

3. Turn on **Developer mode** in the top-right corner.
4. Click **Load unpacked**.
5. Select this project folder:

```text
C:\github-audit\PhishGuard-Browser-Threat-And-Link-Risk-Analyzer
```

6. Pin the PhishGuard extension to your browser toolbar.
7. Open any webpage.
8. PhishGuard will automatically scan the page in the background.
9. If the page looks risky, PhishGuard can show a warning banner.
10. Click the PhishGuard icon to view the full risk report.
11. After changing code, return to `chrome://extensions` and click **Reload** on the PhishGuard extension.

## Install / Load The Extension Locally In Microsoft Edge

PhishGuard must also be loaded into Edge before it can scan pages.

1. Open Edge.
2. Go to:

```text
edge://extensions
```

3. Turn on **Developer mode**.
4. Click **Load unpacked**.
5. Select this project folder:

```text
C:\github-audit\PhishGuard-Browser-Threat-And-Link-Risk-Analyzer
```

6. Pin the PhishGuard extension to your browser toolbar.
7. Open any webpage.
8. PhishGuard will automatically scan the page in the background.
9. If the page looks risky, PhishGuard can show a warning banner.
10. Click the extension icon to view the full risk report.
11. After changing code, return to `edge://extensions` and click **Reload** on the PhishGuard extension.

## Manual URL Scan

You can also paste a URL directly into the extension popup and click **Scan**.

This is useful for:

- Classroom demonstrations
- Suspicious links copied from messages
- Links that do not load in the browser
- Explaining warning signs without visiting a real website

## Risk Signals Reviewed

PhishGuard reviews indicators such as:

- Non-HTTPS pages
- URL shorteners
- Raw IP address links
- Many subdomains
- Unusual top-level domains
- Long URLs
- Many query parameters
- Urgency wording
- Account or password wording
- Possible brand lookalikes
- Login form signals
- Password input fields
- External link count

## Safe Demo Boundary

PhishGuard is defensive and educational.

It is intended for:

- Browser security awareness
- Student ICT demonstrations
- Defensive URL review
- Portfolio demonstrations
- Helpdesk-style phishing triage examples

It should not be used to generate phishing links, bypass controls, or test systems without permission.

## Key Features

- Chrome/Edge Manifest V3 extension
- Automatic current-page scanning
- Current-tab URL scanning
- Manual URL scanner
- Phishing risk score
- Low Risk / Watch Closely / High Risk labels
- Explainable warning cards
- Extension badge risk status
- On-page warning banner for suspicious pages
- Page signal collection
- Password field and login-signal awareness
- Scan history
- Clear history control
- Export JSON report
- Student safety reminder
- Custom neon shield-and-hook browser icon
- CI validation for manifest and JavaScript files

## Browser Icon

PhishGuard uses a custom neon yellow shield-and-hook icon to make the extension easier to recognize in Chrome and Edge.

Icon files:

- `icons/icon-16.png`
- `icons/icon-32.png`
- `icons/icon-48.png`
- `icons/icon-128.png`

## Project Structure

| File / Folder | Purpose |
|---|---|
| `manifest.json` | Chrome/Edge extension configuration |
| `popup.html` | Extension popup UI |
| `popup.js` | Popup interaction, scan flow, history, and export |
| `riskEngine.js` | Defensive URL scoring logic |
| `content.js` | Page signal collector and warning banner injector |
| `background.js` | Extension lifecycle, badge state, and history clearing |
| `styles.css` | Popup styling |
| `icons/` | Browser extension icon assets |
| `screenshots/` | Portfolio screenshots |
| `.github/workflows/ci.yml` | Extension validation workflow |

## Local Validation

Run these checks before pushing changes:

```powershell
node --check ".\riskEngine.js"
node --check ".\popup.js"
node --check ".\background.js"
node --check ".\content.js"
node -e "JSON.parse(require('fs').readFileSync('manifest.json', 'utf8')); console.log('manifest ok')"
```

## Portfolio Positioning

PhishGuard demonstrates browser security awareness, explainable risk scoring, frontend security UX, extension development, and defensive phishing education.

It connects naturally to cloud/security support work because phishing is one of the most common entry points for account compromise, helpdesk escalation, and security awareness training.

## Final Project Name

PhishGuard Browser Threat & Link Risk Analyzer
