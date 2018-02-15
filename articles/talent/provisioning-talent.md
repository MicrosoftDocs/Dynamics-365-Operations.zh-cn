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
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: zh-cn
ms.lasthandoff: 01/31/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="43cee-103">配置 Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="43cee-103">Provision Microsoft Dynamics 365 for Talent</span></span>
<span data-ttu-id="43cee-104">此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-104">This topic walks you through the process of provisioning a new environment for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="43cee-105">此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。</span><span class="sxs-lookup"><span data-stu-id="43cee-105">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="43cee-106">如果您有已包括 Talent 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。</span><span class="sxs-lookup"><span data-stu-id="43cee-106">If you have an existing Microsoft Dynamics 365 license that already includes the Talent service plan, and you can't complete the steps in this topic, contact Support.</span></span>

<span data-ttu-id="43cee-107">若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) 并创建新的 Talent 项目。</span><span class="sxs-lookup"><span data-stu-id="43cee-107">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) and create a new Talent project.</span></span> <span data-ttu-id="43cee-108">除非许可问题妨碍了您配置 Talent，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。</span><span class="sxs-lookup"><span data-stu-id="43cee-108">Unless a licensing issue prevents you from provisioning Talent, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="43cee-109">创建 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="43cee-109">Create an LCS project</span></span>
<span data-ttu-id="43cee-110">若要使用 LCS 来管理您的 Talent 环境，您必须先创建 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="43cee-110">To use LCS to manage your Talent environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="43cee-111">使用您用于订阅 Talent 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。</span><span class="sxs-lookup"><span data-stu-id="43cee-111">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Talent.</span></span>
2. <span data-ttu-id="43cee-112">选择加号 (**+**) 创建项目。</span><span class="sxs-lookup"><span data-stu-id="43cee-112">Select the plus sign (**+**) to create a project.</span></span>
3. <span data-ttu-id="43cee-113">选择 **Microsoft Dynamics 365 for Talent** 作为产品名称和产品版本。</span><span class="sxs-lookup"><span data-stu-id="43cee-113">Select **Microsoft Dynamics 365 for Talent** as the product name and product version.</span></span>
4. <span data-ttu-id="43cee-114">选择 **Dynamics 365 for Talent** 方法。</span><span class="sxs-lookup"><span data-stu-id="43cee-114">Select the **Dynamics 365 for Talent** methodology.</span></span>
5. <span data-ttu-id="43cee-115">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="43cee-115">Select **Create**.</span></span>

<span data-ttu-id="43cee-116">有关如何开始 Talent 的信息，请参阅在新项目中创建的 **Talent** 方法。</span><span class="sxs-lookup"><span data-stu-id="43cee-116">For information about how to get started with Talent, see the **Talent** methodology that you created in your new project.</span></span> <span data-ttu-id="43cee-117">在您完成创建项目后，请完成以下过程来设置您的 Talent 环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-117">After you've finished creating the project, complete the following procedure to provision your Talent environment.</span></span>

## <a name="provision-a-talent-project"></a><span data-ttu-id="43cee-118">配置 Talent 项目</span><span class="sxs-lookup"><span data-stu-id="43cee-118">Provision a Talent project</span></span>
<span data-ttu-id="43cee-119">在创建 LCS 项目之后，您可以将 Talent 配置到环境中。</span><span class="sxs-lookup"><span data-stu-id="43cee-119">After you've created an LCS project, you can provision Talent into an environment.</span></span>

1. <span data-ttu-id="43cee-120">在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="43cee-120">In your LCS project, select the **Talent App Management** tile.</span></span>
2. <span data-ttu-id="43cee-121">Talent 始终配置到 Microsoft PowerApps 环境，以支持 PowerApps 集成和可扩展性。</span><span class="sxs-lookup"><span data-stu-id="43cee-121">Talent is always provisioned into a Microsoft PowerApps environment, to enable PowerApps integration and extensibility.</span></span> <span data-ttu-id="43cee-122">如果您还没有 PowerApps 环境，在继续前请先执行本主题“创建新的 PowerApps 环境（如果需要）”部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="43cee-122">If you don't already have a PowerApps environment, follow the steps in the "Create a new PowerApps environment (if required)" section of this topic before you continue.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43cee-123">若要查看现有的环境或创建新环境，必须为配置 Talent 的租户管理员分配 PowerApps P2 许可证。</span><span class="sxs-lookup"><span data-stu-id="43cee-123">To view existing environments or create new environments, the tenant admin who provisions Talent must be assigned to the PowerApps P2 license.</span></span> <span data-ttu-id="43cee-124">如果您的组织没有 PowerApps P2 许可证，则可以从 CSP 或从 [PowerApps 定价页面](https://powerapps.microsoft.com/en-us/pricing/)获取一个。</span><span class="sxs-lookup"><span data-stu-id="43cee-124">If your organization doesn't have a PowerApps P2 license, you can get one from your CSP or from the [PowerApps pricing page](https://powerapps.microsoft.com/en-us/pricing/).</span></span>

3. <span data-ttu-id="43cee-125">选择**添加**，然后选择要为 Talent 配置的环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-125">Select **Add**, and then select the environment to provision Talent into.</span></span>
4. <span data-ttu-id="43cee-126">选择**是**同意条款并开始部署。</span><span class="sxs-lookup"><span data-stu-id="43cee-126">Select **Yes** to agree to the terms and begin deployment.</span></span>

    <span data-ttu-id="43cee-127">您的新环境将出现在左侧导航窗格的环境列表中。</span><span class="sxs-lookup"><span data-stu-id="43cee-127">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="43cee-128">不过，在部署状态更新为**已部署**前，您无法开始使用此环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-128">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="43cee-129">此过程通常需要几分钟。</span><span class="sxs-lookup"><span data-stu-id="43cee-129">This process typically takes just a few minutes.</span></span> <span data-ttu-id="43cee-130">如果配置失败，您必须与支持人员联系。</span><span class="sxs-lookup"><span data-stu-id="43cee-130">If provisioning fails, you must contact Support.</span></span>

6. <span data-ttu-id="43cee-131">选择**登录 Talent** 来使用您的新环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-131">Select **Log on to Talent** to use your new environment.</span></span>

> [!NOTE]
> <span data-ttu-id="43cee-132">如果您尚未验证最终要求，您可以在项目中部署 Talent 的测试实例。</span><span class="sxs-lookup"><span data-stu-id="43cee-132">If you haven't yet signed off on the final requirements, you can deploy a test instance of Talent in the project.</span></span> <span data-ttu-id="43cee-133">您可以随后使用此实例来测试您的解决方案，直到验证完成。</span><span class="sxs-lookup"><span data-stu-id="43cee-133">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="43cee-134">如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-134">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

## <a name="create-a-new-powerapps-environment-if-required"></a><span data-ttu-id="43cee-135">创建新的 PowerApps 环境（如果需要）</span><span class="sxs-lookup"><span data-stu-id="43cee-135">Create a new PowerApps environment (if required)</span></span>

<span data-ttu-id="43cee-136">Talent 与 PowerApps 环境集成背后的愿景是通过使用 PowerApps 工具和 Talent 数据，启用数据集成和扩展流。</span><span class="sxs-lookup"><span data-stu-id="43cee-136">The vision behind Talent’s integration with PowerApps environments is to enable data integration and extensions flows through the use of PowerApps tools on top of Talent data.</span></span> <span data-ttu-id="43cee-137">因此，选择要用于 Talent 的环境时，务必了解 PowerApps 环境的用途。</span><span class="sxs-lookup"><span data-stu-id="43cee-137">As a result, it is important to understand the purpose of PowerApps environments when choosing the environment to use for Talent.</span></span> <span data-ttu-id="43cee-138">有关 PowerApps 环境的详细信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 PowerApps 环境](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/)。</span><span class="sxs-lookup"><span data-stu-id="43cee-138">For more information about PowerApps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing PowerApps environments](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).</span></span>  <span data-ttu-id="43cee-139">由于默认 PowerApps 环境中将自动设置每个租户，所以该环境可能不是最适合用于您的 Talent 部署的环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-139">While each tenant is automatically provisioned in a Default PowerApps environment, it may not be the best environment to use for your Talent deployment.</span></span> <span data-ttu-id="43cee-140">此步骤中应考虑数据集成和测试策略，所以建议您注意对您的部署的各种影响，因为以后不容易更改。</span><span class="sxs-lookup"><span data-stu-id="43cee-140">Data integration and testing strategies should be considered during this step, so we recommend that you consider the various implications for your deployment, since it is not easy to change later.</span></span>

1. <span data-ttu-id="43cee-141">在 LCS 中选择**管理环境**。</span><span class="sxs-lookup"><span data-stu-id="43cee-141">Select **Manage Environments** in LCS.</span></span> <span data-ttu-id="43cee-142">您会被带到 [PowerApps 管理员中心](https://preview.admin.powerapps.com/environments)，从中您可以查看现有的环境并创建新环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-142">You're taken to the [PowerApps Admin Center](https://preview.admin.powerapps.com/environments), where you can view existing environments and create new environments.</span></span>
2. <span data-ttu-id="43cee-143">选择 (**+**) **新建环境**按钮。</span><span class="sxs-lookup"><span data-stu-id="43cee-143">Select the (**+**) **New environment** button.</span></span>
3. <span data-ttu-id="43cee-144">为环境输入唯一名称，然后选择要部署的位置。</span><span class="sxs-lookup"><span data-stu-id="43cee-144">Enter a unique name for the environment, and select the location to deploy to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43cee-145">Talent 不是在所有地区都可用。</span><span class="sxs-lookup"><span data-stu-id="43cee-145">Talent isn't available in all regions.</span></span> <span data-ttu-id="43cee-146">因此，在您为环境选择位置之前，请务必检查可用性。</span><span class="sxs-lookup"><span data-stu-id="43cee-146">Therefore, be sure to check for availability before you select the location for your environment.</span></span>

4. <span data-ttu-id="43cee-147">在询问您是否要创建数据库时，请选择**创建数据库**来创建必须承载Talent 数据的一部分的 Common Data Service (CDS) 数据库。</span><span class="sxs-lookup"><span data-stu-id="43cee-147">When you're asked whether you want to create a database, select **Create database** to create the Common Data Service (CDS) database that must host part of your Talent data.</span></span> <span data-ttu-id="43cee-148">通过创建数据库，您还可以将 PowerApps 应用程序与 Talent 集成。</span><span class="sxs-lookup"><span data-stu-id="43cee-148">By creating a database, you can also integrate PowerApps applications with Talent.</span></span>
5. <span data-ttu-id="43cee-149">您将被询问要用于数据库的访问级别。</span><span class="sxs-lookup"><span data-stu-id="43cee-149">You're asked about the access level that you want to use for the database.</span></span> <span data-ttu-id="43cee-150">我们建议您选择**限制访问**，因为此选项通过使用 PowerApps 应用程序阻止 Talent 用户直接访问敏感数据。</span><span class="sxs-lookup"><span data-stu-id="43cee-150">We recommend that you select **Restrict access**, because this option prevents Talent users from directly accessing sensitive data by using a PowerApps application.</span></span>
6. <span data-ttu-id="43cee-151">创建的 CDS 数据库包含演示数据。</span><span class="sxs-lookup"><span data-stu-id="43cee-151">The CDS database that is created contains demo data.</span></span> <span data-ttu-id="43cee-152">此演示数据很有用，因为您可以使用演示数据公司进行测试，或创建任务录制或任务指南。</span><span class="sxs-lookup"><span data-stu-id="43cee-152">This demo data is useful, because you can use the demo data company for testing, or to create task recordings or task guides.</span></span> <span data-ttu-id="43cee-153">但是，演示数据会将其他信息中的非活动员工和虚构地址添加到您的生产环境中。</span><span class="sxs-lookup"><span data-stu-id="43cee-153">However, the demo data adds inactive employees and fictitious addresses, among other information, to your production environment.</span></span> <span data-ttu-id="43cee-154">若要删除演示数据，在您完成创建 CDS 数据库后执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="43cee-154">To remove the demo data, follow these steps after you've finished creating the CDS database:</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="43cee-155">如果您以前已创建了 CDS 数据库并在其中输入了您公司的任何生产数据，请注意，以下步骤将删除所选数据库中的**所有**数据，甚至您公司的生产数据。</span><span class="sxs-lookup"><span data-stu-id="43cee-155">If you previously created a CDS database and entered any of your company's production data into it, be aware that these steps remove **all** the data in the selected database, even your company's production data.</span></span>

    1. <span data-ttu-id="43cee-156">登录 [PowerApps](https://preview.web.powerapps.com/home)，然后从页面右侧的下拉列表中选择步骤 2 中创建的环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-156">Sign in to [PowerApps](https://preview.web.powerapps.com/home), and select the environment that you created in step 2 from the drop-down on the right side of the page.</span></span>
    2. <span data-ttu-id="43cee-157">展开左导航窗格中的 **Common Data Service**，然后选择**实体**。</span><span class="sxs-lookup"><span data-stu-id="43cee-157">Expand the **Common Data Service** on the left navigation pane and choose **Entities**.</span></span>
    3. <span data-ttu-id="43cee-158">在页面的右侧，请选择椭圆形 (**…**) 按钮，然后选择**清除所有数据**。</span><span class="sxs-lookup"><span data-stu-id="43cee-158">On the right side of the page, select the ellipse (**…**) button, and then select **Clear all data**.</span></span>
    4. <span data-ttu-id="43cee-159">选择**删除数据**以确认您要删除该数据。</span><span class="sxs-lookup"><span data-stu-id="43cee-159">Select **Delete data** to confirm that you want to remove the data.</span></span> <span data-ttu-id="43cee-160">此操作默认情况下将删除 CDS 中包括的所有演示数据。</span><span class="sxs-lookup"><span data-stu-id="43cee-160">This action removes all the demo data that is included in the CDS by default.</span></span> <span data-ttu-id="43cee-161">它还会删除在所选数据库中输入的任何其他数据。</span><span class="sxs-lookup"><span data-stu-id="43cee-161">It also removes any other data that has been entered in the selected database.</span></span>
    
<span data-ttu-id="43cee-162">您现在可以使用您的新环境了。</span><span class="sxs-lookup"><span data-stu-id="43cee-162">You can now use your new environment.</span></span>

## <a name="granting-access-to-the-environment"></a><span data-ttu-id="43cee-163">创建对环境的访问</span><span class="sxs-lookup"><span data-stu-id="43cee-163">Granting access to the environment</span></span>
<span data-ttu-id="43cee-164">默认情况下，创建环境的全局管理员拥有访问权，但是必须为其他应用程序用户明确授予访问权。</span><span class="sxs-lookup"><span data-stu-id="43cee-164">The global administrator that created the environment will have access by default, but additional application users must be explicitly granted access.</span></span> <span data-ttu-id="43cee-165">方法是，在 Core HR 环境内部[添加用户](../dev-itpro/sysadmin/tasks/create-new-users.md)并[为其分配相应角色](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="43cee-165">This can be done by [adding users](../dev-itpro/sysadmin/tasks/create-new-users.md) and [assigning them the appropriate roles](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) within the Core HR environment.</span></span> <span data-ttu-id="43cee-166">此外，还必须将这些用户添加到 PowerApps 环境，以便他们可以访问 Attract 和 Onboard 应用程序。</span><span class="sxs-lookup"><span data-stu-id="43cee-166">In addition to this, it is also necessary to add those users to the PowerApps environment so they can access the Attract and Onboard applications.</span></span>  <span data-ttu-id="43cee-167">博客文章[介绍 PowerApps 管理中心](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/)可能可以帮助您完成下面概述的这些步骤：</span><span class="sxs-lookup"><span data-stu-id="43cee-167">The blog post, [Introducing the PowerApps admin center](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) might help you to complete those steps, which are outlined here:</span></span>

> 1.    <span data-ttu-id="43cee-168">部署 Talent 环境的全局管理员应导航到 [PowerApps 管理中心](https://preview.admin.powerapps.com/environments)。</span><span class="sxs-lookup"><span data-stu-id="43cee-168">The global administrator that deployed the Talent environment should navigate to the [PowerApps Admin center](https://preview.admin.powerapps.com/environments).</span></span>   
> 2.    <span data-ttu-id="43cee-169">选择所讨论的环境。</span><span class="sxs-lookup"><span data-stu-id="43cee-169">Select the environment(s) in question.</span></span>
> 3.    <span data-ttu-id="43cee-170">在"安全性:选项卡下，将必要的用户添加到“环境制造者”角色。</span><span class="sxs-lookup"><span data-stu-id="43cee-170">Under the Security tab, add the necessary users to the “Environment Maker” role.</span></span>

<span data-ttu-id="43cee-171">请注意，这个将用户添加到 PowerApps 环境的最后一步是暂时的。</span><span class="sxs-lookup"><span data-stu-id="43cee-171">Note that this final step of adding users to the PowerApps environment is temporary.</span></span> <span data-ttu-id="43cee-172">我们最终将增加功能，以便在 Core HR 内添加了用户时，自动实现此步骤。</span><span class="sxs-lookup"><span data-stu-id="43cee-172">We will eventually add functionality to enable this automatically when the user is added within Core HR.</span></span>


