---
title: 预配 Human Resources
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3a7987a9b385fb6ba0294dc46b0d66be8228f06
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026259"
---
# <a name="provision-human-resources"></a><span data-ttu-id="f2fe2-102">预配 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f2fe2-102">Provision Human Resources</span></span>

<span data-ttu-id="f2fe2-103">本文将指导您如何为 Microsoft Dynamics 365 Human Resources 预配新生产环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-103">This article walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f2fe2-104">本文假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-104">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="f2fe2-105">如果您有已包括 Human Resources 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本文中的步骤，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-105">If you have an existing Microsoft Dynamics 365 license that already includes the Human Resources service plan, and you can't complete the steps in this article, contact Support.</span></span>

<span data-ttu-id="f2fe2-106">若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) 并创建新的 Human Resources 项目。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-106">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) and create a new Human Resources project.</span></span> <span data-ttu-id="f2fe2-107">除非许可问题妨碍了您预配 Human Resources，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-107">Unless a licensing issue prevents you from provisioning Human Resource, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="f2fe2-108">创建 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="f2fe2-108">Create an LCS project</span></span>

<span data-ttu-id="f2fe2-109">若要使用 LCS 来管理您的 Human Resources 环境，您必须先创建 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-109">To use LCS to manage your Human Resources environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="f2fe2-110">使用您用于订阅 Human Resources 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-110">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Human Resources.</span></span>

2. <span data-ttu-id="f2fe2-111">选择加号 (**+**) 创建项目。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-111">Select the plus sign (**+**) to create a project.</span></span>

3. <span data-ttu-id="f2fe2-112">选择 **Microsoft Dynamics 365 Human Resources** 作为产品名称和产品版本。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-112">Select **Microsoft Dynamics 365 Human Resources** as the product name and product version.</span></span>

4. <span data-ttu-id="f2fe2-113">选择 **Dynamics 365 Human Resources** 方法。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-113">Select the **Dynamics 365 Human Resources** methodology.</span></span>

5. <span data-ttu-id="f2fe2-114">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-114">Select **Create**.</span></span>

<span data-ttu-id="f2fe2-115">有关如何开始 Human Resources 的信息，请参阅在新项目中创建的 **Human Resources** 方法。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-115">For information about how to get started with Human Resources, see the **Human Resources** methodology that you created in your new project.</span></span> <span data-ttu-id="f2fe2-116">在您完成创建项目后，请完成以下过程来设置您的 Human Resources 环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-116">After you've finished creating the project, complete the following procedure to provision your Human Resources environment.</span></span>

## <a name="provision-a-human-resources-project"></a><span data-ttu-id="f2fe2-117">预配 Human Resources 项目</span><span class="sxs-lookup"><span data-stu-id="f2fe2-117">Provision a Human Resources project</span></span>

<span data-ttu-id="f2fe2-118">在创建 LCS 项目之后，您可以将 Human Resources 预配到环境中。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-118">After you've created an LCS project, you can provision Human Resources into an environment.</span></span>

1. <span data-ttu-id="f2fe2-119">在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-119">In your LCS project, select the **Human Resources App Management** tile.</span></span>

2. <span data-ttu-id="f2fe2-120">指示这是 Human Resources 的沙盒实例还是生产实例。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-120">Indicate whether this is a Sandbox or Production instance of Human Resource.</span></span> <span data-ttu-id="f2fe2-121">沙盒实例中可能提供提前预览功能以便提前反馈和测试。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-121">Early preview features may be available in Sandbox instances to allow for early feedback and testing.</span></span>
   
    > [!NOTE]
    > <span data-ttu-id="f2fe2-122">Talent 实例类型一旦设置就无法更改。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-122">The Talent instance type cannot be changed once set.</span></span> <span data-ttu-id="f2fe2-123">在继续之前，请验证是否选择了正确的实例类型。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-123">Verify the correct instance type is selected before continuing.</span></span></br></br>
    > <span data-ttu-id="f2fe2-124">Human Resources 实例类型独立于 Microsoft Power Apps 环境的实例类型，后者是您在 Power Apps 管理中心中设置的。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-124">The Human Resources instance type is separate from the instance type of the Microsoft Power Apps environment, which you set in the Power Apps Admin center.</span></span>
    
3. <span data-ttu-id="f2fe2-125">如果希望环境中包含 Human Resources 测试驱动器体验中使用的相同演示数据集，请选择**包括演示数据**选项。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-125">Select the **Include Demo Data** option if you want your environment to include the same demo data set used in the Human Resources Test Drive experience.</span></span> <span data-ttu-id="f2fe2-126">这对长期演示或培训环境有益，但切勿用于生产环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-126">This is beneficial for long-term demo or training environments, and should never be used for production environments.</span></span>  <span data-ttu-id="f2fe2-127">请注意，必须在初始部署之后立即选择此选项。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-127">Note that you must choose this option upon initial deployment.</span></span> <span data-ttu-id="f2fe2-128">不能在以后更新现有部署。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-128">You cannot update an existing deployment later.</span></span>

4. <span data-ttu-id="f2fe2-129">Human Resources 始终预配到 Microsoft Power Apps 环境，以支持 Power Apps 集成和可扩展性。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-129">Human Resources is always provisioned into a Microsoft Power Apps environment to enable Power Apps integration and extensibility.</span></span> <span data-ttu-id="f2fe2-130">在继续之前，请阅读本文的“选择 Power Apps 环境”部分。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-130">Read the “Selecting a Power Apps environment” section of this article before you continue.</span></span> <span data-ttu-id="f2fe2-131">如果您没有 Power Apps 环境，在 LCS 中选择“管理环境”或导航到 Power Apps 管理员中心。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-131">If you don't already have a Power Apps environment, select Manage environments in LCS or navigate to the Power Apps Admin center.</span></span> <span data-ttu-id="f2fe2-132">然后按照步骤[创建 Power Apps 环境](https://docs.microsoft.com/powerapps/administrator/create-environment)。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-132">Then follow the steps to [Create a Power Apps environment](https://docs.microsoft.com/powerapps/administrator/create-environment).</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2fe2-133">若要查看现有的环境或创建新环境，必须为预配 Human Resources 的租户管理员分配 Power Apps P2 许可证。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-133">To view existing environments or create new environments, the tenant admin who provisions Human Resources must be assigned to the Power Apps P2 license.</span></span> <span data-ttu-id="f2fe2-134">如果您的组织没有 Power Apps P2 许可证，则可以从 CSP 或从 [Power Apps 定价](https://powerapps.microsoft.com/pricing/)页面获取一个。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-134">If your organization doesn't have a Power Apps P2 license, you can get one from your CSP or from the [Power Apps pricing page](https://powerapps.microsoft.com/pricing/).</span></span>

5. <span data-ttu-id="f2fe2-135">选择要预配 Human Resources 的环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-135">Select the environment to provision Human Resources into.</span></span>

6. <span data-ttu-id="f2fe2-136">选择**是**同意条款并开始部署。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-136">Select **Yes** to agree to the terms and begin deployment.</span></span>

   <span data-ttu-id="f2fe2-137">您的新环境将出现在左侧导航窗格的环境列表中。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-137">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="f2fe2-138">不过，在部署状态更新为**已部署**前，您无法开始使用此环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-138">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="f2fe2-139">此过程通常需要几分钟。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-139">This process typically takes a few minutes.</span></span> <span data-ttu-id="f2fe2-140">如果配置过程失败，您必须与支持人员联系。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-140">If the provisioning process is unsuccessful, you must contact Support.</span></span>

7. <span data-ttu-id="f2fe2-141">选择**登录 Human Resources** 来使用您的新环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-141">Select **Log on to Human Resource** to use your new environment.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2fe2-142">如果您尚未验证最终要求，您可以在项目中部署 Human Resources 的测试实例。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-142">If you haven't yet signed off on the final requirements, you can deploy a test instance of Human Resources in the project.</span></span> <span data-ttu-id="f2fe2-143">您可以随后使用此实例来测试您的解决方案，直到验证完成。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-143">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="f2fe2-144">如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-144">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

    > <span data-ttu-id="f2fe2-145">由于 Human Resources 预订中仅允许两个 LCS 环境，所以可以考虑利用免费的 60 天的 [Human Resources 试用环境](https://dynamics.microsoft.com/talent/overview/)。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-145">Because only two LCS environments are allowed as part of the Human Resources subscription, you might consider leveraging a free 60-day [Human Resources trial environment](https://dynamics.microsoft.com/talent/overview/).</span></span> <span data-ttu-id="f2fe2-146">尽管试用环境归其请求用户所有，仍然可以通过 Human Resources 的系统管理体验邀请其他用户。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-146">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Human Resources.</span></span> <span data-ttu-id="f2fe2-147">试用环境中包含可用于以安全方式探索该程序的虚拟数据。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-147">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="f2fe2-148">不应将其用作生产环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-148">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="f2fe2-149">请注意，如果试用环境在 60 天后到期，其中的所有数据都将被删除且不可恢复。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-149">Note that when a trial environment expires after 60 days, all the data that's in it is deleted and can't be recovered.</span></span> <span data-ttu-id="f2fe2-150">现有环境过期后，可以注册新试用环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-150">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-power-apps-environment"></a><span data-ttu-id="f2fe2-151">选择 Power Apps 环境</span><span class="sxs-lookup"><span data-stu-id="f2fe2-151">Select a Power Apps environment</span></span>

<span data-ttu-id="f2fe2-152">通过 Human Resources 与 Power Apps 环境之间的集成，可使用 Power Apps 工具集成和扩展 Human Resources 数据的使用。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-152">The integration between Human Resources and the Power Apps environments lets you integrate and extend the use of Human Resources data using Power Apps tools.</span></span> <span data-ttu-id="f2fe2-153">了解 Power Apps 环境的用途不仅有助于您构建扩展 Human Resources 的应用，还将帮助您在预配 Human Resources 时选择正确的环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-153">Understanding the purpose of Power Apps environments will not only help you build apps to extend Human Resource, but will also help you select the correct environment when provisioning Human Resource.</span></span> <span data-ttu-id="f2fe2-154">有关 Power Apps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 Power Apps 环境](https://powerapps.microsoft.com/blog/powerapps-environments/)。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-154">For information about Power Apps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing Power Apps environments](https://powerapps.microsoft.com/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="f2fe2-155">在确定部署 Human Resources 的目标 Power Apps 环境时请使用以下指南：</span><span class="sxs-lookup"><span data-stu-id="f2fe2-155">Use the following guidance when determining which Power Apps environment to deploy Human Resources into:</span></span> 

1. <span data-ttu-id="f2fe2-156">在 LCS 中，选择**管理环境**，或直接转到 Power Apps 管理员中心，您可以在那里查看现有的环境和创建新的环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-156">In LCS, select **Manage environments**, or go directly to the Power Apps Admin center where you can view existing environments and create new environments.</span></span>

2. <span data-ttu-id="f2fe2-157">单个 Human Resources 环境映射到单个 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-157">A single Human Resources environment is mapped to a single Power Apps environment.</span></span>

3. <span data-ttu-id="f2fe2-158">Power Apps 环境包含 Human Resources，以及相应的 Power Apps、Power Automate 和 Common Data Service 应用程序。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-158">A Power Apps environment contains Human Resources, along with the corresponding Power Apps, Power Automate, and Common Data Service applications.</span></span> <span data-ttu-id="f2fe2-159">如果 Power Apps 环境被删除，其中的应用也会被删除。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-159">If the Power Apps environment is deleted, so are the apps within it.</span></span> <span data-ttu-id="f2fe2-160">在预配 Human Resources 环境时，可以预配**试用**或**生产**环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-160">When provisioning a Human Resources environment, you can provision either a **Trial** or **Production** environment.</span></span> <span data-ttu-id="f2fe2-161">根据环境使用方式选择环境类型。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-161">Choose the type of environment based on how the environment will be used.</span></span> 

4. <span data-ttu-id="f2fe2-162">应该考虑数据集成和测试策略，如沙盒、UAT 或生产。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-162">Data integration and testing strategies should be considered, such as Sandbox, UAT, or Production.</span></span> <span data-ttu-id="f2fe2-163">建议您考虑对您的部署的各种影响，因为以后不容易更改将哪个 Human Resources 环境映射到 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-163">We recommend that you consider the various implications for your deployment, because it isn't easy to later change which Human Resources environment is mapped to a Power Apps environment.</span></span>

5. <span data-ttu-id="f2fe2-164">以下 Power Apps 环境不能用于 Human Resources，将从 LCS 内的选择列表中筛除：</span><span class="sxs-lookup"><span data-stu-id="f2fe2-164">The following Power Apps environments cannot be used for Human Resources and will be filtered from the selection list within LCS:</span></span>
 
    - <span data-ttu-id="f2fe2-165">**默认 Power Apps 环境** - 虽然每个租户均自动预配为默认的 Power Apps 环境，但我们不建议在 Human Resources 中使用它们，因为所有租户用户均有权访问 Power Apps 环境，有可能会在使用 Power Apps 或 Power Automate 集成进行测试和探索时意外损坏生产数据。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-165">**Default Power Apps environments** - Although each tenant is automatically provisioned with a default Power Apps environment, we don't recommend using them with Human Resources because all tenant users have access to the Power Apps environment and could unintentionally corrupt production data when testing and exploring with Power Apps or Power Automate integrations.</span></span>
   
    - <span data-ttu-id="f2fe2-166">**试用环境** - 这些环境在创建时有到期日期，在此时间过后将到期，从而导致自动删除您的环境和其中包含的所有 Human Resources 实例。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-166">**Trial environments** - These environments are created with an expiration date and will expire after that time, causing your environment and any Human Resources instances contained within to be removed automatically.</span></span>
   
    - <span data-ttu-id="f2fe2-167">**不受支持的地区** - 目前仅在以下地区支持 Human Resources：美国、欧洲、英国、澳大利亚、加拿大和亚洲。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-167">**Unsupported regions** - Currently Human Resources is only supported in the following regions: United States, Europe, United Kingdom, Australia, Canada and Asia.</span></span>
  
6. <span data-ttu-id="f2fe2-168">确定了要使用的正确环境之后，可以继续进行配置流程。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-168">After you have determined the correct environment to use, you can continue with the provisioning process.</span></span> 
 
## <a name="grant-access-to-the-environment"></a><span data-ttu-id="f2fe2-169">授予对环境的访问</span><span class="sxs-lookup"><span data-stu-id="f2fe2-169">Grant access to the environment</span></span>

<span data-ttu-id="f2fe2-170">默认情况下，创建环境的全局管理员可以访问环境。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-170">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="f2fe2-171">但是，必须为更多应用程序用户明确授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-171">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="f2fe2-172">若要授予访问权限，需要在 Human Resources 环境中添加用户并为其分配相应角色。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-172">To grant access, you need to add users and assign the appropriate roles to them in the Human Resources environment.</span></span> <span data-ttu-id="f2fe2-173">部署了 Human Resources 的全局管理员还必须启动 Attract 和 Onboard 以完成初始化和允许其他租户用户访问。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-173">The global administrator that deployed Human Resources must also launch both Attract and Onboard to complete the initialization and enable access for other tenant users.</span></span>  <span data-ttu-id="f2fe2-174">在此之前，其他用户不能访问 Attract 和 Onboard，并且将发生访问冲突错误。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-174">Until this happens, other users will not be able to access Attract and Onboard and will get access violation errors.</span></span> <span data-ttu-id="f2fe2-175">有关详细信息，请参阅[创建新用户](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users)和[向安全角色分配用户](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles)。</span><span class="sxs-lookup"><span data-stu-id="f2fe2-175">For more information, see [Create new users](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) and [Assign users to security roles](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).</span></span> 
