---
title: "还原数据库后重置财务申报数据市场"
description: "此主题介绍如何在还原 Microsoft Dynamics 365 for Finance and Operations 数据库之后重置财务申报数据市场。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="a7efe-103">还原数据库后重置财务申报数据市场</span><span class="sxs-lookup"><span data-stu-id="a7efe-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7efe-104">此主题介绍如何在还原 Microsoft Dynamics 365 for Finance and Operations 数据库之后重置财务申报数据市场。</span><span class="sxs-lookup"><span data-stu-id="a7efe-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="a7efe-105">如果你从备份恢复 Finance and Operations 数据库或从其他环境复制该数据库，则必须执行本主题中的步骤，以确保财务申报数据市场正确使用恢复的 Finance and Operations 数据库。</span><span class="sxs-lookup"><span data-stu-id="a7efe-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="a7efe-106">此流程中的步骤支持 Dynamics 365 for Operation May 2016 版本（应用程序版本 7.0.1265.23014 和财务申报版本 7.0.10000.4）及更高版本。</span><span class="sxs-lookup"><span data-stu-id="a7efe-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="a7efe-107">如果您的 Finance and Operations 版本较低，请联系我们的支持团队获取协助。</span><span class="sxs-lookup"><span data-stu-id="a7efe-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="a7efe-108">导出报表定义</span><span class="sxs-lookup"><span data-stu-id="a7efe-108">Export report definitions</span></span>
<span data-ttu-id="a7efe-109">首先，使用以下步骤导出报表设计器中的报表设计：</span><span class="sxs-lookup"><span data-stu-id="a7efe-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="a7efe-110">在报表设计器中，转至**公司** &gt; **构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="a7efe-111">选择要导出的构建基块组，然后单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="a7efe-112">对于 Finance and Operations，仅支持一个构建块组，即**默认**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="a7efe-113">选择要导出的报表定义：</span><span class="sxs-lookup"><span data-stu-id="a7efe-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="a7efe-114">要导出您的所有报表定义和关联的构建基块，请单击**“全选”**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="a7efe-115">要导出特定报表、行、列、树或维度集，请单击相应选项卡，然后选择要导出的项。</span><span class="sxs-lookup"><span data-stu-id="a7efe-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="a7efe-116">按住 Ctrl 键选择选项卡上的多个项目。当您选择要导出的报表时，系统将选择关联的行、列、树和维度集。</span><span class="sxs-lookup"><span data-stu-id="a7efe-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="a7efe-117">单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-117">Click **Export**.</span></span>
5.  <span data-ttu-id="a7efe-118">输入文件名，然后选择要用于保存所导出报表定义的安全位置。</span><span class="sxs-lookup"><span data-stu-id="a7efe-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="a7efe-119">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-119">Click **Save**.</span></span>

<span data-ttu-id="a7efe-120">可将文件复制或上传到安全位置，使其可在其他时间导入到其他环境中。</span><span class="sxs-lookup"><span data-stu-id="a7efe-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="a7efe-121">可在[使用 AzCopy 命令行实用程序传输数据](/azure/storage/storage-use-azcopy)中找到有关使用 Microsoft Azure 存储帐户的信息。</span><span class="sxs-lookup"><span data-stu-id="a7efe-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="a7efe-122">根据您的 Finance and Operations 协议，Microsoft 不提供存储帐户。</span><span class="sxs-lookup"><span data-stu-id="a7efe-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="a7efe-123">您必须购买存储帐户，或使用单独 Azure 订阅的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="a7efe-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="a7efe-124">请注意 Azure 虚拟机 D 盘的行为。</span><span class="sxs-lookup"><span data-stu-id="a7efe-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="a7efe-125">请勿将导出的构建块永久保留在此处。</span><span class="sxs-lookup"><span data-stu-id="a7efe-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="a7efe-126">有关临时驱动器的详细信息，请参阅[了解 Windows Azure 虚拟机上的临时驱动器](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)。</span><span class="sxs-lookup"><span data-stu-id="a7efe-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="a7efe-127">停止服务</span><span class="sxs-lookup"><span data-stu-id="a7efe-127">Stop services</span></span>
<span data-ttu-id="a7efe-128">使用远程桌面连接到环境中的所有计算机，并通过使用 services.msc 停止以下 Windows 服务：</span><span class="sxs-lookup"><span data-stu-id="a7efe-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="a7efe-129">万维网 Web 发布服务（在所有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="a7efe-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="a7efe-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="a7efe-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="a7efe-131">Management Reporter 2012 Process Service（仅限于 BI 计算机上）</span><span class="sxs-lookup"><span data-stu-id="a7efe-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="a7efe-132">这些服务具有到 Finance and Operations 数据库的开放连接。</span><span class="sxs-lookup"><span data-stu-id="a7efe-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="a7efe-133">重置</span><span class="sxs-lookup"><span data-stu-id="a7efe-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="a7efe-134">找到并下载最新的 MinorVersionDataUpgrade.zip 程序包</span><span class="sxs-lookup"><span data-stu-id="a7efe-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="a7efe-135">使用[下载最新的数据升级可部署程序包](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages)中的说明找到最新的 MinorVersionDataUpgrade.zip 包。</span><span class="sxs-lookup"><span data-stu-id="a7efe-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="a7efe-136">这些说明介绍如何找到并下载正确的数据升级包版本。</span><span class="sxs-lookup"><span data-stu-id="a7efe-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="a7efe-137">无需下载 MinorVersionDataUpgrade.zip 程序包即可升级。</span><span class="sxs-lookup"><span data-stu-id="a7efe-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="a7efe-138">只需完成“下载最新的数据升级可部署程序包”部分中的步骤即可检索 MinorVersionDataUpgrade.zip 程序包的副本，无需执行本文中的其他任何步骤。</span><span class="sxs-lookup"><span data-stu-id="a7efe-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="a7efe-139">对 Finance and Operations 数据库执行脚本</span><span class="sxs-lookup"><span data-stu-id="a7efe-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="a7efe-140">对 Finance and Operations 数据库（而非对财务申报数据库）运行以下脚本。</span><span class="sxs-lookup"><span data-stu-id="a7efe-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="a7efe-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="a7efe-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="a7efe-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="a7efe-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="a7efe-143">这些脚本确保用户、角色和更改跟踪设置正确无误。</span><span class="sxs-lookup"><span data-stu-id="a7efe-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="a7efe-144">执行 PowerShell 命令重置数据库</span><span class="sxs-lookup"><span data-stu-id="a7efe-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="a7efe-145">在 AOS 计算机上，作为管理员在 PowerShell 执行以下命令以重置 Finance and Operations 与财务报告之间的集成：</span><span class="sxs-lookup"><span data-stu-id="a7efe-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="a7efe-146">执行这些命令后，将请您输入“Y”予以确认。</span><span class="sxs-lookup"><span data-stu-id="a7efe-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="a7efe-147">参数的说明：</span><span class="sxs-lookup"><span data-stu-id="a7efe-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="a7efe-148">-Reason 的有效值为：SERVICING、BADDATA、OTHER。</span><span class="sxs-lookup"><span data-stu-id="a7efe-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="a7efe-149">-ReasonDetail 参数为自由文本。</span><span class="sxs-lookup"><span data-stu-id="a7efe-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="a7efe-150">原因和 reasonDetail 将记录到 telemetry/environment monitoring 中。</span><span class="sxs-lookup"><span data-stu-id="a7efe-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="a7efe-151">启动服务</span><span class="sxs-lookup"><span data-stu-id="a7efe-151">Start services</span></span>
<span data-ttu-id="a7efe-152">使用 services.msc 重新启动您前面停止的服务：</span><span class="sxs-lookup"><span data-stu-id="a7efe-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="a7efe-153">万维网 Web 发布服务（在所有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="a7efe-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="a7efe-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="a7efe-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="a7efe-155">Management Reporter 2012 Process Service（仅限于 BI 计算机上）</span><span class="sxs-lookup"><span data-stu-id="a7efe-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="a7efe-156">导入报表定义</span><span class="sxs-lookup"><span data-stu-id="a7efe-156">Import report definitions</span></span>
<span data-ttu-id="a7efe-157">使用导出期间创建的文件从报表设计器导入您的报表设计：</span><span class="sxs-lookup"><span data-stu-id="a7efe-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="a7efe-158">在报表设计器中，转至**公司** &gt; **构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="a7efe-159">选择要导出的构建基块组，然后单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a7efe-160">对于 Finance and Operations，仅支持一个构建块组，即**默认**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="a7efe-161">选择**默认**构建块，然后单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="a7efe-162">选择包含所导出报表定义的文件，然后单击**打开**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="a7efe-163">在“导入”对话框中，选择要导入的报表定义：</span><span class="sxs-lookup"><span data-stu-id="a7efe-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="a7efe-164">要导入所有报表定义和支持构建基块，请单击**全选**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="a7efe-165">要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。</span><span class="sxs-lookup"><span data-stu-id="a7efe-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="a7efe-166">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="a7efe-166">Click **Import**.</span></span>





