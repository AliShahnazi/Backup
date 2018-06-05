---

copyright:
  years: 1994, 2018
lastupdated: "2018-05-31"

---
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Backup and Restore from one VSI to another within the same datacenter

Sometimes you want to restore data to a different server in the same data center. These instructions will help you accomplish this task. This procedure only applies to file-level restores of non-OS files. To restore a system image, follow the [Windows BMR](restoring-evault-bmr-system-volume-image.html) instructions.

This process includes reregistering the EVault agent on the second server to access the EVAult location of the first server and performing a **Restore from another Computer**.


## Pre-requisites

- Server1 and Server 2 must have the same OS. Cross-platform restores aren't supported.
- Server1 and Server2 must have configured EVAult agents. To learn how to configure the EVault agents, click [here](index.html#configuring-evault-agent-in-webcc)
- A backup job for Server1 produced a backup to the Server1 EVault location.

**Note**: Disable all Schedule tasks on both servers to avoid any conflicts. 

## Start WebCC of Server2

**Note**: Remember to start your {{site.data.keyword.BluVPN}} connection to get access to the {{site.data.keyword.BluSoftlayer_full}} private network or the WebCC links won't work.

1. Log in to the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} and click **Storage** > **Backup** from the main menu to display the servers with EVault backup service. 
2. Select Server2. Click the right-pointing expansion arrow to reveal the WebCC link.
3. Click **WebCC Login** to start the WebCC client in your browser.

## Reregister the EVault:
1. Click **All Agents** and open the specific agent you want to modify.
2. Click **Edit** and select *Vault Settings".
3. Click **Reregister** to connect Server1 to Server2.
4. On the **Re-register Vault** screen for the **Use a Vault Profile** entry select **Enter Vault Settings**.
5. Enter the Vault Name, which is the same as the EVault name of Server1.
6. Enter credentials for Server1 to log in to the EVault for Server1.
7. Click **Load Computers**, this displays the servers that are attached to the vault location.
8. Click **Save Changes**.
9. When prompted, click **Yes** to confirm the reregistration of the EVault.

## Run the Backup Job from Server1 as the Restore Job on Server2

1. Click **All Agents**. <br/> **Note**: You may need to refresh the page to see the jobs defined on Server1 as accessible/synchronized under the Server 2 **Jobs** tab
2. Hover over **Advanced** and select **Restore from another Computer**.
3. On the **Restore From Another Computer** screen, make the following selections:
  - Vault: this entry should default to Server1's EVault
  - Computer: select Server1 as the backup computer to restore from. 
  - Job: select the backup job from Server1.
4. Click **Next**
5. Confirm Source information
  - **Safeset location** should be the Vault location for Server1.
  - In the **Select a Backup Version** section, the backup version specified should be your backup from Server1
  - The encryption password should be the password you used while performing the backup on Server1.
6. Click **Next**
7. Data Selection: select which files need to be restored from the Server1 backup. Select the check boxes next to the files and directories you want to include, then click **Include** to save your choices.
8. Click **Next** to move to the restore options.
9. In Options:
  - Destination: Select **Restore to original location**
  - File Overwrite: Select **Overwrite existing files**
10. Click **Run Restore**.
11. The Process Detail screen displays the status of the restore job.


## Verify the restore

1. Connect to the root of Server2 through SSH.
2. List the files including all directory entries in a long format.
  ```
  ls -la
  ```
  {: pre}
  
3. Compare the output.
  
## Resume normal backup schedule.

1. When the restore is complete, remove the registration information of server1, where the data was restored from. 
2. Enter the current server2 registration and enable Schedule tasks.
 

  

 
 
  
  