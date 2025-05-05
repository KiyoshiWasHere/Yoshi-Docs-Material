# MkDocs Installation Guide (Windows)

This guide walks you through setting up **MkDocs** with the **Material Theme** on a local Windows machine.

---

## Prerequisites

Before installing MkDocs, ensure you have the following:

- **Python 3.8 or newer** ([Download here](https://www.python.org/downloads/windows/)).
  - During installation, check **"Add Python to PATH"**.
- **Visual Studio Code** ([Download here](https://code.visualstudio.com/)).

Verify Python installation by opening a Command Prompt:

```bash
python --version
pip --version
```

---

## Step-by-Step Installation

### Step 1: Install MkDocs and Material Theme

Open your command prompt or VS Code terminal (`Ctrl + ~`) and enter:

```bash
pip install mkdocs mkdocs-material
```

Verify the installation:

```bash
mkdocs --version
```

### Step 2: Create a New MkDocs Project

In your terminal, navigate to your desired folder location, then run:

```bash
mkdocs new my-docs-site
cd my-docs-site
```

### Step 3: Configure the Material Theme

Open `mkdocs.yml` (located in your project folder) and replace its contents with:

```yaml
site_name: My MkDocs Documentation

# Activate the Material theme
theme:
  name: material

# Navigation (optional)
nav:
  - Home: index.md
```

---

## Step 4: Start Your Documentation Site

Launch the live-reloading server by running:

```bash
mkdocs serve
```

Visit the site by navigating your browser to:

```
http://127.0.0.1:8000
```

---

## Step 5: Editing and Adding Documentation

All documentation pages reside in the `docs/` folder:

Example project structure:

```
mkdocs.yml
/docs
    index.md
    installation.md
    usage.md
```

Example `index.md`:

```markdown
# Welcome to My MkDocs Site

This site provides documentation for my project.

## Documentation Sections

- [Installation](installation.md)
- [Usage Guide](usage.md)
```

---

## Step 6: Build Your Site

Generate a static version of your documentation:

```bash
mkdocs build
```

Your static files will be in the `site/` directory, ready to deploy.

---

## Common MkDocs Commands

| Command                  | Purpose                          |
|--------------------------|----------------------------------|
| `mkdocs new [dir-name]`  | Create a new MkDocs project      |
| `mkdocs serve`           | Start the local dev server       |
| `mkdocs build`           | Build static documentation files |
| `mkdocs -h`              | Display help                     |

---

## Further Resources

- [MkDocs Official Documentation](https://www.mkdocs.org)
- [Material Theme Documentation](https://squidfunk.github.io/mkdocs-material/)