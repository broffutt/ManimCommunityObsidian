
```toml
[tool.poetry]
name = "manim"
version = "0.18.1"
description = "Animation engine for explanatory math videos."
authors = ["The Manim Community Developers <contact@manim.community>", "3b1b <grant@3blue1brown.com>"]
license="MIT"
readme="README.md"
repository="https://github.com/manimcommunity/manim"
documentation="https://docs.manim.community/"
homepage="https://www.manim.community/"
classifiers= [
    "Development Status :: 4 - Beta",
    "License :: OSI Approved :: MIT License",
    "Topic :: Scientific/Engineering",
    "Topic :: Multimedia :: Video",
    "Topic :: Multimedia :: Graphics",
    "Programming Language :: Python :: 3.8",
    "Programming Language :: Python :: 3.9",
    "Programming Language :: Python :: 3.10",
    "Programming Language :: Python :: 3.11",
    "Programming Language :: Python :: 3.12",
    "Natural Language :: English",
]
exclude = ["scripts/","logo/","readme-assets/"]
packages = [
    { include = "manim" },
]

[tool.poetry.dependencies]
python = ">=3.9,<3.13"
av = ">=9.0.0"
click = ">=8.0"
cloup = ">=2.0.0"
dearpygui = { version = ">=1.0.0", optional = true }
decorator = ">=4.3.2"
importlib-metadata = {version = ">=3.6", python = "<=3.9"}  # Required to discover plugins
isosurfaces = ">=0.1.0"
jupyterlab = { version = ">=3.0.0", optional = true }
manimpango = ">=0.5.0,<1.0.0"  # Complete API change in 1.0.0
mapbox-earcut = ">=1.0.0"
moderngl = ">=5.0.0,<6.0.0"
moderngl-window = ">=2.0.0"
networkx = ">=2.6"
notebook = { version = ">=6.0.0", optional = true }
numpy = ">=1.26"
Pillow = ">=9.1"
pycairo = ">=1.13,<2.0.0"
pydub = ">=0.20.0"
Pygments = ">=2.0.0"
rich = ">=12.0.0"
scipy = ">=1.6.0"
screeninfo = ">=0.7"
skia-pathops = ">=0.7.0"
srt = ">=3.0.0"
svgelements = ">=1.8.0"
tqdm = ">=4.0.0"
typing-extensions = ">=4.0.0"
watchdog = ">=2.0.0"

[tool.poetry.extras]
jupyterlab = ["jupyterlab", "notebook"]
gui = ["dearpygui"]

[tool.poetry.group.dev.dependencies]
black = ">=23.11,<25.0"
flake8 = "^6.1.0"
flake8-bugbear = "^23.11.28"
flake8-builtins = "^2.2.0"
flake8-comprehensions = "^3.7.0"
flake8-docstrings = "^1.7.0"
flake8-pytest-style = "^1.7.2"
flake8-simplify = "^0.14.1"
flake8-rst-docstrings = "^0.3.0"
furo = "^2023.09.10"
gitpython = "^3"
isort = "^5.12.0"
matplotlib = "^3.8.2"
myst-parser = "^2.0.0"
pre-commit = "^3.5.0"
psutil = {version = "^5.8.0", python = "<3.10"}
psutil-wheels = {version = "5.8.0", python = ">=3.10"}
pytest = "^7.4.3"
pygithub = "^2.1.1"
pytest-cov = "^4.1.0"
pytest-xdist = "^2.2"  # Using latest gives flaky tests
ruff = "*"
Sphinx = "^7.2.6"
sphinx-copybutton = "^0.5.2"
sphinxcontrib-programoutput = "^0.17"
sphinxext-opengraph = "^0.9.1"
types-decorator = "^0.1.7"
types-Pillow = "^10.1.0.2"
types-Pygments = "^2.17.0.0"

[tool.poetry.urls]
"Bug Tracker" = "https://github.com/ManimCommunity/manim/issues"
"Changelog" = "https://docs.manim.community/en/stable/changelog.html"
"Twitter" = "https://twitter.com/manim_community"
"Discord" = "https://www.manim.community/discord/"

[tool.pytest.ini_options]
markers = "slow: Mark the test as slow. Can be skipped with --skip_slow"
addopts = "--no-cov-on-fail --cov=manim --cov-report xml --cov-report term -n auto --dist=loadfile --durations=0"

[tool.isort]
profile = "black"

[tool.coverage.run]
omit = ["*tests*"]

[tool.coverage.report]
exclude_lines = ["pragma: no cover"]

[tool.poetry.plugins]
[tool.poetry.plugins."console_scripts"]
"manim" = "manim.__main__:main"
"manimce" = "manim.__main__:main"

[build-system]
requires = ["setuptools", "poetry-core>=1.0.0"]
build-backend = "poetry.core.masonry.api"

[tool.ruff]
line-length = 88
target-version = "py39"
extend-exclude = [
  ".github",
  ".hg",
  ".env",
  "env",
  "build",
  "buck-out",
  "media",
]
fix = true

[tool.ruff.lint]
select = [
  "E",
  "F",
  "I",
  "UP",
]

ignore = [
  # due to the import * used in manim
  "F403",
  "F405",
  # as recommended by https://docs.astral.sh/ruff/formatter/#conflicting-lint-rules
  "E111",
  "E114",
  "E117",
  "E501",
]

# Allow unused variables when underscore-prefixed.
dummy-variable-rgx = "^(_+|(_+[a-zA-Z0-9_]*[a-zA-Z0-9]+?))$"

[tool.ruff.lint.per-file-ignores]
"tests/*" = [
  # unused variable
  "F841",
  # from __future__ import annotations
  "I002",
]

"example_scenes/*" = [
  "I002",
]

"__init__.py" = [
  "F401",
  "F403",
]

[tool.ruff.lint.isort]
required-imports = ["from __future__ import annotations"]

[tool.ruff.format]
docstring-code-format = true

[tool.codespell]
write-changes = true
ignore-words-list = ["medias", "nam"]
```
