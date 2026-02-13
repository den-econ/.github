# Contributing to DEN Economic Lab

Thank you for your interest in our work. DEN Economic Lab is committed to open,
reproducible economic analysis in service of the Indonesian public. This guide
explains how anyone — inside or outside the lab — can engage with our repositories.

---

## Table of Contents

- [Who Can Contribute](#who-can-contribute)
- [Ways to Contribute](#ways-to-contribute)
- [Reporting Errors](#reporting-errors)
- [Suggesting Improvements](#suggesting-improvements)
- [Submitting Code or Data Corrections](#submitting-code-or-data-corrections)
- [Replication Issues](#replication-issues)
- [Style & Standards](#style--standards)
- [Pull Request Process](#pull-request-process)
- [Code of Conduct](#code-of-conduct)
- [Contact](#contact)

---

## Who Can Contribute

**External researchers, students, and the public** are welcome to:
- Report errors in our analysis (data, code, or methodology)
- Ask questions about our methods via GitHub Discussions
- Suggest improvements or extensions to our work
- Submit corrections via Pull Request

**Lab members** follow the internal workflow documented in our
[`.github-private`](https://github.com/den-econ/.github-private) repository.

---

## Ways to Contribute

### 1. Ask a Question
Use [GitHub Discussions](https://github.com/orgs/den-econ/discussions) for:
- Questions about methodology
- Requests for clarification on data sources
- General discussion about our research

Please search existing discussions before opening a new one.

### 2. Report an Error
Use **GitHub Issues** (see [Reporting Errors](#reporting-errors) below) for:
- Bugs in code (wrong output, errors when running)
- Data errors (wrong values, missing observations)
- Methodology concerns (potential errors in analytical approach)
- Replication failures (cannot reproduce our results)

### 3. Submit a Fix
If you have already identified an error *and* have a correction ready,
you may open a Pull Request directly (see [Pull Request Process](#pull-request-process)).

---

## Reporting Errors

Open an Issue using the appropriate template:

| Template | Use For |
|----------|---------|
| 🐛 **Code Error** | Script fails, wrong output, missing output |
| 📊 **Data Error** | Wrong values, source mismatch, missing data |
| 🔁 **Replication Issue** | Cannot reproduce results from our paper |
| ❓ **Method Question** | Not an error, just a question about approach |

When reporting, please include:
- Which repository and which file
- What you expected vs. what you observed
- Your operating system, Stata/R/Python version
- Steps to reproduce the problem

---

## Suggesting Improvements

We welcome suggestions for:
- Extensions to existing analyses
- Additional robustness checks
- Alternative methodological approaches
- Better data sources

Please open a Discussion rather than an Issue for suggestions, as they are
not errors and benefit from open conversation before any decision is made.

---

## Submitting Code or Data Corrections

If you have identified an error and have a fix ready:

1. **Fork** the repository
2. **Create a branch** named descriptively:
   ```
   fix/correct-cpi-deflator-2022
   fix/typo-in-regression-table-3
   ```
3. **Make your changes** — keep them minimal and focused on one issue
4. **Test your changes** — run the relevant do-files or scripts and confirm output
5. **Open a Pull Request** — reference the related Issue number

We aim to review external Pull Requests within **10 working days**.

---

## Replication Issues

Reproducibility is central to our mission. If you cannot replicate our results:

1. Open a **Replication Issue** using the issue template
2. Tell us exactly which paper/working paper you are replicating
3. Specify which table or figure you cannot reproduce
4. Share the error message or discrepancy you encounter

We take replication issues seriously and will respond within **5 working days**.

If replication requires data that is not publicly available due to licensing
restrictions, we will explain this in the repository README and provide
instructions for obtaining access.

---

## Style & Standards

All contributions should follow our lab standards:

### Stata
- Do-files must run from top to bottom without error on a clean session
- Use relative file paths — never hardcode absolute paths
- All packages must be listed in `00_setup.do` with `ssc install` or `net install`
- Variables must be labelled
- Use `// comments` to explain non-obvious steps
- Output files go in `/output` — never overwrite raw data

### R
- Follow the [tidyverse style guide](https://style.tidyverse.org/)
- Use `renv` for package management and commit `renv.lock`
- All scripts must run from a clean R environment
- Use `here::here()` for file paths — never `setwd()`

### Python
- Follow [PEP 8](https://peps.python.org/pep-0008/)
- Use `requirements.txt` or `pyproject.toml` for dependencies
- Use relative paths throughout

### General
- No sensitive data, credentials, or API keys in any commit
- No large data files (>50MB) — use Harvard Dataverse or Zenodo links instead
- Commit messages should be clear and describe *what* changed and *why*

---

## Pull Request Process

1. Ensure your changes are limited to the fix or feature described
2. Update the relevant README if your change affects how to run the code
3. Reference any related Issues in your PR description
4. A lab member will review your PR — please be patient and responsive to feedback
5. Once approved, a lab member with write access will merge it

We reserve the right to decline contributions that fall outside the scope
of the repository or do not meet our standards, but we will explain why.

---

## Code of Conduct

All interactions with DEN Economic Lab repositories are governed by our
[Code of Conduct](CODE_OF_CONDUCT.md). We expect respectful, constructive
engagement from everyone. Harassment or bad-faith contributions will result
in removal from the community.

---

## Contact

For questions not suited to public Issues or Discussions:

📧 **General**: [contact@den-econ.id](mailto:contact@den-econ.id)  
🐛 **Technical**: Open an Issue in the relevant repository  
💬 **Discussion**: [github.com/orgs/den-econ/discussions](https://github.com/orgs/den-econ/discussions)

---

*DEN Economic Lab — Open Analysis for Public Good*
