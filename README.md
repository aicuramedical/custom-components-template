# Requirements
You will need the python package cookiecutter to create your project from this template.
```bash
pip install cookiecutter
```
# Usage
Execute the following command:
```bash
cookiecutter git@gitlab.aicuramedical.com:app-templates/custom-component-template.git
```
Answer the questions and you're ready to start.

# Build your package

## Install a few helper packages
```bash
pip install poetry poetry-dynamic-versioning
```
## Start the build
In order to build your package it has to be an git repository (a requirement of poetry-dynamic-versioning).
```bash
cd <your-project-directory>
git init
git add .
git commit -m "Initial commit"
# If you want to push to origin like gitlab (has to exist on gitlab instance)
git remote add origin git@gitlab.aicuramedical.com:aicura_apps/<your-package-repository>.git
```
Now you can build your package and the package version is automatically inferred from the git repository.
```bash
cd <your-project-directory>
poetry build
```

## Testing which of your custom components will be discovered
For your custom components to be discovered correctly by the Aicura IDE they have to correctly
implement the interfaces defined in the cbdf-api. You can test which of your custom components will
be discovered correctly by running the following command:
```
tox -e components
```
