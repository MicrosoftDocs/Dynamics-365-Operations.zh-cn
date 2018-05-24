---
title: "配置 Microsoft Dynamics 365 for Talent"
description: "此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新环境。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 343e372ad9e29372649e975a5bee16e8913b66c8
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="6f453-103">配置 Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="6f453-103">Provision Microsoft Dynamics 365 for Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f453-104">此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新生产环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-104">This topic walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="6f453-105">此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。</span><span class="sxs-lookup"><span data-stu-id="6f453-105">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="6f453-106">如果您有已包括 Talent 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="6f453-106">If you have an existing Microsoft Dynamics 365 license that already includes the Talent service plan, and you can't complete the steps in this topic, contact Support.</span></span>

<span data-ttu-id="6f453-107">若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) 并创建新的 Talent 项目。</span><span class="sxs-lookup"><span data-stu-id="6f453-107">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) and create a new Talent project.</span></span> <span data-ttu-id="6f453-108">除非许可问题妨碍了您配置 Talent，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。</span><span class="sxs-lookup"><span data-stu-id="6f453-108">Unless a licensing issue prevents you from provisioning Talent, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="6f453-109">创建 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="6f453-109">Create an LCS project</span></span>
<span data-ttu-id="6f453-110">若要使用 LCS 来管理您的 Talent 环境，您必须先创建 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="6f453-110">To use LCS to manage your Talent environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="6f453-111">使用您用于订阅 Talent 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。</span><span class="sxs-lookup"><span data-stu-id="6f453-111">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Talent.</span></span>
2. <span data-ttu-id="6f453-112">选择加号 (**+**) 创建项目。</span><span class="sxs-lookup"><span data-stu-id="6f453-112">Select the plus sign (**+**) to create a project.</span></span>
3. <span data-ttu-id="6f453-113">选择 **Microsoft Dynamics 365 for Talent** 作为产品名称和产品版本。</span><span class="sxs-lookup"><span data-stu-id="6f453-113">Select **Microsoft Dynamics 365 for Talent** as the product name and product version.</span></span>
4. <span data-ttu-id="6f453-114">选择 **Dynamics 365 for Talent** 方法。</span><span class="sxs-lookup"><span data-stu-id="6f453-114">Select the **Dynamics 365 for Talent** methodology.</span></span>
5. <span data-ttu-id="6f453-115">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="6f453-115">Select **Create**.</span></span>

<span data-ttu-id="6f453-116">有关如何开始 Talent 的信息，请参阅在新项目中创建的 **Talent** 方法。</span><span class="sxs-lookup"><span data-stu-id="6f453-116">For information about how to get started with Talent, see the **Talent** methodology that you created in your new project.</span></span> <span data-ttu-id="6f453-117">在您完成创建项目后，请完成以下过程来设置您的 Talent 环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-117">After you've finished creating the project, complete the following procedure to provision your Talent environment.</span></span>

## <a name="provision-a-talent-project"></a><span data-ttu-id="6f453-118">配置 Talent 项目</span><span class="sxs-lookup"><span data-stu-id="6f453-118">Provision a Talent project</span></span>
<span data-ttu-id="6f453-119">在创建 LCS 项目之后，您可以将 Talent 配置到环境中。</span><span class="sxs-lookup"><span data-stu-id="6f453-119">After you've created an LCS project, you can provision Talent into an environment.</span></span>

1. <span data-ttu-id="6f453-120">在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="6f453-120">In your LCS project, select the **Talent App Management** tile.</span></span>
2. <span data-ttu-id="6f453-121">Talent 始终配置到 Microsoft PowerApps 环境，以支持 PowerApps 集成和可扩展性。</span><span class="sxs-lookup"><span data-stu-id="6f453-121">Talent is always provisioned into a Microsoft PowerApps environment, to enable PowerApps integration and extensibility.</span></span> <span data-ttu-id="6f453-122">在继续之前，请阅读本主题的“选择 PowerApps 环境”部分。</span><span class="sxs-lookup"><span data-stu-id="6f453-122">Read the “Selecting a PowerApps environment” section of this topic before you continue.</span></span> 
3. <span data-ttu-id="6f453-123">如果您还没有 PowerApps 环境，在继续前请先执行本主题“创建新的 PowerApps 环境（如果需要）”部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="6f453-123">If you don't already have a PowerApps environment, follow the steps in the "Create a new PowerApps environment (if required)" section of this topic before you continue.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f453-124">若要查看现有的环境或创建新环境，必须为配置 Talent 的租户管理员分配 PowerApps P2 许可证。</span><span class="sxs-lookup"><span data-stu-id="6f453-124">To view existing environments or create new environments, the tenant admin who provisions Talent must be assigned to the PowerApps P2 license.</span></span> <span data-ttu-id="6f453-125">如果您的组织没有 PowerApps P2 许可证，则可以从 CSP 或从 [PowerApps 定价页面](https://powerapps.microsoft.com/en-us/pricing/)获取一个。</span><span class="sxs-lookup"><span data-stu-id="6f453-125">If your organization doesn't have a PowerApps P2 license, you can get one from your CSP or from the [PowerApps pricing page](https://powerapps.microsoft.com/en-us/pricing/).</span></span>

4. <span data-ttu-id="6f453-126">选择**添加**，然后选择要为 Talent 配置的环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-126">Select **Add**, and then select the environment to provision Talent into.</span></span>
5. <span data-ttu-id="6f453-127">如果希望环境中包含 Talent 测试驱动器体验中使用的相同演示数据集，请选择“包括演示数据”选项。</span><span class="sxs-lookup"><span data-stu-id="6f453-127">Select the ‘Include Demo Data’ option if you want your environment to include the same Demo data set used in the Talent Test Drive experience.</span></span>  <span data-ttu-id="6f453-128">这对长期演示或培训环境有益，但切勿用于生产环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-128">This is beneficial for long-term demo or training environments, and should never be used for production environments.</span></span>  <span data-ttu-id="6f453-129">请注意，初始部署后就必须选择此选项，因为以后不能更新现有部署。</span><span class="sxs-lookup"><span data-stu-id="6f453-129">Note that you must choose this option upon initial deployment and can't update an existing deployment later.</span></span>
6. <span data-ttu-id="6f453-130">选择**是**同意条款并开始部署。</span><span class="sxs-lookup"><span data-stu-id="6f453-130">Select **Yes** to agree to the terms and begin deployment.</span></span>

    <span data-ttu-id="6f453-131">您的新环境将出现在左侧导航窗格的环境列表中。</span><span class="sxs-lookup"><span data-stu-id="6f453-131">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="6f453-132">不过，在部署状态更新为**已部署**前，您无法开始使用此环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-132">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="6f453-133">此过程通常需要几分钟。</span><span class="sxs-lookup"><span data-stu-id="6f453-133">This process typically takes just a few minutes.</span></span> <span data-ttu-id="6f453-134">如果配置过程失败，您必须与支持人员联系。</span><span class="sxs-lookup"><span data-stu-id="6f453-134">If the provisioning process is unsuccessful, you must contact Support.</span></span>

7. <span data-ttu-id="6f453-135">选择**登录 Talent** 来使用您的新环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-135">Select **Log on to Talent** to use your new environment.</span></span>

> [!NOTE]
> <span data-ttu-id="6f453-136">如果您尚未验证最终要求，您可以在项目中部署 Talent 的测试实例。</span><span class="sxs-lookup"><span data-stu-id="6f453-136">If you haven't yet signed off on the final requirements, you can deploy a test instance of Talent in the project.</span></span> <span data-ttu-id="6f453-137">您可以随后使用此实例来测试您的解决方案，直到验证完成。</span><span class="sxs-lookup"><span data-stu-id="6f453-137">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="6f453-138">如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-138">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="6f453-139">由于 Talent 预订中仅允许两个 LCS 环境，所以也可以考虑利用免费的 60 天的 [Talent 试用环境](https://dynamics.microsoft.com/en-us/talent/overview/)。</span><span class="sxs-lookup"><span data-stu-id="6f453-139">Since only two LCS environments are allowed as part of the Talent subscription, you may also consider leveraging a free 60-day [Talent trial environment](https://dynamics.microsoft.com/en-us/talent/overview/).</span></span> <span data-ttu-id="6f453-140">尽管试用环境归其请求用户所有，仍然可以通过 Core HR 的系统管理体验邀请其他用户。</span><span class="sxs-lookup"><span data-stu-id="6f453-140">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Core HR.</span></span> <span data-ttu-id="6f453-141">试用环境中包含可用于以安全方式探索该程序的虚拟数据。</span><span class="sxs-lookup"><span data-stu-id="6f453-141">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="6f453-142">不应将其用作生产环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-142">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="6f453-143">请注意，如果试用环境在 60 天后到期，其中的所有数据都将被删除且不可恢复。</span><span class="sxs-lookup"><span data-stu-id="6f453-143">Note that when a trial environment expires after 60 days, all the data that's in it is deleted and can't be recovered.</span></span> <span data-ttu-id="6f453-144">现有环境过期后，可以注册新试用环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-144">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-powerapps-environment"></a><span data-ttu-id="6f453-145">选择 PowerApps 环境</span><span class="sxs-lookup"><span data-stu-id="6f453-145">Select a PowerApps environment</span></span>

<span data-ttu-id="6f453-146">通过 Talent 与 PowerApps 环境之间的集成，可使用 PowerApps 工具集成和扩展 Talent 数据的使用。</span><span class="sxs-lookup"><span data-stu-id="6f453-146">The integration between Talent and the PowerApps environments lets you integrate and extend the use of Talent data using PowerApps tools.</span></span> <span data-ttu-id="6f453-147">了解 PowerApps 环境的用途不仅有助于您构建扩展 Talent 的应用，还可以帮助您在配置 Talent 时选择正确的环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-147">Understanding the purpose of PowerApps environments will not only help you build apps to extend Talent, but also can also help you select the correct environment when provisioning Talent.</span></span> <span data-ttu-id="6f453-148">有关 PowerApps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 PowerApps 环境](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/)。</span><span class="sxs-lookup"><span data-stu-id="6f453-148">For information about PowerApps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing PowerApps environments](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="6f453-149">在确定部署 Talent 的目标 PowerApps 环境时请使用以下指南：</span><span class="sxs-lookup"><span data-stu-id="6f453-149">Use the following guidance when determining which PowerApps environment to deploy Talent into:</span></span> 
1. <span data-ttu-id="6f453-150">在 LCS 中，选择“管理环境”，或直接导航到“PowerApps 管理员中心”，您可以在那里查看现有的环境和创建新的环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-150">In LCS, select Manage environments, or navigate directly to the PowerApps Admin center , where you can view existing environments and create new environments.</span></span>
2. <span data-ttu-id="6f453-151">单个 Talent 环境映射到单个 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-151">A single Talent environment is mapped to a single PowerApps environment.</span></span>
3. <span data-ttu-id="6f453-152">PowerApps 环境“包含”Talent 应用程序，以及相应的 PowerApps、流和 CDS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="6f453-152">A PowerApps environment “contains” the Talent application, along with the corresponding PowerApps, Flow, and CDS applications.</span></span> <span data-ttu-id="6f453-153">如果 PowerApps 环境被删除，其中的应用也会被删除。</span><span class="sxs-lookup"><span data-stu-id="6f453-153">If the PowerApps environment is deleted, so are the apps within it.</span></span>
4. <span data-ttu-id="6f453-154">应该考虑数据集成和测试策略，例如：沙盒、UAT、生产。</span><span class="sxs-lookup"><span data-stu-id="6f453-154">Data integration and testing strategies should be considered, for example: Sandbox, UAT, Production.</span></span> <span data-ttu-id="6f453-155">因此，建议您考虑对您的部署的各种影响，因为以后不容易更改将哪个 Talent 环境映射到 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-155">Therefore, we recommend that you consider the various implications for your deployment, because it isn't easy to change which Talent environment is mapped to a PowerApps environment later.</span></span>
5. <span data-ttu-id="6f453-156">以下 PowerApps 环境不能用于 Talent，将从 LCS 内的选择列表中筛除：</span><span class="sxs-lookup"><span data-stu-id="6f453-156">The following PowerApps environments cannot be used for Talent and will be filtered from the selection list within LCS:</span></span>
 
    <span data-ttu-id="6f453-157">**CDS 2.0 环境** CDS 2.0 将于 2018 年 3 月 21 日公开提供；不过，Talent 尚不支持 CDS 2.0。</span><span class="sxs-lookup"><span data-stu-id="6f453-157">**CDS 2.0 Environments** CDS 2.0 will be made publicly available on March 21, 2018; however, Talent does not yet support CDS 2.0.</span></span> <span data-ttu-id="6f453-158">尽管您可以在 PowerApps 管理员中心查看和创建 CDS 2.0 数据库，但它们不能在 Talent 中使用。</span><span class="sxs-lookup"><span data-stu-id="6f453-158">Though you can view and create CDS 2.0 databases in the PowerApps Admin center, they will not be usable in Talent.</span></span> <span data-ttu-id="6f453-159">Talent 部署中的使用 2.0 CDS 环境选项将在以后提供。</span><span class="sxs-lookup"><span data-stu-id="6f453-159">The option to use CDS 2.0 Environments in Talent deployments will be available at a later date.</span></span>
   
   > [!Note]
   > <span data-ttu-id="6f453-160">若要区分管理门户中的 CDS 1.0 和 2.0 环境，选择环境并查看**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6f453-160">To differentiate between CDS 1.0 and 2.0 environments in the administration portal, select an environment and look at the **Details**.</span></span> <span data-ttu-id="6f453-161">CDS 2.0 环境全部参考“您可以在 Dynamics 365 管理中心管理这些设置”的事实，指向实例版本，并且没有“数据库”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6f453-161">CDS 2.0 environments all reference the fact that "You can manage these settings in the Dynamics 365 Administration Center," point to an instance version, and have no Database tab.</span></span> 
 
   <span data-ttu-id="6f453-162">**默认 PowerApps 环境**虽然每个租户均自动配置为默认的 PowerApps 环境，但我们不建议在 Talent 中使用它们，因为所有租户用户均有权访问 PowerApps 环境，有可能会在使用 PowerApps 或流集成进行测试和探索时意外损坏生产数据。</span><span class="sxs-lookup"><span data-stu-id="6f453-162">**Default Power Apps environments** Although each tenant is automatically provisioned with a default PowerApps environment, we don't recommend using them with Talent since all tenant users have access to the PowerApps environment and may unintentionally corrupt production data when testing and exploring with PowerApps or Flow integrations.</span></span>
   
   <span data-ttu-id="6f453-163"><strong>测试驱动器环境</strong>具有类似“TestDrive – alias@domain”这样的名称的环境创建后有 60 天的到期期间，此时间过后，会导致您的环境自动删除。</span><span class="sxs-lookup"><span data-stu-id="6f453-163"><strong>Test Drive environments</strong> Environments with a name like ‘TestDrive – alias@domain’ are created with a 60-day expiration period and will expire after that time, causing your environment to be removed automatically.</span></span>
   
   <span data-ttu-id="6f453-164">**不支持的地区**Talent 当前仅在以下地区受支持：美国、欧洲或澳大利亚。</span><span class="sxs-lookup"><span data-stu-id="6f453-164">**Unsupported regions** Currently Talent is only supported in the following regions: United States, Europe, or Australia.</span></span>
  
6. <span data-ttu-id="6f453-165">一旦您确定了要使用的正确环境，则没有要采取的特定行动。</span><span class="sxs-lookup"><span data-stu-id="6f453-165">There is no specific action to take once you have determined the correct environment to use.</span></span> <span data-ttu-id="6f453-166">继续配置流程。</span><span class="sxs-lookup"><span data-stu-id="6f453-166">Continue with the provisioning process.</span></span> 
 
## <a name="create-a-new-powerapps-environment-if-required"></a><span data-ttu-id="6f453-167">创建新的 PowerApps 环境（如果需要）</span><span class="sxs-lookup"><span data-stu-id="6f453-167">Create a new PowerApps environment (if required)</span></span>

<span data-ttu-id="6f453-168">运行 PowerShell 脚本以在具有 PowerApps 计划 2 许可证的租户管理员上下文中为 Talent 创建新 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-168">Run a PowerShell script to create a new PowerApps environment for Talent in the context of the tenant admin that has the PowerApps Plan 2 license.</span></span> <span data-ttu-id="6f453-169">脚本将自动完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6f453-169">The script automates the following steps:</span></span>


 + <span data-ttu-id="6f453-170">创建 PowerApps 环境</span><span class="sxs-lookup"><span data-stu-id="6f453-170">Creation of a PowerApps environment</span></span>
 + <span data-ttu-id="6f453-171">创建 CDS 1.0 数据库</span><span class="sxs-lookup"><span data-stu-id="6f453-171">Creation of a CDS 1.0 database</span></span>
 + <span data-ttu-id="6f453-172">清除 CDS 1.0 数据库中的所有示例数据</span><span class="sxs-lookup"><span data-stu-id="6f453-172">Clear all sample data in the CDS 1.0 database</span></span>


<span data-ttu-id="6f453-173">完成以下说明中的步骤以运行脚本：</span><span class="sxs-lookup"><span data-stu-id="6f453-173">Complete the following instructions to run the script:</span></span>

1. <span data-ttu-id="6f453-174">从以下位置下载 ProvisionCDSEnvironment.zip 文件：[ProvisionCDSEnvironment 脚本](https://go.microsoft.com/fwlink/?linkid=870436)</span><span class="sxs-lookup"><span data-stu-id="6f453-174">Download the ProvisionCDSEnvironment.zip file from the following location: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)</span></span>  

2. <span data-ttu-id="6f453-175">在下载文件夹中，右键单击刚才下载的 ProvisionCDSEnvironment.zip 文件，然后选择**属性**。</span><span class="sxs-lookup"><span data-stu-id="6f453-175">From your downloads folder, right click on the ProvisionCDSEnvironment.zip file just downloaded and select **Properties**.</span></span>  <span data-ttu-id="6f453-176">如果对话框底部有安全声明宣称“此文件来自另一台计算机，可能已锁定，以帮助保护此计算机”，请将复选框标记为**解锁**，单击**应用**，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="6f453-176">If there is a Security note at the bottom of the dialog that states “This file came from another computer and might be blocked to help protect this computer”, mark the checkbox to **Unblock**, then click **Apply** and then **OK**.</span></span>

3. <span data-ttu-id="6f453-177">将整个 ProvisionCDSEnviroinment.zip 文件的内容解压缩到非根文件夹中。</span><span class="sxs-lookup"><span data-stu-id="6f453-177">Unzip the entire contents of the ProvisionCDSEnviroinment.zip file into a folder, other than your root folder.</span></span>

4. <span data-ttu-id="6f453-178">作为管理员运行 Windows PowerShell 或 Windows PowerShell ISE 程序。</span><span class="sxs-lookup"><span data-stu-id="6f453-178">Run the Windows PowerShell or Windows PowerShell ISE program as the administrator.</span></span>

   <span data-ttu-id="6f453-179">访问[设置执行策略](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6)主题，了解有关设置执行策略以使脚本运行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6f453-179">Visit the [Set Execution Policy](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) topic to learn more about setting the execution policy so that scripts can be run.</span></span> <span data-ttu-id="6f453-180">建议使用下面的的“Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process”，但务必遵守公司的安全策略，并在完成时关闭 PowerShell 窗口。</span><span class="sxs-lookup"><span data-stu-id="6f453-180">We suggest using the following, “Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process”, but be sure to follow your company security policies and close the PowerShell window when finished.</span></span> 
  
5. <span data-ttu-id="6f453-181">在 PowerShell 中，导航到您解压缩文件的文件夹并运行以下命令，按下方指示替换值：</span><span class="sxs-lookup"><span data-stu-id="6f453-181">Within PowerShell, navigate to the folder where you unzipped the file and run the following command, replacing values as directed below:</span></span>
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   <span data-ttu-id="6f453-182">**MyNewEnvironment** 应该替换为您的环境名称。</span><span class="sxs-lookup"><span data-stu-id="6f453-182">**MyNewEnvironment** should be replaced with your environment name.</span></span> <span data-ttu-id="6f453-183">此名称将出现在 LCS 中，并且在用户选择要使用的 Talent 环境时可见。</span><span class="sxs-lookup"><span data-stu-id="6f453-183">This name will appear in LCS and will be visible when users select which Talent environment to use.</span></span> 

   <span data-ttu-id="6f453-184">**YourLocation** 应替换为以下一个支持 Talent 的地区：美国、欧洲、澳大利亚。</span><span class="sxs-lookup"><span data-stu-id="6f453-184">**YourLocation** should be replaced with one of the supported regions for Talent: unitedstates, europe, australia.</span></span> 

   <span data-ttu-id="6f453-185">**-Verbose** 是可选的，将提供在出现问题时发送的用于提供支持的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6f453-185">**-Verbose** is optional and will provide detailed information to send to support if problems are encountered.</span></span>

6. <span data-ttu-id="6f453-186">继续配置流程。</span><span class="sxs-lookup"><span data-stu-id="6f453-186">Continue with the provisioning process.</span></span>
 

## <a name="grant-access-to-the-environment"></a><span data-ttu-id="6f453-187">授予对环境的访问</span><span class="sxs-lookup"><span data-stu-id="6f453-187">Grant access to the environment</span></span>
<span data-ttu-id="6f453-188">默认情况下，创建环境的全局管理员可以访问环境。</span><span class="sxs-lookup"><span data-stu-id="6f453-188">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="6f453-189">但是，必须为更多应用程序用户明确授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="6f453-189">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="6f453-190">要授予访问权限，请在 Core HR 环境中[添加用户](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users)并[为其分配相应角色](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles)。</span><span class="sxs-lookup"><span data-stu-id="6f453-190">To grant access, you [add users](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) and [assign the appropriate roles to them](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) in the Core HR environment.</span></span> <span data-ttu-id="6f453-191">部署了 Talent 的全局管理员还必须启动 Attract 和 Onboard 应用程序以完成初始化和允许其他租户用户访问。</span><span class="sxs-lookup"><span data-stu-id="6f453-191">The global administrator that deployed Talent must also launch both the Attract and Onboard applications to complete the initialization and enable access for other tenant users.</span></span>  <span data-ttu-id="6f453-192">在此之前，其他用户不能访问 Attract 和 Onboard 应用程序，并且将发生访问冲突错误。</span><span class="sxs-lookup"><span data-stu-id="6f453-192">Until this happens, other users will not be able to access Attract and Onboard applications and will get access violation errors.</span></span>


