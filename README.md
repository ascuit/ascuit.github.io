# ascuit.github.io

A Quarto-rendered website containing data analysis posts written in Python and R and more.
_This dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license. DOI: 10.24432/C5PC7J_

The Python data analysis uses the `Wine` dataset, and R data analysis uses the `Iris` dataset.
_This dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license._

## Requirements

Install [Quarto](https://quarto.org/), [uv](https://docs.astral.sh/uv/), [R](https://www.r-project.org/), and [renv](https://rstudio.github.io/renv/)

Python dependencies are recorded in `pyproject.toml` and `uv.lock`. R dependencies are recorded in `renv.lock`.

## Build

Install python dependencies:

```sh
$ uv sync
```

Update R env:

```sh
$ Rscript -e 'renv::restore()'
```

Render the website:

```sh
$ uv run quarto render
```
