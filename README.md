# Python Poetry Dependency Management Test Project


## [Poetry docs](https://python-poetry.org/docs/basic-usage/)

The goal of this project is to demonstrate how [poetry](https://python-poetry.org) can be used to manage python dependencies.

---

### How to install poetry

[https://python-poetry.org/docs/#installation](https://python-poetry.org/docs/#installation)

---

### How to update poetry

```bash
# Updating Poetry to the latest stable version is 
# as simple as calling the self update command.

poetry self update
```

---

### How to create a new python project using poetry


```bash
# Creates the project in a subfolder with given name.

poetry new <project-name>
```

```bash
# Creates the project in the current folder.

poetry new .
```

---

### Initialising a pre-existing project

```bash
# Poetry can be used to ‘initialise’ a pre-populated directory. 
# To interactively create a pyproject.toml file in directory pre-existing-project

cd pre-existing-project
poetry init
```

---

### Add dependency

```bash
poetry add <dependecy>
```

---

### How to use the virtual environment

```bash
# Use poetry run to execute without explicitly activating 
# the virtual environment in the current terminal. 
# (Poetry still uses the virtual environment behind the scenes)

poetry run python <your_script>.py
```

```bash
# Use poetry shell to activate the virtual environment in the current terminal.

poetry shell
```

---

### How to find where the virtual environment is installed

```bash
# Poetry does not install the virtual environment in the project's 
# directory. It instead installs at {cache-dir}\virtualenvs. 
# You can change the cache-dir value by editing the poetry config.

poetry env info --path
```

---

### How to install dependencies

```bash
# So you just got a repo that uses poetry, use poetry install to 
# install all the dependencies and create your virtual environment 
# and the poetry.lock file if they are not already created.

poetry install
```

---

### Commit your poetry.lock file to version control

> Committing this file to VC is important because it will cause anyone who sets up the project to use the exact same versions of the dependencies that you are using. 

Cited from [here.](https://python-poetry.org/docs/basic-usage/#commit-your-poetrylock-file-to-version-control)

---

### How to update the dependencies to their latest versions

```bash
# This will fetch the latest matching versions 
# (according to your pyproject.toml file) and update the lock file with the new versions. 
# (This is equivalent to deleting the poetry.lock file and running install again.)

poetry update 
```