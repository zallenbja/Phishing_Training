# Phishing Awareness Training

Interactive security awareness training for Bob Johnson Auto Group employees. Built and maintained by the IT Security team.

---

## Overview

This is a browser-based phishing awareness training module hosted on GitHub Pages. Employees are directed to the training link, complete 5 content modules, and must pass a 5-question quiz to finish. Results are automatically emailed to the IT security team via EmailJS.

**Live URL:** https://bjaitservicedesk.github.io/Phishing_Training/

---

## What the Training Covers

| Module | Topic |
|--------|-------|
| 1 | How to spot a phishing email — red flags and warning signs |
| 2 | Safe browsing and link inspection — how to read a URL |
| 3 | Real vs. fake email examples — phishing, legitimate, and CEO fraud (BEC) |
| 4 | What to do if you clicked or submitted credentials |
| 5 | Incident response and reporting procedures |

**Quiz:** 5 questions, must score 5/5 to pass. Up to 3 attempts allowed. Results (name, email, score, pass/fail, timestamp) are emailed to IT on completion.

---

## Tech Stack

- **HTML / CSS / JavaScript** — single self-contained file, no frameworks
- **EmailJS** — sends completion results to IT inbox via connected Outlook account, no backend required
- **GitHub Pages** — free static hosting, auto-deploys on push to `main`

---

## How to Access

Send employees this link:

```
https://bjaitservicedesk.github.io/Phishing_Training/
```

The training runs entirely in the browser. No login, no install, no account required.

---

## How to Update Content

1. Clone or download the repo
2. Open `index.html` in VS Code
3. Make your changes — module content is in the `SLIDES` array, quiz questions are in the `QUIZ` array near the top of the script
4. Test locally using VS Code Live Server (right-click `index.html` → Open with Live Server)
5. Upload the updated `index.html` to the repo on GitHub
6. GitHub Pages will automatically redeploy within ~60 seconds

### Key placeholders to keep up to date

| Placeholder | Location | Current value |
|-------------|----------|---------------|
| IT security email | Multiple places in HTML body | `it_servicedesk@bobjohnsonauto.com` |
| EmailJS public key | `CONFIG` block | Set |
| EmailJS service ID | `CONFIG` block | Set |
| EmailJS template ID | `CONFIG` block | Set |
| Admin email (results recipient) | `CONFIG` block | `zallen@bobjohnsonauto.com` |

---

## EmailJS Configuration

Completion emails are sent via EmailJS connected to an Outlook account. If the Outlook account password changes or the EmailJS connection breaks, submissions will fail silently with a "Failed to send" error on the training page.

To re-authenticate: [emailjs.com](https://emailjs.com) → Email Services → Phishing_Results → reconnect Outlook account.

---

## Files

```
/
├── index.html        # Full training — all content, quiz, and EmailJS logic
└── README.md         # This file
```

---

*Maintained by the IT Security team. For questions contact it_servicedesk@bobjohnsonauto.com*
