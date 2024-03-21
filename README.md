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

### Publish Github page for Repo
1. Go to the repository on GitHub and navigate to the **Settings** tab.
2. Scroll down and click the **Pages** section on the left sidebar.
3. Select the main branch as the source for the site.
4. Change from the root folder to the docs folder to publish from.
5. Click Save and wait for the site to build.
6. Eventually, be patient; your app will be published. If you scroll to the top of the Pages tab, you'll see your `github.io` URL for the hosted web app. Copy this to your clipboard.
7. Back on the main repo page, find the About section of the repo (upper right).
8. Edit the "About" section of the repository to include a link to your hosted web app using the Pages URL.

### Change the browser tab title
1. Find the index.html file in the docs folder.
2. Add new title between <title> and </title>

### Add a custom favicon
1. Download favicon from website https://favicon.io/
2. Add favicon.ico file to docs folder
3. Edit index.html to add favicon
```shell
<link rel="icon" type="image/x-icon" href="./favicon.ico">
```