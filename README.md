Langflow Installation Guide
This guide will walk you through the steps to install and use Langflow locally on your Linux system. For Windows users, you'll need to set up a WSL (Windows Subsystem for Linux) environment first.

Prerequisites
Linux: If you're using Windows, you'll need to install WSL and set up an Ubuntu Linux distribution.
Node.js: Version 20
npm: Version 10.8.1
pipx: Python package installer
Poetry: Python dependency management
Installation Steps
1. Setting Up WSL (Windows Only)
Open PowerShell with admin rights.
Type the following command to install WSL:
<POWERSHELL>
wsl --install
Follow the prompts to create a user (username, password).
Open Command Prompt and type:
<POWERSHELL>
start ubuntu.exe
2. Installing Node Version Manager (nvm) and Node.js
Install nvm:
<BASH>
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
Download and install Node.js (you may need to restart the terminal):
<BASH>
nvm install 20
Verify the Node.js version:
<BASH>
node -v # should print `v20.16.0`
Verify the npm version:
<BASH>
npm -v # should print `10.8.1`
3. Installing pipx and Poetry
Install pipx:
<BASH>
sudo apt install pipx
Install Poetry with pipx:
<BASH>
pipx install poetry
4. Cloning the Repository and Setting Up the Environment
Clone the Langflow repository:
<BASH>
git clone [URL_OF_REPOSITORY]
Create and activate a Python environment.
5. Setting Up the Code Editor
In your code editor, open the repository folder in the WSL Ubuntu environment.
Use the shortcut Ctrl + Shift + P and select "Connect to WSL" using your Ubuntu distribution.
6. Building and Running Langflow
In the command line, run the following commands:
<BASH>
make install_frontend && make build_frontend && make install_backend
Finally, run Langflow:
<BASH>
python -m langflow run
And that's it! You should now have Langflow installed and running on your system. If you encounter any issues, please refer to the project's documentation or seek help from the community.
