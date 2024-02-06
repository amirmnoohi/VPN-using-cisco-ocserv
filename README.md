
# **CISCO Project** [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://gitlab.com/limner/bank-tornadowebserver)

![GitHub release](https://img.shields.io/github/release/qubyte/rubidium.svg?style=for-the-badge)

![Compatibility Check](https://img.shields.io/badge/CENTOS_7-compatible-brightgreen)
![Compatibility Check](https://img.shields.io/badge/CENTOS_8-compatible-brightgreen)
![Compatibility Check](https://img.shields.io/badge/CENTOS_9-compatible-brightgreen)

This project integrates OCSERV with CENTOS, ensuring compatibility and successful deployment across CENTOS versions 7, 8, and 9.

Version: 3.0.0

Build: ![Build Status](https://img.shields.io/badge/build-passing-brightgreen)

Author: Amir Masoud Noohi

Language: Bash Script

# **Pre-Requirements**

This project requires the following:
- A VPS with a Dedicated IP and root Access
- CENTOS 7, 8, or 9 Operating System
- [optional] A valid SSL certificate

# **Requirements**

To run the `code.py` file, install the following packages for Python:

- radcli
- epel-release
- net-tools

```shell
yum install git -y
```

# **Installation**
## Step 0: Cloning

Start by cloning the project:

```shell
git clone https://github.com/amirmnoohi/VPN-using-cisco-ocserv.git && cd VPN-using-cisco-ocserv/
```

## Step 1: Grant Access

Grant execution access to `ocserv.sh` and make it runnable:

```shell
chmod +x ocserv.sh
sed -i -e 's/\r$//' ocserv.sh
./ocserv.sh
```

### Step 1.1: Edit Encryption Info

To modify encryption details, edit `ocserv.sh` using nano or vim:

- For organization and server IP address details, edit lines 138-139 and 153-154:
  - CN[138] = "Your Company Name"
  - organization[139] = "Your Company Name"
  - CN[153] = "Server IP Address or any A record to IP"
  - organization[154] = "Your Company Name"

## Step 2: Answering Questions

Run the script and answer the prompted questions for configuration and default settings. Wait for the script to complete.

## Step 3: Creating Users

Create a Cisco user with the following command:

```shell
$ ocpasswd -c /etc/ocserv/ocpasswd Name
```

This ensures broad compatibility across various CENTOS releases, facilitating a smooth setup process regardless of the specific CENTOS version you are using.

# **Usage**

For using this service, you can use Cisco Anyconnect for any platform. All necessary files are gathered [here](https://noohi.org/cisco).

# **Support**

For support, reach out to me at:
- Telegram: [@amirmnoohi](https://t.me/amirmnoohi)
- Gmail: [highlimner@gmail.com](mailto:highlimner@gmail.com)

# **License**

![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=for-the-badge)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2018 © [CISCO VPN SERVICE](https://github.com/amirmnoohi/VPN-using-cisco-ocserv).
