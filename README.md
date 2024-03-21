# cintel-04-local
Project 4 CI 

# Environment Setup 

### Start a new project repository in GitHub and then clone down to local machine. I leveraged VS Code clone functionality

### Create Virtual Environment

```shell

py -m venv .venv
.venv\Scripts\Activate
```

### Create .gitignore file
```shell
ni .gitignore
```
add .venv/ to .gitignore file to not be tracked in github

### Add requirements folder

```shell

ni requirements.txt
py -m pip install -r requirements.txt
```

# Install and Setup the Project

### Freeze dependencies

```shell

py -m pip freeze > requirements.txt
```

# Start Project

### Build Client Side APP
```shell
shiny static-assets remove
shinylive export penguins docs
```

```shell
py -m http.server --directory docs --bind localhost 8008
```

### Git add and commit 

```shell
git add .
git commit -m "add .gitignore, cmds to readme"
git push origin main
```