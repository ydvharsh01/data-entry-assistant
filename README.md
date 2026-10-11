# 🗂️ Data Entry Assistant

**A free, browser-based tool to import, clean, validate, deduplicate and verify data entries. No signup, no server, no installation.**

[![Deploy to GitHub Pages](https://github.com/ydvharsh01/data-entry-assistant/actions/workflows/deploy.yml/badge.svg)](https://github.com/ydvharsh01/data-entry-assistant/actions/workflows/deploy.yml)
![Single file](https://img.shields.io/badge/app-single%20HTML%20file-0E8C88)
![No dependencies](https://img.shields.io/badge/dependencies-none-1E8A4C)
![License](https://img.shields.io/badge/license-MIT-blue)

### 🔗 [**Live Demo → ydvharsh01.github.io/data-entry-assistant**](https://ydvharsh01.github.io/data-entry-assistant/)

---

## 📌 What is this?

Data entry work usually means messy spreadsheets: extra spaces, wrong capitalization, broken phone numbers, invalid emails, duplicate rows, and no easy way to double-check everything.

**Data Entry Assistant** puts the whole workflow in one page: import your data, clean it with one click, validate it with rules, remove duplicates, verify record by record, and export the result.

> 🔒 **Privacy first:** everything runs inside your browser. Your data is stored only in your own browser (`localStorage`). **Nothing is uploaded to any server.**

---

## ✨ Features

| Module | What it does |
|---|---|
| 🏠 **Dashboard** | Overview of your dataset and progress, with Start / Pause / Resume / Stop session controls |
| 📥 **Import** | Import `.csv`, `.json`, `.txt`, or paste tabular / unstructured text (e.g. `Name: Rahul Sharma`) |
| 🗂️ **Data Table** | View and edit all records, with Undo support |
| 🧹 **Clean** | One-click cleaning: trim spaces, normalize name capitalization, standardize dates (YYYY-MM-DD) and numbers, flag invalid phones/emails, flag suspicious characters, detect empty cells. Ambiguous values are **never** changed automatically |
| ✅ **Validate** | Set a rule per column, with custom regex support |
| 🧩 **Duplicates** | Detect duplicates by entire row or by specific column(s), grouped for review |
| 🔍 **Verify** | Side-by-side view of source data vs entered data. Accept, Reject, Edit, or Mark Verified |
| ⌨️ **Fast Entry** | Keyboard-first form for quick data entry with auto-save |
| 🚨 **Error Center** | All problem records in one place |
| 📤 **Export** | CSV / JSON export for full, cleaned, verified, error and duplicate records, plus full project backup and restore |
| 🗒️ **Activity Log** | Track every action taken |
| 🌙 **Dark mode** | Easy on the eyes for long sessions |

### ⌨️ Keyboard shortcuts (Verify mode)

| Key | Action |
|---|---|
| `Enter` | Next record |
| `Ctrl + Enter` | Verify / accept |
| `Ctrl + Z` | Undo |
| `Esc` | Cancel edit |
| `← / →` | Previous / next record |

---

## 🚀 How to use

1. Open the **[live demo](https://ydvharsh01.github.io/data-entry-assistant/)**.
2. Click **Load Demo Data** on the dashboard to try it instantly, or go to **Import** to bring your own data.
3. Run **Clean** → **Validate** → **Duplicates**.
4. Go through records in **Verify**.
5. **Export** your final data as CSV or JSON.

### Run locally

No build step, no install:

```bash
git clone https://github.com/ydvharsh01/data-entry-assistant.git
cd data-entry-assistant
# just open index.html in any browser
xdg-open index.html     # Linux
# or: open index.html   (macOS) / start index.html (Windows)
```

---

## ⚙️ DevOps: how this project is deployed

This project uses a **CI/CD pipeline** so every change goes live automatically.

```
git push → GitHub Actions → GitHub Pages → live site
```

- **Source control:** Git + GitHub
- **CI/CD:** GitHub Actions workflow ([`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)) triggers on every push to `main`
- **Hosting:** GitHub Pages (static hosting, free)
- **SEO:** meta description, canonical URL, Open Graph tags, `robots.txt`, `sitemap.xml`, and Google Search Console verification

Workflow steps: `checkout` → `configure-pages` → `upload-pages-artifact` → `deploy-pages`.

### Project structure

```
data-entry-assistant/
├── .github/workflows/deploy.yml   # CI/CD pipeline
├── index.html                     # the entire app (HTML + CSS + JS)
├── robots.txt                     # crawler rules
├── sitemap.xml                    # sitemap for search engines
└── README.md
```

---

## 🛠️ Tech stack

- **HTML5, CSS3, vanilla JavaScript** (no frameworks, no libraries, no CDN)
- **localStorage** for client-side persistence
- **Git, GitHub Actions, GitHub Pages** for version control and deployment

---

## ⚠️ Known limitations

- **`.xlsx` import/export is not supported.** Parsing Excel files needs a bundled library, which would break the "single offline file, no dependencies" design. Workaround: save your Excel file as **CSV** and import that. CSV opens directly in Excel and Google Sheets.
- Data lives in your browser's `localStorage`. Clearing browser data or switching browsers/devices will remove it, so use **Export → Create Backup (.json)** regularly.
- Very large datasets (tens of thousands of rows) may feel slow, since everything runs in the browser.

---

## 🗺️ Roadmap

- [ ] Add an automated check in the CI pipeline to catch broken HTML/JS before deploy
- [ ] Docker + nginx container option
- [ ] Lighthouse CI for performance and SEO scores
- [ ] Custom domain
- [ ] Optional `.xlsx` support

---

## 🤝 Contributing

Suggestions and bug reports are welcome. Open an [issue](https://github.com/ydvharsh01/data-entry-assistant/issues) or submit a pull request.

---

## 📄 License

Released under the [MIT License](LICENSE).

---

## 👤 Author

**Harsh Yadav**, BCA student and aspiring DevOps engineer.

- GitHub: [@ydvharsh01](https://github.com/ydvharsh01)
- LinkedIn:www.linkedin.com/in/harsh-yadav-013359367

If this tool helped you, consider giving the repo a ⭐
