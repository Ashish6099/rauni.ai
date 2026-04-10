[README.md](https://github.com/user-attachments/files/26635263/README.md)[Uploading# Rauni.ai — Coming Soon

Live at: https://YOUR_USERNAME.github.io/YOUR_REPO_NAME

---

## 🔐 How secrets are protected

Real EmailJS keys are **never stored in this code**.
The file `rauni.html` contains safe placeholders like `__EMAILJS_PUBLIC_KEY__`.

GitHub Actions injects real values from **GitHub Secrets** at deploy time,
builds the final site, and serves it — the real keys only exist inside
GitHub's encrypted vault and briefly in memory during the build.

---

## ⚙️ First-time setup

### 1. Add secrets to GitHub

Repo → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**

| Secret Name | Where to find it |
|---|---|
| `EMAILJS_PUBLIC_KEY` | EmailJS → Account → Public Key |
| `EMAILJS_SERVICE_ID` | EmailJS → Email Services → your Service ID |
| `EMAILJS_TEMPLATE_USER` | EmailJS → Email Templates → subscriber template ID |
| `EMAILJS_TEMPLATE_ADMIN` | EmailJS → Email Templates → company template ID |

### 2. Enable GitHub Pages via GitHub Actions

Repo → **Settings** → **Pages** → under **Source** select **GitHub Actions**

### 3. Push to main

```bash
git add .
git commit -m "deploy"
git push origin main
```

Actions runs automatically → injects secrets → deploys live. ✅

### 4. Lock EmailJS to your domain

EmailJS → **Account** → **Security** → **Allowed origins**:
```
https://YOUR_USERNAME.github.io
```

---

## 📁 File structure

```
├── .github/
│   └── workflows/
│       └── deploy.yml   ← auto build + secret injection
├── rauni-ai.html           ← coming soon page (safe placeholders)
├── index.html           ← linktree page
├── .gitignore           ← blocks .env files
└── README.md
```
 README.md…]()

