# Try Out Development Containers: WordPress

A **development container** is a running [Docker](https://www.docker.com) container with a well-defined tool/runtime stack and its prerequisites. You can try out development containers with **[GitHub Codespaces](https://github.com/features/codespaces)** or **[Visual Studio Code Remote - Containers](https://aka.ms/vscode-remote/containers)**.

This is a sample project that lets you try out either option in a few easy steps.

> **Note:** If you already have a Codespace or dev container, you can jump to the [Things to try](#things-to-try) section.

## Setting up the development container

### GitHub Codespaces

Follow these steps to open this sample in a Codespace:

1. Click the Code drop-down menu and select the **Open with Codespaces** option.
1. Select **+ New codespace** at the bottom on the pane.

For more info, check out the [GitHub documentation](https://docs.github.com/en/free-pro-team@latest/github/developing-online-with-codespaces/creating-a-codespace#creating-a-codespace).

### VS Code Remote - Containers

Follow these steps to open this sample in a container using the VS Code Remote - Containers extension:

1. If this is your first time using a development container, please ensure your system meets the pre-reqs (i.e. have Docker installed) in the [getting started steps](https://aka.ms/vscode-remote/containers/getting-started).

2. To use this repository, you can open the repository in an isolated Docker volume:

   - Clone this repository to your local filesystem.
   - Press <kbd>F1</kbd> and select the **Remote-Containers: Open Folder in Container...** command.
   - Select the cloned copy of this folder, **wait for the container to start**, and try things out!

## Things to try

When the container has started, you can try out the following:

- Go to http://localhost:8080/wp-admin/
  - Username: admin
  - Password: password
- or, if running in GitHub Codespaces (I haven't tested this myself), go to https://CODESPACE_NAME-8080.githubpreview.dev
  - Username: admin
  - Password: password

You'll see that the [vscode-remote-try-wp](index.php) plugin is [installed and activated](http://localhost:8080/wp-admin/plugins.php).

### WordPress Multisite or theme

You can modify the container by editing the [.devcontainer/.env](.devcontainer/.env) file.

```bash
SLUG=vscode-remote-try-wp
PROJECT_TYPE=plugin
IS_MULTISITE=0
```

The variables are:

- `SLUG`: The slug of the container. (plugin or theme folder name)
- `PROJECT_TYPE`: Either `plugin` or `theme`.
- `IS_MULTISITE` is either `0` (false) or `1` (true).

## Copyright and License

vscode-remote-try-wp is copyright 2022+ Per Soderlind

vscode-remote-try-wp is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 2 of the License, or (at your option) any later version.

vscode-remote-try-wp is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU Lesser General Public License along with the Extension. If not, see http://www.gnu.org/licenses/.
