# godevcontainer

## Go Development Environment with VS Code Devcontainer

This repository provides a pre-configured development container (devcontainer) for Go projects using Visual Studio Code (VS Code). This ensures a consistent and isolated development environment for your Go applications.

## Prerequisites

Before you begin, ensure you have the following installed:

1) **VS Code:** Download and install Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com/).
2) **Remote - Containers Extension:** Install the "Remote - Containers" extension in VS Code from the Extensions marketplace (search for "Remote - Containers").
3) **Container Runtime:** You need a container runtime to build and run the development container. While **Docker Desktop** ([https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)) is a popular choice, viable alternatives include:
    * **Podman:** A daemonless container engine for developing, managing, and running OCI Containers on Linux. It's often available in Linux distributions' repositories. Learn more at [https://podman.io/](https://podman.io/).
    * **Colima:** Container runtime on macOS (and Linux) with minimal setup. See [https://github.com/abiosoft/colima](https://github.com/abiosoft/colima).
    * **Rancher Desktop:** An open-source desktop application for Kubernetes and container management on macOS and Windows. It offers Docker and containerd as runtime options. Find it at [https://rancherdesktop.io/](https://rancherdesktop.io/).

    Ensure your chosen container runtime is installed and running.

## Setup and Usage in Your Go Project

Follow these steps to use this devcontainer in your own Go projects:

1.  **Copy the `.devcontainer` Folder:**
    * Navigate to the root of this repository.
    * Copy the entire `.devcontainer` folder.

2.  **Paste into Your Go Project:**
    * Go to the root directory of your Go project where you want to use the devcontainer.
    * Paste the copied `.devcontainer` folder into this root directory.

    ```
    your-go-project/
    ├── .devcontainer/
    │   ├── devcontainer.json
    │   └── Dockerfile
    ├── main.go
    └── go.mod
    ```

3.  **Open Your Go Project in VS Code:**
    * Open the root folder of your Go project in Visual Studio Code.

4.  **Reopen in Container:**
    * VS Code should automatically detect the `.devcontainer` folder. You might see a notification in the bottom right corner prompting you to "**Reopen in Container**". Click this notification.
    * If you don't see the notification, you can manually trigger the command palette (Ctrl+Shift+P or Cmd+Shift+P on macOS) and type or search for "**Remote-Containers: Reopen in Container**" and select it.

5.  **Wait for Container Build (First Time Only):**
    * The first time you reopen the project in the container, VS Code will build the Docker image (or the image used by your chosen container runtime) based on the `Dockerfile` located in the `.devcontainer` folder. This process might take several minutes depending on your internet connection and the complexity of your container setup.
    * You can monitor the build progress in the VS Code terminal.

6.  **Start Developing!**
    * Once the container is built and running, VS Code will automatically connect to it. You'll notice that the VS Code window title will indicate that you are now working inside the container (e.g., "[your-go-project] - Dev Container").
    * You can now open your Go files (`.go`), run your code, debug, use the integrated terminal, and leverage all of VS Code's features within the isolated Go development environment defined by your devcontainer configuration.

## Benefits of Using a Devcontainer

* **Consistent Environment:** Ensures everyone working on the project has the same development environment, eliminating "it works on my machine" issues.
* **Isolated Dependencies:** Project dependencies are contained within the container, preventing conflicts with your local system.
* **Easy Onboarding:** New team members can quickly get a fully configured development environment up and running.
* **Clean Local Machine:** Keeps your local development machine clean by isolating project-specific tools and dependencies.

Enjoy developing your Go projects with this streamlined devcontainer setup!

See https://containers.dev/ for details

Forked from https://github.com/qdm12/godevcontainer
