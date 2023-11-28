# SDP-CW2-TDD-Analysis

This project analysis patterns for software development using the TDD paradigm. 

## Usage 

This project uses [Poetry](https://python-poetry.org/) for dependency management. 

To install dependencies, run: 

```bash
poetry install 
```

To spawn virtual environment, run:

```bash
poetry shell
```

## Development 

The project uses [pre-commit](https://pre-commit.com/) to run checks before commits. 
Please install the hooks before start developing

```bash
# after installing poetry and the dependencies 
poetry run pre-commit install --hook-type pre-commit
```

This project uses [ruff](https://docs.astral.sh/ruff/) for style formatting. Please install corresponding 
plugins to your IDE to enable automatic formatting. 
The instructions can be found [here](https://docs.astral.sh/ruff/integrations/#integrations)


## Project Structure 

### Repo Data Collection 

The repo data should be cloned locally with [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

The git repositories located under `test_submodules` are used for testing and are not real data source for generating the final results. 

The git repositories located under `production_submodules` are used in statistical analysis and generating final results. 

### Rationale For Using Submodules

Using submodules allows us to mine the data locally without experiencing network issues and latencies. In addition, git tracks the specific comomit used for each submodule. This means we can analysis consistetnt data sets without management overhead. 

