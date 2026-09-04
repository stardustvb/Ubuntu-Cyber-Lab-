
     #Ubuntu Cyber Security SOC Lab
     
     ## Overview

      This project documents my hands-on cybersecurity laboratory built using Ubuntu Server in VirtualBox.


      The purpose of this lab is to learn and demonstrate pratical Cyber security skills including:



       - Linux system administartion
       - Network configuration
       - SSH security
       - Firewall configuration 
       - Network monitoring
       - Security logging 
       - SIEM implementation
       - Threat detection
       - Incident response


        ## Lab Environment

        |---|---|
        | Ubuntu server | SOC server/monitored system |
        | Kali linux  | Security testing machine |
        | VirtualBox  | Virtual lab environment |
        | Github  | Documentation and version control |
        | UFW  | Host firewall |
        | SSH  | secure remote administration |
        | Wazhu  | SIEM / secuirty monitoring |



       ## Current Progress 
 
        - Ubuntu Server install
        - Network connectivity verified 
        - SSH service configured 
        - UFW firewall enabled 
        - SSH port 22 permitted 
        - Listening network services examined using `ss`
        - Git repository initialized 
        - Main Git branch configured 


         ## Learning Approach 

         All security testing will be performed inside my controlled virtual laboratory.
         
         The lab will gradually progress from system configuration to security monitoring, controlled attacks, log analysis, detection, 
         and incident response.
    
         ## Project Status 

          **phase 1: Linux server & Network Foundation - In Progress**
           
          More documentation, configuration evidence, and security investigations will be added as the lab develops.      

# Local Cybersecurity Practice Lab

A deliberately isolated, Docker-based practice environment for an Ubuntu virtual machine. It includes OWASP Juice Shop and WebGoat, two intentionally vulnerable training applications.

## Safety boundaries

- Run this only in your personal Ubuntu VM.
- Services bind to `127.0.0.1`, so they are accessible from the VM only.
- Do not change the port mappings to `0.0.0.0` or bridge them to your home/office network.
- Use snapshot/restore in VMware before experimenting.
- These applications are intentionally insecure: never use real credentials, files, or data in them.

## Prerequisites

- Ubuntu 22.04+ VM with at least 4 GB RAM and 20 GB free disk space
- Docker Engine with the Compose plugin
- Internet access from the VM for the first image download

## Setup on Ubuntu

1. Copy or clone this folder into the Ubuntu VM.
2. Run the installer:

   ```bash
   chmod +x scripts/install-docker-ubuntu.sh scripts/lab.sh
   ./scripts/install-docker-ubuntu.sh
   ```

3. Log out and back in (so Docker group access takes effect), then start the lab:

   ```bash
   ./scripts/lab.sh start
   ```

4. In the Ubuntu VM browser, open:

   - Juice Shop: http://127.0.0.1:3000
   - WebGoat: http://127.0.0.1:8080/WebGoat

## Everyday commands

```bash
./scripts/lab.sh status
./scripts/lab.sh logs
./scripts/lab.sh stop
./scripts/lab.sh reset   # deletes only the lab's containers and volumes
```

## VMware network setup

Use **NAT** networking for convenient updates, or **Host-only** networking for the most isolation. Avoid Bridged mode for this lab. Do not configure port forwarding from the host or router.

## Learning path

Start with Juice Shop's built-in Score Board and WebGoat's introductory lessons. Keep notes on what you learned, not reusable attack steps against third-party systems.

## Publish to GitHub

After creating an empty GitHub repository, run from this project directory:

```bash
git init
git add .
git commit -m "Add isolated Ubuntu cyber lab"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

