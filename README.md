# Wazuh-Setup
Wazuh Quickstart is a hassle-free installation method designed to streamline the setup process of Wazuh, a leading open-source security information and event management (SIEM) solution. 

# Wazuh Quickstart Installation Guide
## Prerequisites
A Linux server (Ubuntu, CentOS, Debian, etc.) with internet access.
Root or sudo access to the server.
## Steps

Update System Packages
```bash
sudo apt-get update
```
Download the Quickstart script to your server:

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh && sudo bash ./wazuh-install.sh -a
```

Run the script to install Wazuh
Once the assistant finishes the installation, the output shows the access credentials and a message that confirms that the installation was successful.

```bash
INFO: --- Summary ---
INFO: You can access the web interface https://<wazuh-dashboard-ip>
    User: admin
    Password: <ADMIN_PASSWORD>
INFO: Installation finished.
```

Access Wazuh Web Interface

Start and Enable Services
Use:- 

``` bash
sudo systemctl enable wazuh-manager
sudo systemctl start wazuh-manager
```


Once the installation is complete, open a web browser and navigate to http://your-server-ip:5601. The Wazuh Kibana app will guide you through the setup process.
