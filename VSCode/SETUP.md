# Initial VSCode Setup Prompt
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
    - **Remote - WSL** (Microsoft)
    - **Python** (Microsoft
    - **Jupyter** (Microsoft)
    - **Data Wrangler** (Microsoft)
    - **C/C++ Extension Pack** (Microsoft)
    - **Serial Monitor** (Microsoft)
    - **Simplicity Studio for VX Code**
    - **Emacs Freindly Keymap** (`lfs.vscode-emacs-friendly`)
    - **Prettier**
    - **GitLens** (`eamodio.gitlens`)
    - **GitHub Copilot** (`GitHub.copilot`)
    - **GitHub Copilot Chat**
    - **GitLens**
    - **Subversion** (`johnstoncode.svn-scm`)
    - **Beyond Compare** (configure as external diff/merge tool)

### 8. Configure Beyond Compare as Diff/Merge Tool
- In VSCode, open settings and search for "diff tool".
- For Git, set Beyond Compare as the default diff/merge tool:
    ```bash
    git config --global diff.tool bc
    git config --global merge.tool bc
    ```

### 9. Install and Configure Jupyter Notebooks Desktop App
- Setup for printing/export (Latex, etc.)

### 10. Additional Configuration
- Set up your GitHub account in VSCode.
- Configure Python interpreter (use the WSL Python).
- Set Simplicity Studio Version 6 to the default in VSCode settings: SiLabs: Feature Select

### 11. Setup Keybindings
#### User Customizations
| Keycode | Function | 
| ----- | ----- |
| Ctrl + M | emacs.cursorRight (User) |
| Alt + P | emacs.cursorPageUp (User) |
| Alt + N | emacs.cursorPageDown (User) |
| Alt + M | emacs.cursorWordRight (User) |
| Shift + Alt + P | emacs.cursorTop (User) |
| Shift + Alt + N | emacs.cursorBottom (User) |
| Ctrl+X Ctrl+X | System.Cut (User) |
| Ctrl+X Ctrl+C | System.Copy (User) |
| Ctrl+X Ctrl+V | System.Paste (User) |
| Ctrl+X Ctrl+I | editor.action.reindentselectedlines (User) |
| Ctrl+X Ctrl+P | editor.action.formatSelection (User) |
| Ctrl + X, S | Workbench.action.files.save (User) |
| Ctrl + X, Ctrl + S | Workbench.action.files.saveFiles (DELETE Emacs - User) |
| Ctrl + F | Find (DELETE Emacs - System) |
| Ctrl + V | Paste selection (DELETE Emacs - System) |

#### Commonly Used
| Keycode | Function | 
| ----- | ----- |
| Ctrl + B | emacs.cursorLeft (Emacs) |
| Ctrl + P | emacs.cursorUp (Emacs) |
| Ctrl + N | emacs.cursorDown (Emacs) |
| Ctrl + A | emacs.cursorHome (Emacs) |
| Ctrl + E | emacs.cursorEnd (Emacs) |
| Alt + F | emacs.cursorWordRight (Emacs) |
| Alt + B | emacs.cursorWordLeft (Emacs) |
| Ctrl + Space | emacs.enterMarkMode (Emacs) |
| Ctrl + C | Copy selection (System) |
| Shift + Delete | Cut (System) |
| Ctrl+K | emacs.C-k (Emacs) |
| Ctrl+Y | emacs.C-y (Emacs) |
| Shift + Tab | outdent (System) |
| F5 | Debug Continue (System) |
| Ctrl + F5 | Debug Start Without Debugging (System) |
| Shift + F5 | Debug Stop (System) |
| F9 | Debug: Toggle Breakpoint (System) |
| F6 | Debug: Pause (System) |
| F10 | Debug: Step Over (System) |
| F11 | Debug: Step Into (System) |
| Ctrl + S | Search forward (Emacs) |
| Ctrl + R | Search Reverse (Emacs) |
| Ctrl + D | deleteRight right (Emacs) |
| Ctrl + H | deleteLeft (Emacs) |
| Ctrl - ; | Toggle line comment (Emacs) |
| Alt - ; | Toggle block comment (Emacs) |
| Ctrl + X, K | View: Close Editor (Emacs) |
| Ctrl + X, Ctrl + K | View: Close All Editors (Emacs) |
| Ctrl + X, Ctrl + L | Transform to lowercase (Emacs) |
| Ctrl + X, Ctrl + U | Transform to uppercase (Emacs) |

