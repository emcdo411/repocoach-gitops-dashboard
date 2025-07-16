# 🧠 RepoCoach + PromptPilot-Pro: GitOps AI Assistant & Dashboard

> **Suggested Repo Name:** `repocoach-gitops-dashboard`

---

## ✨ Summary

**RepoCoach + PromptPilot-Pro** is a powerful GitOps toolkit that blends:
- 🔹 A **C# .NET 8 CLI tool** (`PromptPilot-Pro`) for generating Git-aware prompt pipelines  
- 🔹 An **AI-enhanced Shiny dashboard** (`RepoCoach`) that visualizes Git commit history, explains workflows, and provides natural language guidance

Together, they form a unified Git education and analytics system for developers, analysts, and instructors.

---

## 🔗 Clickable Sections

* [Tech Stack](#-tech-stack)
* [Installed R Packages](#-installed-r-packages)
* [Repo Capabilities](#-repo-capabilities)
* [Natural Language GitOps](#-natural-language-gitops)
* [VS Code Commands + C# CLI](#-vs-code-commands--c-cli)
* [Shiny App Code](#-shiny-app-code)
* [Why This Matters](#-why-this-matters)
* [Conclusion](#-conclusion)

---

## 🛠️ Tech Stack

![R](https://img.shields.io/badge/Language-R-276DC3?style=for-the-badge)
![Shiny](https://img.shields.io/badge/Framework-Shiny-00BFC4?style=for-the-badge)
![PowerShell](https://img.shields.io/badge/Scripting-PowerShell-blue?style=for-the-badge)
![.NET](https://img.shields.io/badge/CLI-.NET%208-blue?style=for-the-badge)
![Spectre.Console](https://img.shields.io/badge/UI-Spectre.Console-orange?style=for-the-badge)
![GitHub API](https://img.shields.io/badge/API-GitHub-181717?style=for-the-badge)
![Plotly](https://img.shields.io/badge/Charts-Plotly-yellow?style=for-the-badge)
![JSON](https://img.shields.io/badge/Data-JSON-lightgrey?style=for-the-badge)

---

## 📦 Installed R Packages

![shiny](https://img.shields.io/badge/Package-shiny-brightgreen?style=for-the-badge)
![shinydashboard](https://img.shields.io/badge/Package-shinydashboard-success?style=for-the-badge)
![plotly](https://img.shields.io/badge/Package-plotly-yellow?style=for-the-badge)
![jsonlite](https://img.shields.io/badge/Package-jsonlite-orange?style=for-the-badge)
![dplyr](https://img.shields.io/badge/Package-dplyr-green?style=for-the-badge)
![DT](https://img.shields.io/badge/Package-DT-purple?style=for-the-badge)
![glue](https://img.shields.io/badge/Package-glue-red?style=for-the-badge)
![httr](https://img.shields.io/badge/Package-httr-blue?style=for-the-badge)

---

## 📃 Repo Capabilities

* ✅ Visualizes commit flow in 3D and signal timelines
* ✅ Auto-parses Git commit types (merge, fix, hotfix, branch)
* ✅ Tracks stale branches, tags, and commit activity
* ✅ Logs and visualizes frequency, intensity, and author patterns
* ✅ Integrates with GitHub API to show stars, forks, PRs, branches

---

## 🧠 Natural Language GitOps

**RepoCoach** interprets natural queries and guides users step-by-step:

| Natural Input | Translated Command |
|---------------|--------------------|
| “Create a new branch” | `git checkout -b new-branch` |
| “Undo last commit”    | `git reset --soft HEAD~1` |
| “Fix merge conflict”  | Guides user through merge resolution |
| “Open my repo in CMD” | Powershell command: `cd` + `start cmd` |

---

## 💻 VS Code Commands + C# CLI

### ⚙️ Git Workflow in VS Code

```bash
# Clone repo
git clone https://github.com/emcdo411/PromptPilot-Pro.git
cd PromptPilot-Pro

# Build C# CLI
dotnet build
dotnet run --project PromptPilot.csproj

# Generate pipeline
dotnet run --project PromptPilot.csproj --generate-pipeline "QuickFix"

# Switch to dashboard
cd dashboard
Rscript -e "shiny::runApp('app.R', port=3838)"
````

### 🧾 Sample C# Code (`Program.cs`)

```csharp
using Spectre.Console;
using System.Diagnostics;

AnsiConsole.MarkupLine("[green]Welcome to PromptPilot-Pro![/]");

Console.Write("Enter your branch name: ");
var branch = Console.ReadLine();

Process.Start("git", $"checkout -b {branch}");
AnsiConsole.MarkupLine($"[yellow]Created new branch: {branch}[/]");
```

---

## 📄 Shiny App Code

<details>
<summary>Click to Expand app.R</summary>

```r
# Copy the full app.R Shiny code here
# (You already have it from our earlier fixes)
```

</details>

To run:

```r
shiny::runApp('app.R')
```

---

## 🕵️ Why This Matters

While GitHub Copilot helps you write **code**, it doesn't help you understand or safely navigate **Git workflows**.
**RepoCoach + PromptPilot-Pro** is built for:

* 🚀 Developers looking to master branching, merging, and rebasing
* 📊 Analysts who need visual Git insights, not terminal-only tools
* 🎓 Educators explaining real-world version control
* 🧪 Anyone debugging commits or reconciling team workflows

This project demystifies Git with code, visuals, and natural guidance.

---

## ✅ Conclusion

**RepoCoach + PromptPilot-Pro** is more than a dashboard — it’s a Git workflow assistant.
By combining a robust C# CLI with a visually powerful Shiny UI, it bridges the gap between code generation and commit comprehension.

> Built with 💡 by Maurice McDonald
> GitHub: [@emcdo411](https://github.com/emcdo411)
> LinkedIn: [in/mauricemcdonald](https://www.linkedin.com/in/mauricemcdonald)

---

*Ready to simplify Git? Clone this repo and make your commits make sense.*

```

---

Would you like me to:
- Push this as `README.md` to your `repocoach-gitops-dashboard` repo?
- Style the C# and R code sections more for print/PDF?
- Generate a preview banner image for the repo?
```


---
