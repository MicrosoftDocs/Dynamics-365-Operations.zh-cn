---
title: 配置 Dynamics 365 Commerce 预览环境
description: 本主题说明如何预配 Microsoft Dynamics 365 Commerce 预览环境。
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426457"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="3660a-103">配置 Dynamics 365 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="3660a-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3660a-104">本主题说明如何预配 Dynamics 365 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="3660a-105">在开始之前，我们建议您快速浏览本主题以了解该过程的要求。</span><span class="sxs-lookup"><span data-stu-id="3660a-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="3660a-106">如果您尚未获得 Dynamics 365 Commerce 预览的访问权限，可以从 [Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)申请预览访问权限。</span><span class="sxs-lookup"><span data-stu-id="3660a-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="3660a-107">概览</span><span class="sxs-lookup"><span data-stu-id="3660a-107">Overview</span></span>

<span data-ttu-id="3660a-108">要成功预配 Commerce 预览环境，您必须创建一个具有特定产品名称和类型的项目。</span><span class="sxs-lookup"><span data-stu-id="3660a-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="3660a-109">此环境和 Commerce Scale Unit (CSU) 还具有某些特定参数，以后在预配电子商务时必须使用这些参数。</span><span class="sxs-lookup"><span data-stu-id="3660a-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="3660a-110">本主题中的说明介绍完成预配所需的所有步骤以及必须使用的参数。</span><span class="sxs-lookup"><span data-stu-id="3660a-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="3660a-111">成功预配 Commerce 预览环境后，还必须完成一些预配后步骤来准备它。</span><span class="sxs-lookup"><span data-stu-id="3660a-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="3660a-112">其中一些步骤可选，具体取决于要评估系统的哪些方面。</span><span class="sxs-lookup"><span data-stu-id="3660a-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="3660a-113">您可以在以后随时完成可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3660a-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="3660a-114">有关在预配后如何预配 Commerce 预览环境的信息，请参阅[预配 Commerce 预览环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="3660a-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="3660a-115">有关为 Commerce 预览环境预配可选功能的信息，请参阅[为 Commerce 预览环境预配可选功能](cpe-optional-features.md)。</span><span class="sxs-lookup"><span data-stu-id="3660a-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="3660a-116">如果对预配步骤有任何疑问或遇到了任何问题，请通过 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)告知 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3660a-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3660a-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="3660a-117">Prerequisites</span></span>

<span data-ttu-id="3660a-118">必须先满足以下先决条件，才能预配 Commerce 预览环境：</span><span class="sxs-lookup"><span data-stu-id="3660a-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="3660a-119">您拥有 Microsoft Dynamics Lifecycle Services (LCS) 门户的访问权限。</span><span class="sxs-lookup"><span data-stu-id="3660a-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="3660a-120">您是现有的 Microsoft Dynamics 365 合作伙伴或客户，并能够创建 Dynamics 365 Commerce 项目。</span><span class="sxs-lookup"><span data-stu-id="3660a-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="3660a-121">您已获准加入 Dynamics 365 Commerce 预览计划。</span><span class="sxs-lookup"><span data-stu-id="3660a-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="3660a-122">您拥有必需的权限，可以为**迁移、创建解决方案和了解**创建项目。</span><span class="sxs-lookup"><span data-stu-id="3660a-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="3660a-123">您是我们将为其预配环境的项目的**环境管理员**或**项目负责人**角色的成员。</span><span class="sxs-lookup"><span data-stu-id="3660a-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="3660a-124">您有 Microsoft Azure 订阅的管理员访问权限，或您与可以代表您完成需要管理员权限的两步的订阅管理员有联系。</span><span class="sxs-lookup"><span data-stu-id="3660a-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="3660a-125">您有可用的 Azure Active Directory (Azure AD) 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="3660a-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="3660a-126">您已创建了可以用作电子商务系统管理员组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="3660a-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="3660a-127">您已创建了可以用作评级和审查仲裁者组的 Azure AD 安全组，并且您有它的可用 ID。</span><span class="sxs-lookup"><span data-stu-id="3660a-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="3660a-128">（此安全组可以与电子商务系统管理员组相同。）</span><span class="sxs-lookup"><span data-stu-id="3660a-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="3660a-129">预配您的 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="3660a-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="3660a-130">这些过程说明如何预配 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="3660a-131">成功完成这些过程之后，Commerce 预览环境将可以进行配置。</span><span class="sxs-lookup"><span data-stu-id="3660a-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="3660a-132">此处介绍的所有活动都在 LCS 门户中进行。</span><span class="sxs-lookup"><span data-stu-id="3660a-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3660a-133">预览访问权限与您在 Commerce 预览应用程序中指定的 LCS 帐户和组织关联。</span><span class="sxs-lookup"><span data-stu-id="3660a-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="3660a-134">您必须使用相同的帐户来预配 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="3660a-135">如果需要为 Commerce 预览环境使用其他 LCS 帐户或租户，则必须将这些详细信息提供给 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3660a-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="3660a-136">有关联系信息，请参阅本主题后面的 [Commerce 预览环境支持](#commerce-preview-environment-support)一节。</span><span class="sxs-lookup"><span data-stu-id="3660a-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="3660a-137">确认预览功能可用且已在 LCS 中打开</span><span class="sxs-lookup"><span data-stu-id="3660a-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="3660a-138">要确认预览功能可用且已在 LCS 中打开，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3660a-139">使用用于请求预览访问权限的相同 LCS 帐户登录到 [LCS 门户](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="3660a-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="3660a-140">在 LCS 主页上，滚动到最右侧，然后选择**预览功能管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="3660a-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![预览管理磁贴](./media/preview1.png)

1. <span data-ttu-id="3660a-142">向下滚动到**专用预览功能**，确认以下功能可用且已打开：</span><span class="sxs-lookup"><span data-stu-id="3660a-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="3660a-143">电子商务评估</span><span class="sxs-lookup"><span data-stu-id="3660a-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="3660a-144">商务预览计划环境</span><span class="sxs-lookup"><span data-stu-id="3660a-144">Commerce Preview Program Environments</span></span>

    ![专用预览功能](./media/preview2.png)

1. <span data-ttu-id="3660a-146">如果这些功能没有出现在列表中，请与 Microsoft 联系，并提供您的工作电子邮件地址、LCS 帐户和租户详细信息。</span><span class="sxs-lookup"><span data-stu-id="3660a-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="3660a-147">有关联系信息，请参阅 [Commerce 预览环境支持](#commerce-preview-environment-support)一节。</span><span class="sxs-lookup"><span data-stu-id="3660a-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="3660a-148">创建新项目</span><span class="sxs-lookup"><span data-stu-id="3660a-148">Create a new project</span></span>

<span data-ttu-id="3660a-149">若要在 LCS 中创建新项目，请按以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3660a-150">在 LCS 主页上，选择加号 (**+**) 创建一个项目。</span><span class="sxs-lookup"><span data-stu-id="3660a-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="3660a-151">在右窗格中，请按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="3660a-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="3660a-152">如果您是合作伙伴，请选择**迁移，创建解决方案，了解**。</span><span class="sxs-lookup"><span data-stu-id="3660a-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="3660a-153">如果您是客户，请选择**潜在售前支持**。</span><span class="sxs-lookup"><span data-stu-id="3660a-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="3660a-154">输入名称、描述和行业。</span><span class="sxs-lookup"><span data-stu-id="3660a-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="3660a-155">在**产品名称**字段中，选择 **Dynamics 365 Retail**。</span><span class="sxs-lookup"><span data-stu-id="3660a-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="3660a-156">在**产品版本**字段中，选择 **Dynamics 365 Retail**。</span><span class="sxs-lookup"><span data-stu-id="3660a-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="3660a-157">在**方法**字段中，选择 **Dynamics Retail 实施方法**。</span><span class="sxs-lookup"><span data-stu-id="3660a-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="3660a-158">可选：您可以从现有项目导入角色和用户。</span><span class="sxs-lookup"><span data-stu-id="3660a-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="3660a-159">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="3660a-159">Select **Create**.</span></span> <span data-ttu-id="3660a-160">将出现项目视图。</span><span class="sxs-lookup"><span data-stu-id="3660a-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="3660a-161">添加 Azure 连接器</span><span class="sxs-lookup"><span data-stu-id="3660a-161">Add the Azure Connector</span></span>

<span data-ttu-id="3660a-162">要将 Azure 连接器添加到您的 LCS 项目，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="3660a-163">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="3660a-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="3660a-164">如果您是合作伙伴，请选择最右边的**项目设置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="3660a-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="3660a-165">如果您是客户，请在顶部菜单中选择**项目设置**。</span><span class="sxs-lookup"><span data-stu-id="3660a-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="3660a-166">选择 **Azure 连接器**。</span><span class="sxs-lookup"><span data-stu-id="3660a-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="3660a-167">选择**添加**添加 Azure 连接器。</span><span class="sxs-lookup"><span data-stu-id="3660a-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="3660a-168">输入名称。</span><span class="sxs-lookup"><span data-stu-id="3660a-168">Enter a name.</span></span>
1. <span data-ttu-id="3660a-169">输入您的 Azure 订阅 ID。</span><span class="sxs-lookup"><span data-stu-id="3660a-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="3660a-170">打开**配置为使用 Azure 资源管理器(ARM)** 选项。</span><span class="sxs-lookup"><span data-stu-id="3660a-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="3660a-171">验证 **Azure 订阅 AAD 租户域(或 ID)** 值是否正确。</span><span class="sxs-lookup"><span data-stu-id="3660a-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="3660a-172">根据需要咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="3660a-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="3660a-173">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="3660a-173">Select **Next**.</span></span>
1. <span data-ttu-id="3660a-174">按照页面上的说明为所需应用程序授予订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="3660a-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="3660a-175">根据需要咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="3660a-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="3660a-176">登录 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="3660a-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="3660a-177">确保选择了正确的目录，然后在左侧菜单上选择**订阅**。</span><span class="sxs-lookup"><span data-stu-id="3660a-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="3660a-178">在列表中找到正确的订阅并选择它。</span><span class="sxs-lookup"><span data-stu-id="3660a-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="3660a-179">根据需要使用搜索功能。</span><span class="sxs-lookup"><span data-stu-id="3660a-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="3660a-180">在菜单上，选择**访问控制(IAM)**。</span><span class="sxs-lookup"><span data-stu-id="3660a-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="3660a-181">在右侧，在**添加角色分配**下，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="3660a-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="3660a-182">将显示**添加角色分配**窗格。</span><span class="sxs-lookup"><span data-stu-id="3660a-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="3660a-183">在**角色**字段中，选择**参与者**。</span><span class="sxs-lookup"><span data-stu-id="3660a-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="3660a-184">在**将访问权限分配到**字段中，保留默认值 **Azure AD 用户、组或服务主体**。</span><span class="sxs-lookup"><span data-stu-id="3660a-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="3660a-185">在**选择**下，输入 **b96b7e94-b82e-4e71-99a0-cf7fb188acea**。</span><span class="sxs-lookup"><span data-stu-id="3660a-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="3660a-186">在列表中选择**动态部署服务 \[wsfed-enabled\]**。</span><span class="sxs-lookup"><span data-stu-id="3660a-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="3660a-187">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="3660a-187">Select **Save**.</span></span>

1. <span data-ttu-id="3660a-188">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="3660a-188">Select **Next**.</span></span>
1. <span data-ttu-id="3660a-189">按照页面上的说明为所需应用程序授予订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="3660a-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="3660a-190">根据需要咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="3660a-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="3660a-191">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="3660a-191">Select **Next**.</span></span>
1. <span data-ttu-id="3660a-192">在 **Azure 区域**字段中，选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="3660a-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="3660a-193">选择**连接**。</span><span class="sxs-lookup"><span data-stu-id="3660a-193">Select **Connect**.</span></span> <span data-ttu-id="3660a-194">应该会在列表中显示您的 Azure 连接器。</span><span class="sxs-lookup"><span data-stu-id="3660a-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="3660a-195">导入 Commerce 预览演示库扩展</span><span class="sxs-lookup"><span data-stu-id="3660a-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="3660a-196">要将 Commerce 预览演示库扩展导入到您的项目中，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="3660a-197">通过选择顶部的项目名称打开项目的主页。</span><span class="sxs-lookup"><span data-stu-id="3660a-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="3660a-198">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="3660a-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="3660a-199">如果您是合作伙伴，请选择最右边的**资产库**磁贴。</span><span class="sxs-lookup"><span data-stu-id="3660a-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="3660a-200">如果您是客户，请在顶部菜单中选择**资产库**。</span><span class="sxs-lookup"><span data-stu-id="3660a-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="3660a-201">在左侧列表中，选择**软件可部署包**。</span><span class="sxs-lookup"><span data-stu-id="3660a-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="3660a-202">选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="3660a-202">Select **Import**.</span></span>
1. <span data-ttu-id="3660a-203">在**共享资产库**下，在资产列表中选择 **Commerce 预览演示库扩展**。</span><span class="sxs-lookup"><span data-stu-id="3660a-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="3660a-204">选择**选取**。</span><span class="sxs-lookup"><span data-stu-id="3660a-204">Select **Pick**.</span></span> <span data-ttu-id="3660a-205">您已回到资产库，应该可以在列表中看到此扩展。</span><span class="sxs-lookup"><span data-stu-id="3660a-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="3660a-206">下图显示了必须在 LCS **资产库**页上执行的操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![导入 Commerce 预览演示库扩展](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="3660a-208">部署环境</span><span class="sxs-lookup"><span data-stu-id="3660a-208">Deploy the environment</span></span>

<span data-ttu-id="3660a-209">要部署环境，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3660a-210">您可能不必完成步骤 6、7 和/或 8，因为将跳过具有单个选项的页面。</span><span class="sxs-lookup"><span data-stu-id="3660a-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="3660a-211">在**环境参数**视图中时，请确认文本 **Dynamics 365 Commerce - 演示(具有平台更新 *xx* 的 10.0.* x*)**直接出现在**环境名称\*\*字段上方。</span><span class="sxs-lookup"><span data-stu-id="3660a-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="3660a-212">有关详细信息，请参阅步骤 8 之后出现的图示。</span><span class="sxs-lookup"><span data-stu-id="3660a-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="3660a-213">在顶级菜单上，选择**云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="3660a-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3660a-214">选择**添加**添加环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="3660a-215">在**应用程序版本**字段中，选择最新版本。</span><span class="sxs-lookup"><span data-stu-id="3660a-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="3660a-216">如果您明确需要选择除最新版本以外的其他应用程序版本，请不要选择 **10.0.8** 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="3660a-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="3660a-217">在**平台版本**字段中，使用为所选应用程序版本自动选择的平台版本。</span><span class="sxs-lookup"><span data-stu-id="3660a-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![选择应用程序和平台版本](./media/project1.png)

1. <span data-ttu-id="3660a-219">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="3660a-219">Select **Next**.</span></span>
1. <span data-ttu-id="3660a-220">选择**演示**作为环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="3660a-220">Select **Demo** as the environment topology.</span></span>

    ![选择环境拓扑 1](./media/project2.png)

1. <span data-ttu-id="3660a-222">选择 **Dynamics 365 Commerce - 演示**作为环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="3660a-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="3660a-223">如果前面仅配置了一个 Azure 连接器，将把该连接器用于此环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="3660a-224">如果配置了多个 Azure 连接器，则可以选择要使用的连接器：**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="3660a-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="3660a-225">（为获得最佳的端到端性能，我们建议您选择**美国西部 2**。）</span><span class="sxs-lookup"><span data-stu-id="3660a-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![选择环境拓扑 2](./media/project3.png)

1. <span data-ttu-id="3660a-227">在**部署环境**页面上，输入环境名称。</span><span class="sxs-lookup"><span data-stu-id="3660a-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="3660a-228">高级设置保持原样。</span><span class="sxs-lookup"><span data-stu-id="3660a-228">Leave the advanced settings as they are.</span></span>

    ![部署环境页面](./media/project4.png)

1. <span data-ttu-id="3660a-230">根据需要调整 VM 大小。</span><span class="sxs-lookup"><span data-stu-id="3660a-230">Adjust the VM size as required.</span></span> <span data-ttu-id="3660a-231">（我们建议使用 VM 库存单位 \[SKU\] **D13 v2**。）</span><span class="sxs-lookup"><span data-stu-id="3660a-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="3660a-232">查看定价和许可条款，然后选中指示您同意这些条款的复选框。</span><span class="sxs-lookup"><span data-stu-id="3660a-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="3660a-233">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="3660a-233">Select **Next**.</span></span>
1. <span data-ttu-id="3660a-234">在部署确认页面，验证详细信息是否正确，然后选择**部署**。</span><span class="sxs-lookup"><span data-stu-id="3660a-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="3660a-235">您已返回到**云托管的环境**视图，列表中应该会显示您的环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="3660a-236">您请求的环境将显示为已入队列，然后是正在部署。</span><span class="sxs-lookup"><span data-stu-id="3660a-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="3660a-237">环境工作流将需要一些时间完成。</span><span class="sxs-lookup"><span data-stu-id="3660a-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="3660a-238">因此，请在大约六到九小时后再次检查。</span><span class="sxs-lookup"><span data-stu-id="3660a-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="3660a-239">继续操作之前，确保环境的状态为**已部署**。</span><span class="sxs-lookup"><span data-stu-id="3660a-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="3660a-240">初始化 Commerce Scale Unit（云）</span><span class="sxs-lookup"><span data-stu-id="3660a-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="3660a-241">要初始化您的 CSU，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3660a-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="3660a-242">在**云托管的环境**视图中，在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="3660a-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="3660a-243">在右侧的环境视图中，选择**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="3660a-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="3660a-244">将显示环境详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="3660a-244">The environment details view appears.</span></span>
1. <span data-ttu-id="3660a-245">在**环境功能**下，选择**管理**。</span><span class="sxs-lookup"><span data-stu-id="3660a-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="3660a-246">在**商业**选项卡上，选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="3660a-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="3660a-247">将显示 CSU 初始化参数视图。</span><span class="sxs-lookup"><span data-stu-id="3660a-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="3660a-248">在**区域**字段中，选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="3660a-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="3660a-249">在**版本**字段中，在列表中选择**指定版本**，然后在出现的字段中指定 **9.18.20014.4**。</span><span class="sxs-lookup"><span data-stu-id="3660a-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="3660a-250">请确保指定此处指示的确切版本。</span><span class="sxs-lookup"><span data-stu-id="3660a-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="3660a-251">否则，您以后不得不将 RCSU 更新到正确的版本。</span><span class="sxs-lookup"><span data-stu-id="3660a-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="3660a-252">打开**应用扩展**选项。</span><span class="sxs-lookup"><span data-stu-id="3660a-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="3660a-253">在扩展列表中，选择 **Commerce 预览演示库扩展**。</span><span class="sxs-lookup"><span data-stu-id="3660a-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="3660a-254">选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="3660a-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="3660a-255">在部署确认页面，验证详细信息是否正确，然后选择**是**。</span><span class="sxs-lookup"><span data-stu-id="3660a-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="3660a-256">**商业管理**视图再次显示，其中的**商业**选项卡被选中。</span><span class="sxs-lookup"><span data-stu-id="3660a-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="3660a-257">您的 CSU 现在已进入队列等待配置。</span><span class="sxs-lookup"><span data-stu-id="3660a-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="3660a-258">继续操作之前，确保 CSU 的状态为**成功**。</span><span class="sxs-lookup"><span data-stu-id="3660a-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="3660a-259">初始化大约需要两到五个小时。</span><span class="sxs-lookup"><span data-stu-id="3660a-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="3660a-260">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="3660a-260">Initialize e-Commerce</span></span>

<span data-ttu-id="3660a-261">要初始化电子商务，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3660a-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3660a-262">在**电子商务**选项卡上，查看预览同意内容，然后选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="3660a-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="3660a-263">在**电子商务租户名称**字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="3660a-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="3660a-264">但是，请注意，某些指向您的电子商务实例的 URL 中将显示此名称。</span><span class="sxs-lookup"><span data-stu-id="3660a-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="3660a-265">在 **Commerce Scale Unit 名称**字段中，在列表中选择您的 CSU。</span><span class="sxs-lookup"><span data-stu-id="3660a-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="3660a-266">（此列表应该只有一个选项。）</span><span class="sxs-lookup"><span data-stu-id="3660a-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="3660a-267">**电子商务地理位置**字段是自动设置的，此值无法更改。</span><span class="sxs-lookup"><span data-stu-id="3660a-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="3660a-268">选择**下一步**继续。</span><span class="sxs-lookup"><span data-stu-id="3660a-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="3660a-269">在**支持的主机名**字段中，输入任意有效域，例如 `www.fabrikam.com`。</span><span class="sxs-lookup"><span data-stu-id="3660a-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="3660a-270">在**系统管理员的 AAD 安全组**字段中，输入要使用的安全组的名称的前几个字母。</span><span class="sxs-lookup"><span data-stu-id="3660a-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="3660a-271">选择放大镜图标以显示搜索结果。</span><span class="sxs-lookup"><span data-stu-id="3660a-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="3660a-272">从列表中选择正确的安全组。</span><span class="sxs-lookup"><span data-stu-id="3660a-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="3660a-273">在**评级和审查仲裁者的 AAD 安全组**字段中，输入要使用的安全组的名称的前几个字母。</span><span class="sxs-lookup"><span data-stu-id="3660a-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="3660a-274">选择放大镜图标以显示搜索结果。</span><span class="sxs-lookup"><span data-stu-id="3660a-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="3660a-275">从列表中选择正确的安全组。</span><span class="sxs-lookup"><span data-stu-id="3660a-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="3660a-276">保留**启用评级和审查服务**选项为打开。</span><span class="sxs-lookup"><span data-stu-id="3660a-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="3660a-277">选择**初始化**。</span><span class="sxs-lookup"><span data-stu-id="3660a-277">Select **Initialize**.</span></span> <span data-ttu-id="3660a-278">**商业管理**视图再次显示，其中的**电子商务**选项卡被选中。</span><span class="sxs-lookup"><span data-stu-id="3660a-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="3660a-279">电子商务初始化已开始。</span><span class="sxs-lookup"><span data-stu-id="3660a-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="3660a-280">请等待电子商务初始化的状态成为**初始化成功**，再继续操作。</span><span class="sxs-lookup"><span data-stu-id="3660a-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="3660a-281">在右下方的**链接**下，记下以下链接的 URL：</span><span class="sxs-lookup"><span data-stu-id="3660a-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="3660a-282">**电子商务站点** – 指向您的电子商务站点的根目录的链接。</span><span class="sxs-lookup"><span data-stu-id="3660a-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="3660a-283">**电子商务站点管理工具** – 站点管理工具的链接。</span><span class="sxs-lookup"><span data-stu-id="3660a-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="3660a-284">Commerce 预览环境支持</span><span class="sxs-lookup"><span data-stu-id="3660a-284">Commerce preview environment support</span></span>

<span data-ttu-id="3660a-285">如果您在完成预配步骤时遇到问题，请访问 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)获取帮助。</span><span class="sxs-lookup"><span data-stu-id="3660a-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3660a-286">后续步骤</span><span class="sxs-lookup"><span data-stu-id="3660a-286">Next steps</span></span>

<span data-ttu-id="3660a-287">要继续 Commerce 预览环境的预配和配置过程，请参阅[配置 Commerce 预览环境](cpe-post-provisioning.md)。</span><span class="sxs-lookup"><span data-stu-id="3660a-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3660a-288">其他资源</span><span class="sxs-lookup"><span data-stu-id="3660a-288">Additional resources</span></span>

[<span data-ttu-id="3660a-289">Dynamics 365 Commerce 预览环境概览</span><span class="sxs-lookup"><span data-stu-id="3660a-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3660a-290">配置 Dynamics 365 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="3660a-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3660a-291">为 Dynamics 365 Commerce 预览环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="3660a-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3660a-292">Dynamics 365 Commerce 预览环境常见问题</span><span class="sxs-lookup"><span data-stu-id="3660a-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="3660a-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="3660a-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="3660a-294">Commerce Scale Unit（云）</span><span class="sxs-lookup"><span data-stu-id="3660a-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="3660a-295">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="3660a-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="3660a-296">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="3660a-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

