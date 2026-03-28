# 🦞 PicoClaw Ecom-Researcher Agent

This is a specialized workspace for [PicoClaw](https://github.com/sipeed/picoclaw). It is optimized for mobile deployment (Termux) but managed via Mac.

## 📂 Features
- **Winning Product Logic**: Implements the professional 6-criteria research protocol.
- **SQL Storage**: Automatically logs findings to a local MariaDB database.
- **Low Resource**: Designed to run on older Android hardware via Termux.

## 🛠 Installation
1. **Clone the Repo** to your device:
   `git clone https://github.com/YOUR_USERNAME/picoclaw-ecom-agent.git`
2. **Setup Database**: 
   Ensure MariaDB is installed and run:
   `mariadb -u root -e "CREATE DATABASE IF NOT EXISTS ecom_research;"`
3. **Configure PicoClaw**: 
   Point your `config.json` to the `workspace/` folder in this repo.

## 🚀 Execution
Run the agent using the following environment override:
```bash
PICOCLAW_AGENTS_DEFAULTS_WORKSPACE=$(pwd)/workspace picoclaw agent

