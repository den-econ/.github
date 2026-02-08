# Contributing to DEN Economic Lab 🔬

Welcome to the team! To maintain high academic standards and reproducible code, please follow these guidelines.

## 📂 Project Structure
We use a **Modular Quarto Manuscript** structure. Do not write directly in `index.qmd`. 
- **Writing:** Edit your assigned file in the `/sections` folder.
- **Code:** Place data scripts in `/analysis`.
- **Data:** Put raw files in `/data/raw`. Never modify these; only read them.

## 🌿 Branching Strategy
We follow a "Feature Branch" workflow to avoid merge conflicts:
1. **Never** push directly to the `main` branch.
2. Create a new branch for your task: `git checkout -b feature/your-task-name`
3. Examples: `feature/intro-draft`, `feature/inflation-model`, `fix/biblio-links`.

## ✍️ Writing & Inclusion
We use the `{{< include >}}` method. If you are assigned the Introduction:
1. Open `sections/01-intro.qmd`.
2. Write your content and save.
3. The Lead will ensure it is correctly linked in the master `index.qmd`.

## 📊 Code Standards
- **Python/R:** Use relative paths (e.g., `../data/raw/data.csv`) so scripts work on everyone's computer.
- **Environment:** If you add a new library (e.g., `pandas` or `tidyverse`), update the `requirements.txt` or `renv.lock` file.
- **Notebooks:** If your code is complex, create a supplementary `.qmd` in `/analysis` so it appears in the Manuscript sidebar.

## 🚀 The Review Process (Pull Requests)
When your section is ready:
1. Push your branch to GitHub.
2. Open a **Pull Request (PR)** against the `main` branch.
3. Tag at least one other team member for a "Peer Review."
4. Once approved, the Lab Lead will merge your changes.
