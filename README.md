# Dev Containers

## Getting Started

This repository contains dedicated scripts to automate the management of [Dev Containers](https://containers.dev/). Any IDE that supports the Dev Container specification can use these containers.

These dev containers are specifically designed to provide a consistent and reproducible development environment. Here is an overview of the available containers:

- [C](./images/base/Dockerfile.c)
- [DevOps](./images/base/Dockerfile.devops)
- [Go](./images/base/Dockerfile.go)
- [Java](./images/base/Dockerfile.java)
- [Node.js](./images/base/Dockerfile.nodejs)
- [Python](./images/base/Dockerfile.python)
- [Rust](./images/base/Dockerfile.rust)
- [Rust embedded](./images/base/Dockerfile.rust-embedded)
- [Texlive](./images/base/Dockerfile.texlive)

All of the containers are based on a [common base image](./images/base/Dockerfile.core), which is a pre-configured Fedora Linux distribution.

To use this repository, follow these steps:

1. Run the `dev-container-sync-config` script to pull the necessary configuration files from your system.
2. Build the desired dev container using the `dev-container-sync-images -v VARIANT` command where `VARIANT` is the name of the container you want to build.
3. Create the `.devcontainer` folder inside your project using the `dev-container-create -v VARIANT` command. Warning: this command must be called from the root of your project.
4. Open the folder of your project with your IDE. It should detect the `.devcontainer` configuration and offer to reopen the project inside the container.
