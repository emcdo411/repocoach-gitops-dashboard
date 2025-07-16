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
# 📦 Git Log Visualizer: app.R

library(shiny)
library(shinydashboard)
library(plotly)
library(tools)
library(shinyjs)

custom_css <- "
  body, .content-wrapper, .main-sidebar {
    background-color: #121212 !important;
    color: #ffffff !important;
  }
  .box {
    background-color: #1f1f1f !important;
    border: 1px solid #333;
  }
  .box-header {
    background-color: #2c2c2c !important;
  }
  .skin-blue .main-header .logo {
    background-color: #222 !important;
  }
  .skin-blue .main-header .navbar {
    background-color: #1a1a1a !important;
  }
  .box-primary > .box-header {
    background-color: #3a3a3a !important;
  }
"

ui <- dashboardPage(
  dashboardHeader(title = span("📊 Git Log Visualizer", style = "color: #00d1b2")),
  dashboardSidebar(
    textInput("repo_url", "Enter GitHub Repo URL or 'user/repo'", value = "emcdo411/PromptPilot-Pro"),
    actionButton("load_repo", "Clone & Visualize Logs", icon = icon("download"))
  ),
  dashboardBody(
    useShinyjs(),
    tags$head(tags$style(HTML(custom_css))),
    tabsetPanel(
      tabPanel("📦 Commit Flow (3D View)",
               box(width = 12, title = "🧾 Git Log Activity Viewer", status = "primary", solidHeader = TRUE,
                   plotlyOutput("log_activity_plot"),
                   tags$div(style = "margin-top:10px;",
                            tags$strong("Color Legend:"),
                            tags$ul(
                              tags$li(span(style = "color:#00c8ff", "➤ Blue: Commits")),
                              tags$li(span(style = "color:#f97306", "➤ Orange: Merges")),
                              tags$li(span(style = "color:#39ff14", "➤ Green: Branches")),
                              tags$li(span(style = "color:#ff2052", "➤ Red: Tag or Hotfixes"))
                            )
                   )
               )
      ),
      tabPanel("📈 Commit Signal Timeline",
               box(width = 12, title = "📈 Commit Signal Timeline", status = "primary", solidHeader = TRUE,
                   plotlyOutput("radio_wave_plot")
               )
      )
    )
  )
)

server <- function(input, output, session) {
  temp_path <- NULL
  
  observeEvent(input$load_repo, {
    repo_input <- trimws(input$repo_url)
    if (!grepl("https://", repo_input)) {
      repo_input <- paste0("https://github.com/", repo_input, ".git")
    }
    
    temp_path <<- file.path(tempdir(), gsub("[/:]", "_", repo_input))
    if (!dir.exists(temp_path)) {
      system2("git", c("clone", repo_input, temp_path))
    }
    
    output$log_activity_plot <- renderPlotly({
      log_data <- tryCatch({
        raw_log <- system2("git", c("-C", temp_path, "log", "--pretty=format:%h|%an|%s|%cr"), stdout = TRUE)
        df <- strsplit(raw_log, "\\|")
        data.frame(
          Hash = sapply(df, `[`, 1),
          Author = sapply(df, `[`, 2),
          Message = sapply(df, `[`, 3),
          TimeAgo = sapply(df, `[`, 4),
          Type = sapply(df, function(x) {
            msg <- tolower(x[3])
            if (grepl("merge", msg)) return("Merge")
            else if (grepl("fix|hotfix|patch", msg)) return("Hotfix")
            else if (grepl("branch", msg)) return("Branch")
            else return("Commit")
          }),
          stringsAsFactors = FALSE
        )
      }, error = function(e) data.frame())
      
      if (nrow(log_data) == 0) {
        return(plot_ly() %>% layout(title = "No Git logs found"))
      }
      
      log_data$Index <- seq_len(nrow(log_data))
      log_data$Weight <- ifelse(log_data$Type == "Merge", 1.5,
                                ifelse(log_data$Type == "Hotfix", 2,
                                       ifelse(log_data$Type == "Branch", 0.5, 1)))
      log_data$Intensity <- cumsum(log_data$Weight)
      log_data$Frequency <- jitter(as.numeric(factor(log_data$Type)) * 10)
      
      color_map <- c("Commit" = "#00c8ff", "Merge" = "#f97306", "Branch" = "#39ff14", "Hotfix" = "#ff2052")
      
      plot_ly(log_data, x = ~Index, y = ~Frequency, z = ~Intensity, type = "scatter3d", mode = "lines+markers",
              line = list(width = 2),
              marker = list(size = 5),
              text = ~paste("<b>", Message, "</b><br>", Author, " - ", TimeAgo),
              color = ~Type, colors = color_map) %>%
        layout(title = paste("Commit Flow (3D View) for:", basename(temp_path)),
               scene = list(
                 xaxis = list(title = "Chronological Index"),
                 yaxis = list(title = "Type Frequency"),
                 zaxis = list(title = "Weighted Intensity")
               ))
    })
  })
  
  output$radio_wave_plot <- renderPlotly({
    if (is.null(temp_path)) return(plot_ly() %>% layout(title = "Load a repo to see data"))
    
    log_data <- tryCatch({
      raw_log <- system2("git", c("-C", temp_path, "log", "--pretty=format:%h|%an|%s|%cr"), stdout = TRUE)
      df <- strsplit(raw_log, "\\|")
      data.frame(
        Hash = sapply(df, `[`, 1),
        Author = sapply(df, `[`, 2),
        Message = sapply(df, `[`, 3),
        TimeAgo = sapply(df, `[`, 4),
        Type = sapply(df, function(x) {
          msg <- tolower(x[3])
          if (grepl("merge", msg)) return("Merge")
          else if (grepl("fix|hotfix|patch", msg)) return("Hotfix")
          else if (grepl("branch", msg)) return("Branch")
          else return("Commit")
        }),
        stringsAsFactors = FALSE
      )
    }, error = function(e) data.frame())
    
    if (nrow(log_data) == 0) {
      return(plot_ly() %>% layout(title = "No Git logs found"))
    }
    
    log_data$Index <- seq_len(nrow(log_data))
    log_data$MessageLength <- nchar(log_data$Message)
    log_data$MessageLength[is.na(log_data$MessageLength)] <- 1
    
    max_length <- max(log_data$MessageLength, na.rm = TRUE)
    if (max_length == 0) max_length <- 1
    
    log_data$Amplitude <- sin(log_data$Index / 2) *
      log_data$MessageLength / max_length * 10
    log_data$Amplitude <- jitter(log_data$Amplitude, factor = 2)
    
    color_map <- c("Commit" = "#00c8ff", "Merge" = "#f97306", "Branch" = "#39ff14", "Hotfix" = "#ff2052")
    
    plot_ly(log_data, x = ~Index, y = ~Amplitude, type = 'scatter', mode = 'lines+markers',
            color = ~Type, colors = color_map,
            line = list(width = 2),
            marker = list(size = 6),
            text = ~paste("<b>", Message, "</b><br>", Author, " - ", TimeAgo)) %>%
      layout(title = "📈 Commit Signal Timeline",
             xaxis = list(title = "Commit Index"),
             yaxis = list(title = "Amplitude (Signal Simulation)"),
             plot_bgcolor = "#121212",
             paper_bgcolor = "#121212",
             font = list(color = "#ffffff"))
  })
}

shinyApp(ui, server)

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
