# Terraform AWS Devcontainer

This repository contains a development environment using a Docker container, pre-configured with [Terraform](https://www.terraform.io/) and the [AWS CLI](https://aws.amazon.com/cli/). The setup leverages VSCode's devcontainer feature along with Docker Compose to provide a seamless environment for developing and deploying cloud infrastructure.

## Features

- **Pre-installed Terraform**: Ready-to-use Terraform to simplify infrastructure automation.
- **Pre-installed AWS CLI**: Interact with AWS services from within the container.
- **Docker Compose Integration**: Automatically mounts the user's credentials directory for seamless access to AWS profiles.

## Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Visual Studio Code](https://code.visualstudio.com/) with the [Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Setup Instructions

1. **Clone this repository**:
   ``` bash
    git clone https://github.com/yourusername/your-repo.git
    cd your-repo ```
2. **Open the project in VSCode**:
   - Open VSCode, then choose `File > Open Folder` and select the cloned repository.

3. **Reopen in Container**:
   - After opening the folder, VSCode will detect the devcontainer configuration. Click the prompt to "Reopen in Container" or use the `Remote-Containers: Reopen in Container` command from the command palette (`Ctrl+Shift+P`).

4. **Mount your AWS credentials**:
   - The `docker-compose.yml` in this repository mounts your local AWS credentials file (`~/.aws/credentials`) into the container. Ensure that your credentials are correctly configured on your host machine.
5. **Start Working**:
    - Once the container is up and running, you can execute `terraform` and `aws` commands directly within the VSCode terminal.