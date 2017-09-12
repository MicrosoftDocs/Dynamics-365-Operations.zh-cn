---
title: "还原数据库后重置财务申报数据市场"
description: "此主题介绍如何在还原 Microsoft Dynamics 365 for Finance and Operations 数据库之后重置财务申报数据市场。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: zh-cn
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="59531-103">还原数据库后重置财务申报数据市场</span><span class="sxs-lookup"><span data-stu-id="59531-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="59531-104">此主题介绍如何在还原 Microsoft Dynamics 365 for Finance and Operations 数据库之后重置财务申报数据市场。</span><span class="sxs-lookup"><span data-stu-id="59531-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="59531-105">如果你从备份恢复 Finance and Operations 数据库或从其他环境复制该数据库，则必须执行本主题中的步骤，以确保财务申报数据市场正确使用恢复的 Finance and Operations 数据库。</span><span class="sxs-lookup"><span data-stu-id="59531-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="59531-106">此流程中的步骤支持 Dynamics 365 for Operation May 2016 版本（应用程序版本 7.0.1265.23014 和财务申报版本 7.0.10000.4）及更高版本。</span><span class="sxs-lookup"><span data-stu-id="59531-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="59531-107">如果您的 Finance and Operations 版本较低，请联系我们的支持团队获取协助。</span><span class="sxs-lookup"><span data-stu-id="59531-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="59531-108">导出报表定义</span><span class="sxs-lookup"><span data-stu-id="59531-108">Export report definitions</span></span>
<span data-ttu-id="59531-109">首先，使用以下步骤导出报表设计器中的报表设计：</span><span class="sxs-lookup"><span data-stu-id="59531-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="59531-110">在报表设计器中，转至**公司** &gt; **构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="59531-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="59531-111">选择要导出的构建基块组，然后单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="59531-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="59531-112">对于 Finance and Operations，仅支持一个构建块组，即**默认**。</span><span class="sxs-lookup"><span data-stu-id="59531-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="59531-113">选择要导出的报表定义：</span><span class="sxs-lookup"><span data-stu-id="59531-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="59531-114">要导出您的所有报表定义和关联的构建基块，请单击**“全选”**。</span><span class="sxs-lookup"><span data-stu-id="59531-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="59531-115">要导出特定报表、行、列、树或维度集，请单击相应选项卡，然后选择要导出的项。</span><span class="sxs-lookup"><span data-stu-id="59531-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="59531-116">按住 Ctrl 键选择选项卡中的多个项。</span><span class="sxs-lookup"><span data-stu-id="59531-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="59531-117">当选择要导出的报表时，将选择关联的行、列、树和维度集。</span><span class="sxs-lookup"><span data-stu-id="59531-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="59531-118">单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="59531-118">Click **Export**.</span></span>
5.  <span data-ttu-id="59531-119">输入文件名，然后选择要用于保存所导出报表定义的安全位置。</span><span class="sxs-lookup"><span data-stu-id="59531-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="59531-120">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="59531-120">Click **Save**.</span></span>

<span data-ttu-id="59531-121">可将文件复制或上传到安全位置，使其可在其他时间导入到其他环境中。</span><span class="sxs-lookup"><span data-stu-id="59531-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="59531-122">可在[使用 AzCopy 命令行实用程序传输数据](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy)中找到有关使用 Microsoft Azure 存储帐户的信息。</span><span class="sxs-lookup"><span data-stu-id="59531-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="59531-123">根据您的 Finance and Operations 协议，Microsoft 不提供存储帐户。</span><span class="sxs-lookup"><span data-stu-id="59531-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="59531-124">您必须购买存储帐户，或使用单独 Azure 订阅的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="59531-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="59531-125">请注意 Azure 虚拟机 D 盘的行为。</span><span class="sxs-lookup"><span data-stu-id="59531-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="59531-126">请勿将导出的构建块永久保留在此处。</span><span class="sxs-lookup"><span data-stu-id="59531-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="59531-127">有关临时驱动器的详细信息，请参阅[了解 Windows Azure 虚拟机上的临时驱动器](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)。</span><span class="sxs-lookup"><span data-stu-id="59531-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="59531-128">停止服务</span><span class="sxs-lookup"><span data-stu-id="59531-128">Stop services</span></span>
<span data-ttu-id="59531-129">使用远程桌面连接到环境中的所有计算机，并通过使用 services.msc 停止以下 Windows 服务：</span><span class="sxs-lookup"><span data-stu-id="59531-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="59531-130">万维网 Web 发布服务（在所有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="59531-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="59531-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="59531-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="59531-132">Management Reporter 2012 Process Service（仅限于 BI 计算机上）</span><span class="sxs-lookup"><span data-stu-id="59531-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="59531-133">这些服务具有到 Finance and Operations 数据库的开放连接。</span><span class="sxs-lookup"><span data-stu-id="59531-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="59531-134">重置</span><span class="sxs-lookup"><span data-stu-id="59531-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="59531-135">找到并下载最新的 MinorVersionDataUpgrade.zip 程序包</span><span class="sxs-lookup"><span data-stu-id="59531-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="59531-136">使用[下载最新的数据升级可部署程序包](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package)中的说明找到最新的 MinorVersionDataUpgrade.zip 包。</span><span class="sxs-lookup"><span data-stu-id="59531-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="59531-137">这些说明介绍如何找到并下载正确的数据升级包版本。</span><span class="sxs-lookup"><span data-stu-id="59531-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="59531-138">无需下载 MinorVersionDataUpgrade.zip 程序包即可升级。</span><span class="sxs-lookup"><span data-stu-id="59531-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="59531-139">只需完成“下载最新的数据升级可部署程序包”部分中的步骤即可检索 MinorVersionDataUpgrade.zip 程序包的副本，无需执行本文中的其他任何步骤。</span><span class="sxs-lookup"><span data-stu-id="59531-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="59531-140">对 Finance and Operations 数据库执行脚本</span><span class="sxs-lookup"><span data-stu-id="59531-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="59531-141">对 Finance and Operations 数据库（而非对财务申报数据库）运行以下脚本。</span><span class="sxs-lookup"><span data-stu-id="59531-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="59531-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="59531-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="59531-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="59531-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="59531-144">这些脚本确保用户、角色和更改跟踪设置正确无误。</span><span class="sxs-lookup"><span data-stu-id="59531-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="59531-145">执行 PowerShell 命令重置数据库</span><span class="sxs-lookup"><span data-stu-id="59531-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="59531-146">直接在 AOS 计算机上执行以下命令，以便重置 Finance and Operations 与财务申报之间的集成：</span><span class="sxs-lookup"><span data-stu-id="59531-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="59531-147">以管理员身份打开 Windows PowerShell。</span><span class="sxs-lookup"><span data-stu-id="59531-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="59531-148">执行：F:</span><span class="sxs-lookup"><span data-stu-id="59531-148">Execute: F:</span></span>
3.  <span data-ttu-id="59531-149">执行：cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="59531-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="59531-150">执行：Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="59531-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="59531-151">执行：Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span><span class="sxs-lookup"><span data-stu-id="59531-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="59531-152">将请您输入“Y”予以确认。</span><span class="sxs-lookup"><span data-stu-id="59531-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="59531-153">参数的说明：</span><span class="sxs-lookup"><span data-stu-id="59531-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="59531-154">-Reason 的有效值为：SERVICING、BADDATA、OTHER。</span><span class="sxs-lookup"><span data-stu-id="59531-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="59531-155">-ReasonDetail 参数为自由文本。</span><span class="sxs-lookup"><span data-stu-id="59531-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="59531-156">原因和 reasonDetail 将记录到 telemetry/environment monitoring 中。</span><span class="sxs-lookup"><span data-stu-id="59531-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="59531-157">启动服务</span><span class="sxs-lookup"><span data-stu-id="59531-157">Start services</span></span>
<span data-ttu-id="59531-158">使用 services.msc 重新启动您前面停止的服务：</span><span class="sxs-lookup"><span data-stu-id="59531-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="59531-159">万维网 Web 发布服务（在所有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="59531-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="59531-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="59531-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="59531-161">Management Reporter 2012 Process Service（仅限于 BI 计算机上）</span><span class="sxs-lookup"><span data-stu-id="59531-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="59531-162">导入报表定义</span><span class="sxs-lookup"><span data-stu-id="59531-162">Import report definitions</span></span>
<span data-ttu-id="59531-163">使用导出期间创建的文件从报表设计器导入您的报表设计：</span><span class="sxs-lookup"><span data-stu-id="59531-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="59531-164">在报表设计器中，转至**公司** &gt; **构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="59531-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="59531-165">选择要导出的构建基块组，然后单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="59531-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="59531-166">对于 Finance and Operations，仅支持一个构建块组，即**默认**。</span><span class="sxs-lookup"><span data-stu-id="59531-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="59531-167">选择**默认**构建块，然后单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="59531-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="59531-168">选择包含所导出报表定义的文件，然后单击**打开**。</span><span class="sxs-lookup"><span data-stu-id="59531-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="59531-169">在“导入”对话框中，选择要导入的报表定义：</span><span class="sxs-lookup"><span data-stu-id="59531-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="59531-170">要导入所有报表定义和支持构建基块，请单击**全选**。</span><span class="sxs-lookup"><span data-stu-id="59531-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="59531-171">要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。</span><span class="sxs-lookup"><span data-stu-id="59531-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="59531-172">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="59531-172">Click **Import**.</span></span>





