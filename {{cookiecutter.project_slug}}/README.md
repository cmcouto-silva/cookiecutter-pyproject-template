# Cookiecutter Python Project Template

A template for Python projects using [Cookiecutter](https://www.cookiecutter.io/) with predefined `pyproject.toml` and `.gitignore`.

## Features

- Predefined `pyproject.toml` with:
  - Author and email placeholders
  - Rules for Ruff (Black, Flake8, and isort)
  - Dependency groups for development and notebooks
- Organized folder structure:
  - `configs/` for configuration files
  - `data/` for datasets
  - `docs/` for documentation
  - `notebooks/` for Jupyter notebooks
  - `scripts/` for standalone scripts
  - `tests/` for test cases

## Usage

1. Install [Cookiecutter](https://github.com/cookiecutter/cookiecutter) and [UV](https://github.com/astral-sh/uv) if you haven't already.

2. Generate a new project using this template:

   ```bash
   cookiecutter https://github.com/cmcouto-silva/cookiecutter-pyproject-template.git
   ```

3. During the generation process, you will be prompted to provide values for:
   - `project_name`: The full name of your project
   - `project_slug`: The name of your project in slug format (auto-generated from `project_name`)
   - `project_short_description`: A brief description of your project
   - `author_name`: Your name
   - `author_email`: Your email

4. Navigate to the generated project folder and create a Python virtual environment with project dependencies:

   ```bash
   uv sync
   ```

5. Start coding! 😊

---

### Using pre-commit check for linter/formatter:

Initiate your repository:

```bash
git init .
```

Create a pre-commit hook:
```bash
uv run pre-commit install
```

You can manually check the linting/formatting with `make check` and apply fixes with `make fix`. 

You're all set! 🎉

## Notes

- Python 3.10 or higher is required to use this template.
- Update the `pyproject.toml` file as needed to suit your project requirements.
- The `README.md` file in the generated project will need to be customized for your specific project.
