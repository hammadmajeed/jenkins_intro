[![Python application](https://github.com/hammadmajeed/ci_cd_demo/actions/workflows/python-app.yml/badge.svg)](https://github.com/hammadmajeed/ci_cd_demo/actions/workflows/python-app.yml)

Scaffolding

Makefile: Contains all the commands to execute and install

requirements.txt: contains the list of all the packages that needs to be installed. Its always a good practice to add the version number of all the packages

*.py: Python files of the repository

Create a virtual environment
``python -m venv ~/.ci_cd_pipeline``

Source the virtual environment
``source ~/.ci_cd_pipeline/bin/activate``

Install the packages required for execution
``make install``


