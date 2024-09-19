# Terminal Assistant

A handy guide for essential terminal commands used in development workflows. This README covers setting up virtual environments, managing packages, and performing common Git operations.

---

## Table of Contents

- [Virtual Environments](#virtual-environments)
  - [Python's Built-in `venv`](#pythons-built-in-venv)
  - [Virtualenv](#virtualenv)
  - [Conda Environments](#conda-environments)
- [Package Management](#package-management)
  - [Installing the Latest Commit from a Git Repository](#installing-the-latest-commit-from-a-git-repository)
  - [Setting Up Build from Source](#setting-up-build-from-source)
- [Git Commands](#git-commands)
  - [Basic Git Workflow](#basic-git-workflow)
  - [Advanced Git Techniques](#advanced-git-techniques)
- [Additional Commands](#additional-commands)
- [References](#references)

---

## Virtual Environments

Isolating your development environment prevents conflicts between dependencies and makes managing packages easier. Below are commands for setting up virtual environments using different tools.

<details>
<summary><strong>Using in-built <code>venv</code></strong></summary>

**Create a Virtual Environment:**

```bash
python -m venv venv
```

**Activate the Virtual Environment:**

- **Windows:**

  ```bash
  venv\Scripts\activate
  ```

- **Unix or MacOS:**

  ```bash
  source venv/bin/activate
  ```

**Deactivate the Virtual Environment:**

```bash
deactivate
```

</details>

<details>
<summary><strong>Using <code>virtualenv</code></strong></summary>

**Install Virtualenv:**

```bash
pip install virtualenv
```

**Create a Virtual Environment:**

```bash
virtualenv venv
```

**Activate and Deactivate:**

Same as above.

</details>

<details>
<summary><strong>Using <code>conda</code></strong></summary>

**Create a Conda Environment:**

```bash
conda create -n myenv python=3.9
```

**Activate the Conda Environment:**

```bash
conda activate myenv
```

**Deactivate the Conda Environment:**

```bash
conda deactivate
```
</details>
<details>
<summary><strong>Using <code>uv</code></strong></summary>

**Install UV:**

```bash
pip install uv
```

**Create a Virtual Environment:**

```bash
uv venv venv
```

**Activate the Virtual Environment:**

- **Windows:**

  ```bash
  venv\Scripts\activate
  ```

- **Unix or MacOS:**

  ```bash
  source venv/bin/activate
  ```

**Deactivate the Virtual Environment:**

```bash
deactivate
```

</details>

---

## Package Management

<details>
<summary><strong>Installing the Latest Commit from a Git Repository</strong></summary>

You can install the latest version of a package directly from a Git repository.

**Using HTTPS:**

```bash
pip install git+https://github.com/username/repository.git
```

**Using SSH:**

```bash
pip install git+ssh://git@github.com/username/repository.git
```

</details>

<details>
<summary><strong>Setting Up Build from Source</strong></summary>

For development purposes, you might want to install a package in editable mode to reflect changes in real-time.

**Clone the Repository:**

```bash
git clone https://github.com/username/repository.git
```

**Navigate to the Project Directory:**

```bash
cd repository
```

**Install in Editable Mode:**

```bash
pip install -e .
```

</details>

---

## Git Commands

<details>
<summary><strong>Basic Git Workflow</strong></summary>

**Initialize a New Git Repository:**

```bash
git init
```

**Clone an Existing Repository:**

```bash
git clone https://github.com/username/repository.git
```

**Check Repository Status:**

```bash
git status
```

**Add Changes to Staging Area:**

```bash
git add filename
```

**Commit Changes:**

```bash
git commit -m "Commit message"
```

**Push Changes to Remote Repository:**

```bash
git push origin branch_name
```

</details>

<details>
<summary><strong>Advanced Git Techniques</strong></summary>

**View Commit History:**

```bash
git log
```

**Switch to a Different Branch:**

```bash
git checkout branch_name
```

**Create a New Branch and Switch to It:**

```bash
git checkout -b new_branch_name
```

**Merge Another Branch into Current Branch:**

```bash
git merge branch_name
```

**Rebase Current Branch onto Another Branch:**

```bash
git rebase branch_name
```

</details>

---

## Additional Commands

<details>
<summary><strong>Pip Commands</strong></summary>

**List All Installed Packages:**

```bash
pip list
```

**Show Package Details:**

```bash
pip show package_name
```

**Freeze Installed Packages to `requirements.txt`:**

```bash
pip freeze > requirements.txt
```

**Install Packages from `requirements.txt`:**

```bash
pip install -r requirements.txt
```

**Search for a Package on PyPI:**

```bash
pip search package_name
```

</details>
