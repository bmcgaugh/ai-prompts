# VSCode Generation Prompt
Create instructions for installation and setup of VSCode and recommended extensions on a Windows 11 PC that will utilize WSL, Python3, embedded C, Silicon Labs, Emacs keyboard mappings, Git, Beyond compare, Github copilot, and subversion.

## Installation and Setup Instructions

### 1. Install VSCode
- Download and install [Visual Studio Code](https://code.visualstudio.com/) for Windows.

### 2. Install Windows Subsystem for Linux (WSL)
- Open PowerShell as Administrator and run:
    ```powershell
    wsl --install
    ```
- Restart your PC if prompted.
- Set up your preferred Linux distribution from the Microsoft Store (e.g., Ubuntu).

### 3. Install Python 3
- In your WSL terminal, run:
    ```bash
    sudo apt update
    sudo apt install python3 python3-pip
    ```

### 4. Install Embedded C Toolchains
- For ARM development, install `gcc-arm-none-eabi`:
    ```bash
    sudo apt install gcc-arm-none-eabi
    ```
- For Silicon Labs, download and install [Simplicity Studio](https://www.silabs.com/developers/simplicity-studio) on Windows.

### 5. Install Git and Subversion
- In WSL:
    ```bash
    sudo apt install git subversion
    ```
- Optionally, install [Git for Windows](https://git-scm.com/download/win).

### 6. Install Beyond Compare
- Download and install [Beyond Compare](https://www.scootersoftware.com/download.php) for Windows.

### 7. Install Recommended VSCode Extensions
- Open VSCode and go to Extensions (`Ctrl+Shift+X`), then search and install:
    - **Remote - WSL** (`ms-vscode-remote.remote-wsl`)
    - **Python** (`ms-python.python`)
    - **C/C++** (`ms-vscode.cpptools`)
    - **Silicon Labs IDE Support** (if available)
    - **Emacs Keymap** (`tuttieee.emacs-mcx`)
    - **GitLens** (`eamodio.gitlens`)
    - **GitHub Copilot** (`GitHub.copilot`)
    - **Subversion** (`johnstoncode.svn-scm`)
    - **Beyond Compare** (configure as external diff/merge tool)

### 8. Configure Beyond Compare as Diff/Merge Tool
- In VSCode, open settings and search for "diff tool".
- For Git, set Beyond Compare as the default diff/merge tool:
    ```bash
    git config --global diff.tool bc
    git config --global merge.tool bc
    ```

### 9. Additional Configuration
- Set up your GitHub account in VSCode.
- Configure Python interpreter (use the WSL Python).
- Customize Emacs keybindings as needed.

You are now ready to develop with VSCode, WSL, Python, Embedded C, Silicon Labs tools, Emacs keybindings, Git, Beyond Compare, GitHub Copilot, and Subversion on Windows 11.

Please provide the code selection you want documented.
