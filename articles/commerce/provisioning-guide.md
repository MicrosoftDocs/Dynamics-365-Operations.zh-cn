---
title: 预配 Dynamics 365 Commerce 评估环境
description: 本主题说明如何预配 Microsoft Dynamics 365 Commerce 评估环境。
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8cda79a6be1aca7ad3826b9409e110524e6560e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969893"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="d9f30-103">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="d9f30-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9f30-104">本主题说明如何预配 Microsoft Dynamics 365 Commerce 评估环境。</span><span class="sxs-lookup"><span data-stu-id="d9f30-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="d9f30-105">在开始之前，我们建议您快速浏览本主题以了解该过程的要求。</span><span class="sxs-lookup"><span data-stu-id="d9f30-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="d9f30-106">Commerce 评估环境不是公开发布的服务，它根据请求授予合作伙伴和客户使用权。</span><span class="sxs-lookup"><span data-stu-id="d9f30-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="d9f30-107">有关详细信息，请联系您的 Microsoft 合作伙伴联系人。</span><span class="sxs-lookup"><span data-stu-id="d9f30-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="d9f30-108">概览</span><span class="sxs-lookup"><span data-stu-id="d9f30-108">Overview</span></span>

<span data-ttu-id="d9f30-109">要成功预配 Commerce 评估环境，您必须创建一个具有特定产品名称和类型的项目。</span><span class="sxs-lookup"><span data-stu-id="d9f30-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="d9f30-110">此环境和 Commerce Scale Unit (CSU) 还具有一些特定的参数，当您以后希望预配电子商务时必须使用这些参数。</span><span class="sxs-lookup"><span data-stu-id="d9f30-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="d9f30-111">本主题中的说明介绍完成预配所需的所有步骤以及必须使用的参数。</span><span class="sxs-lookup"><span data-stu-id="d9f30-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="d9f30-112">成功预配 Commerce 评估环境后，还必须完成一些预配后步骤来为使用作准备。</span><span class="sxs-lookup"><span data-stu-id="d9f30-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="d9f30-113">其中一些步骤可选，具体取决于要评估系统的哪些方面。</span><span class="sxs-lookup"><span data-stu-id="d9f30-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="d9f30-114">您可以在以后随时完成可选步骤。</span><span class="sxs-lookup"><span data-stu-id="d9f30-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="d9f30-115">有关在预配后如何预配 Commerce 评估环境的信息，请参阅[预配 Commerce 评估环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="d9f30-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="d9f30-116">有关为 Commerce 评估环境预配可选功能的信息，请参阅[为 Commerce 评估环境预配可选功能](cpe-optional-features.md)。</span><span class="sxs-lookup"><span data-stu-id="d9f30-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9f30-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="d9f30-117">Prerequisites</span></span>

<span data-ttu-id="d9f30-118">必须先满足以下先决条件，才能预配 Commerce 评估环境：</span><span class="sxs-lookup"><span data-stu-id="d9f30-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="d9f30-119">您已加入评估计划，并获得了评估环境的能力。</span><span class="sxs-lookup"><span data-stu-id="d9f30-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="d9f30-120">您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。</span><span class="sxs-lookup"><span data-stu-id="d9f30-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="d9f30-121">您是现有的 Microsoft Dynamics 365 合作伙伴或客户，并能够创建 Dynamics 365 Commerce 项目。</span><span class="sxs-lookup"><span data-stu-id="d9f30-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="d9f30-122">您具有对 Microsoft Azure 订阅的管理员访问权限，或者在需要时与可以帮助您的订阅管理员联系。</span><span class="sxs-lookup"><span data-stu-id="d9f30-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="d9f30-123">您有可用的 Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="d9f30-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="d9f30-124">您已创建了可以用作电子商务系统管理员组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="d9f30-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="d9f30-125">您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="d9f30-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="d9f30-126">（此安全组可以与电子商务系统管理员组相同。）</span><span class="sxs-lookup"><span data-stu-id="d9f30-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="d9f30-127">请注意，此列表并不详尽。</span><span class="sxs-lookup"><span data-stu-id="d9f30-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="d9f30-128">如果您遇到任何问题，请联系您的 Microsoft 合作伙伴联系人寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="d9f30-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="d9f30-129">预配您的 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="d9f30-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="d9f30-130">这些过程说明如何预配 Commerce 评估环境。</span><span class="sxs-lookup"><span data-stu-id="d9f30-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="d9f30-131">成功完成这些过程之后，Commerce 评估环境将可以进行配置。</span><span class="sxs-lookup"><span data-stu-id="d9f30-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="d9f30-132">此处介绍的所有活动都在 LCS 门户中进行。</span><span class="sxs-lookup"><span data-stu-id="d9f30-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="d9f30-133">创建新项目</span><span class="sxs-lookup"><span data-stu-id="d9f30-133">Create a new project</span></span>

<span data-ttu-id="d9f30-134">若要在 LCS 中创建新项目，请按以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="d9f30-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="d9f30-135">在 LCS 主页上，选择加号 (**+**) 创建一个项目。</span><span class="sxs-lookup"><span data-stu-id="d9f30-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="d9f30-136">在右窗格中，请按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="d9f30-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="d9f30-137">如果您是合作伙伴，请选择 **迁移，创建解决方案，了解**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="d9f30-138">如果您是客户，请选择 **潜在售前支持**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="d9f30-139">输入名称、描述和行业。</span><span class="sxs-lookup"><span data-stu-id="d9f30-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="d9f30-140">在 **产品名称** 字段中，选择 **Dynamics 365 Commerce**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="d9f30-141">在 **产品版本** 字段中，选择 **Dynamics 365 Commerce**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="d9f30-142">在 **方法** 字段中，选择 **Dynamics Retail 实施方法**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="d9f30-143">可选：您可以从现有项目导入角色和用户。</span><span class="sxs-lookup"><span data-stu-id="d9f30-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="d9f30-144">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-144">Select **Create**.</span></span> <span data-ttu-id="d9f30-145">将出现项目视图。</span><span class="sxs-lookup"><span data-stu-id="d9f30-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="d9f30-146">添加 Azure 连接器</span><span class="sxs-lookup"><span data-stu-id="d9f30-146">Add the Azure Connector</span></span>

<span data-ttu-id="d9f30-147">要将 Azure 连接器添加到您的 LCS 项目，请按照[完成 Azure 资源管理器 (ARM) 加入流程](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9f30-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="d9f30-148">部署环境</span><span class="sxs-lookup"><span data-stu-id="d9f30-148">Deploy the environment</span></span>

<span data-ttu-id="d9f30-149">要部署环境，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9f30-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="d9f30-150">您可能不必完成步骤 6、7 和/或 8，因为将跳过具有单个选项的页面。</span><span class="sxs-lookup"><span data-stu-id="d9f30-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="d9f30-151">在 **环境参数** 视图中时，请确认文本 **Dynamics 365 Commerce - 演示(具有平台更新 *xx* 的 10.0.* x*)\*\*直接出现在 **环境名称** 字段上方。</span><span class="sxs-lookup"><span data-stu-id="d9f30-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="d9f30-152">有关详细信息，请参阅步骤 8 之后出现的图示。</span><span class="sxs-lookup"><span data-stu-id="d9f30-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="d9f30-153">在顶级菜单上，选择 **云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d9f30-154">选择 **添加** 添加环境。</span><span class="sxs-lookup"><span data-stu-id="d9f30-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="d9f30-155">在 **应用程序版本** 字段中，选择最新版本。</span><span class="sxs-lookup"><span data-stu-id="d9f30-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="d9f30-156">如果您明确需要选择除最新版本以外的其他应用程序版本，请不要选择 **10.0.14** 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="d9f30-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="d9f30-157">在 **平台版本** 字段中，使用为所选应用程序版本自动选择的平台版本。</span><span class="sxs-lookup"><span data-stu-id="d9f30-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![选择应用程序和平台版本](./media/project1.png)

1. <span data-ttu-id="d9f30-159">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-159">Select **Next**.</span></span>
1. <span data-ttu-id="d9f30-160">选择 **演示** 作为环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="d9f30-160">Select **Demo** as the environment topology.</span></span>

    ![选择环境拓扑 1](./media/project2.png)

1. <span data-ttu-id="d9f30-162">在 **部署环境** 页面上，输入环境名称。</span><span class="sxs-lookup"><span data-stu-id="d9f30-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="d9f30-163">高级设置保持原样。</span><span class="sxs-lookup"><span data-stu-id="d9f30-163">Leave the advanced settings as they are.</span></span>

    ![部署环境页面](./media/project4.png)

1. <span data-ttu-id="d9f30-165">根据需要调整 VM 大小。</span><span class="sxs-lookup"><span data-stu-id="d9f30-165">Adjust the VM size as required.</span></span> <span data-ttu-id="d9f30-166">（我们建议使用 VM 库存单位 \[SKU\] **D13 v2**。）</span><span class="sxs-lookup"><span data-stu-id="d9f30-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="d9f30-167">查看定价和许可条款，然后选中指示您同意这些条款的复选框。</span><span class="sxs-lookup"><span data-stu-id="d9f30-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="d9f30-168">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-168">Select **Next**.</span></span>
1. <span data-ttu-id="d9f30-169">在部署确认页面，验证详细信息是否正确，然后选择 **部署**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="d9f30-170">您已返回到 **云托管的环境** 视图，列表中应该会显示您的环境。</span><span class="sxs-lookup"><span data-stu-id="d9f30-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="d9f30-171">您请求的环境将显示为已入队列，然后是正在部署。</span><span class="sxs-lookup"><span data-stu-id="d9f30-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="d9f30-172">环境工作流将需要一些时间完成。</span><span class="sxs-lookup"><span data-stu-id="d9f30-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="d9f30-173">因此，请在大约六到九小时后再次检查。</span><span class="sxs-lookup"><span data-stu-id="d9f30-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="d9f30-174">继续操作之前，确保环境的状态为 **已部署**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="d9f30-175">初始化 Commerce Scale Unit（云）</span><span class="sxs-lookup"><span data-stu-id="d9f30-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="d9f30-176">要初始化 CSU，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d9f30-176">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="d9f30-177">在 **云托管的环境** 视图中，在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="d9f30-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="d9f30-178">在右侧的环境视图中，选择 **完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="d9f30-179">将显示环境详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="d9f30-179">The environment details view appears.</span></span>
1. <span data-ttu-id="d9f30-180">在 **环境功能** 下，选择 **管理**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="d9f30-181">在 **商业** 选项卡上，选择 **初始化**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="d9f30-182">将显示 CSU 初始化参数视图。</span><span class="sxs-lookup"><span data-stu-id="d9f30-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="d9f30-183">在 **区域** 字段中，选择与您将环境部署到的区域相同或接近的区域。</span><span class="sxs-lookup"><span data-stu-id="d9f30-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="d9f30-184">保留 **版本** 字段不变。</span><span class="sxs-lookup"><span data-stu-id="d9f30-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="d9f30-185">选择 **初始化**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="d9f30-186">在部署确认页面，验证详细信息是否正确，然后选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="d9f30-187">**商业管理** 视图再次显示，其中的 **商业** 选项卡被选中。</span><span class="sxs-lookup"><span data-stu-id="d9f30-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="d9f30-188">您的 CSU 现在已进入队列等待配置。</span><span class="sxs-lookup"><span data-stu-id="d9f30-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="d9f30-189">继续操作之前，确保 CSU 的状态为 **成功**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="d9f30-190">初始化大约需要两到五个小时。</span><span class="sxs-lookup"><span data-stu-id="d9f30-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="d9f30-191">如果在环境详细信息视图中找不到 **管理** 链接，请联系您的 Microsoft 联系人寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="d9f30-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="d9f30-192">在部署流程期间，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="d9f30-192">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="d9f30-193">评估（演示/测试）环境需要在总部注册缩放单元连接器应用程序 \<application ID\>。</span><span class="sxs-lookup"><span data-stu-id="d9f30-193">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="d9f30-194">如果 CSU 初始化失败，您收到此错误消息，请记下应用程序 ID，是一个全局唯一标识符 (GUID)，然后按照下一节中的步骤在 Commerce headquarters 中注册 CSU 部署应用程序。</span><span class="sxs-lookup"><span data-stu-id="d9f30-194">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="d9f30-195">在 Commerce headquarters 中注册 CSU 部署应用程序（如果需要）</span><span class="sxs-lookup"><span data-stu-id="d9f30-195">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="d9f30-196">要在 Commerce headquarters 中注册 CSU 部署应用程序，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9f30-196">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d9f30-197">在 Commerce headquarters 中，转到 **系统管理 \> 设置 \> Azure Active Directory 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-197">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="d9f30-198">在 **客户端 ID** 列中，输入您收到的 CSU 初始化错误消息中的应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="d9f30-198">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="d9f30-199">在 **名称** 列中，输入任何描述性文本（例如，**CSU 评估**）。</span><span class="sxs-lookup"><span data-stu-id="d9f30-199">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="d9f30-200">在 **用户 ID** 列中，输入 **RetailServiceAccount**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-200">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="d9f30-201">从 LCS 重试 CSU 初始化和部署。</span><span class="sxs-lookup"><span data-stu-id="d9f30-201">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="d9f30-202">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="d9f30-202">Initialize e-Commerce</span></span>

<span data-ttu-id="d9f30-203">要初始化电子商务，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d9f30-203">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d9f30-204">在 **电子商务** 选项卡上，查看评估同意内容，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-204">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="d9f30-205">在 **电子商务环境名称** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="d9f30-205">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="d9f30-206">请注意，某些指向您的电子商务实例的 URL 中将显示此名称。</span><span class="sxs-lookup"><span data-stu-id="d9f30-206">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="d9f30-207">在 **Commerce Scale Unit 名称** 字段中，在列表中选择您的 CSU。</span><span class="sxs-lookup"><span data-stu-id="d9f30-207">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="d9f30-208">（此列表应该只有一个选项。）</span><span class="sxs-lookup"><span data-stu-id="d9f30-208">(The list should have only one option.)</span></span>

    <span data-ttu-id="d9f30-209">**电子商务地理位置** 字段是自动设置的。</span><span class="sxs-lookup"><span data-stu-id="d9f30-209">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="d9f30-210">选择 **下一步** 继续。</span><span class="sxs-lookup"><span data-stu-id="d9f30-210">Select **Next** to continue.</span></span>
1. <span data-ttu-id="d9f30-211">在 **支持的主机名** 字段中，输入任意有效域，例如 `www.fabrikam.com`。</span><span class="sxs-lookup"><span data-stu-id="d9f30-211">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="d9f30-212">在 **系统管理员的 AAD 安全组** 字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。</span><span class="sxs-lookup"><span data-stu-id="d9f30-212">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="d9f30-213">在列表中选择正确的安全组。</span><span class="sxs-lookup"><span data-stu-id="d9f30-213">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="d9f30-214">在 **评级和审查仲裁者的 AAD 安全组** 字段中，输入要使用的安全组名称的前几个字母，然后选择放大镜符号查看搜索结果。</span><span class="sxs-lookup"><span data-stu-id="d9f30-214">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="d9f30-215">在列表中选择正确的安全组。</span><span class="sxs-lookup"><span data-stu-id="d9f30-215">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="d9f30-216">**启用评分和评价服务** 选项设置保留为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-216">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="d9f30-217">选择 **初始化**。</span><span class="sxs-lookup"><span data-stu-id="d9f30-217">Select **Initialize**.</span></span> <span data-ttu-id="d9f30-218">**商业管理** 视图再次显示，其中的 **电子商务** 选项卡被选中。</span><span class="sxs-lookup"><span data-stu-id="d9f30-218">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="d9f30-219">电子商务初始化已开始。</span><span class="sxs-lookup"><span data-stu-id="d9f30-219">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="d9f30-220">请等待电子商务初始化的状态成为 **初始化成功**，再继续操作。</span><span class="sxs-lookup"><span data-stu-id="d9f30-220">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="d9f30-221">在右下方的 **链接** 下，记下以下链接的 URL：</span><span class="sxs-lookup"><span data-stu-id="d9f30-221">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="d9f30-222">**电子商务站点** – 指向您的电子商务站点的根目录的链接。</span><span class="sxs-lookup"><span data-stu-id="d9f30-222">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="d9f30-223">**电子商务站点构建器** – 站点管理工具的链接。</span><span class="sxs-lookup"><span data-stu-id="d9f30-223">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d9f30-224">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d9f30-224">Next steps</span></span>

<span data-ttu-id="d9f30-225">要继续 Commerce 评估环境的预配和配置过程，请参阅[配置 Commerce 评估环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="d9f30-225">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9f30-226">其他资源</span><span class="sxs-lookup"><span data-stu-id="d9f30-226">Additional resources</span></span>

[<span data-ttu-id="d9f30-227">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="d9f30-227">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d9f30-228">配置 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="d9f30-228">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="d9f30-229">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="d9f30-229">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="d9f30-230">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="d9f30-230">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d9f30-231">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="d9f30-231">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d9f30-232">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d9f30-232">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d9f30-233">Commerce Scale Unit（云）</span><span class="sxs-lookup"><span data-stu-id="d9f30-233">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d9f30-234">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="d9f30-234">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d9f30-235">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="d9f30-235">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
