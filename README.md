RussianHousingMarket
==============================

Project structure for Kaggle [Russian housing market competition](https://www.kaggle.com/c/sberbank-russian-housing-market)

Analysis Guidelines
-------------

- Data is in `data/raw` folder. _**Do not change the files in here**_. Do the analysis in python, R whatever, and if you need to save modified data files, save them under `data/interim` or `data/processed`.
- Data dictionary, samples and other stuff are in `references`.
- Use the `notebooks` folder for Jupyter notebooks. _**Don't**_ collaborate on notebooks on git (json with binary blobs are hard to `git diff`), instead use notebooks for exploratory analysis, visualization, creating outputs, etc. Save actual processing scripts under `src`.

Steps for Automatic Environment and Project Initialization
-------------

1. Ensure you have python installed, or just install [anaconda](https://www.continuum.io/downloads).
2. Clone this repository.
3. cd into this repository.
3. `make check_vars` and ensure everything's in order (python detected, conda detected, etc.)
4. `make create_environment` to create the necessary python environment with conda (preferred) or pip.
5. `source activate <env_name>` (conda) or `workon <env_name>` (pip) to change into environment (make sure the prompt changes to `(<env_name>) ... $` etc.). Assume everything will be carried on inside this environment from now on.
6. `make check_vars` and ensure everything's in order again.
7. `make requirements` to install packages required for project.
8. `python -m ipykernel install --user --name <env_name> --display-name "Python (<env_name>)"` to install jupyter kernel for project environment.
9. `make test_environment` and `make check_vars` again to ensure everything's cool.


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │   environment.yml       generated with `pip freeze > ..` or `conda env export > ..`
    │
    └── src                <- Source code for use in this project.
        ├── __init__.py    <- Makes src a Python module
        │
        ├── data           <- Scripts to download or generate data
        │   └── make_dataset.py
        │
        ├── features       <- Scripts to turn raw data into features for modeling
        │   └── build_features.py
        │
        ├── models         <- Scripts to train models and then use trained models to make
        │   │                 predictions
        │   ├── predict_model.py
        │   └── train_model.py
        │
        └── visualization  <- Scripts to create exploratory and results oriented visualizations
            └── visualize.py


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
