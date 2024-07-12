# Introduction

This project is an archtype development environment for a react app with [Pocketbase](https://pocketbase.io/) as the backend.

The dev container is based on the [official React dev container](https://github.com/microsoft/vscode-dev-containers/tree/main/containers/javascript-node-lts) and the [official PNPM dev container](https://github.com/microsoft/vscode-dev-containers/tree/main/containers/javascript-node-pnpm).

# Features

* pnpm as package manager with global store shared with the host and 
all the dev containers. ($HOME/.local/share/pnpm)
* Pocketbase as the backend.
* VSCode dev container with the react recommended extensions.


# Requirements:

Create the local folder structure as the local store for all the pnpm store files shared accross all dev containers. This way the pnpm will be faster and will use less space.

```bash
# If the folder does not exist, docker will create it with 
# root user ownership so it might be better to create it as the host 
# user to avoid any permission issues.
mkdir -p ${HOME}/.local/share/pnpm
```

# Launch the local dev env.

1. Fork or Clone this repo 

```bash
git clone https://github.com/marcitqualab/dev-container-react-app-pocketbase.git
```
This is primerly been tested in VSCode, but this should be compatible with any [dev container tool](https://containers.dev/supporting).

Open the repository in VSCode or any dev container compatible tool.

2. Install Dev Containers extension to VSCode

*Identifier: ms-vscode-remote.remote-containers*

3. Start the dev server and the Pocketbase backend at once.

```bash
pnpm install
pnpm run dev
```

# Ract app Frontend
* http://localhost:3000/

# Pocketbase Backend
* http://localhost:8080/api/
* http://localhost:8080/_/


# Tips:

* Delete the react-app folder and open a terminal session inside the docker dev environment and use [Vite to create new starter applications](https://vitejs.dev/guide/).


# Support:
DM [Marc Andreu at linkedin](https://www.linkedin.com/in/marcandreuf/) for any issues or open an issue to this repository.
