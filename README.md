# 🧠 RepoCoach: AI-Powered GitOps Assistant Dashboard

> **Suggested repo name:** `repocoach-gitops-dashboard`

---

## ✨ Summary

**RepoCoach** is an AI-assisted GitOps dashboard built in **R**, **Shiny**, and **PowerShell** that helps new and intermediate developers, data analysts, and technical teams manage Git repositories more effectively.

It does what GitHub Copilot doesn't: it *explains* Git workflows, *guides* users through every step, and translates natural language into actionable Git commands.

With visualizations, query history, GitHub API integration, and smart error handling, RepoCoach offers a **developer-friendly interface** for mastering Git without intimidation.

---

## 🔗 Clickable Sections

* [Tech Stack](#-tech-stack)
* [Installed R Packages](#-installed-r-packages)
* [Repo Knowledge & Capabilities](#-repo-knowledge--capabilities)
* [Natural Language Capabilities](#-natural-language-capabilities)
* [UI Features](#-ui-features)
* [Full app.R Code](#-full-appr-code)
* [Why This Matters](#-why-this-matters)
* [Conclusion](#-conclusion)

---

## 🛠️ Tech Stack

![R](https://img.shields.io/badge/Language-R-276DC3?style=for-the-badge)
![Shiny](https://img.shields.io/badge/Framework-Shiny-00BFC4?style=for-the-badge)
![PowerShell](https://img.shields.io/badge/Scripting-PowerShell-blue?style=for-the-badge)
![GitHub API](https://img.shields.io/badge/API-GitHub-181717?style=for-the-badge)
![JSON](https://img.shields.io/badge/Format-JSON-lightgrey?style=for-the-badge)
![Plotly](https://img.shields.io/badge/Charts-Plotly-orange?style=for-the-badge)

---

## 📊 Installed R Packages

![shiny](https://img.shields.io/badge/Package-shiny-brightgreen?style=for-the-badge)
![shinydashboard](https://img.shields.io/badge/Package-shinydashboard-success?style=for-the-badge)
![httr](https://img.shields.io/badge/Package-httr-blue?style=for-the-badge)
![jsonlite](https://img.shields.io/badge/Package-jsonlite-orange?style=for-the-badge)
![glue](https://img.shields.io/badge/Package-glue-red?style=for-the-badge)
![dplyr](https://img.shields.io/badge/Package-dplyr-green?style=for-the-badge)
![DT](https://img.shields.io/badge/Package-DT-purple?style=for-the-badge)
![plotly](https://img.shields.io/badge/Package-plotly-yellow?style=for-the-badge)
![rmarkdown](https://img.shields.io/badge/Package-rmarkdown-darkgreen?style=for-the-badge)
![cachem](https://img.shields.io/badge/Package-cachem-grey?style=for-the-badge)

---

## 📃 Repo Knowledge & Capabilities

* ✅ Uses GitHub API to track branches, pull requests, stars, forks, and commit activity
* ✅ Parses repo structure in real time and detects stale branches
* ✅ Checks local Git repo status using PowerShell from within R
* ✅ Detects and helps resolve common Git errors ("not a git repo", merge conflicts, etc.)
* ✅ Suggests full command chains to create branches, commit, push, and merge
* ✅ Outputs summaries of repo activity with human-like insights

---

## 🔎 Natural Language Capabilities

RepoCoach can understand input like:

* “How do I create a new branch?”
* “Undo last commit”
* “Fix merge conflict”
* “Push changes”
* “Clone the repo”
* “Open my repo folder in CMD”

It translates these into contextual command suggestions and walks users through the correct order of operations.

---

## 🎨 UI Features

* Sidebar navigation with tabs: **Dashboard**, **Query History**, and **Insights**
* Dark theme, VS Code-style color scheme
* PDF report generation of your Git activity
* DataTables for viewing historical command suggestions
* Plotly visualization of commit frequency
* Error-aware helper system for troubleshooting

---

## 📄 Full app.R Code

Full working code is available in [`app.R`](./app.R). It includes:

* GitHub authentication logic
* API error handling
* Query history and PDF rendering
* Git-aware suggestions
* Plotly visual chart of commit history

To run:

```r
shiny::runApp('app.R')
```

Make sure to export your GitHub token as an environment variable:

```bash
export GITHUB_PAT=your_token_here
```

---

## 🕵️‍ Why This Matters

While tools like GitHub Copilot help **write code**, they don’t necessarily help people **understand Git workflows**. RepoCoach was designed for:

* New developers struggling with Git sequences
* Analysts who don’t live in the terminal every day
* Instructors teaching version control in real-world workflows
* Solo developers who need a confidence boost when branching or merging

It demystifies Git. It teaches by doing. And it enables better DevOps hygiene.

---

## 🌟 Conclusion

**RepoCoach** is not just a Git UI. It’s a logic-driven, AI-enhanced command assistant that fills the gaps in learning and applying Git workflows. Built from scratch with R, it’s a testament to what’s possible when open-source tools, APIs, and human curiosity come together.

---

> Built by Maurice McDonald | GitHub: [@emcdo411](https://github.com/emcdo411) | LinkedIn: [in/mauricemcdonald](https://www.linkedin.com/in/mauricemcdonald)

---
