---
title: 常规故障排除
description: 本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的常规故障排除信息。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8c2ae3368db47363a65e8ecd6317bb0432829802
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748817"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="311fb-103">常规故障排除</span><span class="sxs-lookup"><span data-stu-id="311fb-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="311fb-104">本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的常规故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="311fb-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="311fb-105">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="311fb-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="311fb-106">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="311fb-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="311fb-107">当您尝试使用 Package Deployer 工具安装双写入包时，没有显示可用的解决方案</span><span class="sxs-lookup"><span data-stu-id="311fb-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="311fb-108">某些版本的 Package Deployer 工具与双写入解决方案包不兼容。</span><span class="sxs-lookup"><span data-stu-id="311fb-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="311fb-109">要成功安装包，请务必使用[版本 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) 或更高版本的 Package Deployer 工具。</span><span class="sxs-lookup"><span data-stu-id="311fb-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="311fb-110">安装 Package Deployer 工具后，请按照以下步骤安装解决方案包。</span><span class="sxs-lookup"><span data-stu-id="311fb-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="311fb-111">从 Yammer.com 下载最新的解决方案包文件。</span><span class="sxs-lookup"><span data-stu-id="311fb-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="311fb-112">下载包 zip 文件后，右键单击它，然后选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="311fb-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="311fb-113">选择 **解锁** 复选框，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="311fb-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="311fb-114">如果看不到 **解锁** 复选框，则说明 zip 文件已被解锁，您可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="311fb-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![属性对话框](media/unblock_option.png)

2. <span data-ttu-id="311fb-116">提取包 zip 文件，然后将所有文件复制到 **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="311fb-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 文件夹的内容](media/extract_package.png)

3. <span data-ttu-id="311fb-118">将所有复制的文件粘贴到 Package Deployer 工具的 **工具** 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="311fb-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="311fb-119">运行 **PackageDeployer.exe** 以选择 Dataverse 环境并安装解决方案。</span><span class="sxs-lookup"><span data-stu-id="311fb-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![“工具”文件夹的内容](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="311fb-121">在 Dataverse 中启用和查看插件跟踪日志以查看错误详细信息</span><span class="sxs-lookup"><span data-stu-id="311fb-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="311fb-122">**打开跟踪日志和查看错误所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="311fb-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="311fb-123">若要打开跟踪日志，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="311fb-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="311fb-124">在 Dynamics 365 中登录到模型驱动应用，打开 **设置** 页面，然后在 **系统** 下面选择 **管理**。</span><span class="sxs-lookup"><span data-stu-id="311fb-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="311fb-125">在 **管理** 页面中，选择 **系统设置**。</span><span class="sxs-lookup"><span data-stu-id="311fb-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="311fb-126">在 **自定义** 选项卡上，在 **插件和自定义工作流活动跟踪** 列中，选择 **所有** 启用插件跟踪日志。</span><span class="sxs-lookup"><span data-stu-id="311fb-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** column, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="311fb-127">如果只想在发生异常时记录跟踪日志，则可以改为选择 **异常**。</span><span class="sxs-lookup"><span data-stu-id="311fb-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="311fb-128">若要查看跟踪日志，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="311fb-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="311fb-129">在 Dynamics 365 中登录到模型驱动应用，打开 **设置** 页面，然后在 **自定义** 下面选择 **插件跟踪日志**。</span><span class="sxs-lookup"><span data-stu-id="311fb-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="311fb-130">找到 **类型名称** 列设置为 **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** 的跟踪日志。</span><span class="sxs-lookup"><span data-stu-id="311fb-130">Find the trace logs where the **Type Name** column is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="311fb-131">双击一个项目查看完整日志，然后在 **执行** 快速选项卡上，查看 **消息块** 文本。</span><span class="sxs-lookup"><span data-stu-id="311fb-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="311fb-132">启用调试模式来解决 Finance and Operations 应用中的实时同步问题</span><span class="sxs-lookup"><span data-stu-id="311fb-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="311fb-133">**查看错误所需的角色：** 系统管理员，源自 Dataverse 的双写入错误可能会出现在 Finance and Operations 应用中。</span><span class="sxs-lookup"><span data-stu-id="311fb-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="311fb-134">在某些情况下，错误消息的完整文本不可用，因为消息太长或包含个人身份信息 (PII)。</span><span class="sxs-lookup"><span data-stu-id="311fb-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="311fb-135">您可以按照以下步骤打开详细错误日志记录。</span><span class="sxs-lookup"><span data-stu-id="311fb-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="311fb-136">Finance and Operations 应用中的所有项目配置在 **DualWriteProjectConfiguration** 表中均具有 **IsDebugMode** 属性。</span><span class="sxs-lookup"><span data-stu-id="311fb-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** table.</span></span> <span data-ttu-id="311fb-137">使用 Excel 加载项打开 **DualWriteProjectConfiguration** 表。</span><span class="sxs-lookup"><span data-stu-id="311fb-137">Open the **DualWriteProjectConfiguration** table by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="311fb-138">打开表的一种简单方法是在 Excel 加载项中打开 **设计** 模式，然后将 **DualWriteProjectConfigurationEntity** 添加到工作表。</span><span class="sxs-lookup"><span data-stu-id="311fb-138">An easy way to open the table is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="311fb-139">有关详细信息，请参阅[在 Excel 中打开表数据并使用 Excel 加载项更新](../../office-integration/use-excel-add-in.md)。</span><span class="sxs-lookup"><span data-stu-id="311fb-139">For more information, see [Open table data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="311fb-140">将项目的 **IsDebugMode** 属性设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="311fb-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="311fb-141">运行产生错误的方案。</span><span class="sxs-lookup"><span data-stu-id="311fb-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="311fb-142">详细日志在 DualWriteErrorLog 表中提供。</span><span class="sxs-lookup"><span data-stu-id="311fb-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="311fb-143">要在表浏览器中查找数据，请使用以下 URL（根据需要替换 **XXX**）：</span><span class="sxs-lookup"><span data-stu-id="311fb-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="311fb-144">检查 Finance and Operations 应用的虚拟机上的同步错误</span><span class="sxs-lookup"><span data-stu-id="311fb-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="311fb-145">**查看错误所需的角色：** 系统管理员</span><span class="sxs-lookup"><span data-stu-id="311fb-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="311fb-146">登录 Microsoft Dynamics Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="311fb-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="311fb-147">打开选择要对其进行双写入测试的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="311fb-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="311fb-148">选择 **云托管的环境** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="311fb-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="311fb-149">使用远程桌面登录到 Finance and Operations 应用的虚拟机 (VM)。</span><span class="sxs-lookup"><span data-stu-id="311fb-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="311fb-150">使用 LCS 中显示的本地帐户。</span><span class="sxs-lookup"><span data-stu-id="311fb-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="311fb-151">打开事件查看器。</span><span class="sxs-lookup"><span data-stu-id="311fb-151">Open Event viewer.</span></span>
6. <span data-ttu-id="311fb-152">选择 **应用程序和服务日志 \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**。</span><span class="sxs-lookup"><span data-stu-id="311fb-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="311fb-153">查看最近错误的列表。</span><span class="sxs-lookup"><span data-stu-id="311fb-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="311fb-154">从 Finance and Operations 应用取消链接并链接另一个 Dataverse 环境</span><span class="sxs-lookup"><span data-stu-id="311fb-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="311fb-155">**取消环境链接所需的角色：** Finance and Operations 应用或 Dataverse 的系统管理员。</span><span class="sxs-lookup"><span data-stu-id="311fb-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="311fb-156">登录到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="311fb-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="311fb-157">转到 **工作区 \> 数据管理**，然后选择 **双写入** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="311fb-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="311fb-158">选择所有正在运行的映射，然后选择 **停止**。</span><span class="sxs-lookup"><span data-stu-id="311fb-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="311fb-159">选择 **取消链接环境**。</span><span class="sxs-lookup"><span data-stu-id="311fb-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="311fb-160">选择 **是** 以确认操作。</span><span class="sxs-lookup"><span data-stu-id="311fb-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="311fb-161">现在，您可以链接新环境。</span><span class="sxs-lookup"><span data-stu-id="311fb-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="311fb-162">无法查看销售订单行“信息”窗体</span><span class="sxs-lookup"><span data-stu-id="311fb-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="311fb-163">在 Dynamics 365 Sales 中创建销售订单时，单击 **+ 添加产品** 可能会将您重定向到 Dynamics 365 Project Operations 订单行窗体。</span><span class="sxs-lookup"><span data-stu-id="311fb-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="311fb-164">从该窗体无法查看销售订单行 **信息** 窗体。</span><span class="sxs-lookup"><span data-stu-id="311fb-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="311fb-165">**信息** 选项未出现在 **新订单行** 下方的下拉菜单中。</span><span class="sxs-lookup"><span data-stu-id="311fb-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="311fb-166">发生这种情况是因为您的环境中已经安装了 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="311fb-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="311fb-167">要重新启用 **信息** 窗体选项，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="311fb-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="311fb-168">导航到 **订单行** 表。</span><span class="sxs-lookup"><span data-stu-id="311fb-168">Navigate to the **Order Line** table.</span></span>
2. <span data-ttu-id="311fb-169">在窗体节点下找到 **信息** 窗体。</span><span class="sxs-lookup"><span data-stu-id="311fb-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="311fb-170">选择 **信息** 窗体并单击 **启用安全角色**。</span><span class="sxs-lookup"><span data-stu-id="311fb-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="311fb-171">将安全设置更改为 **向所有人显示**。</span><span class="sxs-lookup"><span data-stu-id="311fb-171">Change the security setting to **Display to everyone**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]