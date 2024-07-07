# Installing Git

### Windows Installation

1. **Download the Git Installer**:
   - Visit the official Git website: [https://git-scm.com/](https://git-scm.com/)
   - Click on "Download" for Windows. The download should automatically start based on your OS.

2. **Run the Installer**:
   - Once the download is complete, run the executable file to start the installer.
   - Follow the installation prompts. Keep the default settings unless you need a specific configuration. Notably, when prompted to choose the default editor used by Git, you may select the one you prefer (e.g., Nano, Vim, or choose from installed applications like Notepad++).
   - Ensure that Git Bash and Git GUI are checked for installation.
   - Choose how Git handles line endings (recommended to use the default setting which is "Checkout Windows-style, commit Unix-style line endings").
   - Finish the installation.

3. **Verify Installation**:
   - Open Git Bash (search for it in your Start Menu).
   - Type `git --version` to ensure it displays the installed version of Git.

### macOS Installation

1. **Install with Homebrew** (recommended):
   - If you haven’t installed Homebrew yet, you can do so by pasting the following in your terminal:
     ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
     ```
   - After installing Homebrew, type the following command to install Git:
     ```bash
     brew install git
     ```

2. **Alternative: Install with Installer**:
   - Visit [https://git-scm.com/download/mac](https://git-scm.com/download/mac). This will redirect to the latest downloadable installer.
   - Open the downloaded file and follow the instructions to install Git.

3. **Verify Installation**:
   - Open the Terminal.
   - Type `git --version` to check if Git is installed properly.

### Ubuntu Linux Installation

1. **Update Your Package List**:
   - Open your terminal.
   - Update your package list with the following command:
     ```bash
     sudo apt update
     ```

2. **Install Git**:
   - Install Git by running:
     ```bash
     sudo apt install git
     ```

3. **Verify Installation**:
   - After the installation is complete, verify it by typing:
     ```bash
     git --version
     ```

### Arch Linux Installation

#### Using Pacman

1. **Update Your Package Database**:
   - Open your terminal.
   - Synchronize and update your package database with the following command:
     ```bash
     sudo pacman -Sy
     ```

2. **Install Git**:
   - Install Git using `pacman`:
     ```bash
     sudo pacman -S git
     ```

#### Using Pamac

1. **Update Your Package Database** (if using the CLI):
   - You can also update your system with `pamac`:
     ```bash
     pamac update
     ```

2. **Install Git**:
   - To install Git using the command line interface of Pamac, run:
     ```bash
     pamac install git
     ```

### Verify Installation for Arch Linux

- Confirm that Git is properly installed by checking its version:
  ```bash
  git --version
  ```

### Configure Git (For All Systems)

- Set up your Git user information (necessary for commits):
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your_email@example.com"
  ```

