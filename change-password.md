---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

keywords: EVault, Carbonite, Backup, password, password reset

subcollection: Backup

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}

# Changing the password for the backup service
{: #changePassword}

Each {{site.data.keyword.backup_full}} service has an associated password that is used to access the vault within the {{site.data.keyword.backup_notm}} portal.

For many {{site.data.keyword.BluSoftlayer_full}} products and services, the password storage feature within the {{site.data.keyword.slportal}} is used solely for the tracking of the password. For those products and services, the changes that are made to the password within the {{site.data.keyword.slportal}} aren't applied to the product or service. It's **not** the case for {{site.data.keyword.backup_notm}}.

Changes that are made to the {{site.data.keyword.backup_notm}} password within the {{site.data.keyword.slportal}} are made to the service itself. When you change your password, keep in mind that it impacts your service directly.
{:important}

## Changing the password

1. Log in to the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/catalog/){:new_window} and click the **menu** icon on the upper left. Select **Classic Infrastructure**.<br/>
   Alternatively, you can log in to the [{{site.data.keyword.slportal}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){:new_window}.
2. Click **Storage** > **Backup** to display the servers with backup service.
3. Click anywhere on the row of the vault to expand the view.
4. Click **Show** to view the current password.
5. Enter the new password in the **Password** field.
6. Click **Update**.
