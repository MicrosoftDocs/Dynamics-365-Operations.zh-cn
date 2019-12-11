---
title: 配置电子商务评估环境
description: 此指南提供有关设置和配置 Microsoft Dynamics 365 Commerce 预览环境的分步说明。
author: v-chgri
manager: annbe
ms.date: 10/15/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771672"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a><span data-ttu-id="6633c-103">配置电子商务评估环境</span><span class="sxs-lookup"><span data-stu-id="6633c-103">Configure an e-Commerce evaluation environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6633c-104">此指南提供有关设置和配置 Microsoft Dynamics 365 Commerce 预览环境的分步说明。</span><span class="sxs-lookup"><span data-stu-id="6633c-104">This guide provides step-by-step instructions for provisioning and configuring your Microsoft Dynamics 365 Commerce Preview environment.</span></span> <span data-ttu-id="6633c-105">建议您首先至少快速浏览本文档以大致了解流程涉及的内容和指南包含的内容。</span><span class="sxs-lookup"><span data-stu-id="6633c-105">Before you begin, we recommend that you at least skim through the documentation to get an idea of what the process entails and what the guide contains.</span></span>

<span data-ttu-id="6633c-106">*注意：如果您尚未获得 Microsoft Dynamics 365 Commerce 预览的访问权限，可以从 [Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)申请预览访问权限。*</span><span class="sxs-lookup"><span data-stu-id="6633c-106">*Note: If you have not been granted access to the Microsoft Dynamics 365 Commerce Preview yet, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).*</span></span>

## <a name="summary"></a><span data-ttu-id="6633c-107">摘要</span><span class="sxs-lookup"><span data-stu-id="6633c-107">Summary</span></span>
<span data-ttu-id="6633c-108">若要成功配置环境，需要使用特定项目名称和类型创建项目。</span><span class="sxs-lookup"><span data-stu-id="6633c-108">To provision the environment successfully, the project needs to be created with a specific product name and type.</span></span> <span data-ttu-id="6633c-109">环境和 Retail Cloud Scale Unit 页采用一些您需要用来以后启动电子商务配置的特定参数。</span><span class="sxs-lookup"><span data-stu-id="6633c-109">The environment and Retail Cloud Scale Unit also have some specific parameters you need to use to start the e-Commerce provisioning later.</span></span> <span data-ttu-id="6633c-110">本指南中的说明包含您必须执行的所有步骤和需要使用的参数。</span><span class="sxs-lookup"><span data-stu-id="6633c-110">The instructions in this guide contain all the required steps you need to take and parameters you need to use.</span></span>

<span data-ttu-id="6633c-111">成功配置之后，需要执行一些配置后步骤来准备预览环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-111">After successful provisioning, there are a few post-provisioning steps you need to take to prepare your Preview environment.</span></span> <span data-ttu-id="6633c-112">其中一些步骤可选，具体取决于要评估系统的哪些方面。</span><span class="sxs-lookup"><span data-stu-id="6633c-112">Some steps are optional, depending on which aspects of the system you wish to evaluate.</span></span> <span data-ttu-id="6633c-113">如果以后更改主意，以后始终可以运行可选步骤。</span><span class="sxs-lookup"><span data-stu-id="6633c-113">Should you later change your mind, you can always run the optional steps later.</span></span>

<span data-ttu-id="6633c-114">如果对配置步骤有任何疑问或遇到了任何问题，请通过 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)告知我们。</span><span class="sxs-lookup"><span data-stu-id="6633c-114">If you have any questions about the provisioning steps or you encounter any issues, please let us know on [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="6633c-115">先决条件</span><span class="sxs-lookup"><span data-stu-id="6633c-115">Prerequisites</span></span>
<span data-ttu-id="6633c-116">下面是配置 Dynamics 365 预览环境的先决条件：</span><span class="sxs-lookup"><span data-stu-id="6633c-116">The following are prerequisites for provisioning your Dynamics 365 Preview environment:</span></span>
* <span data-ttu-id="6633c-117">您拥有 **Lifecycle Services 门户 (LCS)** 的访问权限</span><span class="sxs-lookup"><span data-stu-id="6633c-117">You have access to the **Lifecycle Services portal (LCS)**</span></span>
* <span data-ttu-id="6633c-118">您已**获准加入 Dynamics 365 Commerce 预览计划**</span><span class="sxs-lookup"><span data-stu-id="6633c-118">You have been **accepted into the Dynamics 365 Commerce Preview program**</span></span>
* <span data-ttu-id="6633c-119">您拥有足够权限，可以为**潜在售前支持**或**迁移，创建解决方案，了解**创建项目</span><span class="sxs-lookup"><span data-stu-id="6633c-119">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**</span></span>
* <span data-ttu-id="6633c-120">您是我们将为其配置环境的项目的**环境管理员**或**项目负责人**角色的成员</span><span class="sxs-lookup"><span data-stu-id="6633c-120">You are a member of the **Environment manager** or **Project Owner** role in the project where you will be provisioning the environment</span></span>
* <span data-ttu-id="6633c-121">您有 Azure 订阅的管理员访问权限，或您与可以代表您执行需要管理员权限的两步的订阅管理员联系</span><span class="sxs-lookup"><span data-stu-id="6633c-121">You have admin access to your Azure subscription, or contact with a subscription admin who can perform the two steps that require admin permissions on your behalf</span></span>
* <span data-ttu-id="6633c-122">您有 **AAD 租户 ID**</span><span class="sxs-lookup"><span data-stu-id="6633c-122">You have your **AAD Tenant Id** available</span></span>
* <span data-ttu-id="6633c-123">您已创建了要用作**电子商务系统管理员组**的 **AAD 安全组**，并且您有其 ID</span><span class="sxs-lookup"><span data-stu-id="6633c-123">You have created a **AAD security group** to be used as **e-Commerce system admins group** and you have its ID available</span></span>
* <span data-ttu-id="6633c-124">您已创建了要用作**评分和评价审查者组**的 **AAD 安全组**，并且您有其 ID（与上面的系统管理员组是同一个 SG）</span><span class="sxs-lookup"><span data-stu-id="6633c-124">You have created a **AAD security group** to be used as **Ratings and Reviews moderator group** and you have its ID available (can be the same SG as the system admin group above)</span></span>
## <a name="provisioning-preview-environment"></a><span data-ttu-id="6633c-125">配置预览环境</span><span class="sxs-lookup"><span data-stu-id="6633c-125">Provisioning preview environment</span></span>
<span data-ttu-id="6633c-126">这些说明介绍如何配置 Microsoft Dynamics 365 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-126">These instructions cover the provisioning of a Microsoft Dynamics 365 Commerce Preview environment.</span></span> <span data-ttu-id="6633c-127">成功完成这些步骤后，即准备好了要配置的预览环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-127">After successfully completing these steps, you will have a Preview environment that is ready to be configured.</span></span> <span data-ttu-id="6633c-128">此处介绍的所有活动都在 LCS 门户中进行。</span><span class="sxs-lookup"><span data-stu-id="6633c-128">All the activities described here take place in the LCS portal.</span></span>

<span data-ttu-id="6633c-129">*请注意，预览访问权限与您在预览应用程序中指定的 LCS 帐户和组织绑定。您需要使用同一个帐户来进行配置。如果必须对预览环境使用其他 LCS 帐户或租户，您需要向我们提供这些详细信息。有关联系信息，请参阅下面的“其他资源”。*</span><span class="sxs-lookup"><span data-stu-id="6633c-129">*Please note that the preview access is tied to the LCS account and organization you specified in your preview application. You need to use that same account for provisioning. If you have to use different LCS account or tenant for the Preview environment, you need to provide us with those details. For contact information, please see "Additional resources" below.*</span></span>
### <a name="before-starting"></a><span data-ttu-id="6633c-130">准备工作</span><span class="sxs-lookup"><span data-stu-id="6633c-130">Before starting</span></span>
##### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="6633c-131">授予电子商务应用程序的访问权限</span><span class="sxs-lookup"><span data-stu-id="6633c-131">Grant access to e-Commerce applications</span></span>

<span data-ttu-id="6633c-132">*注意：**只有 AAD 租户管理员才能登录**。如果无法完成此步骤，其余配置步骤将失败。*</span><span class="sxs-lookup"><span data-stu-id="6633c-132">*Note: **The person logging in needs to be AAD tenant administrator**. Without successfully completing this step, the rest of the provisioning steps will fail.*</span></span>

1. <span data-ttu-id="6633c-133">需要 **AAD 租户 ID** 才能完成此步骤。您需要为电子商务应用程序授予您的 Azure 订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6633c-133">For this step, you need your **AAD Tenant Id**. You need to authorize e-Commerce applications to access your Azure subscription.</span></span> <span data-ttu-id="6633c-134">最简单的方法是创建如下 URL：</span><span class="sxs-lookup"><span data-stu-id="6633c-134">The easiest way to accomplish this is to assemble a URL like this:</span></span>

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. <span data-ttu-id="6633c-135">**切勿直接单击此 URL**，而是将其复制粘贴到浏览器或文本编辑器中，然后将 **\{AAD_TENANT_ID\}** 替换为您的 **AAD 租户 ID**，之后再导航到此 URL。</span><span class="sxs-lookup"><span data-stu-id="6633c-135">**Do not click the URL directly**, instead copy and paste it into your browser or text editor and replace **\{AAD_TENANT_ID\}** with your **AAD Tenant Id**, before navigating to the URL.</span></span>
3. <span data-ttu-id="6633c-136">将显示 Microsoft AAD 登录对话框，您需要在这里确认要为“Dynamics 365 Commerce (预览)”授予您的订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6633c-136">You will be presented with the Microsoft AAD login dialog where you will confirm that you wish to grant "Dynamics 365 Commerce (Preview)" access to your subscription.</span></span>
4. <span data-ttu-id="6633c-137">将把您带到一个页面，用于确定操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="6633c-137">You will be sent to a page which confirms whether the operation was successful.</span></span>

##### <a name="log-in-to-the-lcs"></a><span data-ttu-id="6633c-138">登录到 LCS</span><span class="sxs-lookup"><span data-stu-id="6633c-138">Log in to the LCS</span></span>
1. <span data-ttu-id="6633c-139">登录到 LCS 门户：https://lcs.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="6633c-139">Log in to the LCS portal: https://lcs.dynamics.com</span></span>
1. <span data-ttu-id="6633c-140">确保使用用于申请预览访问权限的同一个 LCS 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="6633c-140">Make sure that you are logged in with the same LCS account you used to request access to the Preview.</span></span>
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a><span data-ttu-id="6633c-141">确认预览功能可用且已启用</span><span class="sxs-lookup"><span data-stu-id="6633c-141">Confirm that preview features are available and enabled</span></span>
1. <span data-ttu-id="6633c-142">在 LCS 标题页中，滚动到最右侧，然后单击**预览功能管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="6633c-142">On the LCS front page, scroll all the way to the right and click the **Preview feature management** tile.</span></span>
1. <span data-ttu-id="6633c-143">向下滚动到“专用预览功能”，并确保以下功能可用且已启用：</span><span class="sxs-lookup"><span data-stu-id="6633c-143">Scroll down to the "PRIVATE PREVIEW FEATURES" and make sure that the following features are available and enabled:</span></span>
    1. <span data-ttu-id="6633c-144">**电子商务评估**</span><span class="sxs-lookup"><span data-stu-id="6633c-144">**e-Commerce Evaluation**</span></span>
    1. <span data-ttu-id="6633c-145">**商务预览计划环境**</span><span class="sxs-lookup"><span data-stu-id="6633c-145">**Commerce Preview Program Environments**</span></span>
1. <span data-ttu-id="6633c-146">如果在列表中看不到这些功能，请联系我们，并提供您的工作电子邮件、LCS 帐户和租户详细信息。</span><span class="sxs-lookup"><span data-stu-id="6633c-146">If you are unable to see these features in the list, please reach out to us with your work email, LCS account, and tenant details.</span></span> <span data-ttu-id="6633c-147">有关如何联系我们的信息，请参阅下面的**其他资源**。</span><span class="sxs-lookup"><span data-stu-id="6633c-147">Please see **Additional resources** below for information on how to contact us.</span></span>

![预览管理磁贴](./media/preview1.png)

![预览功能](./media/preview2.png)
### <a name="create-project"></a><span data-ttu-id="6633c-150">创建项目</span><span class="sxs-lookup"><span data-stu-id="6633c-150">Create project</span></span>
##### <a name="creating-new-project"></a><span data-ttu-id="6633c-151">创建新项目</span><span class="sxs-lookup"><span data-stu-id="6633c-151">Creating new project</span></span>
1. <span data-ttu-id="6633c-152">单击 **+** 创建新项目。</span><span class="sxs-lookup"><span data-stu-id="6633c-152">Click **+** to create a new project.</span></span>
1. <span data-ttu-id="6633c-153">如果您是合作伙伴，请选择**迁移，创建解决方案，了解**。</span><span class="sxs-lookup"><span data-stu-id="6633c-153">If you are a partner, choose **Migrate, create solutions, and learn**.</span></span>
1. <span data-ttu-id="6633c-154">如果您是客户，请选择**潜在售前支持**。</span><span class="sxs-lookup"><span data-stu-id="6633c-154">If you are a customer, choose **Prospective presales**.</span></span>
1. <span data-ttu-id="6633c-155">输入您认为适合的名称、描述和行业。</span><span class="sxs-lookup"><span data-stu-id="6633c-155">Enter a name, description and industry as you see fit.</span></span>
1. <span data-ttu-id="6633c-156">**产品名称**选择 **Dynamics 365 Retail**。</span><span class="sxs-lookup"><span data-stu-id="6633c-156">For **Product name**, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="6633c-157">**产品版本**选择 **Dynamics 365 Retail**。</span><span class="sxs-lookup"><span data-stu-id="6633c-157">For **Product version**, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="6633c-158">**方法**选择 **Dynamics Retail 实施方法**。</span><span class="sxs-lookup"><span data-stu-id="6633c-158">For **Methodology**, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="6633c-159">如果需要，可以从现有项目导入角色和用户。</span><span class="sxs-lookup"><span data-stu-id="6633c-159">You may import roles and users from an existing project if that is desired.</span></span>
1. <span data-ttu-id="6633c-160">单击**创建**。</span><span class="sxs-lookup"><span data-stu-id="6633c-160">Click **Create**.</span></span>
1. <span data-ttu-id="6633c-161">将把您带到项目视图。</span><span class="sxs-lookup"><span data-stu-id="6633c-161">You are sent to the project view.</span></span>
##### <a name="add-azure-connector"></a><span data-ttu-id="6633c-162">添加 Azure 连接器</span><span class="sxs-lookup"><span data-stu-id="6633c-162">Add Azure Connector</span></span>
1. <span data-ttu-id="6633c-163">如果您是合作伙伴，请单击最右侧工具磁贴中的**项目设置**。</span><span class="sxs-lookup"><span data-stu-id="6633c-163">If you are a partner, click **Project settings** from the tools tiles to the far right.</span></span>
1. <span data-ttu-id="6633c-164">如果您是客户，请从顶部菜单选择**项目设置**。</span><span class="sxs-lookup"><span data-stu-id="6633c-164">If you are a customer, choose **Project settings** from the top menu.</span></span>
1. <span data-ttu-id="6633c-165">选择 **Azure 连接器**。</span><span class="sxs-lookup"><span data-stu-id="6633c-165">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="6633c-166">单击 **+ 添加**添加 Azure 连接器。</span><span class="sxs-lookup"><span data-stu-id="6633c-166">Click **+ Add** to add Azure Connector.</span></span>
1. <span data-ttu-id="6633c-167">输入名称。</span><span class="sxs-lookup"><span data-stu-id="6633c-167">Enter a name.</span></span>
1. <span data-ttu-id="6633c-168">输入您的 **Azure 订阅 ID**。</span><span class="sxs-lookup"><span data-stu-id="6633c-168">Enter your **Azure Subscription ID**.</span></span>
1. <span data-ttu-id="6633c-169">启用**配置为使用 Azure 资源管理器(ARM)**。</span><span class="sxs-lookup"><span data-stu-id="6633c-169">Enable **Configure to use Azure Resource Manager (ARM)**.</span></span>
1. <span data-ttu-id="6633c-170">验证 **Azure 订阅 AAD 租户域(或 ID)** 是否正确。</span><span class="sxs-lookup"><span data-stu-id="6633c-170">Verify that **Azure subscription AAD Tenant Domain (or ID)** is correct.</span></span> <span data-ttu-id="6633c-171">如有必要，咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="6633c-171">Consult your Azure subscription admin, if necessary.</span></span>
1. <span data-ttu-id="6633c-172">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-172">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-173">按照屏幕中的说明为所需应用程序授予订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6633c-173">Follow the instructions on the screen to grant the required application(s) access to your subscription.</span></span> <span data-ttu-id="6633c-174">如有必要，咨询 Azure 订阅管理员：</span><span class="sxs-lookup"><span data-stu-id="6633c-174">Consult your Azure subscription admin, if necessary:</span></span>
    1. <span data-ttu-id="6633c-175">登录到 Azure 门户：https://portal.azure.com/</span><span class="sxs-lookup"><span data-stu-id="6633c-175">Log in to the Azure portal: https://portal.azure.com/</span></span>
    1. <span data-ttu-id="6633c-176">确保已选择了正确的目录。</span><span class="sxs-lookup"><span data-stu-id="6633c-176">Make sure that you have the correct directory selected.</span></span>
    1. <span data-ttu-id="6633c-177">单击左侧菜单中的**订阅**。</span><span class="sxs-lookup"><span data-stu-id="6633c-177">Click **Subscriptions** from the menu on the left.</span></span>
    1. <span data-ttu-id="6633c-178">在列表中找到正确的订阅并选择。</span><span class="sxs-lookup"><span data-stu-id="6633c-178">Locate the correct subscription from the list and select it.</span></span> <span data-ttu-id="6633c-179">如果需要，使用搜索。</span><span class="sxs-lookup"><span data-stu-id="6633c-179">Use search if required.</span></span>
    1. <span data-ttu-id="6633c-180">在菜单中选择**访问控制 (IAM)**。</span><span class="sxs-lookup"><span data-stu-id="6633c-180">Choose **Access control (IAM)** from the menu.</span></span>
    1. <span data-ttu-id="6633c-181">单击右侧**添加角色分配**下的**添加**。</span><span class="sxs-lookup"><span data-stu-id="6633c-181">Click **Add** under **Add a role assignment** on the right side.</span></span> <span data-ttu-id="6633c-182">将打开**添加角色分配**窗格。</span><span class="sxs-lookup"><span data-stu-id="6633c-182">The **Add role assignment** pane opens.</span></span>
    1. <span data-ttu-id="6633c-183">**角色**选择**参与者**。</span><span class="sxs-lookup"><span data-stu-id="6633c-183">For **Role**, select **Contributor**.</span></span>
    1. <span data-ttu-id="6633c-184">对于**将访问权限分配到**，保持为 **Azure AD 用户、组或服务主体**。</span><span class="sxs-lookup"><span data-stu-id="6633c-184">For **Assign access to**, leave as **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="6633c-185">在**选择**下，输入 **b96b7e94-b82e-4e71-99a0-cf7fb188acea**。</span><span class="sxs-lookup"><span data-stu-id="6633c-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="6633c-186">从列表选择**动态部署服务 [已启用 wsfed]**。</span><span class="sxs-lookup"><span data-stu-id="6633c-186">Select **Dynamics Deployment Services [wsfed-enabled]** from the list.</span></span>
    1. <span data-ttu-id="6633c-187">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="6633c-187">Click **Save**.</span></span>
1. <span data-ttu-id="6633c-188">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-188">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-189">按照屏幕中的说明为所需应用程序授予订阅的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6633c-189">Follow the instructions on the screen to grant required application(s) access to your subscription.</span></span> <span data-ttu-id="6633c-190">如有必要，咨询 Azure 订阅管理员。</span><span class="sxs-lookup"><span data-stu-id="6633c-190">Consult your Azure subscription admin, if necessary.</span></span>
1. <span data-ttu-id="6633c-191">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-191">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-192">**Azure 区域**选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="6633c-192">For **Azure region**, choose either **East US**, **East US 2**, **West US** or **West US 2**.</span></span>
1. <span data-ttu-id="6633c-193">单击**连接**。</span><span class="sxs-lookup"><span data-stu-id="6633c-193">Click **Connect**.</span></span>
1. <span data-ttu-id="6633c-194">应该会在列表中显示您的 Azure 连接器。</span><span class="sxs-lookup"><span data-stu-id="6633c-194">Your Azure Connector should appear in the list.</span></span>
### <a name="import-extension"></a><span data-ttu-id="6633c-195">导入扩展</span><span class="sxs-lookup"><span data-stu-id="6633c-195">Import Extension</span></span>
1. <span data-ttu-id="6633c-196">通过单击顶部的项目名称回到项目标题页。</span><span class="sxs-lookup"><span data-stu-id="6633c-196">Navigate back to your project front page by clicking the project name on the top.</span></span>
1. <span data-ttu-id="6633c-197">如果您是合作伙伴，请单击最右侧工具磁贴中的**资产库**。</span><span class="sxs-lookup"><span data-stu-id="6633c-197">If you are a partner, click **Asset library** from the tools tiles to the far right.</span></span>
1. <span data-ttu-id="6633c-198">如果您是客户，请从顶部菜单选择**资产库**。</span><span class="sxs-lookup"><span data-stu-id="6633c-198">If you are a customer, choose **Asset library** from the top menu.</span></span>
1. <span data-ttu-id="6633c-199">从左侧列表选择**软件可部署包**。</span><span class="sxs-lookup"><span data-stu-id="6633c-199">Select **Software deployable package** from the list on the left.</span></span>
1. <span data-ttu-id="6633c-200">单击操作窗格中的**导入**。</span><span class="sxs-lookup"><span data-stu-id="6633c-200">Click **IMPORT** from the action pane.</span></span>
1. <span data-ttu-id="6633c-201">在**共享资产库**下的资产列表中选择**商务预览演示库扩展**。</span><span class="sxs-lookup"><span data-stu-id="6633c-201">Select **Commerce Preview Demo Base Extension** from the list of assets under **SHARED ASSET LIBRARY**.</span></span>
1. <span data-ttu-id="6633c-202">单击**选择**。</span><span class="sxs-lookup"><span data-stu-id="6633c-202">Click **Pick**.</span></span>
1. <span data-ttu-id="6633c-203">将回到资产库，应该可以在列表中看到此扩展。</span><span class="sxs-lookup"><span data-stu-id="6633c-203">You will be returned to the Asset library and you should see the extension in the list.</span></span>

![项目创建 - 版本](./media/import.png)
### <a name="deploy-environment"></a><span data-ttu-id="6633c-205">部署环境</span><span class="sxs-lookup"><span data-stu-id="6633c-205">Deploy environment</span></span>

<span data-ttu-id="6633c-206">*注意：步骤 6、7 和/或 8 可能不显示，因为跳过了有一个选项的屏幕。在**环境参数**视图中，确定**环境名称**正上方有文本“Dynamics 365 Commerce(预览) - 演示(带平台更新 30 的 10.0.6)”。请参见下面的屏幕截图。*</span><span class="sxs-lookup"><span data-stu-id="6633c-206">*Note: It is possible that steps 6, 7, and/or 8 will not be shown, as the screens with single option are skipped. When you are in the **Environment parameters** view, please confirm that you have the text "Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)" directly above the **Environment name** field. See the screenshot below.*</span></span>

1. <span data-ttu-id="6633c-207">从顶级菜单，请选择 **管理云的环境**。</span><span class="sxs-lookup"><span data-stu-id="6633c-207">From the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6633c-208">单击 **+ 添加**添加环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-208">Click **+ Add** to add an environment.</span></span>
1. <span data-ttu-id="6633c-209">**应用程序版本**选择 **10.0.6**。</span><span class="sxs-lookup"><span data-stu-id="6633c-209">For **Application version**, select **10.0.6**.</span></span>
1. <span data-ttu-id="6633c-210">**平台版本**选择**平台更新 30**。</span><span class="sxs-lookup"><span data-stu-id="6633c-210">For **Platform version**, select **Platform Update 30**.</span></span>
1. <span data-ttu-id="6633c-211">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-211">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-212">环境拓扑选择 **DEMO**。</span><span class="sxs-lookup"><span data-stu-id="6633c-212">For environment topology, choose **DEMO**.</span></span>
1. <span data-ttu-id="6633c-213">环境拓扑选择 **Dynamics 365 Commerce(预览) - 演示**。</span><span class="sxs-lookup"><span data-stu-id="6633c-213">For environment topology, choose **Dynamics 365 Commerce (Preview) - Demo**.</span></span>
1. <span data-ttu-id="6633c-214">如果前面仅配置了一个 Azure 连接器，将把该连接器用于此环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-214">If you configured a single Azure Connector earlier, that will be used for this environment.</span></span> <span data-ttu-id="6633c-215">如果配置了多个 Azure 连接器，则提供了选项用于选择要使用哪个连接器：**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**（针对最佳端到端性能推荐）</span><span class="sxs-lookup"><span data-stu-id="6633c-215">If you configured multiple Azure Connectors, you have the option to select which connector you would like to use: **East US**, **East US 2**, **West US** or **West US 2** (recommended for best end-to-end performance)</span></span>
1. <span data-ttu-id="6633c-216">输入一个**环境名称**。</span><span class="sxs-lookup"><span data-stu-id="6633c-216">Enter an **Environment name**.</span></span>
1. <span data-ttu-id="6633c-217">根据需要调整 VM 大小。</span><span class="sxs-lookup"><span data-stu-id="6633c-217">Adjust the VM size as you see fit.</span></span> <span data-ttu-id="6633c-218">（建议使用 VM SKU **D13 v2**。）</span><span class="sxs-lookup"><span data-stu-id="6633c-218">(We recommend VM SKU **D13 v2**.)</span></span>
1. <span data-ttu-id="6633c-219">**高级设置**保持原样。</span><span class="sxs-lookup"><span data-stu-id="6633c-219">Leave **Advanced settings** as they are.</span></span>
1. <span data-ttu-id="6633c-220">检查屏幕中的定价和许可条款后，选中框表示同意。</span><span class="sxs-lookup"><span data-stu-id="6633c-220">After reviewing the pricing and licensing terms on the screen, check the box to indicate agreement.</span></span>
1. <span data-ttu-id="6633c-221">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-221">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-222">在部署确认屏幕中，验证详细信息正确无误之后，单击**部署**。</span><span class="sxs-lookup"><span data-stu-id="6633c-222">On the deployment confirmation screen, after verifying that the details are correct, click **Deploy**.</span></span>
1. <span data-ttu-id="6633c-223">将回到**云托管的环境**视图，列表中应该会显示您的环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-223">You will return to the **Cloud-hosted environments** view and your environment should appear in the list.</span></span>
1. <span data-ttu-id="6633c-224">您请求的环境将显示为已入队列，然后是正在部署。</span><span class="sxs-lookup"><span data-stu-id="6633c-224">Your requested environment will show as queued and then deploying.</span></span> <span data-ttu-id="6633c-225">需要一些时间才能完成所有环境工作流，收益请在几小时（大约 6 – 9 个小时）后回来检查。</span><span class="sxs-lookup"><span data-stu-id="6633c-225">It will take some time for all of the environment workflows to complete, so please check back after a few hours (approximately 6 – 9 hours).</span></span>
1. <span data-ttu-id="6633c-226">继续操作之前，确保环境状态为**已部署**。</span><span class="sxs-lookup"><span data-stu-id="6633c-226">Before proceeding, make sure that your environment status is **Deployed**.</span></span>

![项目创建 - 版本](./media/project1.png)

![项目创建 - 拓扑 1](./media/project2.png)

![项目创建 - 拓扑 2](./media/project3.png)

![项目创建 - 环境参数](./media/project4.png)
### <a name="initialize-rcsu"></a><span data-ttu-id="6633c-231">初始化 RCSU</span><span class="sxs-lookup"><span data-stu-id="6633c-231">Initialize RCSU</span></span>
1. <span data-ttu-id="6633c-232">进入**云托管的环境**视图之后，从列表选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-232">While in the **Cloud-hosted environments** view, select your environment from the list.</span></span>
1. <span data-ttu-id="6633c-233">在屏幕右侧的环境视图中，单击**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6633c-233">From the environment view on the right side of the screen, click **Full details**.</span></span> <span data-ttu-id="6633c-234">将显示环境详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="6633c-234">The environment details view will display.</span></span>
1. <span data-ttu-id="6633c-235">在**环境功能**下，单击**管理**。</span><span class="sxs-lookup"><span data-stu-id="6633c-235">Under **ENVIRONMENT FEATURES**, click **Manage**.</span></span>
1. <span data-ttu-id="6633c-236">在 **Retail** 选项卡中，单击**初始化**。</span><span class="sxs-lookup"><span data-stu-id="6633c-236">From **Retail** tab, click **Initialize**.</span></span> <span data-ttu-id="6633c-237">将显示 RCSU 初始化参数视图。</span><span class="sxs-lookup"><span data-stu-id="6633c-237">The RCSU initialization parameters view will display.</span></span>
1. <span data-ttu-id="6633c-238">**区域**选择**美国东部**、**美国东部 2**、**美国西部**或**美国西部 2**。</span><span class="sxs-lookup"><span data-stu-id="6633c-238">For **REGION**, select **East US**, **East US 2**, **West US** or **West US 2**.</span></span>
1. <span data-ttu-id="6633c-239">对于**版本**，先从下拉列表选择**指定版本**，然后在下面显示的文本字段中指定 **9.16.19262.5**。</span><span class="sxs-lookup"><span data-stu-id="6633c-239">For **VERSION**, first select **Specify a version** from the drop down list, then specify **9.16.19262.5** in the text field that appears below.</span></span> <span data-ttu-id="6633c-240">*注意：请务必在此处**指定此处列出的精确版本**，以避免以后必须将 RCSU 更新为正确版本。*</span><span class="sxs-lookup"><span data-stu-id="6633c-240">*Note: Please make sure to **specify the exact version** listed here to avoid having to update RCSU later to correct version.*</span></span>
1. <span data-ttu-id="6633c-241">启用**应用扩展**。</span><span class="sxs-lookup"><span data-stu-id="6633c-241">Enable **Apply extension**.</span></span>
1. <span data-ttu-id="6633c-242">在扩展列表中，选择**商务预览演示库扩展**。</span><span class="sxs-lookup"><span data-stu-id="6633c-242">From the list of extensions, choose **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="6633c-243">单击**初始化**。</span><span class="sxs-lookup"><span data-stu-id="6633c-243">Click **Initialize**.</span></span>
1. <span data-ttu-id="6633c-244">在部署确认屏幕中，验证详细信息正确无误之后，单击**是**。</span><span class="sxs-lookup"><span data-stu-id="6633c-244">On the deployment confirmation screen, after verifying that the details are correct, click **Yes**.</span></span>
1. <span data-ttu-id="6633c-245">将回到 **Retail 管理**视图，其中已激活了 **Retail** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6633c-245">You are returned to the **Retail management** view with the **Retail** tab activated.</span></span> <span data-ttu-id="6633c-246">您的 RCSU 现在已进入队列等待配置。</span><span class="sxs-lookup"><span data-stu-id="6633c-246">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="6633c-247">等到 RCSU 状态成为**成功**，再继续操作（需要大约 2 - 5 小时）。</span><span class="sxs-lookup"><span data-stu-id="6633c-247">Wait until your RCSU status is **SUCCESS** before proceeding (will take approximately 2 - 5 hours).</span></span>
### <a name="initialize-e-commerce"></a><span data-ttu-id="6633c-248">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="6633c-248">Initialize e-Commerce</span></span>
1. <span data-ttu-id="6633c-249">切换到**电子商务(预览)** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6633c-249">Switch to the **e-Commerce (Preview)** tab.</span></span>
1. <span data-ttu-id="6633c-250">查看预览同意之后，单击**设置**。</span><span class="sxs-lookup"><span data-stu-id="6633c-250">After reviewing the Preview consent, click **Setup**.</span></span>
1. <span data-ttu-id="6633c-251">输入**电子商务租户名称**的名称。</span><span class="sxs-lookup"><span data-stu-id="6633c-251">Enter a name for **e-Commerce tenant name**.</span></span> <span data-ttu-id="6633c-252">但是，请注意，某些指向您的电子商务实例的 URL 中将显示该名称。</span><span class="sxs-lookup"><span data-stu-id="6633c-252">However, note that this will be visible in some of the URLs pointing to your e-Commerce instance.</span></span>
1. <span data-ttu-id="6633c-253">对于 **Retail Cloud Scale Unit 名称**，从列表选择您的 RCSU（列表只有一个选项）。</span><span class="sxs-lookup"><span data-stu-id="6633c-253">For **Retail cloud scale unit name**, select your RCSU from the list (list should only have one option).</span></span>
1. <span data-ttu-id="6633c-254">将自动填充**电子商务地理**且不可更改。</span><span class="sxs-lookup"><span data-stu-id="6633c-254">**e-Commerce geography** is automatically populated and cannot be changed.</span></span>
1. <span data-ttu-id="6633c-255">单击**下一步**继续。</span><span class="sxs-lookup"><span data-stu-id="6633c-255">Click **Next** to continue.</span></span>
1. <span data-ttu-id="6633c-256">对于**支持的主机名**，输入任何有效域（例如，www.fabrikam.com）。</span><span class="sxs-lookup"><span data-stu-id="6633c-256">For **Supported host names**, enter any valid domain (e.g. www.fabrikam.com).</span></span>
1. <span data-ttu-id="6633c-257">对于**系统管理员的 AAD 安全组**，输入要用作电子商务系统管理员组的 AAD SG ID。</span><span class="sxs-lookup"><span data-stu-id="6633c-257">For **AAD security group for system admin**, enter the AAD SG ID that you wish to use as e-Commerce system admin group.</span></span>
1. <span data-ttu-id="6633c-258">对于**评分和评价模块审查者的 AAD 安全组**，输入要用作评分和评价审查者组的 AAD SG ID。</span><span class="sxs-lookup"><span data-stu-id="6633c-258">For **AAD security group for ratings and review moderator**, enter the AAD SG ID that you wish to use as Ratings and Reviews moderator group.</span></span>
1. <span data-ttu-id="6633c-259">将 **B2C** 值保留为空（7 个以 B2C 开头的字段）。</span><span class="sxs-lookup"><span data-stu-id="6633c-259">Leave the **B2C** values empty (7 fields that start with B2C).</span></span>
1. <span data-ttu-id="6633c-260">让**启用评分和评价服务**保持启用状态。</span><span class="sxs-lookup"><span data-stu-id="6633c-260">Leave **Enable ratings and review service** enabled.</span></span>
1. <span data-ttu-id="6633c-261">单击**初始化**。</span><span class="sxs-lookup"><span data-stu-id="6633c-261">Click **Initialize**.</span></span>
1. <span data-ttu-id="6633c-262">将回到**零售管理**视图，其中已激活了**电子商务(预览)** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6633c-262">You are returned to the **Retail management** view with the **e-Commerce (Preview)** tab activated.</span></span> <span data-ttu-id="6633c-263">已开始初始化您的电子商务。</span><span class="sxs-lookup"><span data-stu-id="6633c-263">Your e-Commerce initialization has started.</span></span>
1. <span data-ttu-id="6633c-264">等待电子商务初始化状态成为**初始化成功**，再继续操作。</span><span class="sxs-lookup"><span data-stu-id="6633c-264">Before proceeding, wait until your e-Commerce initialization status is **INITIALIZATION SUCCESSFUL**.</span></span>
1. <span data-ttu-id="6633c-265">在右下部的**链接**下。</span><span class="sxs-lookup"><span data-stu-id="6633c-265">Under **LINKS** on the bottom right.</span></span>
    * <span data-ttu-id="6633c-266">记下**电子商务站点**链接。</span><span class="sxs-lookup"><span data-stu-id="6633c-266">Make note of the link **e-Commerce site**.</span></span> <span data-ttu-id="6633c-267">这是您的 C2 站点的根的链接。</span><span class="sxs-lookup"><span data-stu-id="6633c-267">This is the link to the root of your C2 site.</span></span>
    * <span data-ttu-id="6633c-268">记下**电子商务站点管理工具**链接。</span><span class="sxs-lookup"><span data-stu-id="6633c-268">Make note of the link **e-Commerce site management tool**.</span></span> <span data-ttu-id="6633c-269">这是站点管理工具（C1 创作工具）的链接。</span><span class="sxs-lookup"><span data-stu-id="6633c-269">This is the link to the site management tool (C1 authoring tool).</span></span>
## <a name="post-provisioning-steps"></a><span data-ttu-id="6633c-270">配置后步骤</span><span class="sxs-lookup"><span data-stu-id="6633c-270">Post-provisioning steps</span></span>
<span data-ttu-id="6633c-271">此阶段已端到端配置了环境，但是还需要执行配置步骤，才能开始评估环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-271">At this stage, the environment has been provisioned end-to-end, but there are still configuration steps that need to be taken care of before you can start evaluating the environment.</span></span>
### <a name="before-starting"></a><span data-ttu-id="6633c-272">准备工作</span><span class="sxs-lookup"><span data-stu-id="6633c-272">Before starting</span></span>
1. <span data-ttu-id="6633c-273">从顶级菜单，请选择 **管理云的环境**。</span><span class="sxs-lookup"><span data-stu-id="6633c-273">From the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6633c-274">从列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-274">Select your environment from the list.</span></span>
1. <span data-ttu-id="6633c-275">单击右侧环境信息中的**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6633c-275">Click **Full details** from the environment info on the right.</span></span>
1. <span data-ttu-id="6633c-276">单击**登录**打开菜单，选择**登录到环境**。</span><span class="sxs-lookup"><span data-stu-id="6633c-276">Click **Login** to open a menu, choose **Log on to environment**.</span></span>

<span data-ttu-id="6633c-277">确保选择 **USRT** 法人（右上角）。</span><span class="sxs-lookup"><span data-stu-id="6633c-277">Make sure that **USRT** legal entity is selected (top right corner).</span></span>

### <a name="configure-pos"></a><span data-ttu-id="6633c-278">配置 POS</span><span class="sxs-lookup"><span data-stu-id="6633c-278">Configure POS</span></span>
##### <a name="associate-worker-with-your-identity"></a><span data-ttu-id="6633c-279">将工作人员与您的标识关联</span><span class="sxs-lookup"><span data-stu-id="6633c-279">Associate worker with your identity</span></span>
1. <span data-ttu-id="6633c-280">使用左侧菜单转到**模块 > Retail > 员工 > 工作人员**。</span><span class="sxs-lookup"><span data-stu-id="6633c-280">Using the menu on the left, go to **Modules > Retail > Employees > Workers**.</span></span>
1. <span data-ttu-id="6633c-281">在列表中，找到并选择 **000713 - Andrew Collette**。</span><span class="sxs-lookup"><span data-stu-id="6633c-281">In the list, find and select record **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="6633c-282">在操作窗格上，单击 **Retail**。</span><span class="sxs-lookup"><span data-stu-id="6633c-282">On the Action Pane, click **Retail**.</span></span>
1. <span data-ttu-id="6633c-283">单击**关联现有标识**。</span><span class="sxs-lookup"><span data-stu-id="6633c-283">Click **Associate existing identity**.</span></span>
1. <span data-ttu-id="6633c-284">在（**使用电子邮件搜索**右侧的）**电子邮件**字段中，键入您的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6633c-284">In the **Email** field (to the right of **Search using email**), type your email address.</span></span>
1. <span data-ttu-id="6633c-285">单击**搜索**。</span><span class="sxs-lookup"><span data-stu-id="6633c-285">Click **Search**.</span></span>
1. <span data-ttu-id="6633c-286">选择包含您的姓名的记录。</span><span class="sxs-lookup"><span data-stu-id="6633c-286">Select the record with your name.</span></span>
1. <span data-ttu-id="6633c-287">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6633c-287">Click **OK**.</span></span>
1. <span data-ttu-id="6633c-288">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="6633c-288">Click **Save**.</span></span>
##### <a name="activate-cloud-pos"></a><span data-ttu-id="6633c-289">激活 Cloud POS</span><span class="sxs-lookup"><span data-stu-id="6633c-289">Activate Cloud POS</span></span>
1. <span data-ttu-id="6633c-290">登录到 LCS 门户。</span><span class="sxs-lookup"><span data-stu-id="6633c-290">Log in to the LCS portal.</span></span>
1. <span data-ttu-id="6633c-291">导航到您的项目。</span><span class="sxs-lookup"><span data-stu-id="6633c-291">Navigate to your project.</span></span>
1. <span data-ttu-id="6633c-292">从顶级菜单，请选择 **管理云的环境**。</span><span class="sxs-lookup"><span data-stu-id="6633c-292">From the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6633c-293">从列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-293">Select your environment from the list.</span></span>
1. <span data-ttu-id="6633c-294">单击右侧环境信息中的**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6633c-294">Click **Full details** from the environment info on the right.</span></span>
1. <span data-ttu-id="6633c-295">单击**登录**打开菜单，选择**登录到云销售点**，应该将加载 POS。</span><span class="sxs-lookup"><span data-stu-id="6633c-295">Click **Login** to open a menu, choose **Log on to Cloud Point of Sale**, POS should load up.</span></span>
1. <span data-ttu-id="6633c-296">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-296">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-297">使用您的 AAD 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="6633c-297">Log in with your AAD account.</span></span>
1. <span data-ttu-id="6633c-298">在**商店名称**下，选择**旧金山**。</span><span class="sxs-lookup"><span data-stu-id="6633c-298">Under **Store name**, choose **San Francisco**.</span></span>
1. <span data-ttu-id="6633c-299">单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-299">Click **Next**.</span></span>
1. <span data-ttu-id="6633c-300">在**收银机和设备**下，选择 **SANFRAN-1**。</span><span class="sxs-lookup"><span data-stu-id="6633c-300">Under **Register and device**, choose **SANFRAN-1**.</span></span>
1. <span data-ttu-id="6633c-301">单击**启用**。</span><span class="sxs-lookup"><span data-stu-id="6633c-301">Click **Activate**.</span></span>
1. <span data-ttu-id="6633c-302">应该会注销并进入 POS 登录屏幕中。</span><span class="sxs-lookup"><span data-stu-id="6633c-302">You should be logged out and end up in the POS login screen.</span></span>
1. <span data-ttu-id="6633c-303">现在可使用操作员 ID **000713** 和密码 **123** 登录到云 POS 体验。</span><span class="sxs-lookup"><span data-stu-id="6633c-303">You can now log in to the Cloud POS experience using Operator ID **000713** and password **123**.</span></span>
### <a name="site-setup"></a><span data-ttu-id="6633c-304">站点设置</span><span class="sxs-lookup"><span data-stu-id="6633c-304">Site setup</span></span>
1. <span data-ttu-id="6633c-305">使用前面记下的 URL 登录到**站点管理工具**。</span><span class="sxs-lookup"><span data-stu-id="6633c-305">Log in to the **site management tool** using the URL you noted earlier.</span></span>
1. <span data-ttu-id="6633c-306">单击 **Fabrikam** 站点打开站点设置对话框。</span><span class="sxs-lookup"><span data-stu-id="6633c-306">Click on the **Fabrikam** site to open the site setup dialog.</span></span>
1. <span data-ttu-id="6633c-307">对于域，选择之前初始化电子商务时输入的域。</span><span class="sxs-lookup"><span data-stu-id="6633c-307">For domain, select the domain you entered earlier when initializing the e-Commerce.</span></span>
1. <span data-ttu-id="6633c-308">默认渠道选择 **Fabrikam 扩展的在线商店**。</span><span class="sxs-lookup"><span data-stu-id="6633c-308">For default channel, select **Fabrikam extended online store**.</span></span> <span data-ttu-id="6633c-309">*注意：务必选择**扩展的**在线商店*</span><span class="sxs-lookup"><span data-stu-id="6633c-309">*Note: Make sure you select the **extended** online store*</span></span>
1. <span data-ttu-id="6633c-310">默认语言选择 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="6633c-310">For default language, select **en-us**.</span></span>
1. <span data-ttu-id="6633c-311">**路径**保持原样。</span><span class="sxs-lookup"><span data-stu-id="6633c-311">Leave **Path** as it is.</span></span>
1. <span data-ttu-id="6633c-312">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6633c-312">Click **OK**.</span></span>
1. <span data-ttu-id="6633c-313">将把您带到站点中的页面列表。</span><span class="sxs-lookup"><span data-stu-id="6633c-313">You will be sent to the list of pages on the site.</span></span>
### <a name="enable-jobs"></a><span data-ttu-id="6633c-314">启用作业</span><span class="sxs-lookup"><span data-stu-id="6633c-314">Enable jobs</span></span>
1. <span data-ttu-id="6633c-315">登录到环境（总部）。</span><span class="sxs-lookup"><span data-stu-id="6633c-315">Log in to the environment (HQ).</span></span>
1. <span data-ttu-id="6633c-316">使用左侧菜单转到 **Retail > 查询和报表 > 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="6633c-316">Using the menu on the left, go to **Retail > Inquiries and reports > Batch jobs**.</span></span>
1. <span data-ttu-id="6633c-317">对下面列表中的每个作业执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6633c-317">Perform the following steps for each of the jobs in the list below:</span></span>
    * <span data-ttu-id="6633c-318">**处理零售订单电子邮件通知**。</span><span class="sxs-lookup"><span data-stu-id="6633c-318">**Process retail order email notification**.</span></span>
    * <span data-ttu-id="6633c-319">**产品可用性**。</span><span class="sxs-lookup"><span data-stu-id="6633c-319">**Product availability**.</span></span>
    * <span data-ttu-id="6633c-320">**P-0001**。</span><span class="sxs-lookup"><span data-stu-id="6633c-320">**P-0001**.</span></span>
    * <span data-ttu-id="6633c-321">**同步订单作业**。</span><span class="sxs-lookup"><span data-stu-id="6633c-321">**Synchronize orders job**.</span></span>
1. <span data-ttu-id="6633c-322">使用快速筛选器和（上面列出的）作业名称搜索作业。</span><span class="sxs-lookup"><span data-stu-id="6633c-322">Use the Quick Filter to search for the job using its name (listed above).</span></span>
1. <span data-ttu-id="6633c-323">如果作业的状态为**预扣**，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6633c-323">If the Status of the job is **Withhold**, perform the following steps:</span></span>
    1. <span data-ttu-id="6633c-324">选择记录。</span><span class="sxs-lookup"><span data-stu-id="6633c-324">Select the record.</span></span>
    1. <span data-ttu-id="6633c-325">在操作窗格中，打开**批处理作业**功能区，然后单击**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="6633c-325">From the action pane, open **Batch job**-ribbon and click **Change status**.</span></span>
    1. <span data-ttu-id="6633c-326">选择**正在等待**，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="6633c-326">Select **Waiting** and Click **OK**.</span></span>
### <a name="run-full-data-sync"></a><span data-ttu-id="6633c-327">运行完全数据同步</span><span class="sxs-lookup"><span data-stu-id="6633c-327">Run full data sync</span></span>
1. <span data-ttu-id="6633c-328">使用左侧菜单转到 **模块 > Retail > 总部设置 > 零售调度 > 渠道数据库**。</span><span class="sxs-lookup"><span data-stu-id="6633c-328">Using the menu on the left, go to **Modules > Retail > Headquarters setup > Retail scheduler > Channel database**.</span></span>
1. <span data-ttu-id="6633c-329">将从左侧列表选择**默认**渠道。</span><span class="sxs-lookup"><span data-stu-id="6633c-329">**Default** channel is selected from the list on the left.</span></span> <span data-ttu-id="6633c-330">*选择另一个可用渠道（名称为 **scXXXXXXXXX**）*。</span><span class="sxs-lookup"><span data-stu-id="6633c-330">*Select the other available channel (named **scXXXXXXXXX**)*.</span></span>
1. <span data-ttu-id="6633c-331">单击操作窗格中的**完全数据同步**。</span><span class="sxs-lookup"><span data-stu-id="6633c-331">Click **Full data sync** from the action pane.</span></span>
1. <span data-ttu-id="6633c-332">输入 **9999** 作为配送计划。</span><span class="sxs-lookup"><span data-stu-id="6633c-332">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="6633c-333">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6633c-333">Click **OK**.</span></span>
1. <span data-ttu-id="6633c-334">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6633c-334">Click **OK**.</span></span>
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a><span data-ttu-id="6633c-335">执行这些步骤之后，即可开始评估您的预览环境！</span><span class="sxs-lookup"><span data-stu-id="6633c-335">After these steps you are ready to start evaluating your preview environment!</span></span>
<span data-ttu-id="6633c-336">使用**电子商务站点管理工具** URL 导航到 C1 创作体验，然后使用**电子商务站点** URL 导航到 C2 站点体验。</span><span class="sxs-lookup"><span data-stu-id="6633c-336">Use the **e-Commerce site management tool** URL to navigate to the C1 authoring experience and the **e-Commerce site** URL to navigate to the C2 site experience.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6633c-337">其他资源</span><span class="sxs-lookup"><span data-stu-id="6633c-337">Additional resources</span></span>
### <a name="how-to-find-your-aad-tenant-id"></a><span data-ttu-id="6633c-338">如何查找您的 AAD 租户 ID</span><span class="sxs-lookup"><span data-stu-id="6633c-338">How to find your AAD Tenant Id</span></span>
<span data-ttu-id="6633c-339">AAD 租户 ID 是 GUID，如以下示例所示：**72f988bf-86f1-41af-91ab-2d7cd011db47**</span><span class="sxs-lookup"><span data-stu-id="6633c-339">AAD Tenant Id is a GUID and looks like this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**</span></span>
##### <a name="from-azure-portal"></a><span data-ttu-id="6633c-340">从 Azure 门户</span><span class="sxs-lookup"><span data-stu-id="6633c-340">From Azure Portal</span></span>
1. <span data-ttu-id="6633c-341">登录到 Azure 门户：https://portal.azure.com/</span><span class="sxs-lookup"><span data-stu-id="6633c-341">Log in to the Azure portal: https://portal.azure.com/</span></span>
1. <span data-ttu-id="6633c-342">确保已选择了正确的目录。</span><span class="sxs-lookup"><span data-stu-id="6633c-342">Make sure that you have the correct directory selected.</span></span>
1. <span data-ttu-id="6633c-343">单击左侧菜单中的 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="6633c-343">Click **Azure Active Directory** from the menu on the left.</span></span>
1. <span data-ttu-id="6633c-344">选择**管理**下的**属性**。</span><span class="sxs-lookup"><span data-stu-id="6633c-344">Choose **Properties** under **Manage**.</span></span>
1. <span data-ttu-id="6633c-345">将在**目录 ID** 下显示 AAD 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="6633c-345">AAD Tenant Id is shown under **Directory ID**.</span></span>
##### <a name="from-openid-connect-metadata"></a><span data-ttu-id="6633c-346">从 OpenID 连接元数据</span><span class="sxs-lookup"><span data-stu-id="6633c-346">From OpenID Connect metadata</span></span>
<span data-ttu-id="6633c-347">通过将 **\{YOUR_DOMAIN\}** 替换为您的域（如 microsoft.com）创建 **OpenID URL**：https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration 将成为 https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration</span><span class="sxs-lookup"><span data-stu-id="6633c-347">Create **OpenID URL** by replacing **\{YOUR_DOMAIN\}** with your domain, e.g. microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration would become https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration</span></span>

1. <span data-ttu-id="6633c-348">导航到其中包含您的域的 **OpenID URL**。</span><span class="sxs-lookup"><span data-stu-id="6633c-348">Navigate to the **OpenID URL** with your domain in it.</span></span>
1. <span data-ttu-id="6633c-349">可以在多个属性值中看到 AAD 租户 ID。</span><span class="sxs-lookup"><span data-stu-id="6633c-349">AAD Tenant Id can be seen in multiple property values.</span></span>
1. <span data-ttu-id="6633c-350">找到 **authorization_endpoint**，并提取 **login.microsoftonline.com/** 后的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6633c-350">Locate **authorization_endpoint** and extract the GUID right after **login.microsoftonline.com/**.</span></span>
### <a name="how-to-find-the-id-of-your-aad-security-group"></a><span data-ttu-id="6633c-351">如何查找您的 AAD 安全组的 ID</span><span class="sxs-lookup"><span data-stu-id="6633c-351">How to find the ID of your AAD security group</span></span>
<span data-ttu-id="6633c-352">AAD 安全组 ID 是 GUID，如以下示例所示：**436ea7f5-ee6c-40c1-9f08-825c5811066a**</span><span class="sxs-lookup"><span data-stu-id="6633c-352">AAD security group ID is a GUID and looks like this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**</span></span>

<span data-ttu-id="6633c-353">此步骤假设用户是其尝试查找的 ID 所属组的成员。</span><span class="sxs-lookup"><span data-stu-id="6633c-353">This step assumes that the user is a member of the group they are attempting to locate ID for.</span></span>
1. <span data-ttu-id="6633c-354">导航到 Graph 资源管理器：https://developer.microsoft.com/en-us/graph/graph-explorer#</span><span class="sxs-lookup"><span data-stu-id="6633c-354">Navigate to the Graph Explorer: https://developer.microsoft.com/en-us/graph/graph-explorer#</span></span>
1. <span data-ttu-id="6633c-355">单击**通过 Microsoft 登录**，然后使用您的凭据登录。</span><span class="sxs-lookup"><span data-stu-id="6633c-355">Click **Sign In with Microsoft** and sign in using your credentials.</span></span>
1. <span data-ttu-id="6633c-356">登录后，单击左侧的**显示更多示例**。</span><span class="sxs-lookup"><span data-stu-id="6633c-356">After signing in, click **show more samples** from the left.</span></span>
1. <span data-ttu-id="6633c-357">从右窗格启用**组**。</span><span class="sxs-lookup"><span data-stu-id="6633c-357">Enable **Groups** from the right pane.</span></span>
1. <span data-ttu-id="6633c-358">关闭右窗格。</span><span class="sxs-lookup"><span data-stu-id="6633c-358">Close the right pane.</span></span>
1. <span data-ttu-id="6633c-359">单击**我属于的所有组**。</span><span class="sxs-lookup"><span data-stu-id="6633c-359">Click **all groups I belong to**.</span></span>
1. <span data-ttu-id="6633c-360">从**响应预览**文本框找到您的组。</span><span class="sxs-lookup"><span data-stu-id="6633c-360">Locate your group from the **Response Preview** text box.</span></span>
1. <span data-ttu-id="6633c-361">记下属性 **id** 下的安全组 ID。</span><span class="sxs-lookup"><span data-stu-id="6633c-361">Security group ID is noted under property **id**.</span></span>
### <a name="test-credit-card-information-to-perform-test-purchases"></a><span data-ttu-id="6633c-362">测试信用卡信息以执行测试性购买</span><span class="sxs-lookup"><span data-stu-id="6633c-362">Test credit card information to perform test purchases</span></span>
<span data-ttu-id="6633c-363">若要在站点中执行测试交易，可使用此测试信用卡信息：</span><span class="sxs-lookup"><span data-stu-id="6633c-363">In order to perform test transactions on the site, you can use this test credit card information:</span></span>

<span data-ttu-id="6633c-364">卡号：4111-1111-1111-1111；到期日期：10/20；CVV：737</span><span class="sxs-lookup"><span data-stu-id="6633c-364">Card number: 4111-1111-1111-1111, Expiration: 10/20, CVV: 737</span></span>

<span data-ttu-id="6633c-365">*注意：任何情况下均不应在测试站点中尝试使用真正的信用卡信息！*</span><span class="sxs-lookup"><span data-stu-id="6633c-365">*Note: You should not attempt to use actual credit card information on the test site under any circumstances!*</span></span>
### <a name="useful-links"></a><span data-ttu-id="6633c-366">有用链接</span><span class="sxs-lookup"><span data-stu-id="6633c-366">Useful links</span></span>
* [<span data-ttu-id="6633c-367">LCS (Lifecycle Services)</span><span class="sxs-lookup"><span data-stu-id="6633c-367">LCS (Lifecycle services)</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [<span data-ttu-id="6633c-368">RCSU (Retail Cloud Scale Unit)</span><span class="sxs-lookup"><span data-stu-id="6633c-368">RCSU (Retail Cloud Scale Unit)</span></span>](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [<span data-ttu-id="6633c-369">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="6633c-369">Microsoft Azure portal</span></span>](https://azure.microsoft.com/en-us/features/azure-portal)
* [<span data-ttu-id="6633c-370">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="6633c-370">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
* [<span data-ttu-id="6633c-371">Dynamics 365 Retail 的帮助资源</span><span class="sxs-lookup"><span data-stu-id="6633c-371">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a><span data-ttu-id="6633c-372">Microsoft Dynamics 365 Commerce 预览支持</span><span class="sxs-lookup"><span data-stu-id="6633c-372">Microsoft Dynamics 365 Commerce Preview support</span></span>
<span data-ttu-id="6633c-373">如果在执行配置步骤时遇到问题，请访问 [Microsoft Dynamics 365 Commerce 预览 Yammer 组](https://aka.ms/Dynamics365CommercePreviewYammer)获取帮助。</span><span class="sxs-lookup"><span data-stu-id="6633c-373">If you experience issues while performing the provisioning steps, please visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for assistance.</span></span> 

<span data-ttu-id="6633c-374">如果在访问 Yammer 组时遇到问题，也可以通过电子邮件 **Dynamics365Commerce@microsoft.com** 联系我们。</span><span class="sxs-lookup"><span data-stu-id="6633c-374">If you are having issues accessing the Yammer group, you can also reach us via email at **Dynamics365Commerce@microsoft.com**.</span></span> <span data-ttu-id="6633c-375">不会主动监控此电子邮件地址，因此应该存在响应延迟。</span><span class="sxs-lookup"><span data-stu-id="6633c-375">This email address is not actively monitored so expect a delay in response.</span></span>
***
## <a name="prerequisites-for-optional-features"></a><span data-ttu-id="6633c-376">可选功能的先决条件</span><span class="sxs-lookup"><span data-stu-id="6633c-376">Prerequisites for optional features</span></span>
<span data-ttu-id="6633c-377">如果要评估交易电子邮件功能，必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="6633c-377">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>
* <span data-ttu-id="6633c-378">您有可用的电子邮件服务器（SMTP 服务器），可从 Azure 订阅（在其中配置预览环境）使用该服务器。</span><span class="sxs-lookup"><span data-stu-id="6633c-378">You have an email server available (SMTP server), which can be used from the Azure subscription where you provision the preview environment.</span></span>
* <span data-ttu-id="6633c-379">您有该服务器的 FQDN/IP、SMTP 端口号和身份验证详细信息。</span><span class="sxs-lookup"><span data-stu-id="6633c-379">You have the server's FQDN/IP, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="6633c-380">如果要评估数字资产管理功能，特别是要使用新的全渠道图像，则必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="6633c-380">If you want to evaluate Digital Asset Management features, specifically ingest new omni-channel images, the following pre-requisites must be met:</span></span>
* <span data-ttu-id="6633c-381">需要有您的 **CMS 租户名称**。</span><span class="sxs-lookup"><span data-stu-id="6633c-381">You need to have your **CMS tenant name** available.</span></span> <span data-ttu-id="6633c-382">下面是有关查找此名称的说明。</span><span class="sxs-lookup"><span data-stu-id="6633c-382">Instructions for finding this name are below.</span></span>
### <a name="configure-image-backend-optional"></a><span data-ttu-id="6633c-383">后端配置图像（可选）</span><span class="sxs-lookup"><span data-stu-id="6633c-383">Configure image backend (optional)</span></span>
##### <a name="finding-your-media-base-url"></a><span data-ttu-id="6633c-384">编辑媒体基 URL</span><span class="sxs-lookup"><span data-stu-id="6633c-384">Finding your Media base URL</span></span>
<span data-ttu-id="6633c-385">*注意：必须先完成**站点设置**，才能完成此步骤。*</span><span class="sxs-lookup"><span data-stu-id="6633c-385">*Note: Before you can complete this step, you must complete **Site Setup**.*</span></span>
1. <span data-ttu-id="6633c-386">使用前面记下的 URL 登录到站点管理工具。</span><span class="sxs-lookup"><span data-stu-id="6633c-386">Log in to the site management tool using the URL you noted earlier.</span></span>
1. <span data-ttu-id="6633c-387">打开 **Fabrikam** 站点。</span><span class="sxs-lookup"><span data-stu-id="6633c-387">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="6633c-388">从左侧菜单中选择**资产**。</span><span class="sxs-lookup"><span data-stu-id="6633c-388">Choose **Assets** from the menu on the left.</span></span>
1. <span data-ttu-id="6633c-389">选择任何单个图像资产。</span><span class="sxs-lookup"><span data-stu-id="6633c-389">Select any single image asset.</span></span>
1. <span data-ttu-id="6633c-390">从右侧属性检查器找到**公共 URL**。</span><span class="sxs-lookup"><span data-stu-id="6633c-390">Locate **Public URL** from the property inspector on the right.</span></span> <span data-ttu-id="6633c-391">其中包含一个 URL。</span><span class="sxs-lookup"><span data-stu-id="6633c-391">It has an URL in it.</span></span>
    * <span data-ttu-id="6633c-392">示例 URL：https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC</span><span class="sxs-lookup"><span data-stu-id="6633c-392">Example URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC</span></span>
1. <span data-ttu-id="6633c-393">将 URL 中的最后一个标识符（上面的示例 URL 中为 MA1nQC）替换为以下字符串：**search?fileName=**</span><span class="sxs-lookup"><span data-stu-id="6633c-393">Replace the last identifier in the URL (MA1nQC in the example URL above) with the following string: **search?fileName=**</span></span>
    * <span data-ttu-id="6633c-394">替换后的示例 URL：https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=</span><span class="sxs-lookup"><span data-stu-id="6633c-394">Example URL after replacement: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=</span></span>
    * <span data-ttu-id="6633c-395">这是您的**媒体基 URL** - 请记下。</span><span class="sxs-lookup"><span data-stu-id="6633c-395">This is your **Media base URL** - make note of it.</span></span>
##### <a name="updating-the-media-base-url"></a><span data-ttu-id="6633c-396">更新媒体基 URL</span><span class="sxs-lookup"><span data-stu-id="6633c-396">Updating the media base URL</span></span>
1. <span data-ttu-id="6633c-397">登录到环境（总部）。</span><span class="sxs-lookup"><span data-stu-id="6633c-397">Log in to the environment (HQ).</span></span>
1. <span data-ttu-id="6633c-398">使用左侧菜单转到**模块 > Retail > 渠道设置 > 渠道配置文件**。</span><span class="sxs-lookup"><span data-stu-id="6633c-398">Using the menu on the left, go to **Modules > Retail > Channel setup > Channel profiles**.</span></span>
1. <span data-ttu-id="6633c-399">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="6633c-399">Click **Edit**.</span></span>
1. <span data-ttu-id="6633c-400">在**配置文件属性**中，健康**媒体服务器基 URL** 的属性值替换为您前面创建的**媒体基 URL**。</span><span class="sxs-lookup"><span data-stu-id="6633c-400">From the **Profile properties**, replace the property value for **Media Server Base URL** with the **Media base URL** you created earlier.</span></span>
1. <span data-ttu-id="6633c-401">选择左侧列表中**默认**渠道下的另一个渠道。</span><span class="sxs-lookup"><span data-stu-id="6633c-401">Select the other channel from the list on the left, under **Default** channel.</span></span>
1. <span data-ttu-id="6633c-402">在**配置文件属性**下，单击 **+ 添加**。</span><span class="sxs-lookup"><span data-stu-id="6633c-402">Under **Profile properties**, click **+ Add**.</span></span>
1. <span data-ttu-id="6633c-403">对于创建的属性，选择**媒体服务器基 URL** 作为属性键，为属性值输入您前面创建的**媒体基 URL**。</span><span class="sxs-lookup"><span data-stu-id="6633c-403">For the property that was added, choose **Media Server Base URL** as property key and for property value, enter the **Media base URL** you created earlier.</span></span>
1. <span data-ttu-id="6633c-404">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="6633c-404">Click **Save**.</span></span>

### <a name="configure-email-server-optional"></a><span data-ttu-id="6633c-405">配置电子邮件服务器（可选）</span><span class="sxs-lookup"><span data-stu-id="6633c-405">Configure email server (optional)</span></span>
<span data-ttu-id="6633c-406">请注意，必须可从您用于环境的 Azure 订阅访问您在此处输入的 SMTP 服务器或电子邮件服务。</span><span class="sxs-lookup"><span data-stu-id="6633c-406">Please note that the SMTP server or email service you enter here must be accessible from within the Azure subscription you are using for the environment.</span></span>
1. <span data-ttu-id="6633c-407">登录到环境（总部）。</span><span class="sxs-lookup"><span data-stu-id="6633c-407">Log in to the environment (HQ).</span></span>
1. <span data-ttu-id="6633c-408">使用左侧菜单转到**模块 > Retail > 总部设置 > 参数 > 电子邮件参数**。</span><span class="sxs-lookup"><span data-stu-id="6633c-408">Using the menu on the left, go to **Modules > Retail > Headquarters setup > Parameters > Email parameters**.</span></span>
1. <span data-ttu-id="6633c-409">单击 **SMTP 设置**选项卡。</span><span class="sxs-lookup"><span data-stu-id="6633c-409">Click the **SMTP settings** tab.</span></span>
1. <span data-ttu-id="6633c-410">在**出站邮件服务器**字段中，键入您的 SMTP 服务器或电子邮件服务的 FQDN 或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6633c-410">In the **Outgoing mail server field**, type the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="6633c-411">在 **SMTP 端口号**字段中，输入端口号（不使用 SSL 时，默认值为 25）。</span><span class="sxs-lookup"><span data-stu-id="6633c-411">In the **SMTP port number** field, enter the port number (default is the 25 when not using SSL).</span></span>
1. <span data-ttu-id="6633c-412">在**用户名**字段中，键入一个值（如果需要进行身份验证）。</span><span class="sxs-lookup"><span data-stu-id="6633c-412">In the **User name** field, type a value (if authentication is required).</span></span>
1. <span data-ttu-id="6633c-413">在**密码**字段中，键入一个值（如果需要进行身份验证）。</span><span class="sxs-lookup"><span data-stu-id="6633c-413">In the **Password** field, type a value (if authentication is required).</span></span>
1. <span data-ttu-id="6633c-414">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="6633c-414">Click **Save**.</span></span>
1. <span data-ttu-id="6633c-415">单击**刷新**。</span><span class="sxs-lookup"><span data-stu-id="6633c-415">Click **Refresh**.</span></span>
1. <span data-ttu-id="6633c-416">单击**测试电子邮件**选项卡。</span><span class="sxs-lookup"><span data-stu-id="6633c-416">Click the **Test email** tab.</span></span>
1. <span data-ttu-id="6633c-417">在电子邮件提供程序字段中，选择 **SMTP**。</span><span class="sxs-lookup"><span data-stu-id="6633c-417">In the Email provider field, choose **SMTP**.</span></span>
1. <span data-ttu-id="6633c-418">在**发送到**字段中，输入要将测试电子邮件发送到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6633c-418">In the **Send to** field, enter the email address where you want the test email to be delivered.</span></span>
1. <span data-ttu-id="6633c-419">单击**发送测试电子邮件**。</span><span class="sxs-lookup"><span data-stu-id="6633c-419">Click **Send test email**.</span></span>
### <a name="configure-email-templates-optional"></a><span data-ttu-id="6633c-420">配置电子邮件模板（可选）</span><span class="sxs-lookup"><span data-stu-id="6633c-420">Configure email templates (optional)</span></span>
<span data-ttu-id="6633c-421">需要使用有效的发件人电子邮件地址更新要为其发送电子邮件的每个交易事件的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="6633c-421">The email template for each transactional event that you wish to send emails for needs to be updated with a valid sender email address.</span></span>
1. <span data-ttu-id="6633c-422">使用左侧菜单转到**模块 > 组织管理 > 设置 > 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="6633c-422">Using the menu on the left, go to **Modules > Organization administration > Setup > Organization email templates**.</span></span>
1. <span data-ttu-id="6633c-423">单击**显示列表**。</span><span class="sxs-lookup"><span data-stu-id="6633c-423">Click **Show list**.</span></span>
1. <span data-ttu-id="6633c-424">对于列表中的每个模板：</span><span class="sxs-lookup"><span data-stu-id="6633c-424">For each of the templates in the list:</span></span>
    1. <span data-ttu-id="6633c-425">在**发件人电子邮件**字段中，键入此电子邮件模板的发件人电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6633c-425">In the **Sender email** field, type the sender email address for this email template.</span></span>
    1. <span data-ttu-id="6633c-426">（可选）在**发件人姓名**字段中，键入要用作此电子邮件模板的发件人的姓名。</span><span class="sxs-lookup"><span data-stu-id="6633c-426">(Optional) In the **Sender name** field, type a name that will be used as sender for this email template.</span></span>
1. <span data-ttu-id="6633c-427">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="6633c-427">Click **Save**.</span></span>
### <a name="customizing-email-templates-optional"></a><span data-ttu-id="6633c-428">自定义电子邮件模板（可选）</span><span class="sxs-lookup"><span data-stu-id="6633c-428">Customizing email templates (optional)</span></span>
<span data-ttu-id="6633c-429">您可能希望自定义电子邮件模板以使用其他图像，或更新模板中的链接以链接回您的预览环境。</span><span class="sxs-lookup"><span data-stu-id="6633c-429">You might want to customize the email templates to use different images or update the links in the template to link back to your Preview environment.</span></span> <span data-ttu-id="6633c-430">下面的步骤介绍如何下载默认模板，自定义默认模板和更新系统中的模板。</span><span class="sxs-lookup"><span data-stu-id="6633c-430">The steps below explain how to download the default templates, customize them and update the templates in the system.</span></span>
1. <span data-ttu-id="6633c-431">使用浏览器将 [Microsoft Dynamics 365 Commerce 预览默认电子邮件模板 .zip 文件](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)（其中包含以下 HTML 文档）下载到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="6633c-431">Using a browser, download [the Microsoft Dynamics 365 Commerce Preview default email templates .zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) containing the following HTML documents to your local computer.</span></span>
    1. <span data-ttu-id="6633c-432">订单确认模板</span><span class="sxs-lookup"><span data-stu-id="6633c-432">Order confirmation template</span></span>
    1. <span data-ttu-id="6633c-433">颁发礼品卡模板</span><span class="sxs-lookup"><span data-stu-id="6633c-433">Issue gift card template</span></span>
    1. <span data-ttu-id="6633c-434">新订单模板</span><span class="sxs-lookup"><span data-stu-id="6633c-434">New order template</span></span>
    1. <span data-ttu-id="6633c-435">打包订单模板</span><span class="sxs-lookup"><span data-stu-id="6633c-435">Pack order template</span></span>
    1. <span data-ttu-id="6633c-436">选择订单模板</span><span class="sxs-lookup"><span data-stu-id="6633c-436">Pick order template</span></span>
1. <span data-ttu-id="6633c-437">使用文本编辑器或 HTML 编辑器自定义模板。</span><span class="sxs-lookup"><span data-stu-id="6633c-437">Customize the templates using a text or HTML editor.</span></span> <span data-ttu-id="6633c-438">请参阅下面的支持的令牌的列表。</span><span class="sxs-lookup"><span data-stu-id="6633c-438">Please see a list of supported tokens below.</span></span>
1. <span data-ttu-id="6633c-439">登录到环境（总部）。</span><span class="sxs-lookup"><span data-stu-id="6633c-439">Log in to the environment (HQ).</span></span>
1. <span data-ttu-id="6633c-440">使用左侧菜单转到**模块 > Retail > 总部设置 > 参数 > 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="6633c-440">Using the menu on the left, go to **Modules > Retail > Headquarters setup > Parameters > Organization email templates**.</span></span>
1. <span data-ttu-id="6633c-441">展开左侧列表查看所有模板。</span><span class="sxs-lookup"><span data-stu-id="6633c-441">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="6633c-442">为要自定义的每个模板执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6633c-442">For each of the templates you wish to customize, perform the following steps:</span></span>
    1. <span data-ttu-id="6633c-443">从列表中选择模板。</span><span class="sxs-lookup"><span data-stu-id="6633c-443">Select the template from the list.</span></span>
    1. <span data-ttu-id="6633c-444">在**电子邮件内容**下，从列表选择相应语言版本（默认值为 **en-us**）。</span><span class="sxs-lookup"><span data-stu-id="6633c-444">Under **Email message content**, select the appropriate language version from the list (default **en-us**).</span></span>
    1. <span data-ttu-id="6633c-445">在**电子邮件内容**下，单击**编辑**；您应该会看到打开了**上传电子邮件模板**窗格。</span><span class="sxs-lookup"><span data-stu-id="6633c-445">Under **Email message content**, click **Edit**, you should see **Upload email template** pane opening.</span></span>
    1. <span data-ttu-id="6633c-446">单击**浏览**，然后找到包含自定义的内容的 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="6633c-446">Click **Browse** and locate the HTML file with the customized content.</span></span>
    1. <span data-ttu-id="6633c-447">单击**上传**，将把您的模板上传到系统，并显示预览。</span><span class="sxs-lookup"><span data-stu-id="6633c-447">Click **Upload**, your template is uploaded to the system and a preview is shown.</span></span>
    1. <span data-ttu-id="6633c-448">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6633c-448">Click **OK**.</span></span>
    1. <span data-ttu-id="6633c-449">（可选）自定义模板的**主题**属性。</span><span class="sxs-lookup"><span data-stu-id="6633c-449">(Optional) Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="6633c-450">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="6633c-450">Click **Save**.</span></span>

#### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="6633c-451">电子邮件模板中支持的令牌</span><span class="sxs-lookup"><span data-stu-id="6633c-451">Supported tokens in the email template</span></span>
<span data-ttu-id="6633c-452">将在显示电子邮件时把这些令牌替换为应用于客户及其订单的实际值。</span><span class="sxs-lookup"><span data-stu-id="6633c-452">These tokens will be replaced at email rendering time with the actual values that apply to the customer and their order.</span></span>

<span data-ttu-id="6633c-453">**销售订单** - 以下令牌应用于整个销售订单。</span><span class="sxs-lookup"><span data-stu-id="6633c-453">**Sales order** - The following tokens apply to the overall sales order.</span></span>

|<span data-ttu-id="6633c-454">令牌的名称</span><span class="sxs-lookup"><span data-stu-id="6633c-454">Name of the token</span></span>|<span data-ttu-id="6633c-455">标志</span><span class="sxs-lookup"><span data-stu-id="6633c-455">Token</span></span>|
|---|---|
|<span data-ttu-id="6633c-456">转移单编号</span><span class="sxs-lookup"><span data-stu-id="6633c-456">Order number</span></span>|<span data-ttu-id="6633c-457">%salesid%</span><span class="sxs-lookup"><span data-stu-id="6633c-457">%salesid%</span></span>|
|<span data-ttu-id="6633c-458">客户名称</span><span class="sxs-lookup"><span data-stu-id="6633c-458">Customer's name</span></span>|<span data-ttu-id="6633c-459">%customername%</span><span class="sxs-lookup"><span data-stu-id="6633c-459">%customername%</span></span>|
|<span data-ttu-id="6633c-460">交货地址</span><span class="sxs-lookup"><span data-stu-id="6633c-460">Delivery address</span></span>|<span data-ttu-id="6633c-461">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="6633c-461">%deliveryaddress%</span></span>|
|<span data-ttu-id="6633c-462">帐单地址</span><span class="sxs-lookup"><span data-stu-id="6633c-462">Billing address</span></span>|<span data-ttu-id="6633c-463">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="6633c-463">%customeraddress%</span></span>|
|<span data-ttu-id="6633c-464">订货日期</span><span class="sxs-lookup"><span data-stu-id="6633c-464">Order date</span></span>|<span data-ttu-id="6633c-465">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="6633c-465">%shipdate%</span></span>|
|<span data-ttu-id="6633c-466">传递模式</span><span class="sxs-lookup"><span data-stu-id="6633c-466">Delivery mode</span></span>|<span data-ttu-id="6633c-467">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="6633c-467">%modeofdelivery%</span></span>|
|<span data-ttu-id="6633c-468">折扣</span><span class="sxs-lookup"><span data-stu-id="6633c-468">Discount</span></span>|<span data-ttu-id="6633c-469">%discount%</span><span class="sxs-lookup"><span data-stu-id="6633c-469">%discount%</span></span>|
|<span data-ttu-id="6633c-470">销售税</span><span class="sxs-lookup"><span data-stu-id="6633c-470">Sales tax</span></span>|<span data-ttu-id="6633c-471">%tax%</span><span class="sxs-lookup"><span data-stu-id="6633c-471">%tax%</span></span>|
|<span data-ttu-id="6633c-472">订单合计</span><span class="sxs-lookup"><span data-stu-id="6633c-472">Order total</span></span>|<span data-ttu-id="6633c-473">%total%</span><span class="sxs-lookup"><span data-stu-id="6633c-473">%total%</span></span>|

<span data-ttu-id="6633c-474">**销售行** - 将填写订单中每个产品的以下令牌。</span><span class="sxs-lookup"><span data-stu-id="6633c-474">**Sales line** - The following tokens are populated for each product in the order.</span></span>

<span data-ttu-id="6633c-475">*注意：将**产品列表 - 开始**和**产品列表 - 结束**令牌放到每个产品重复的 HTML 块的开始和结束处。*</span><span class="sxs-lookup"><span data-stu-id="6633c-475">*Note: Place the **Product list - start** and **Product list - end** tokens at the beginning and end of the HTML block that repeats for every product.*</span></span>

|<span data-ttu-id="6633c-476">令牌的名称</span><span class="sxs-lookup"><span data-stu-id="6633c-476">Name of the token</span></span>|<span data-ttu-id="6633c-477">标志</span><span class="sxs-lookup"><span data-stu-id="6633c-477">Token</span></span>|
|---|---|
|<span data-ttu-id="6633c-478">产品列表 - 开始</span><span class="sxs-lookup"><span data-stu-id="6633c-478">Product list - start</span></span>|<span data-ttu-id="6633c-479">\<!--%tablebegin.salesline% --></span><span class="sxs-lookup"><span data-stu-id="6633c-479">\<!--%tablebegin.salesline% --></span></span>|
|<span data-ttu-id="6633c-480">产品列表 - 结束</span><span class="sxs-lookup"><span data-stu-id="6633c-480">Product list - end</span></span>|<span data-ttu-id="6633c-481">\<!--%tableend.salesline%--></span><span class="sxs-lookup"><span data-stu-id="6633c-481">\<!--%tableend.salesline%--></span></span>|
|<span data-ttu-id="6633c-482">产品名称</span><span class="sxs-lookup"><span data-stu-id="6633c-482">Product name</span></span>|<span data-ttu-id="6633c-483">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="6633c-483">%lineproductname%</span></span>|
|<span data-ttu-id="6633c-484">说明</span><span class="sxs-lookup"><span data-stu-id="6633c-484">Description</span></span>|<span data-ttu-id="6633c-485">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="6633c-485">%lineproductdescription%</span></span>|
|<span data-ttu-id="6633c-486">数量</span><span class="sxs-lookup"><span data-stu-id="6633c-486">Quantity</span></span>|<span data-ttu-id="6633c-487">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="6633c-487">%linequantity%</span></span>|
|<span data-ttu-id="6633c-488">行单价</span><span class="sxs-lookup"><span data-stu-id="6633c-488">Line unit price</span></span>|<span data-ttu-id="6633c-489">%lineprice%（验证）</span><span class="sxs-lookup"><span data-stu-id="6633c-489">%lineprice% (verify)</span></span>|
|<span data-ttu-id="6633c-490">行项总数</span><span class="sxs-lookup"><span data-stu-id="6633c-490">line item total</span></span>|<span data-ttu-id="6633c-491">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="6633c-491">%linenetamount%</span></span>|
|<span data-ttu-id="6633c-492">行折扣</span><span class="sxs-lookup"><span data-stu-id="6633c-492">line discount</span></span>|<span data-ttu-id="6633c-493">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="6633c-493">%linediscount%</span></span>|
|<span data-ttu-id="6633c-494">装运日期</span><span class="sxs-lookup"><span data-stu-id="6633c-494">Ship date</span></span>|<span data-ttu-id="6633c-495">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="6633c-495">%lineshipdate%</span></span>|
|<span data-ttu-id="6633c-496">采购方法</span><span class="sxs-lookup"><span data-stu-id="6633c-496">Procurement method</span></span>|<span data-ttu-id="6633c-497">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="6633c-497">%linedeliverymode%</span></span>|
|<span data-ttu-id="6633c-498">delivery address / 交货地址</span><span class="sxs-lookup"><span data-stu-id="6633c-498">delivery address</span></span>|<span data-ttu-id="6633c-499">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="6633c-499">%linedeliveryaddress%</span></span>|
|<span data-ttu-id="6633c-500">行的销售单位</span><span class="sxs-lookup"><span data-stu-id="6633c-500">Sales unit of the line</span></span>|<span data-ttu-id="6633c-501">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="6633c-501">%lineunit%</span></span>|

