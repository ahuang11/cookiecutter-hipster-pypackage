# Cookiecutter Hipster PyPackage

Cookiecutter template for a cutting-edge Python package: Hatch, ruff, mypy, GitHub Actions and more!

## Features

* [X] Lightweight starter
* [X] [Hatch](https://hatch.pypa.io/latest/install/) package management
* [X] Linting and formatting with [`ruff`](https://github.com/charliermarsh/ruff)
* [X] Type checking with [`mypy`](https://github.com/python/mypy)
* [X] Unit tests with [`pytest`](https://github.com/pytest-dev/pytest) with optional asyncio setup.
* [X] Documentation with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and docstring reference support with [mkdocstrings](https://mkdocstrings.github.io/).
* [X] Ready-to-use [GitHub Actions](https://help.github.com/en/actions/automating-your-workflow-with-github-actions) pipelines

## Quickstart

Generate the project:

```bash
cookiecutter https://github.com/ahuang11/cookiecutter-hipster-pypackage
```

The generator will automatically call `hatch env create` at the end.

After pushing to GitHub:

1. Set up `.pypirc` locally thru https://pypi.org/manage/account/

<img width="813" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/47bd9aa0-8faa-45a8-8024-060ad19237ff">

```
[distutils]
index-servers =
    pypi

[pypi]
  username = __token__
  password = pypi-abcdefghij...
```

1. Then push `v0.0.0`

```
hatch build
twine upload dist/*
```

1. Create another API token for the project thru https://pypi.org/manage/account/

<img width="382" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/9b9d2162-9cdf-4bae-8a22-6ee9789a537a">

1. Enable GitHub Pages in settings > pages

<img width="801" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/accd33a5-dc64-4df1-a009-07a3eed0bc38">

1. Set up `PYPI_API_TOKEN` in settings > secrets > actions

<img width="1215" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/7328fc80-4613-40d8-99a3-15af830d2bec">

1. Set up `CODECOV_TOKEN` thru https://app.codecov.io/gh/ in settings > secrets > actions

<img width="668" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/1d6e7af0-25de-4101-849f-ea44ab0f6c50">

1. Now you can release to PyPi by making a tag!

<img width="1169" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/7820461a-d559-4018-b50c-c77a612cb81d">

<img width="938" alt="image" src="https://github.com/ahuang11/cookiecutter-hipster-pypackage/assets/15331990/3ac62bd3-8a1f-47c1-80c9-109db0b9a0ba">

### With cruft

[cruft](https://github.com/cruft/cruft) is a layer above Cookiecutter allowing you to update your project from the template after it has been generated.

```bash
cruft create https://github.com/ahuang11/cookiecutter-hipster-pypackage
```

## License

This project is licensed under the terms of the MIT license.
