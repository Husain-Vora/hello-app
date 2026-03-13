# Signiance DevOps Assignment - Group 7 (B1)

## Architecture
- **Web Server:** Nginx (Reverse Proxy)
- **Runtime:** Node.js managed by PM2
- **Infrastructure:** AWS EC2 (Ubuntu 22.04)
- **CI/CD:** GitHub Actions (Automated Deployment via SSH)

## How to Access
- **Live IP:** http://13.60.203.166
- **Domain (Pending DNS):** https://husain.signiance.com

## Pipeline Logic
1. Code is pushed to `main` branch.
2. GitHub Action triggers an SSH handshake with EC2.
3. Server pulls latest code, runs `npm install`, and restarts the process via `pm2`.