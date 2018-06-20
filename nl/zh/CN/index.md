---

copyright:
  years: 2014, 2018
lastupdated: "2018-06-05"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# EVault Backup 服务入门

通过备份，可确保数据安全地存储在设备外部，以防数据丢失情况发生。EVault Backup 是一种基于代理程序的自动备份系统，可通过 EVault WebCC 基于浏览器的管理实用程序进行管理，用于为用户提供在 {{site.data.keyword.BluSoftlayer_full}} 网络上一个或多个数据中心的服务器之间备份数据的方法。管理员可以将备份设置为按每小时、每日、每周或定制安排进行备份，备份目标可为完整系统、特定目录，甚或个别文件。附加插件支持与 Microsoft Exchange 和 Microsoft SQL 等软件以及其他类型的第三方软件兼容，并允许用户在必要时执行裸机复原。

## 订购 EVault 

有两种方法可购买 EVault Backup 服务：

- 订购服务器时购买 EVault
- 作为升级购买 EVault

### 订购服务器时购买 EVault

1. 登录到 [IBM Cloud 目录](https://console.bluemix.net/catalog/){:new_window}或 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}。
2. 订购按月计费的裸机服务器。您可以在[此处](https://console.bluemix.net/docs/bare-metal/baremetal-provision.html){:new_window}了解有关订购裸机服务器的更多信息。
3. 这会将您重定向到管理门户网站来完成订单。<br/>
  **注**：订购按小时计费的服务器时，EVault Backup 服务不可用。但是，日后可以作为升级添加该服务。 
4. 在**附加组件**部分下，选择一个 EVault 选项（“无”除外）。
6. 在页面底部，单击**添加到订单**。这将显示“结帐”页面。
7. 在**结帐**页面上，找到“主机名和域名”部分，并输入主机名和域名。您可以选择所需的任何主机名和域。
8. 在**结帐**页面右侧，单击**云服务条款**和**第三方服务协议**复选框。
9. 确认或输入付款信息，然后单击**提交订单**。这会将您重定向到具有供应订单号的屏幕。您可以打印此屏幕，因为这也是您的供应订单收据。<br/>**注**：您还可以通过单击**另存为报价**来保存此订单而不购买。

系统将向管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。登录到 {{site.data.keyword.cloud_notm}} 后，供应完成电子邮件包含*设备详细信息*页面的链接。您还可以直接登录到 {{site.data.keyword.slportal}}。

**确认 EVault 服务购买**
1. 在 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中，从主菜单中选择**设备** > **设备列表**。 
2. 找到您订购的新服务器。
  - 如果 URL 旁边有“时钟”图标，说明您需要稍候才能继续确认 EVault 购买。您可以刷新此页面，以查看新服务器的更新状态。“时钟”图标不再显示时，您可以继续执行后续步骤以确认 EVault 服务购买。
  - 服务器的“时钟”图标不再显示时，请单击相应链接（服务器的 URL）以转至**设备详细信息**页面。 
3. 单击**存储**选项卡以显示 EVault 信息。
4. 检查 EVault 部分，并验证 EVault 购买过程中选择的大小是否显示在 EVault 链接旁边。

### 作为升级购买 EVault

**选择要安装 EVault 的服务器**
1. 登录到 [IBM Cloud 目录](https://console.bluemix.net/catalog/){:new_window}或 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}。
2. 从主菜单中选择**设备** > **设备列表**。找到要添加 EVault 服务的设备。
3. 单击设备名以转至“设备详细信息”页面。

**添加（购买）EVault 服务**
1. 单击**存储**选项卡，然后找到页面底部附近的 EVault 部分。
2. 单击**添加**链接。
3. 在弹出窗口中，选择一个位置或接受缺省值，然后选择大小。
4. 单击**继续**。
5. 如果您同意条款和条件，请单击相应复选框。
6. 单击**下单**。

**确认 EVault 服务购买**
1. 刷新**设备详细信息**页面，并确保已选择**存储**选项卡。
2. 检查 EVault 部分，并验证 EVault 购买过程中选择的大小是否显示在 EVault 链接旁边。<br /> **注**：如果 EVault 存储器大小的容量仍然显示为零，说明可能需要再次刷新页面。 

## 在 {{site.data.keyword.slportal}} 中访问和查看 EVault Backup 存储器详细信息

可随时使用 {{site.data.keyword.slportal}} 来查看与 EVault Backup 服务相关的存储器详细信息。可查看的详细信息包括与所选 EVault Backup 服务关联的密码、存储地址和使用情况。 

1. 要访问 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中的 **EVault Backup 存储器**屏幕，请使用您的唯一凭证登录。
2. 单击**存储**，然后从下拉列表中选择**备份**。
2. 单击所需 EVault Backup 所在行上的任意位置以查看其存储器详细信息。在此视图中，无法查看“密码”。请继续执行下一步以查看与 EVault Backup 服务关联的密码。
3. 单击**密码**字段旁边的**显示**复选框，以查看所选 EVault Backup 服务的密码。

对于许多 {{site.data.keyword.BluSoftlayer_full}} 产品和服务，{{site.data.keyword.slportal}} 内的密码存储功能仅用于存储或跟踪密码，因此对 {{site.data.keyword.slportal}} 中的密码进行的更改不会应用于这些产品或服务。但对于 EVault Backup，情况_并非_如此。对 {{site.data.keyword.slportal}} 内的 EVault Backup 密码进行的更改将应用于该服务本身。更改密码时，请牢记更改密码会直接影响您的服务。要重置密码，请执行[如何在 {{site.data.keyword.slportal}} 中更改 EVault Backup 密码](/docs/infrastructure/Backup/change-password-evault-backup-service.html)中的步骤。

## 安装 EVault 代理程序

以下操作系统上支持 EVault 代理程序：

### Windows
 - Windows Server 2012 R2
 - Windows Server 2012
 - Windows Server 2008 R2
 - Windows Server 2008

### Linux
 - CentOS 7.x
 - CentOS 6.x
 - Debian GNU/Linux 9.x
 - Debian GNU/Linux 8.x
 - Debian GNU/Linux 7.x
 - Red Hat Enterprise Linux 7.x
 - Red Hat Enterprise Linux 6.x
 - Ubuntu Linux 16.04
 - Ubuntu Linux 14.04

请遵循适用于您操作系统的指示信息：
- [在 Linux 中安装 EVault Backup 客户机](install-evault-backup-client-linux.html)
- [在 Windows 中安装 EVault Backup 客户机](install-evault-backup-client-windows.html)
- [在 Windows 2016 中安装 EVault Backup 客户机](install-evault-windows2016.html)

## 访问 WebCentralControl (WebCC) for EVault backup

WebCentralControl (WebCC) 是与 {{site.data.keyword.BluSoftlayer_full}} 提供的任何 EVault Backup 服务进行交互时使用的客户机。WebCC 是一种基于浏览器的客户机，在我们的专用网络上运行，支持对任何 EVault Backup 服务进行完全控制，包括配置和复原。执行以下步骤来访问 WebCC for EVault Backup。

1. 通过 VPN 访问专用网络。<br/>
    **注**：WebCC 无法通过公用网络进行访问。必须建立 VPN 连接才能访问 WebCC。
2. 访问 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中的“EVault Backup 存储器”屏幕。
3. 单击所需 EVault Backup 所在行上的任意位置以展开视图。
3. 单击 **WebCC 登录**，以在浏览器中启动 WebCC 客户机。

## 在 WebCC 中配置 EVault 代理程序

订购了 EVault 服务并且在服务器上安装了代理程序之后，即可以开始创建数据备份。执行以下步骤来配置代理程序、保留安排以及启动第一个备份作业。

1. 登录到 WebCC。
2. 单击**所有代理程序** > **未配置的代理程序**。
3. 单击**这是我要配置的新代理程序**链接。逐步完成该过程并指定以下内容：
   1. 代理程序配置 - 提供代理程序描述，然后单击**下一步**。
   2. 作业类型选择 - 输入作业名、作业描述和备份源类型，然后单击**下一步**。
   3. 选择 - 选择目录，然后单击**包含...**
   4. 选项 - 提供密码
   5. 安排 - 单击**添加**以创建安排，然后单击**下一步**。
   6. 选择缺省保险库，然后单击**确定**。
   7. 单击**保存**。
4. 创建保留安排：
   1. 选择**编辑** > **代理程序设置**。
   2. 单击**添加**。
   3. 填写保留时间详细信息。
   4. 单击**确定**。
   5. 单击**保存**。
   **注** - 请在[此处](evault-backup-faq.html#how-do-the-retention-schemes-work-)阅读有关保留方案如何工作的更多信息。
5. 运行代理程序并启动备份。
   1. 单击**所有代理程序**，然后选择刚才配置的代理程序。
   2. 单击**运行备份**。
   3. 确认“目标”并选择保留方案。
   4. 单击**启动备份**。您可以在进程运行时查看备份详细信息。
   5. 完成备份后，单击**关闭**。
   
**注**：请在[此处](configure-simple-file-backup-linux.html)阅读有关如何在 Linux 上配置简单文件级别备份的更多信息。

## 后续情况

WebCC 的系统已完全记录，并且在 WebCC 内提供了对该应用程序的支持。单击右上角的**帮助**（用含有白色问号的蓝色圆圈表示）。单击弹出框左侧导航栏中的任何文章或主题以查看更多信息。

