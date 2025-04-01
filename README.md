# Gensyn AI Testnet Node Setup Guide

Welcome! This guide will walk you through setting up and running a **Gensyn AI Testnet Node** on your system.

## 📌 System Requirements

Before proceeding, ensure your system meets the following minimum requirements:

| Component        | Minimum Requirement                              |
|-----------------|--------------------------------------------------|
| **CPU**         | `arm64` or `amd64`                               |
| **RAM**         | 16 GB                                            |
| **GPU (Optional)** | `RTX 3090`, `RTX 4090`, `A100`, `H100`        |
| **Python**      | Version 3.10 or higher                           |

> **Note:** macOS users may need to upgrade their Python version manually.

---

## 🚀 Installation Steps

To get started, follow these steps:

### 1️⃣ Install Node.js and npm  
If you haven't installed them yet, run:

```bash
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
```

### 2️⃣ Install Required Dependencies  
Update your package list and install essential dependencies:

```bash
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl screen git yarn
```

Set up **Yarn** for package management:

```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install -y yarn
```

### 3️⃣ Clone the Repository  
Now, get the project files:

```bash
git clone https://github.com/zunxbt/rl-swarm.git
cd rl-swarm
```

### 4️⃣ Start a Screen Session  
To ensure the node runs in the background:

```bash
screen -S gensyn
```

### 5️⃣ Launch the Node  
Activate a virtual environment and start the node:

```bash
python3 -m venv .venv
source .venv/bin/activate
./run_rl_swarm.sh
```

Once the process starts successfully, you should see logs indicating the node is running.

---

## 🔧 Troubleshooting

If you encounter any issues, here are some common solutions:

- **Problem:** The script doesn’t execute properly.  
  **Solution:** Ensure you have all dependencies installed and Python is updated.  

- **Problem:** Node fails to sync.  
  **Solution:** Restart the node and check your internet connection.  

For more support, refer to the [official documentation](https://github.com/gensyn-ai/rl-swarm) or ask for help in the community.

---

## 🤝 Contributing

We welcome contributions! If you'd like to improve this guide or the project, fork the repository and submit a pull request.
