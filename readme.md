## Pre-requisite

Install "Remote Development" extenstion from microsoft

# Basic instructions

- Checkout appropriate environment branch
```
## For testing using vs-code rest client
git checkout dev-env-vscode-rest

## For inteliij java17
git checkout dev-env-intelij-java17

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

General environement variables can be configured at multiple places 
    - .vscode/settings.json
    - .devcontainer/devcontainer-compose.yml (services.app.environment)


#### File level variables:

in .http file, use the below syntax

```
 @fileLevelVariable = "blah blah"
```

