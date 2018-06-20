---

copyright:
  years: 1994, 2018
lastupdated: "2018-06-06"

---
{:new_window: target="_blank"}

# Installing the EVault Exchange plug-in

The Exchange plug-in is installed with the Windows Agent on the host. Using the WebCC portal you can configure jobs, back up Oracle databases to a secure, remote vault, and restore Oracle databases. The Oracle Plug-in integrates into the existing architecture.

## Capabilities provided

- Ability to back up and restore Microsoft Exchange databases.

## Order the plug-in

1. Log in to the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}.
2. Click **Storage** > **Backup**.
3. Select your EVault account and click **Order Plugins**.
4. Select **EVault Plugin - Exchange** and click **Continue**.
5. Enter your Promo Code if you have one and click **Recalculate**.
6. The updated charges are displayed. Review your order.
7. Check the boxes to indicate that you read the Master Service Agreement and accept the 3rd Party Software Terms. 
8. Click **Place Order**.

## Install the Exchange plug-in

The Exchange Plug-in is installed during the Windows Agent 64-bit installation. The Plug-in can be installed when installing the Agent or it can be installed later, by re-running the installation with the Modify selection.

**Note**: Before installing the plug-in for your Microsoft Windows server, stop both EVault services in `services.msc`.  

1. Browse to `c:\installs\evault` folder and run the .exe file with the higher revision number.
2. At the language screen click **OK**
3. At the welcome screen click **Next**
4. Select the **Modify installation** and click **Next**.
5. Select the **Leave Unchanged** and click **Next**.
6. At the custom setup screen, select each plug-in you have purchased and select **This feature will be installed on ...**, then click **Next**.
7. Select the **Keep my current registration** radio button and click **Next**.
8. Click **Install**.
9. Once installed, please check to ensure that both services are enabled and running.
10. If WebCC is able to access (view) the database(s), then the installation was successful. 

## User guide

Connect to the {{site.data.keyword.BluSoftlayer_full}} network with {{site.data.keyword.BluVPN}} so that you can download the EVault Agent v8.0 for Microsoft Windows (64-bit) - Exchange Plug-in Guide.pdf from [Downloadable EVault Documentation](http://downloads.service.softlayer.com/evault/Documentation/){:new_window}. This guide describes how to back up and restore Microsoft Exchange databases using the Exchange plug-in. This guide also describes how to share a DR backup safeset so you can restore specific mailboxes, messages or other objects to a .pst file using the Granular Restore for Microsoft Exchange application.

