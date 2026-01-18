# GitHub-Actions
Repository dedicated to learning GitHub Actions and CI/CD workflows.


# What is GitHub Action
It's an automation system built into GitHub

It runs workflows:

- A workflow = a set of steps that run automatically
- Triggered by events like:
    - push
    - pull_request

### Key words

- **Workflow** = automated process (like a script)
- **YAML** = config language (.yml files)
- **Job** = one task group inside a workflow
- **Step** = one command inside a job
- **Runner** = the machine that runs your code (Linux VM)

### Folder rule

All workflows live here: `.github/workflows/`

---

# Syntax


### Minimal workflow

#### Example:
- **name** → workflow name (for UI)
- **on: push** → run when someone pushes
- **jobs** → list of jobs
- **runs-on** → Linux machine
- **run** → terminal command

```yml
name: Hello Action

on: push

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - name: Print message
        run: echo "Hello from GitHub Actions"
```