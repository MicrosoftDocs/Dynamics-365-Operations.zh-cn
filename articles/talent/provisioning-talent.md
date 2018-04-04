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
ms.sourcegitcommit: ba1a3a78d59f3aec91473ba9bb20bda4804ec92e
ms.openlocfilehash: 0a43f5ff0987ede9f0cb80e5b4854f78e19e329b
ms.contentlocale: zh-cn
ms.lasthandoff: 03/23/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="68b17-103">配置 Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="68b17-103">Provision Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="68b17-104">此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新生产环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-104">This topic walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="68b17-105">此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。</span><span class="sxs-lookup"><span data-stu-id="68b17-105">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="68b17-106">如果您有已包括 Talent 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="68b17-106">If you have an existing Microsoft Dynamics 365 license that already includes the Talent service plan, and you can't complete the steps in this topic, contact Support.</span></span>

<span data-ttu-id="68b17-107">若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) 并创建新的 Talent 项目。</span><span class="sxs-lookup"><span data-stu-id="68b17-107">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) and create a new Talent project.</span></span> <span data-ttu-id="68b17-108">除非许可问题妨碍了您配置 Talent，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。</span><span class="sxs-lookup"><span data-stu-id="68b17-108">Unless a licensing issue prevents you from provisioning Talent, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="68b17-109">创建 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="68b17-109">Create an LCS project</span></span>
<span data-ttu-id="68b17-110">若要使用 LCS 来管理您的 Talent 环境，您必须先创建 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="68b17-110">To use LCS to manage your Talent environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="68b17-111">使用您用于订阅 Talent 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。</span><span class="sxs-lookup"><span data-stu-id="68b17-111">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Talent.</span></span>
2. <span data-ttu-id="68b17-112">选择加号 (**+**) 创建项目。</span><span class="sxs-lookup"><span data-stu-id="68b17-112">Select the plus sign (**+**) to create a project.</span></span>
3. <span data-ttu-id="68b17-113">选择 **Microsoft Dynamics 365 for Talent** 作为产品名称和产品版本。</span><span class="sxs-lookup"><span data-stu-id="68b17-113">Select **Microsoft Dynamics 365 for Talent** as the product name and product version.</span></span>
4. <span data-ttu-id="68b17-114">选择 **Dynamics 365 for Talent** 方法。</span><span class="sxs-lookup"><span data-stu-id="68b17-114">Select the **Dynamics 365 for Talent** methodology.</span></span>
5. <span data-ttu-id="68b17-115">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="68b17-115">Select **Create**.</span></span>

<span data-ttu-id="68b17-116">有关如何开始 Talent 的信息，请参阅在新项目中创建的 **Talent** 方法。</span><span class="sxs-lookup"><span data-stu-id="68b17-116">For information about how to get started with Talent, see the **Talent** methodology that you created in your new project.</span></span> <span data-ttu-id="68b17-117">在您完成创建项目后，请完成以下过程来设置您的 Talent 环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-117">After you've finished creating the project, complete the following procedure to provision your Talent environment.</span></span>

## <a name="provision-a-talent-project"></a><span data-ttu-id="68b17-118">配置 Talent 项目</span><span class="sxs-lookup"><span data-stu-id="68b17-118">Provision a Talent project</span></span>
<span data-ttu-id="68b17-119">在创建 LCS 项目之后，您可以将 Talent 配置到环境中。</span><span class="sxs-lookup"><span data-stu-id="68b17-119">After you've created an LCS project, you can provision Talent into an environment.</span></span>

1. <span data-ttu-id="68b17-120">在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="68b17-120">In your LCS project, select the **Talent App Management** tile.</span></span>
2. <span data-ttu-id="68b17-121">Talent 始终配置到 Microsoft PowerApps 环境，以支持 PowerApps 集成和可扩展性。</span><span class="sxs-lookup"><span data-stu-id="68b17-121">Talent is always provisioned into a Microsoft PowerApps environment, to enable PowerApps integration and extensibility.</span></span> <span data-ttu-id="68b17-122">在继续之前，请阅读本主题的“选择 PowerApps 环境”部分。</span><span class="sxs-lookup"><span data-stu-id="68b17-122">Read the “Selecting a PowerApps environment” section of this topic before you continue.</span></span> 
3. <span data-ttu-id="68b17-123">如果您还没有 PowerApps 环境，在继续前请先执行本主题“创建新的 PowerApps 环境（如果需要）”部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="68b17-123">If you don't already have a PowerApps environment, follow the steps in the "Create a new PowerApps environment (if required)" section of this topic before you continue.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68b17-124">若要查看现有的环境或创建新环境，必须为配置 Talent 的租户管理员分配 PowerApps P2 许可证。</span><span class="sxs-lookup"><span data-stu-id="68b17-124">To view existing environments or create new environments, the tenant admin who provisions Talent must be assigned to the PowerApps P2 license.</span></span> <span data-ttu-id="68b17-125">如果您的组织没有 PowerApps P2 许可证，则可以从 CSP 或从 [PowerApps 定价页面](https://powerapps.microsoft.com/en-us/pricing/)获取一个。</span><span class="sxs-lookup"><span data-stu-id="68b17-125">If your organization doesn't have a PowerApps P2 license, you can get one from your CSP or from the [PowerApps pricing page](https://powerapps.microsoft.com/en-us/pricing/).</span></span>

4. <span data-ttu-id="68b17-126">选择**添加**，然后选择要为 Talent 配置的环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-126">Select **Add**, and then select the environment to provision Talent into.</span></span>
5. <span data-ttu-id="68b17-127">选择**是**同意条款并开始部署。</span><span class="sxs-lookup"><span data-stu-id="68b17-127">Select **Yes** to agree to the terms and begin deployment.</span></span>

    <span data-ttu-id="68b17-128">您的新环境将出现在左侧导航窗格的环境列表中。</span><span class="sxs-lookup"><span data-stu-id="68b17-128">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="68b17-129">不过，在部署状态更新为**已部署**前，您无法开始使用此环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-129">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="68b17-130">此过程通常需要几分钟。</span><span class="sxs-lookup"><span data-stu-id="68b17-130">This process typically takes just a few minutes.</span></span> <span data-ttu-id="68b17-131">如果配置过程失败，您必须与支持人员联系。</span><span class="sxs-lookup"><span data-stu-id="68b17-131">If the provisioning process is unsuccessful, you must contact Support.</span></span>

6. <span data-ttu-id="68b17-132">选择**登录 Talent** 来使用您的新环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-132">Select **Log on to Talent** to use your new environment.</span></span>

> [!NOTE]
> <span data-ttu-id="68b17-133">如果您尚未验证最终要求，您可以在项目中部署 Talent 的测试实例。</span><span class="sxs-lookup"><span data-stu-id="68b17-133">If you haven't yet signed off on the final requirements, you can deploy a test instance of Talent in the project.</span></span> <span data-ttu-id="68b17-134">您可以随后使用此实例来测试您的解决方案，直到验证完成。</span><span class="sxs-lookup"><span data-stu-id="68b17-134">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="68b17-135">如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-135">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="68b17-136">通过 LCS 设置的 Talent 环境不包含为人力资源 (HR) 任务配置的演示数据或特定于 Talent 的演示数据。</span><span class="sxs-lookup"><span data-stu-id="68b17-136">Talent environments that are provisioned through LCS don't contain demo data that is configured for Human resources (HR) tasks, or that is specific to Talent.</span></span> <span data-ttu-id="68b17-137">如果需要包含演示数据的环境，建议您注册 60 天的免费 [Talent 试用环境](https://dynamics.microsoft.com/en-us/talent/overview/)。</span><span class="sxs-lookup"><span data-stu-id="68b17-137">If you require an environment that contains demo data, we recommend that you sign up for a free 60-day [Talent trial environment](https://dynamics.microsoft.com/en-us/talent/overview/).</span></span> <span data-ttu-id="68b17-138">尽管试用环境归其请求用户所有，仍然可以通过 Core HR 的系统管理体验邀请其他用户。</span><span class="sxs-lookup"><span data-stu-id="68b17-138">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Core HR.</span></span> <span data-ttu-id="68b17-139">试用环境中包含可用于以安全方式探索该程序的虚拟数据。</span><span class="sxs-lookup"><span data-stu-id="68b17-139">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="68b17-140">不应将其用作生产环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-140">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="68b17-141">请注意，如果试用环境在 60 天后到期，其中的所有数据都将被删除且不可恢复。</span><span class="sxs-lookup"><span data-stu-id="68b17-141">Note that when the trial environment expires after 60 days, all the data in it is deleted and can't be recovered.</span></span> <span data-ttu-id="68b17-142">现有环境过期后，可以注册新试用环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-142">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-powerapps-environment"></a><span data-ttu-id="68b17-143">选择 PowerApps 环境</span><span class="sxs-lookup"><span data-stu-id="68b17-143">Select a PowerApps environment</span></span>

<span data-ttu-id="68b17-144">通过 Talent 与 PowerApps 环境之间的集成，可使用 PowerApps 工具集成和扩展 Talent 数据的使用。</span><span class="sxs-lookup"><span data-stu-id="68b17-144">The integration between Talent and the PowerApps environments lets you integrate and extend the use of Talent data using PowerApps tools.</span></span> <span data-ttu-id="68b17-145">了解 PowerApps 环境的用途不仅有助于您构建扩展 Talent 的应用，还可以帮助您在配置 Talent 时选择正确的环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-145">Understanding the purpose of PowerApps environments will not only help you build apps to extend Talent, but also can also help you select the correct environment when provisioning Talent.</span></span> <span data-ttu-id="68b17-146">有关 PowerApps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 PowerApps 环境](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/)。</span><span class="sxs-lookup"><span data-stu-id="68b17-146">For information about PowerApps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing PowerApps environments](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="68b17-147">在确定部署 Talent 的目标 PowerApps 环境时请使用以下指南：</span><span class="sxs-lookup"><span data-stu-id="68b17-147">Use the following guidance when determining which PowerApps environment to deploy Talent into:</span></span> 
1. <span data-ttu-id="68b17-148">在 LCS 中，选择“管理环境”，或直接导航到“PowerApps 管理员中心”，您可以在那里查看现有的环境和创建新的环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-148">In LCS, select Manage environments, or navigate directly to the PowerApps Admin center , where you can view existing environments and create new environments.</span></span>
2. <span data-ttu-id="68b17-149">单个 Talent 环境映射到单个 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-149">A single Talent environment is mapped to a single PowerApps environment.</span></span>
3. <span data-ttu-id="68b17-150">PowerApps 环境“包含”Talent 应用程序，以及相应的 PowerApps、流和 CDS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="68b17-150">A PowerApps environment “contains” the Talent application, along with the corresponding PowerApps, Flow, and CDS applications.</span></span> <span data-ttu-id="68b17-151">如果 PowerApps 环境被删除，其中的应用也会被删除。</span><span class="sxs-lookup"><span data-stu-id="68b17-151">If the PowerApps environment is deleted, so are the apps within it.</span></span>
4. <span data-ttu-id="68b17-152">应该考虑数据集成和测试策略，例如：沙盒、UAT、生产。</span><span class="sxs-lookup"><span data-stu-id="68b17-152">Data integration and testing strategies should be considered, for example: Sandbox, UAT, Production.</span></span> <span data-ttu-id="68b17-153">因此，建议您考虑对您的部署的各种影响，因为以后不容易更改将哪个 Talent 环境映射到 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-153">Therefore, we recommend that you consider the various implications for your deployment, because it isn't easy to change which Talent environment is mapped to a PowerApps environment later.</span></span>
5. <span data-ttu-id="68b17-154">以下 PowerApps 环境不能用于 Talent，将从 LCS 内的选择列表中筛除：</span><span class="sxs-lookup"><span data-stu-id="68b17-154">The following PowerApps environments cannot be used for Talent and will be filtered from the selection list within LCS:</span></span>
 
    <span data-ttu-id="68b17-155">**CDS 2.0 环境** CDS 2.0 将于 2018 年 3 月 21 日公开提供；不过，Talent 尚不支持 CDS 2.0。</span><span class="sxs-lookup"><span data-stu-id="68b17-155">**CDS 2.0 Environments** CDS 2.0 will be made publicly available on March 21, 2018; however, Talent does not yet support CDS 2.0.</span></span> <span data-ttu-id="68b17-156">尽管您可以在 PowerApps 管理员中心查看和创建 CDS 2.0 数据库，但它们不能在 Talent 中使用。</span><span class="sxs-lookup"><span data-stu-id="68b17-156">Though you can view and create CDS 2.0 databases in the PowerApps Admin center, they will not be usable in Talent.</span></span> <span data-ttu-id="68b17-157">Talent 部署中的使用 2.0 CDS 环境选项将在以后提供。</span><span class="sxs-lookup"><span data-stu-id="68b17-157">The option to use CDS 2.0 Environments in Talent deployments will be available at a later date.</span></span>
   
 > [!Note]
 > <span data-ttu-id="68b17-158">若要区分管理门户中的 CDS 1.0 和 2.0 环境，选择环境并查看**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="68b17-158">To differentiate between CDS 1.0 and 2.0 environments in the administration portal, select an environment and look at the **Details**.</span></span> <span data-ttu-id="68b17-159">CDS 2.0 环境全部参考“您可以在 Dynamics 365 管理中心管理这些设置”的事实，指向实例版本，并且没有“数据库”选项卡。</span><span class="sxs-lookup"><span data-stu-id="68b17-159">CDS 2.0 environments all reference the fact that "You can manage these settings in the Dynamics 365 Administration Center," point to an instance version, and have no Database tab.</span></span> 
 
   <span data-ttu-id="68b17-160">**默认 PowerApps 环境**虽然每个租户均自动配置为默认的 PowerApps 环境，但我们不建议在 Talent 中使用它们，因为所有租户用户均有权访问 PowerApps 环境，有可能会在使用 PowerApps 或流集成进行测试和探索时意外损坏生产数据。</span><span class="sxs-lookup"><span data-stu-id="68b17-160">**Default Power Apps environments** Although each tenant is automatically provisioned with a default PowerApps environment, we don't recommend using them with Talent since all tenant users have access to the PowerApps environment and may unintentionally corrupt production data when testing and exploring with PowerApps or Flow integrations.</span></span>
   
   <span data-ttu-id="68b17-161">**测试驱动器环境**具有类似“TestDrive – alias@domain”这样的名称的环境创建后有 60 天的到期期间，此时间过后，会导致您的环境自动删除。</span><span class="sxs-lookup"><span data-stu-id="68b17-161">**Test Drive environments** Environments with a name like ‘TestDrive – alias@domain’ are created with a 60-day expiration period and will expire after that time, causing your environment to be removed automatically.</span></span>
   
   <span data-ttu-id="68b17-162">**不支持的地区**Talent 当前仅在以下地区受支持：美国、欧洲或澳大利亚。</span><span class="sxs-lookup"><span data-stu-id="68b17-162">**Unsupported regions** Currently Talent is only supported in the following regions: United States, Europe, or Australia.</span></span>
  
6. <span data-ttu-id="68b17-163">一旦您确定了要使用的正确环境，则没有要采取的特定行动。</span><span class="sxs-lookup"><span data-stu-id="68b17-163">There is no specific action to take once you have determined the correct environment to use.</span></span> <span data-ttu-id="68b17-164">继续配置流程。</span><span class="sxs-lookup"><span data-stu-id="68b17-164">Continue with the provisioning process.</span></span> 
 
## <a name="create-a-new-powerapps-environment-if-required"></a><span data-ttu-id="68b17-165">创建新的 PowerApps 环境（如果需要）</span><span class="sxs-lookup"><span data-stu-id="68b17-165">Create a new PowerApps environment (if required)</span></span>

<span data-ttu-id="68b17-166">运行 PowerShell 脚本以在具有 PowerApps 计划 2 许可证的租户管理员上下文中为 Talent 创建新 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-166">Run a PowerShell script to create a new PowerApps environment for Talent in the context of the tenant admin that has the PowerApps Plan 2 license.</span></span> <span data-ttu-id="68b17-167">脚本将自动完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="68b17-167">The script automates the following steps:</span></span>


 + <span data-ttu-id="68b17-168">创建 PowerApps 环境</span><span class="sxs-lookup"><span data-stu-id="68b17-168">Creation of a PowerApps environment</span></span>
 + <span data-ttu-id="68b17-169">创建 CDS 1.0 数据库</span><span class="sxs-lookup"><span data-stu-id="68b17-169">Creation of a CDS 1.0 database</span></span>
 + <span data-ttu-id="68b17-170">清除 CDS 1.0 数据库中的所有示例数据</span><span class="sxs-lookup"><span data-stu-id="68b17-170">Clear all sample data in the CDS 1.0 database</span></span>


<span data-ttu-id="68b17-171">完成以下说明中的步骤以运行脚本：</span><span class="sxs-lookup"><span data-stu-id="68b17-171">Complete the following instructions to run the script:</span></span>

1. <span data-ttu-id="68b17-172">从以下位置下载 ProvisionCDSEnvironment.zip 文件：[ProvisionCDSEnvironment 脚本](https://go.microsoft.com/fwlink/?linkid=870436)</span><span class="sxs-lookup"><span data-stu-id="68b17-172">Download the ProvisionCDSEnvironment.zip file from the following location: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)</span></span>  

2. <span data-ttu-id="68b17-173">将整个 ProvisionCDSEnviroinment.zip 文件的内容解压缩到文件夹中。</span><span class="sxs-lookup"><span data-stu-id="68b17-173">Unzip the entire contents of the ProvisionCDSEnviroinment.zip file into a folder.</span></span>

3. <span data-ttu-id="68b17-174">作为管理员运行 Windows PowerShell 或 Windows PowerShell ISE 程序。</span><span class="sxs-lookup"><span data-stu-id="68b17-174">Run the Windows PowerShell or Windows PowerShell ISE program as the administrator.</span></span>

   <span data-ttu-id="68b17-175">访问[设置执行策略](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6)主题，了解有关设置执行策略以使脚本运行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="68b17-175">Visit the [Set Execution Policy](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) topic to learn more about setting the execution policy so that scripts can be run.</span></span>
  
4. <span data-ttu-id="68b17-176">在 PowerShell 中，导航到您解压缩文件的文件夹并运行以下命令，按下方指示替换值：</span><span class="sxs-lookup"><span data-stu-id="68b17-176">Within PowerShell, navigate to the folder where you unzipped the file and run the following command, replacing values as directed below:</span></span>
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   <span data-ttu-id="68b17-177">**EnvironmentName** 应该替换为您的环境名称。</span><span class="sxs-lookup"><span data-stu-id="68b17-177">**EnvironmentName** should be replaced with your environment name.</span></span> <span data-ttu-id="68b17-178">此名称将出现在 LCS 中，并且在用户选择要使用的 Talent 环境时可见。</span><span class="sxs-lookup"><span data-stu-id="68b17-178">This name will appear in LCS and will be visible when users select which Talent environment to use.</span></span> 

   <span data-ttu-id="68b17-179">**YourLocation** 应替换为以下一个支持 Talent 的地区：美国、欧洲、澳大利亚。</span><span class="sxs-lookup"><span data-stu-id="68b17-179">**YourLocation** should be replaced with one of the supported regions for Talent: unitedsates, europe, australia.</span></span> 

   <span data-ttu-id="68b17-180">**-Verbose** 是可选的，将提供在出现问题时发送的用于提供支持的详细信息。</span><span class="sxs-lookup"><span data-stu-id="68b17-180">**-Verbose** is optional and will provide detailed information to send to support if problems are encountered.</span></span>

5. <span data-ttu-id="68b17-181">继续配置流程。</span><span class="sxs-lookup"><span data-stu-id="68b17-181">Continue with the provisioning process.</span></span>
 


## <a name="grant-access-to-the-environment"></a><span data-ttu-id="68b17-182">授予对环境的访问</span><span class="sxs-lookup"><span data-stu-id="68b17-182">Grant access to the environment</span></span>
<span data-ttu-id="68b17-183">默认情况下，创建环境的全局管理员可以访问环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-183">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="68b17-184">但是，必须为更多应用程序用户明确授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="68b17-184">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="68b17-185">要授予访问权限，请在 Core HR 环境中[添加用户](../dev-itpro/sysadmin/tasks/create-new-users.md)并[为其分配相应角色](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="68b17-185">To grant access, you [add users](../dev-itpro/sysadmin/tasks/create-new-users.md) and [assign the appropriate roles to them](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) in the Core HR environment.</span></span> <span data-ttu-id="68b17-186">还必须将这些用户添加到 PowerApps 环境，以便他们可以访问 Attract 和 Onboard 应用程序。</span><span class="sxs-lookup"><span data-stu-id="68b17-186">You must also add those users to the PowerApps environment, so that they can access the Attract and Onboard applications.</span></span> <span data-ttu-id="68b17-187">下面概述此过程。</span><span class="sxs-lookup"><span data-stu-id="68b17-187">The procedure is outlined here.</span></span> <span data-ttu-id="68b17-188">如果需要帮助才能完成这些步骤，请参阅博客文章[介绍 PowerApps 管理中心](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/)。</span><span class="sxs-lookup"><span data-stu-id="68b17-188">If you require help to complete the steps, see the [Introducing the PowerApps admin center](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) blog post.</span></span>

<span data-ttu-id="68b17-189">应由部署 Talent 环境的全局管理员完成此过程。</span><span class="sxs-lookup"><span data-stu-id="68b17-189">This procedure is completed by the global administrator who deployed the Talent environment.</span></span>

1. <span data-ttu-id="68b17-190">打开 [PowerApps 管理中心](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="68b17-190">Open the [PowerApps Admin center](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="68b17-191">选择相应环境。</span><span class="sxs-lookup"><span data-stu-id="68b17-191">Select the appropriate environments.</span></span>
3. <span data-ttu-id="68b17-192">在**安全性**选项卡中，将所需用户添加到**环境制造者**角色。</span><span class="sxs-lookup"><span data-stu-id="68b17-192">On the **Security** tab, add the required users to the **Environment Maker** role.</span></span>

    <span data-ttu-id="68b17-193">请注意，将用户手动添加到 PowerApps 环境这一最后步骤是暂时的。</span><span class="sxs-lookup"><span data-stu-id="68b17-193">Note that this final step, where you manually add users to the PowerApps environment, is temporary.</span></span> <span data-ttu-id="68b17-194">在 Core HR 中添加用户时，将最终自动完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="68b17-194">Eventually, it will be completed automatically when users are added in Core HR.</span></span>

