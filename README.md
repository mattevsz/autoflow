# AutoFlow Installation Guide

This guide will walk you through the steps to install and use Langflow locally on your Linux system. For Windows users, you'll need to set up a WSL (Windows Subsystem for Linux) environment first.

## Prerequisites

- **Linux**: If you're using Windows, you'll need to install WSL and set up an Ubuntu Linux distribution.
- **Node.js**: Version 20
- **npm**: Version 10.8.1
- **pipx**: Python package installer
- **Poetry**: Python dependency management

## Installation Steps

### 1. Setting Up WSL (Windows Only)

1. Open PowerShell with admin rights.
2. Type the following command to install WSL:
    ```powershell
    wsl --install
    ```
3. Follow the prompts to create a user (username, password).
4. Open Command Prompt and type:
    ```powershell
    start ubuntu.exe
    ```

### 2. Installing Node Version Manager (nvm) and Node.js

1. Install nvm:
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
    ```
2. Download and install Node.js (you may need to restart the terminal):
    ```bash
    nvm install 20
    ```
3. Verify the Node.js version:
    ```bash
    node -v # should print `v20.16.0`
    ```
4. Verify the npm version:
    ```bash
    npm -v # should print `10.8.1`
    ```

### 3. Installing pipx and Poetry

1. Install pipx:
    ```bash
    sudo apt install pipx
    ```
2. Install Poetry with pipx:
    ```bash
    pipx install poetry
    ```

### 4. Cloning the Repository and Setting Up the Environment

1. Clone the repository:
    ```bash
    git clone https://github.com/mattevsz/autoflow.git
    ```

### 5. Setting Up the Code Editor

1. In your code editor, open the repository folder in the WSL Ubuntu environment.
2. Use the shortcut `Ctrl + Shift + P` and select "Connect to WSL" using your Ubuntu distribution.

### 6. Building and Running Langflow

1. Create and activate a Python environment.
   
2. In the command line, run the following commands:
    ```bash
    make install_frontend && make build_frontend && make install_backend
    ```
3. Finally, run Langflow:
    ```bash
    python -m langflow run
    ```

And that's it! You should now have Langflow installed and running on your system. If you encounter any issues, please refer to the project's documentation or seek help from the community.
