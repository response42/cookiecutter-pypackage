# Cookiecutter Modern PyPackage 🐍📦

<div align="center">

<object data="_static/logo.png" type="image/png" width="300">
   <img src="assets/logo.png" width="300"/>
</object>

[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/response42/cookiecutter-pypackage?logo=github)](https://github.com/response42/cookiecutter-pypackage/releases)
[![Python Version](https://img.shields.io/badge/python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12-blue?logo=python)](https://www.python.org/)
[![Tests](https://github.com/response42/cookiecutter-pypackage/workflows/tests/badge.svg)](https://github.com/response42/cookiecutter-pypackage/actions?workflow=tests)
[![Read the Docs](https://readthedocs.org/projects/cookiecutter-pypackage/badge/)](https://cookiecutter-pypackage.readthedocs.io/)
[![License](https://img.shields.io/badge/license-MIT-brightgreen)](https://opensource.org/licenses/MIT)

[![Black](https://img.shields.io/badge/code%20style-black-000000)](https://github.com/psf/black)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)

</div>

[Cookiecutter][cookiecutter] 🍪 template for a modern Python package 🐍📦.

* GitHub repo: <https://github.com/response42/cookiecutter-pypackage.git>
* Documentation: <https://cookiecutter-pypackage.readthedocs.io>
* Free software: MIT license

## 🚀 Features

* **Dependency tracking:** 📦 Utilizes [Poetry][poetry] for efficient package management.
* **Testing setup:** 🧪 Includes [Pytest][pytest] for comprehensive and reliable testing.
* **Continuous Integration:** 🔄 [Github Actions][github_actions] integration for seamless CI testing.
* **Linting:** 🧹 Enhanced code quality with [Ruff][ruff].
* **Docstring:** 📚 Follows the [Google Python Style Guide][google_styleguide] for clear and consistent documentation.
* **Static type checking:** 🔍 Ensured by [Mypy][mypy].
* **Formatting:** ✨ Consistent code formatting with [Black][black] and [Isort][isort].
* **Security checks:** 🔐 Uses [Safety][safety] to identify and address known vulnerabilities.
* **Git hooks:** 🎣 Managed by [pre-commit][pre-commit] for streamlined development workflows.
* **Development tasks CLI:** 🛠️ All-in-one Python CLI provided by [invoke][invoke].
* **Multiple Python environments testing:** 🥁 Supported by [Nox][nox].
* **Documentation:** 📖 Utilizes [Sphinx][sphinx] for clear and comprehensive documentation, ready for [Read the Docs][rtd].
* **Command line interface:** 💻 Optional integration with [Typer][typer].
* **Automated dependency updates:** 🤖 Enabled by [Dependabot][dependabot].
* **Coverage reports:** 📊 Integrated with [Codecov][codecov].
* **Automated releases:** 🚢 Push a new tag to trigger releases to [PyPI][pypi] and [TestPyPI][testpypi].
* **GitHub community health files (optional):**
    - [Code of Condunct][CODE_OF_CONDUCT.md] 🤝
    - [Contributing][CONTRIBUTING.md] 📝
    - [Security][SECURITY.md] 🔒
    - [Code Owners][CODEOWNERS] 👩‍💼
    - [Funding][FUNDING.yml] 💰
    - [Citation][CITATION.cff] 📑

## ⚡️ Quickstart

Get started with your modern Python package in just a few steps:

### 1. Install Dependendencies

#### pip

On Ubuntu 24.04

```sh
sudo apt-get install python3-pip
```

#### [pipx](https://github.com/pypa/pipx)

Ubuntu 24.04: 
[Pipx official  installation instructions](https://github.com/pypa/pipx#install-pipx) leads to installing an old version. [This discussion](https://github.com/pypa/pipx/issues/1481) suggests using pipx to install pipx

```sh
sudo apt install pipx               # installs pipx version 1.4.3 to /usr/local/bin  recall --global is busted
pipx ensurepath                     # adds ~/.local/bin to path
pipx install pipx                   # installs latest pipx to ~/.local/bin 
sudo apt purge --autoremove pipx    # remove pipx 1.4.3 via apt,  and all extra files including autocomplete from /usr/local/bin

# restart shell
```


#### [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/index.html)

If you haven't installed Cookiecutter yet, make sure to have version 1.4.0 or higher:

```sh
pipx install cookiecutter
cookiecutter --version
```

#### [cruft](https://cruft.github.io/cruft/)

```sh
pipx install cruft
```

#### [poetry](https://python-poetry.org/docs/)

```sh
pipx install poetry
```

### 2. Generate your Python Package

Run cruft using the latest release

```sh
cruft create gh:response42/cookiecutter-pypackage
```

### 3. Set up Your Project

Follow these steps to complete the setup:

* Create a new GitHub repository and push your generated project there.
* Install the development requirements into a virtual environment:

    ```sh
    poetry install
    ```

* Install pre-commit hooks:

    ```sh
    poetry run inv install-hooks
    ```

* Configure [Codecov][codecov] repository settings. (Codecov App, `CODECOV_TOKEN`)
* Add your repository to your [Read the Docs][rtd] account and enable the Read the Docs service hook.
* Configure [PyPI][pypi] and [TestPyPI][testpypi] tokens. (`PYPI_TOKEN`, `TEST_PYPI_TOKEN`)
* Release your package by pushing a new tag.

> [!TIP]
> For more details, see the [tutorial][tutorial].

## 📝 Credits

This cookiecutter was forked from 
* [fedejaure/cookiecutter-modern-pypackage](fedejaure/cookiecutter-modern-pypackage)

Which was in turn inspired by inspired by:

* [audreyr/cookiecutter-pypackage][audreyr/cookiecutter-pypackage]: Cookiecutter template for a Python package.
* [briggySmalls/cookiecutter-pypackage][briggySmalls/cookiecutter-pypackage]: A fork from [audreyr/cookiecutter-pypackage][audreyr/cookiecutter-pypackage] using Poetry for package management, with linting, formatting and more.
* [hypermodern-python][hypermodern-python]: Hypermodern Python article series.

[cookiecutter]: https://github.com/cookiecutter/cookiecutter
[poetry]: https://python-poetry.org/
[pytest]: https://github.com/pytest-dev/pytest
[github_actions]: https://github.com/features/actions
[ruff]: https://github.com/astral-sh/ruff
[isort]: https://github.com/timothycrosley/isort
[black]: https://github.com/psf/black
[mypy]: https://github.com/python/mypy
[pre-commit]: https://pre-commit.com/
[safety]: https://github.com/pyupio/safety
[google_styleguide]: https://google.github.io/styleguide/pyguide.html
[invoke]: https://www.pyinvoke.org/
[sphinx]: https://www.sphinx-doc.org/en/master/
[rtd]: https://readthedocs.org/
[nox]: https://nox.thea.codes/en/stable/
[tutorial]: https://cookiecutter-pypackage.readthedocs.io/en/latest/tutorial.html
[typer]: https://typer.tiangolo.com/
[dependabot]: https://dependabot.com/
[audreyr/cookiecutter-pypackage]: https://github.com/audreyr/cookiecutter-pypackage
[briggySmalls/cookiecutter-pypackage]: https://github.com/briggySmalls/cookiecutter-pypackage
[hypermodern-python]: https://cjolowicz.github.io/posts/hypermodern-python-01-setup/
[codecov]: https://codecov.io/
[pypi]: https://pypi.org/
[testpypi]: https://test.pypi.org/
[contributor-covenant]: https://www.contributor-covenant.org/
[CODE_OF_CONDUCT.md]: https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project
[CONTRIBUTING.md]: https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors
[SECURITY.md]: https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository
[CODEOWNERS]: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners
[FUNDING.yml]: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository
[CITATION.cff]: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files
