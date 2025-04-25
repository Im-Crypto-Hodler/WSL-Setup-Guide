# ⚙️ WSL Setup Guide for Windows

Welcome to the ultimate beginner-friendly guide to setting up **WSL (Windows Subsystem for Linux)** on your Windows machine! This repo includes step-by-step instructions, automation scripts, visual guides, and optional Docker setup for developers who want a solid Linux dev environment on Windows.

## 🚀 Features
- 🔧 WSL installation and configuration
- 🛠️ Git setup and GitHub SSH key integration
- 📦 Essential tools for development
- 🐳 Optional Docker installation
- 📚 Organized folder structure with automation scripts and screenshots

## 🔍 Prerequisites
- Windows 10 (Build 19041 or higher) or Windows 11
- Administrative access to your PC
- Minimum 4GB RAM and 10GB free disk space

## 🚀 Detailed Setup Guide

### 1️⃣ Enable WSL
1. Open PowerShell as Administrator
2. Run:
   ```powershell
   wsl --install
   ```
3. Restart your computer when prompted

### 2️⃣ Install a Linux Distribution
1. Choose a distribution through:
   ```powershell
   wsl --install -d Ubuntu
   ```
   (Replace Ubuntu with your preferred distro if needed)
2. Launch from Start menu and set up your username/password

### 3️⃣ Update & Upgrade Packages
```bash
sudo apt update && sudo apt upgrade -y
```

### 4️⃣ Set Up Git
```bash
# Install Git
sudo apt install git -y

# Configure your identity
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 5️⃣ Connect to GitHub
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Display your public key to copy
cat ~/.ssh/id_ed25519.pub

# Test connection after adding to GitHub
ssh -T git@github.com
```

### 6️⃣ Install Essential Tools
```bash
sudo apt install build-essential curl wget -y
```

### 7️⃣ Optional: Install Docker
```bash
# Install Docker
sudo apt install docker.io -y

# Add user to Docker group
sudo usermod -aG docker $USER

# Restart WSL (in PowerShell)
# wsl --shutdown
```

## 📂 Repository Structure
```
wsl-setup-guide/
│
├── README.md              # Main documentation and overview
│
├── setup/                 # Detailed guides
│   ├── install-wsl.md     # WSL installation steps
│   ├── install-git.md     # Git setup instructions
│   ├── connect-github.md  # GitHub SSH connection guide
│   ├── essential-tools.md # Development tools setup
│   └── docker-setup.md    # Docker installation guide
│
├── scripts/               # Automation scripts
│   ├── wsl-setup.sh       # Main setup script
│   ├── git-setup.sh       # Git configuration script
│   └── docker-setup.sh    # Docker installation script
│
└── images/                # Visual guides
    ├── wsl-setup.png      # WSL installation screenshots
    ├── git-config.png     # Git configuration example
    └── github-ssh-key.png # Adding SSH key to GitHub
```

## 💡 Tips & Tricks
- Use VSCode's Remote WSL extension for seamless development
- Access Windows files from WSL at `/mnt/c/`
- Speed up file operations by keeping projects in the WSL filesystem

## 📲 Join Us

![image](https://github.com/user-attachments/assets/8fe3a552-e45c-4005-a6b7-69ab5ece0668)

- 🐦 **X**: [For everything](https://x.com/imcryptohodler)  
- 💬 **Telegram**: [Join](https://t.me/Cryptoland007)  
- 📰 **Substack**: [For exclusive news](https://substack.com/@imcryptohodler)  
- 🎥 **YouTube**: [Tutorial](https://www.youtube.com/@Iamcryptohodler)  
- ✍️ **Medium**: [Article](https://medium.com/@I_am_crypto_hodler)

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
