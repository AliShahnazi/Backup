---

copyright:
  years: 1994, 2017
lastupdated: "2017-10-03"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Installing EVault Backup Client for VMware

Installing the EVault Backup client on a VMware server can be done through a series of commands in the shell or terminal within the target ESX server. This procedure outlines the steps required to install the EVault Backup client on your VMware server:

To install the Agent, download and copy the `Agent-VMware-ESX-Server-6.71.<version-info>.tar.gz` package onto the target ESX Server using the following command:

`wget -N http://downloads.service.softlayer.com/evault/archive/Agent-VMware-ESX-Server-6.71.2105.tar.gz`

**Note**:  You must perform the following steps locally on the target ESX Server.

1. Extract the files from the package. To do so, use this command (in which “PACKAGENAME” could be “Agent-VMware-ESX-Server-6.71”):
    `tar xvfz PACKAGENAME.tar.gz`
2. Go to the directory where you extracted the package.
3. Run the installation script:
    `# ./install.sh`

    **Note**:  The installation script will interactively prompt you for configuration information such as web registration (address, port number, and authentication) and log file name.
     
    - Enter the WebCC username for this server.
    - Enter the WebCC password for this server.
     
4. Enter the **EVault Backup Username** as the input for the prompt requesting the WebCC username. 
5. Enter the **EVault Backup Password** as the input for the prompt requesting the WebCC password.
6. When the installation finishes, a completion message will appear, and the Agent daemon will be running.


### Other Installation Notes:
The Install.log will be in the installation directory if the installation has succeeded.
For example: `/opt/BUAgent/Install.log`

If the installation fails and rolls back, the installation log will be in the `<Installation Failure directory>`.
If it fails and does not roll back, the installation log will be in the `<Installation Kit directory>`.

For more information, download the [VMware_Agent_User_Guide](http://downloads.service.softlayer.com/evault/Documentation/VMware_Agent_User_Guide.pdf){:new_window}. Be sure you are connected to the  {{site.data.keyword.BluVPN}} in order to view this link.