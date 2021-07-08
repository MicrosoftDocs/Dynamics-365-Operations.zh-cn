---
title: 开始使用全球库存核算
description: 本主题介绍了如何开始使用全球库存核算。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301690"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="7eb30-103">开始使用全球库存核算</span><span class="sxs-lookup"><span data-stu-id="7eb30-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="7eb30-104">全球库存核算使您可以在已设置的全球库存核算分类帐中执行多个库存核算。</span><span class="sxs-lookup"><span data-stu-id="7eb30-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="7eb30-105">您必须将每个全球库存核算分类帐与一个 *惯例* 关联。</span><span class="sxs-lookup"><span data-stu-id="7eb30-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="7eb30-106">惯例是以下几种会计政策的集合：</span><span class="sxs-lookup"><span data-stu-id="7eb30-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="7eb30-107">成本对象</span><span class="sxs-lookup"><span data-stu-id="7eb30-107">Cost object</span></span>
- <span data-ttu-id="7eb30-108">输入度量依据</span><span class="sxs-lookup"><span data-stu-id="7eb30-108">Input measurement basis</span></span>
- <span data-ttu-id="7eb30-109">成本流假设</span><span class="sxs-lookup"><span data-stu-id="7eb30-109">Cost flow assumption</span></span>
- <span data-ttu-id="7eb30-110">成本元素</span><span class="sxs-lookup"><span data-stu-id="7eb30-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="7eb30-111">即使在打开全球库存核算后，仍然可以按常规方式在 Microsoft Dynamics 365 Supply Chain Management 中执行库存核算。</span><span class="sxs-lookup"><span data-stu-id="7eb30-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="7eb30-112">全球库存核算是一个加载项。</span><span class="sxs-lookup"><span data-stu-id="7eb30-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="7eb30-113">若要使其功能可用，必须从 Microsoft Dynamics Lifecycle Services (LCS) 进行安装。</span><span class="sxs-lookup"><span data-stu-id="7eb30-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7eb30-114">您可以选择在测试环境中对其进行评估，然后再将其打开以用于生产环境。</span><span class="sxs-lookup"><span data-stu-id="7eb30-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="7eb30-115">全球库存核算目前不支持 Supply Chain Management 中内置的所有成本管理功能。</span><span class="sxs-lookup"><span data-stu-id="7eb30-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="7eb30-116">因此，重要的是要评估当前可用的功能集是否满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="7eb30-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="7eb30-117">如何获得全球库存核算公开预览版</span><span class="sxs-lookup"><span data-stu-id="7eb30-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7eb30-118">若要使用全球库存核算，您必须具有启用了 LCS 的高可用性环境（而不是 OneBox 环境）。</span><span class="sxs-lookup"><span data-stu-id="7eb30-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="7eb30-119">此外，您必须运行 Supply Chain Management 版本 10.0.19 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="7eb30-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="7eb30-120">若要注册全球库存核算公开预览版，请将您的 LCS 环境 ID 通过电子邮件发送至[全球库存核算团队](mailto:GlobalInventoryAccounting@service.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="7eb30-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="7eb30-121">在您获得该计划的批准后，团队将向您发送一封跟进电子邮件，其中包含全球库存核算测试密钥和您的服务终结点。</span><span class="sxs-lookup"><span data-stu-id="7eb30-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="7eb30-122">收到测试密钥后，您可以[安装加载项](#install)。</span><span class="sxs-lookup"><span data-stu-id="7eb30-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="7eb30-123">许可授权</span><span class="sxs-lookup"><span data-stu-id="7eb30-123">Licensing</span></span>

<span data-ttu-id="7eb30-124">全球库存核算与可用于 Supply Chain Management 的库存核算的标准功能一起获得许可。</span><span class="sxs-lookup"><span data-stu-id="7eb30-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="7eb30-125">您无需购买其他许可证即可使用全球库存核算。</span><span class="sxs-lookup"><span data-stu-id="7eb30-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7eb30-126">先决条件</span><span class="sxs-lookup"><span data-stu-id="7eb30-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="7eb30-127">设置 Microsoft Power Platform 集成</span><span class="sxs-lookup"><span data-stu-id="7eb30-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="7eb30-128">您必须先通过执行以下步骤与 Microsoft Power Platform 集成，才能启用加载项功能。</span><span class="sxs-lookup"><span data-stu-id="7eb30-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="7eb30-129">打开要在其中添加服务的 LCS 环境。</span><span class="sxs-lookup"><span data-stu-id="7eb30-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="7eb30-130">转到 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="7eb30-131">在 **Power Platform 集成** 部分中，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="7eb30-132">在 **Power Platform 环境设置** 对话框中，选中该复选框，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="7eb30-133">通常，设置需要 60 到 90 分钟。</span><span class="sxs-lookup"><span data-stu-id="7eb30-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="7eb30-134">在完成 Microsoft Power Platform 环境的设置后，页面将显示您的环境的名称。</span><span class="sxs-lookup"><span data-stu-id="7eb30-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="7eb30-135">此外，**Power Platform 集成** 部分显示声明，“Power Platform 环境设置完成。”</span><span class="sxs-lookup"><span data-stu-id="7eb30-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="7eb30-136">全球库存核算不需要双写入应用程序。</span><span class="sxs-lookup"><span data-stu-id="7eb30-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="7eb30-137">有关详细信息，请参阅[在环境部署后设置](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment)。</span><span class="sxs-lookup"><span data-stu-id="7eb30-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="7eb30-138">设置 Dataverse</span><span class="sxs-lookup"><span data-stu-id="7eb30-138">Set up Dataverse</span></span>

<span data-ttu-id="7eb30-139">在设置 Dataverse 之前，通过执行以下步骤将全球库存核算服务原则添加到您的租户。</span><span class="sxs-lookup"><span data-stu-id="7eb30-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="7eb30-140">如[安装 Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2) 中所述安装 Windows PowerShell v2 的 Azure AD 模块。</span><span class="sxs-lookup"><span data-stu-id="7eb30-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="7eb30-141">运行以下 PowerShell 命令。</span><span class="sxs-lookup"><span data-stu-id="7eb30-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="7eb30-142">接下来，通过执行以下步骤在 Dataverse 中为全球库存核算创建应用程序用户。</span><span class="sxs-lookup"><span data-stu-id="7eb30-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="7eb30-143">打开您的 Dataverse 环境的 URL。</span><span class="sxs-lookup"><span data-stu-id="7eb30-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="7eb30-144">转到 **高级设置 \> 系统 \> 安全 \> 用户**，创建应用程序用户。</span><span class="sxs-lookup"><span data-stu-id="7eb30-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="7eb30-145">使用 **视图** 字段将页面视图更改为 *应用程序用户*。</span><span class="sxs-lookup"><span data-stu-id="7eb30-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="7eb30-146">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-146">Select **New**.</span></span>
1. <span data-ttu-id="7eb30-147">将 **申请 ID** 字段设置为 *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*。</span><span class="sxs-lookup"><span data-stu-id="7eb30-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="7eb30-148">选择 **分配角色**，然后选择 *系统管理员*。</span><span class="sxs-lookup"><span data-stu-id="7eb30-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="7eb30-149">如果有一个名为 *Common Data Service 用户* 的角色，也选择它。</span><span class="sxs-lookup"><span data-stu-id="7eb30-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="7eb30-150">重复前面的步骤，但将 **应用程序 ID** 字段设置为 *5f58fc56-0202-49a8-ac9e-0946b049718b*。</span><span class="sxs-lookup"><span data-stu-id="7eb30-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="7eb30-151">有关详细信息，请参阅[创建应用程序用户](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)。</span><span class="sxs-lookup"><span data-stu-id="7eb30-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="7eb30-152">如果您的 Dataverse 安装的默认语言不是英语，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7eb30-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="7eb30-153">转到 **高级设置 \> 管理 \> 语言**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="7eb30-154">选择 *英语* (*LanguageCode=1033*)，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="7eb30-155">安装加载项</span><span class="sxs-lookup"><span data-stu-id="7eb30-155">Install the add-in</span></span>

<span data-ttu-id="7eb30-156">按照以下步骤安装加载项，以便您可以使用全球库存核算。</span><span class="sxs-lookup"><span data-stu-id="7eb30-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="7eb30-157">[注册](#sign-up)全球库存核算公开预览版。</span><span class="sxs-lookup"><span data-stu-id="7eb30-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="7eb30-158">登录 [LCS](https://lcs.dynamics.com/Logon/Index)。</span><span class="sxs-lookup"><span data-stu-id="7eb30-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="7eb30-159">转到 **预览功能管理**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="7eb30-160">选择加号 (**+**)。</span><span class="sxs-lookup"><span data-stu-id="7eb30-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="7eb30-161">在 **代码** 字段中，输入您的全球库存核算的加载项测试密钥。</span><span class="sxs-lookup"><span data-stu-id="7eb30-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="7eb30-162">（您应该已在注册时通过电子邮件收到您的测试密钥。）</span><span class="sxs-lookup"><span data-stu-id="7eb30-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="7eb30-163">选择 **解锁**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="7eb30-164">打开要在其中添加服务的 LCS 环境。</span><span class="sxs-lookup"><span data-stu-id="7eb30-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="7eb30-165">转到 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="7eb30-166">转到 **Power Platform 集成**，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="7eb30-167">在 **Power Platform 环境设置** 对话框中，选中该复选框，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="7eb30-168">通常，设置需要 60 到 90 分钟。</span><span class="sxs-lookup"><span data-stu-id="7eb30-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="7eb30-169">完成 Microsoft Power Platform 环境的设置后，在 **环境加载项** 快速选项卡上，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="7eb30-170">选择 **全球库存核算**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="7eb30-171">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="7eb30-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="7eb30-172">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-172">Select **Install**.</span></span>
1. <span data-ttu-id="7eb30-173">在 **环境加载项** 快速选项卡上，您应该会看到正在安装全球库存核算。</span><span class="sxs-lookup"><span data-stu-id="7eb30-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="7eb30-174">几分钟后，状态应从 *正在安装* 变为 *已安装*。</span><span class="sxs-lookup"><span data-stu-id="7eb30-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="7eb30-175">（您可能必须刷新页面才能看到此更改。）此时，全球库存核算可以使用了。</span><span class="sxs-lookup"><span data-stu-id="7eb30-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="7eb30-176">设置集成</span><span class="sxs-lookup"><span data-stu-id="7eb30-176">Set up the integration</span></span>

<span data-ttu-id="7eb30-177">按照以下步骤设置全球库存核算和 Supply Chain Management 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="7eb30-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="7eb30-178">登录 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="7eb30-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="7eb30-179">转到 **系统管理 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="7eb30-180">选择 **检查更新**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="7eb30-181">在 **全部** 选项卡上，搜索名为 *全球库存核算* 的功能。</span><span class="sxs-lookup"><span data-stu-id="7eb30-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="7eb30-182">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="7eb30-183">转到 **全球库存核算 \> 设置 \> 全球库存核算参数 \> 集成参数**。</span><span class="sxs-lookup"><span data-stu-id="7eb30-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="7eb30-184">在 **数据服务终结点** 和 **全球库存核算终结点** 字段中，输入全球库存核算团队在您注册预览版时发送的电子邮件中的 URL。</span><span class="sxs-lookup"><span data-stu-id="7eb30-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="7eb30-185">全球库存核算现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="7eb30-185">Global Inventory Accounting is now ready to use.</span></span>
