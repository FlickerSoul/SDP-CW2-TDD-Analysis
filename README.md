# SDP-CW2-TDD-Analysis

This project analysis patterns for software development using the TDD paradigm. The full repository can be found [here](https://github.com/FlickerSoul/SDP-CW2-TDD-Analysis).

## Usage 

This project uses [Poetry](https://python-poetry.org/) for dependency management. 

### Install With Poetry
To install dependencies, run: 

```bash
poetry install 
```

To spawn virtual environment, run:

```bash
poetry shell
```

### Install Without Poetry

```bash
python -m venv ./venv  # create virtual environment
source ./venv/bin/activate  # activate virtual environment
pip install -r requirements.txt  # install dependencies
# do whatever you want 
deactivate  # deactivate virtual environment when you exit
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

The git repositories located under `test_submodules` are used for analysis.

### Rationale For Using Submodules

Using submodules allows us to mine the data locally without experiencing network issues and latencies. In addition, git tracks the specific comomit used for each submodule. This means we can analysis consistetnt data sets without management overhead. 

