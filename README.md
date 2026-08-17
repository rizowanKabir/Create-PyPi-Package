# Create-PyPi-Package 

A Python project template for creating, testing, and packaging a Python project as a distributable **PyPI package**.

This repository demonstrates a structured Python package setup using modern packaging tools, automated testing, development dependencies, and CI/CD with GitHub Actions.

---

## 🚀 Features

* 📦 Python package structure using the `src` layout
* 🛠️ Package configuration with `setuptools`
* 🧪 Automated testing with `pytest`
* 🔍 Code quality and testing with `tox`
* ⚙️ Project configuration using `pyproject.toml`
* 🔄 CI workflow with GitHub Actions
* 📋 Separate production and development requirements
* 📄 MIT License
* 🧩 Example package: `PyInception`

---

## 📁 Project Structure

```text
Create-PyPi-Package/
│
├── .github/
│   └── workflows/
│       └── ...
│
├── src/
│   └── PyInception/
│       ├── __init__.py
│       └── ...
│
├── tests/
│   └── ...
│
├── .gitignore
├── LICENSE
├── README.md
├── demo.excalidraw
├── init_setup.sh
├── pyproject.toml
├── requirements.txt
├── requirements_dev.txt
├── setup.cfg
├── setup.py
├── template.py
└── tox.ini
```

---

## 🛠️ Technologies & Tools

* **Python**
* **setuptools**
* **pytest**
* **tox**
* **Git & GitHub**
* **GitHub Actions**
* **PyPI**

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/rizowanKabir/Create-PyPi-Package.git
```

Navigate into the project:

```bash
cd Create-PyPi-Package
```

---

### 2. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 3. Upgrade pip

```bash
python -m pip install --upgrade pip
```

---

### 4. Install Dependencies

For the main project:

```bash
pip install -r requirements.txt
```

For development:

```bash
pip install -r requirements_dev.txt
```

---

## 📦 Installing the Package Locally

You can install the package in editable mode during development:

```bash
pip install -e .
```

This allows you to modify the source code without reinstalling the package every time.

---

## 🧪 Running Tests

Run the test suite using:

```bash
pytest
```

You can also run tests through `tox`:

```bash
tox
```

---

## 🔨 Building the Package

Install the build tool:

```bash
pip install build
```

Then build the package:

```bash
python -m build
```

This will create distribution files inside the `dist/` directory.

Typical output:

```text
dist/
├── PyInception-0.0.1.tar.gz
└── PyInception-0.0.1-py3-none-any.whl
```

The generated files are:

* **Source Distribution (`.tar.gz`)**
* **Wheel Distribution (`.whl`)**

---

## 📤 Publishing to PyPI

Before publishing, install `twine`:

```bash
pip install twine
```

Check the generated distributions:

```bash
twine check dist/*
```

Upload the package to PyPI:

```bash
twine upload dist/*
```

You will need a PyPI account and appropriate API credentials to publish a package.

> ⚠️ Never commit your PyPI API token or other sensitive credentials to GitHub.

---

## 🔄 Continuous Integration

This project includes a GitHub Actions workflow under:

```text
.github/workflows/
```

The workflow can be used to automatically run project checks and tests when changes are pushed to GitHub.

This helps ensure that new changes do not break the project.

---

## 🧩 Package Development Workflow

A typical development workflow for this project is:

```text
Write Code
    ↓
Run Tests
    ↓
Run Tox
    ↓
Build Package
    ↓
Check Distribution
    ↓
Publish to PyPI
```

Commands:

```bash
pytest
```

```bash
tox
```

```bash
python -m build
```

```bash
twine check dist/*
```

```bash
twine upload dist/*
```

---

## 💡 Why Use the `src` Layout?

This project uses the `src` layout:

```text
src/
└── PyInception/
```

The `src` layout helps prevent accidentally importing the local source directory instead of the installed package.

It also provides a cleaner structure for Python package development and distribution.

---

## 📝 Configuration Files

### `pyproject.toml`

Contains modern Python project/build configuration.

### `setup.py`

Contains package setup information using `setuptools`.

### `setup.cfg`

Provides additional package configuration.

### `tox.ini`

Defines environments and automated testing configuration.

### `requirements.txt`

Contains dependencies required by the project.

### `requirements_dev.txt`

Contains additional dependencies useful for development and testing.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new branch.

    ```bash
    git checkout -b feature/my-feature
    ```

3. Make your changes.
4. Run the tests.

    ```bash
    pytest
    ```

5. Commit your changes.

    ```bash
    git add .
    git commit -m "Add new feature"
    ```

6. Push the branch.

    ```bash
    git push origin feature/my-feature
    ```

7. Open a Pull Request.

---

## 📄 License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for more information.


**Repository:**
https://github.com/rizowanKabir/Create-PyPi-Package
