# Lume 🕯️

Lume is a sleek, modern JSON viewer CLI built for developers who need a better way to explore API responses and local data. It transforms raw JSON into interactive, navigable TUI experiences with a premium aesthetic.

<img src="test-data/lume_tree_demo.gif" width="100%" />

## Features

- **Interactive Tree View**: Browse complex nested structures with a navigable tree.
- **Elegant Box View**: A card-based layout for quick scanning of large datasets.
- **CURL-like Fetching**: Support for custom methods (`-X`), headers (`-H`), and data (`-d`).
- **Fast & Async**: Built on high-performance libraries to handle large responses without freezing.

## Installation

### From PyPI (Recommended)
You can install `lumeview` directly from PyPI:

```bash
pip install lumeview
# or with uv (recommended)
uv tool install lumeview
```

### Install from Source
If you want to use the local version while developing, run this inside the project directory:

```bash
uv tool install .
```

## Development

If you just want to run it without installing:

```bash
uv sync
uv run lume --help
```

## Usage

### Fetch from an API
```bash
lume fetch 'https://api.example.com/data' -X POST -d '{"query": "test"}'
```

### Open a local file
```bash
lume open test.json --display box
```

## Built With

- **[Textual](https://github.com/Textualize/textual)** - TUI Framework.
- **[Rich](https://github.com/Textualize/rich)** - Terminal formatting and rendering.
- **[Click](https://click.palletsprojects.com/)** - CLI argument parsing.
- **[HTTPX](https://www.python-httpx.org/)** - Modern, async HTTP client.
- **[UV](https://github.com/astral-sh/uv)** - Extremely fast Python package manager.
