# ascuit.github.io

A Quarto-rendered website containing data analysis posts written in Python and R.

The Python data analysis uses the **Wine** dataset, while the R data analysis uses the **Iris** dataset. The website also contains a mixed R/Python analysis that uses `reticulate`.

The datasets are licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.

Local copies of the datasets used for analysis are stored in their posts under:

```text
posts/<post-name>/data/
```

## Requirements

Install:

- [Quarto](https://quarto.org/)
- [uv](https://docs.astral.sh/uv/)
- [R](https://www.r-project.org/)
- [renv](https://rstudio.github.io/renv/)

Python dependencies are recorded in `pyproject.toml` and `uv.lock`. R dependencies are recorded in `renv.lock`.

## Build

Install the Python dependencies:

```sh
uv sync
```

Restore the R dependencies:

```sh
Rscript -e 'renv::restore()'
```

Render the website:

```sh
uv run quarto render
```

The rendered website is inside the `docs/` directory.
