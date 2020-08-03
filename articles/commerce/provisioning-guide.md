---
title: 预配 Dynamics 365 Commerce 评估环境
description: 本主题说明如何预配 Microsoft Dynamics 365 Commerce 评估环境。
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e5ce2002c66a1c36d5647d3c76684b394fc1ff79
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599842"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="15db3-103">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="15db3-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15db3-104">本主题说明如何预配 Microsoft Dynamics 365 Commerce 评估环境。</span><span class="sxs-lookup"><span data-stu-id="15db3-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="15db3-105">在开始之前，我们建议您快速浏览本主题以了解该过程的要求。</span><span class="sxs-lookup"><span data-stu-id="15db3-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="15db3-106">Commerce 评估环境不是公开发布的服务，它根据请求授予合作伙伴和客户使用权。</span><span class="sxs-lookup"><span data-stu-id="15db3-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="15db3-107">有关详细信息，请联系您的 Microsoft 合作伙伴联系人。</span><span class="sxs-lookup"><span data-stu-id="15db3-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="15db3-108">概览</span><span class="sxs-lookup"><span data-stu-id="15db3-108">Overview</span></span>

<span data-ttu-id="15db3-109">要成功预配 Commerce 评估环境，您必须创建一个具有特定产品名称和类型的项目。</span><span class="sxs-lookup"><span data-stu-id="15db3-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="15db3-110">此环境和 Commerce Scale Unit (CSU) 还具有一些特定的参数，当您以后希望预配电子商务时必须使用这些参数。</span><span class="sxs-lookup"><span data-stu-id="15db3-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="15db3-111">本主题中的说明介绍完成预配所需的所有步骤以及必须使用的参数。</span><span class="sxs-lookup"><span data-stu-id="15db3-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="15db3-112">成功预配 Commerce 评估环境后，还必须完成一些预配后步骤来为使用作准备。</span><span class="sxs-lookup"><span data-stu-id="15db3-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="15db3-113">其中一些步骤可选，具体取决于要评估系统的哪些方面。</span><span class="sxs-lookup"><span data-stu-id="15db3-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="15db3-114">您可以在以后随时完成可选步骤。</span><span class="sxs-lookup"><span data-stu-id="15db3-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="15db3-115">有关在预配后如何预配 Commerce 评估环境的信息，请参阅[预配 Commerce 评估环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="15db3-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="15db3-116">有关为 Commerce 评估环境预配可选功能的信息，请参阅[为 Commerce 评估环境预配可选功能](cpe-optional-features.md)。</span><span class="sxs-lookup"><span data-stu-id="15db3-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15db3-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="15db3-117">Prerequisites</span></span>

<span data-ttu-id="15db3-118">必须先满足以下先决条件，才能预配 Commerce 评估环境：</span><span class="sxs-lookup"><span data-stu-id="15db3-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="15db3-119">您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。</span><span class="sxs-lookup"><span data-stu-id="15db3-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="15db3-120">您是现有的 Microsoft Dynamics 365 合作伙伴或客户，并能够创建 Dynamics 365 Commerce 项目。</span><span class="sxs-lookup"><span data-stu-id="15db3-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="15db3-121">您具有对 Microsoft Azure 订阅的管理员访问权限，或者在需要时与可以帮助您的订阅管理员联系。</span><span class="sxs-lookup"><span data-stu-id="15db3-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="15db3-122">您有可用的 Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="15db3-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="15db3-123">您已创建了可以用作电子商务系统管理员组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="15db3-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="15db3-124">您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="15db3-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="15db3-125">（此安全组可以与电子商务系统管理员组相同。）</span><span class="sxs-lookup"><span data-stu-id="15db3-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="15db3-126">请注意，此列表并不详尽。</span><span class="sxs-lookup"><span data-stu-id="15db3-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="15db3-127">如果您遇到任何问题，请联系您的 Microsoft 合作伙伴联系人寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="15db3-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="15db3-128">预配您的 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="15db3-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="15db3-129">这些过程说明如何预配 Commerce 评估环境。</span><span class="sxs-lookup"><span data-stu-id="15db3-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="15db3-130">成功完成这些过程之后，Commerce 评估环境将可以进行配置。</span><span class="sxs-lookup"><span data-stu-id="15db3-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="15db3-131">此处介绍的所有活动都在 LCS 门户中进行。</span><span class="sxs-lookup"><span data-stu-id="15db3-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="15db3-132">创建新项目</span><span class="sxs-lookup"><span data-stu-id="15db3-132">Create a new project</span></span>

<span data-ttu-id="15db3-133">若要在 LCS 中创建新项目，请按以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="15db3-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="15db3-134">在 LCS 主页上，选择加号 (**+**) 创建一个项目。</span><span class="sxs-lookup"><span data-stu-id="15db3-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="15db3-135">在右窗格中，请按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="15db3-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="15db3-136">如果您是合作伙伴，请选择**迁移，创建解决方案，了解**。</span><span class="sxs-lookup"><span data-stu-id="15db3-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="15db3-137">如果您是客户，请选择**潜在售前支持**。</span><span class="sxs-lookup"><span data-stu-id="15db3-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="15db3-138">输入名称、描述和行业。</span><span class="sxs-lookup"><span data-stu-id="15db3-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="15db3-139">在**产品名称**字段中，选择 **Dynamics 365 Commerce**。</span><span class="sxs-lookup"><span data-stu-id="15db3-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="15db3-140">在**产品版本**字段中，选择 **Dynamics 365 Commerce**。</span><span class="sxs-lookup"><span data-stu-id="15db3-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="15db3-141">在**方法**字段中，选择 **Dynamics Retail 实施方法**。</span><span class="sxs-lookup"><span data-stu-id="15db3-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="15db3-142">可选：您可以从现有项目导入角色和用户。</span><span class="sxs-lookup"><span data-stu-id="15db3-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="15db3-143">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="15db3-143">Select **Create**.</span></span> <span data-ttu-id="15db3-144">将出现项目视图。</span><span class="sxs-lookup"><span data-stu-id="15db3-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="15db3-145">添加 Azure 连接器</span><span class="sxs-lookup"><span data-stu-id="15db3-145">Add the Azure Connector</span></span>

<span data-ttu-id="15db3-146">要将 Azure 连接器添加到您的 LCS 项目，请按照[完成 Azure 资源管理器 (ARM) 加入流程](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="15db3-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="15db3-147">部署环境</span><span class="sxs-lookup"><span data-stu-id="15db3-147">Deploy the environment</span></span>

<span data-ttu-id="15db3-148">要部署环境，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="15db3-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="15db3-149">您可能不必完成步骤 6、7 和/或 8，因为将跳过具有单个选项的页面。</span><span class="sxs-lookup"><span data-stu-id="15db3-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="15db3-150">在**环境参数**视图中时，请确认文本 **Dynamics 365 Commerce - 演示(具有平台更新 *xx* 的 10.0.* x*)**直接出现在**环境名称\*\*字段上方。</span><span class="sxs-lookup"><span data-stu-id="15db3-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="15db3-151">有关详细信息，请参阅步骤 8 之后出现的图示。</span><span class="sxs-lookup"><span data-stu-id="15db3-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="15db3-152">在顶级菜单上，选择**云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="15db3-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="15db3-153">选择**添加**添加环境。</span><span class="sxs-lookup"><span data-stu-id="15db3-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="15db3-154">在**应用程序版本**字段中，选择最新版本。</span><span class="sxs-lookup"><span data-stu-id="15db3-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="15db3-155">如果您明确需要选择除最新版本以外的其他应用程序版本，请不要选择 **10.0.8** 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="15db3-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="15db3-156">在**平台版本**字段中，使用为所选应用程序版本自动选择的平台版本。</span><span class="sxs-lookup"><span data-stu-id="15db3-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![选择应用程序和平台版本](./media/project1.png)

1. <span data-ttu-id="15db3-158">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="15db3-158">Select **Next**.</span></span>
1. <span data-ttu-id="15db3-159">选择**演示**作为环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="15db3-159">Select **Demo** as the environment topology.</span></span>

    ![选择环境拓扑 1](./media/project2.png)

1. <span data-ttu-id="15db3-161">在**部署环境**页面上，输入环境名称。</span><span class="sxs-lookup"><span data-stu-id="15db3-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="15db3-162">高级设置保持原样。</span><span class="sxs-lookup"><span data-stu-id="15db3-162">Leave the advanced settings as they are.</span></span>

    ![部署环境页面](./media/project4.png)

1. <span data-ttu-id="15db3-164">根据需要调整 VM 大小。</span><span class="sxs-lookup"><span data-stu-id="15db3-164">Adjust the VM size as required.</span></span> <span data-ttu-id="15db3-165">（我们建议使用 VM 库存单位 \[SKU\] **D13 v2**。）</span><span class="sxs-lookup"><span data-stu-id="15db3-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="15db3-166">查看定价和许可条款，然后选中指示您同意这些条款的复选框。</span><span class="sxs-lookup"><span data-stu-id="15db3-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="15db3-167">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="15db3-167">Select **Next**.</span></span>
1. <span data-ttu-id="15db3-168">在部署确认页面，验证详细信息是否正确，然后选择**部署**。</span><span class="sxs-lookup"><span data-stu-id="15db3-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="15db3-169">您已返回到**云托管的环境**视图，列表中应该会显示您的环境。</span><span class="sxs-lookup"><span data-stu-id="15db3-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="15db3-170">您请求的环境将显示为已入队列，然后是正在部署。</span><span class="sxs-lookup"><span data-stu-id="15db3-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="15db3-171">环境工作流将需要一些时间完成。</span><span class="sxs-lookup"><span data-stu-id="15db3-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="15db3-172">因此，请在大约六到九小时后再次检查。</span><span class="sxs-lookup"><span data-stu-id="15db3-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="15db3-173">继续操作之前，确保环境的状态为**已部署**。</span><span class="sxs-lookup"><span data-stu-id="15db3-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="15db3-174">初始化 Commerce Scale Unit（云）</span><span class="sxs-lookup"><span data-stu-id="15db3-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="15db3-175">要初始化您的 CSU，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="15db3-175">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="15db3-176">在**云托管的环境**视图中，在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="15db3-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="15db3-177">在右侧的环境视图中，选择**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="15db3-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="15db3-178">将显示环境详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="15db3-178">The environment details view appears.</span></span>
1. <span data-ttu-id="15db3-179">在**环境功能**下，选择**管理**。</span><span class="sxs-lookup"><span data-stu-id="15db3-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="15db3-180">在**商业**选项卡上，选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="15db3-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="15db3-181">将显示 CSU 初始化参数视图。</span><span class="sxs-lookup"><span data-stu-id="15db3-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="15db3-182">在**区域**字段中，选择与您将环境部署到的区域相同或接近的区域。</span><span class="sxs-lookup"><span data-stu-id="15db3-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="15db3-183">保留**版本**字段不变。</span><span class="sxs-lookup"><span data-stu-id="15db3-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="15db3-184">选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="15db3-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="15db3-185">在部署确认页面，验证详细信息是否正确，然后选择**是**。</span><span class="sxs-lookup"><span data-stu-id="15db3-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="15db3-186">**商业管理**视图再次显示，其中的**商业**选项卡被选中。</span><span class="sxs-lookup"><span data-stu-id="15db3-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="15db3-187">您的 CSU 现在已进入队列等待配置。</span><span class="sxs-lookup"><span data-stu-id="15db3-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="15db3-188">继续操作之前，确保 CSU 的状态为**成功**。</span><span class="sxs-lookup"><span data-stu-id="15db3-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="15db3-189">初始化大约需要两到五个小时。</span><span class="sxs-lookup"><span data-stu-id="15db3-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="15db3-190">如果在环境详细信息视图中找不到**管理**链接，请联系您的 Microsoft 联系人寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="15db3-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="15db3-191">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="15db3-191">Initialize e-Commerce</span></span>

<span data-ttu-id="15db3-192">要初始化电子商务，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="15db3-192">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="15db3-193">在**电子商务**选项卡上，查看评估同意内容，然后选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="15db3-193">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="15db3-194">在**电子商务环境名称**字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="15db3-194">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="15db3-195">请注意，某些指向您的电子商务实例的 URL 中将显示此名称。</span><span class="sxs-lookup"><span data-stu-id="15db3-195">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="15db3-196">在 **Commerce Scale Unit 名称**字段中，在列表中选择您的 CSU。</span><span class="sxs-lookup"><span data-stu-id="15db3-196">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="15db3-197">（此列表应该只有一个选项。）</span><span class="sxs-lookup"><span data-stu-id="15db3-197">(The list should have only one option.)</span></span>

    <span data-ttu-id="15db3-198">**电子商务地理位置**字段是自动设置的。</span><span class="sxs-lookup"><span data-stu-id="15db3-198">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="15db3-199">选择**下一步**继续。</span><span class="sxs-lookup"><span data-stu-id="15db3-199">Select **Next** to continue.</span></span>
1. <span data-ttu-id="15db3-200">在**支持的主机名**字段中，输入任意有效域，例如 `www.fabrikam.com`。</span><span class="sxs-lookup"><span data-stu-id="15db3-200">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="15db3-201">在**系统管理员的 AAD 安全组**字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。</span><span class="sxs-lookup"><span data-stu-id="15db3-201">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="15db3-202">在列表中选择正确的安全组。</span><span class="sxs-lookup"><span data-stu-id="15db3-202">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="15db3-203">在**评级和审查仲裁者的 AAD 安全组**字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。</span><span class="sxs-lookup"><span data-stu-id="15db3-203">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="15db3-204">在列表中选择正确的安全组。</span><span class="sxs-lookup"><span data-stu-id="15db3-204">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="15db3-205">**启用评分和评价服务**选项设置保留为**是**。</span><span class="sxs-lookup"><span data-stu-id="15db3-205">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="15db3-206">选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="15db3-206">Select **Initialize**.</span></span> <span data-ttu-id="15db3-207">**商业管理**视图再次显示，其中的**电子商务**选项卡被选中。</span><span class="sxs-lookup"><span data-stu-id="15db3-207">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="15db3-208">电子商务初始化已开始。</span><span class="sxs-lookup"><span data-stu-id="15db3-208">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="15db3-209">请等待电子商务初始化的状态成为**初始化成功**，再继续操作。</span><span class="sxs-lookup"><span data-stu-id="15db3-209">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="15db3-210">在右下方的**链接**下，记下以下链接的 URL：</span><span class="sxs-lookup"><span data-stu-id="15db3-210">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="15db3-211">**电子商务站点** – 指向您的电子商务站点的根目录的链接。</span><span class="sxs-lookup"><span data-stu-id="15db3-211">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="15db3-212">**电子商务站点构建器** – 站点管理工具的链接。</span><span class="sxs-lookup"><span data-stu-id="15db3-212">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="15db3-213">后续步骤</span><span class="sxs-lookup"><span data-stu-id="15db3-213">Next steps</span></span>

<span data-ttu-id="15db3-214">要继续 Commerce 评估环境的预配和配置过程，请参阅[配置 Commerce 评估环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="15db3-214">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15db3-215">其他资源</span><span class="sxs-lookup"><span data-stu-id="15db3-215">Additional resources</span></span>

[<span data-ttu-id="15db3-216">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="15db3-216">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="15db3-217">配置 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="15db3-217">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="15db3-218">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="15db3-218">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="15db3-219">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="15db3-219">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="15db3-220">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="15db3-220">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="15db3-221">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="15db3-221">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="15db3-222">Commerce Scale Unit（云）</span><span class="sxs-lookup"><span data-stu-id="15db3-222">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="15db3-223">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="15db3-223">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="15db3-224">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="15db3-224">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
