## How to make change 

For all files except .devcontainer/devcontainer.json, (main does not have .devcontainer/devcontainer.json)
    - Change files in main branch
    - rebase other branches using
```
``` 

For .devcontainer/devcontainer.json, change in the environment specific branch. Do not merge to main.

## Pre-requisite

### VS Code
Install "Remote Development" extenstion from microsoft

### Intellij
Windows Dev containers are not supported
refer https://www.jetbrains.com/help/idea/prerequisites-for-dev-containers.html#limitations

## Basic instructions

- Checkout appropriate environment branch
```
## For testing using vs-code rest client
git checkout dev-env-vscode-rest

## For vscode java17
git checkout dev-env-vscode-java17

## For vscode typescript, angular17
git checkout dev-env-vscode-angular17

## For vscode mean
git checkout dev-env-vscode-mean

```

- reopen in dev container
- open workspace

## VScode local setup

Install "Remote Development" extenstion from microsoft


### Enviroment Variables:

#### Secret Environment Variables

Add secret variables e.g. passwors etc. into .devcontainer/devcontainer.env. (*.env files are added to .gitignore). 

Sample .devcontainer/devcontainer.env
```
SECRET=blah
```
These variables are set as env variable at devcontainer boot. 


#### General Environment Variables:

General environement variables 
    - .devcontainer/devcontainer-compose.yml (services.app.environment)


### Http Client vscode plugin 

#### Environment specific variables 

    - .vscode/settings.json

#### File level variables for http reqeusts (*.http files):

use the below syntax in .http files

```
 @fileLevelVariable = "blah blah"
```