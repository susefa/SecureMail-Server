# SecureMail-Server
This project involved setting up a secure email server using Postfix and Dovecot on Rocky Linux in a virtual environment.

# Description
This is a university project, everything was documented in the documentation that is the repository.

The goal was to implement a secure and fully functional mail server while integrating additional services for encryption, logging, and troubleshooting. This project was built on VMWARE using two virtual machines.

* Rocky Linux (Server) - Hosting email services, DNS, DHCP, and centralized logging.
* Ubuntu (Client) - Acting as an email client for testing and validation.

The main objectives of this project were to:
* Learn Linux system administration and network configurations
* Set up and configure email server
* Implement SSL/TLS encryption for secure communication
* Configure DNS & DHCP for domain name resolution and dynamic addressing
* Set up centralized logging using Auditd and Syslog
* Troubleshoot and test email functionality and security

# Installation & Configuration
To replicate this project, these software tools are required:
1. **Virualization Software**: VMware, VirtualBox or Proxmox
2. **Operating Systems**:
   * Rocky Linux (Server)
   * Ubuntu Linux (Client)
3. **Software & Services**:
   * Postfix & Dovecot - For email services
   * OpenSSL - for SSL/TLS encryption
   * Auditd & Syslog - For centralized logging
   * Vsftpd (FTP Server) - For secure file transfers

I performed the following to achieve a fully functional and secure email system:
1. **Network Setup**:
   * Configured static IP addresses on Rocky Linux and Ubuntu
   * Set up Fully Qualified Domain Name
   * Installed and configured DNS and DHCP
2. **Email Server Setup**:
   * Installed Postfix (MTA) to handle outoing emails
   * Installed Dovecot to provide IMAP/POP3 support
   * Configured mail directories, authentication, and message storage
3. **SSL/TLS Encryption**:
   * Generated self-signed SSL certificates using OpenSSL
   * Configured Postfix & Dovecot to enfore encrypted connections
4. **FTP with TLS**:
   * Installed and configured vsftpd
   * Enabled TLS encryption for secure file transfers
5. **Centralized Logging**:
   * Installled Auditd and Syslog on both server and client
   * Configured remote log forwarding to centralized logging server

# Troubleshooting & Testing:
While making the project I encountered several issues, including:
1. Email Delivery Failures - Fixed incorrect SMTP authentication settings and misconfigured mail queue.
2. Logging Issues - Resolved missing logs by adjusting Auditd and Syslog settings, ensuring logs were properly stored and forwarded.
3. SSL/TLS Handshake Failures - Fixed issues with mismatched SSL certificates and ensured encrypted connections between the client and server.

# Author
Umidjon Eshchanov (susefa)
