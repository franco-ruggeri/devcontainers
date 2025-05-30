# Dev Containers

This overlay repository contains my extended dev containers. Each dev container
extends a dev container from a certain project to add the missing tools I use.

## Usage

1. Clone this repo and the project repo:

    ```bash
    git clone git@github.com:franco-ruggeri/devcontainers.git
    git clone <project-url>
    ```

2. In the project repo, create a subdirectory for the extended dev container:

    ```bash
    mkdir .devcontainer/personal
    ```

3. From this repo, create the symlinks:

    ```bash
    stow --target <project-path>/.devcontainer/personal <project-name>
    ```

4. From the project repo, create the dev container:

    ```bash
    devpod up . --devcontainer-path .devcontainer/personal/devcontainer.json
    ```

Enjoy the extended dev container!

## Repo Structure

Keep one subdirectory for each external project:

```bash
devcontainers/
    <project-name-1>/
        devcontainer.json
        ...
    <project-name-2>/
        devcontainer.json
        ...
```
