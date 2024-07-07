# Create SSH Keys

### For Windows

1. **Install Git Bash**: If not already installed, download and install Git for Windows from [gitforwindows.org](https://gitforwindows.org/), which includes Git Bash.
    
2. **Generate SSH Key**:
    
    - Open Git Bash.
    - Run `ssh-keygen -t ed25519 -C "your_email@example.com"`, replacing `your_email@example.com` with your GitHub email address.
    - When prompted to "Enter a file in which to save the key," press Enter to use the default file location.
    - At the prompt, enter a secure passphrase (optional but recommended).
      
3. **Add SSH Key to ssh-agent**:
    
    - Start the ssh-agent in the background by running `eval "$(ssh-agent -s)"`.
    - Add your SSH private key to the ssh-agent by running `ssh-add ~/.ssh/id_ed25519`.
      
4. **Copy SSH Key to GitHub**:
    
    - Run `clip < ~/.ssh/id_ed25519.pub` to copy the SSH public key to your clipboard.
    - Go to GitHub, navigate to **Settings** > **SSH and GPG keys** > **New SSH key**, paste your key into the field, give it a descriptive title, and click **Add SSH key**.

### For macOS

1. **Open Terminal**: You can find Terminal in Applications > Utilities.
    
2. **Generate SSH Key**:
    
    - Run `ssh-keygen -t ed25519 -C "your_email@example.com"`.
    - Follow the on-screen instructions to save the key and enter a passphrase (optional).
      
3. **Add SSH Key to ssh-agent**:
    
    - Ensure ssh-agent is running: `eval "$(ssh-agent -s)"`
    - If you are using macOS Sierra 10.12.2 or later, update your `~/.ssh/config` file to automatically load keys and store passphrases in your keychain:
        
        bash
        
        Copy code
        
        `Host *   AddKeysToAgent yes   UseKeychain yes   IdentityFile ~/.ssh/id_ed25519`
        
    - Add your SSH key to the ssh-agent: `ssh-add -K ~/.ssh/id_ed25519`
      
4. **Copy SSH Key to GitHub**:
    
    - Run `pbcopy < ~/.ssh/id_ed25519.pub` to copy the public key.
    - Paste this key into GitHub under **Settings** > **SSH and GPG keys** > **New SSH key**.

### For Linux

1. **Open Terminal**.
    
2. **Generate SSH Key**:
    - Run `ssh-keygen -t ed25519 -C "your_email@example.com"`.
    - Follow the instructions to save the key and create a passphrase (optional).
      
3. **Add SSH Key to ssh-agent**:
    
    - Start the ssh-agent: `eval "$(ssh-agent -s)"`
    - Add the SSH key: `ssh-add ~/.ssh/id_ed25519`
      
4. **Copy SSH Key to GitHub**:
    
    - Run `xclip -sel clip < ~/.ssh/id_ed25519.pub` (you might need to install `xclip` if it's not already installed).
    - Paste this key into your GitHub account settings under **SSH and GPG keys** > **New SSH key**.