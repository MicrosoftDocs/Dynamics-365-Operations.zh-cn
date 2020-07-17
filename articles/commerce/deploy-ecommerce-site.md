---
title: 部署新的电子商务租户
description: 此主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的电子商务租户。
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00f35b516dbf6ab4d4d9171c84a16b89f6afe832
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533267"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="4d75d-103">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="4d75d-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4d75d-104">此主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="4d75d-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="4d75d-105">概览</span><span class="sxs-lookup"><span data-stu-id="4d75d-105">Overview</span></span>

<span data-ttu-id="4d75d-106">Microsoft Dynamics Lifecycle Services (LCS) 是基于云的协作工作空间，合作伙伴和客户可将其用于管理自己的项目和环境，查看有关 Microsoft Dynamics 产品和功能的最新信息，以及创建，跟踪和浏览支持事件。</span><span class="sxs-lookup"><span data-stu-id="4d75d-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="4d75d-107">电子商务管理功能集成到 LCS 中。</span><span class="sxs-lookup"><span data-stu-id="4d75d-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="4d75d-108">若要详细了解 LCS，请参阅 [Lifecycle Services 用户指南](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)。</span><span class="sxs-lookup"><span data-stu-id="4d75d-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="4d75d-109">入门</span><span class="sxs-lookup"><span data-stu-id="4d75d-109">Get started</span></span>

<span data-ttu-id="4d75d-110">必须先初始化项目、环境和 Retail Cloud Scale Unit (RCSU)，才能初始化电子商务。</span><span class="sxs-lookup"><span data-stu-id="4d75d-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="4d75d-111">若要在 LCS 中执行初始化，必须具有项目负责人或环境管理员角色的权限。</span><span class="sxs-lookup"><span data-stu-id="4d75d-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="4d75d-112">支持生产环境和沙盒环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="4d75d-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="4d75d-113">有关环境的详细信息，请参阅[环境计划](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)。</span><span class="sxs-lookup"><span data-stu-id="4d75d-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="4d75d-114">有关 RCSU 的详细信息，请参阅[初始化 Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)。</span><span class="sxs-lookup"><span data-stu-id="4d75d-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="4d75d-115">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="4d75d-115">Initialize e-Commerce</span></span>

<span data-ttu-id="4d75d-116">此过程用于初始化现有环境中的电子商务功能。</span><span class="sxs-lookup"><span data-stu-id="4d75d-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="4d75d-117">首先，确保具有以下必需信息：</span><span class="sxs-lookup"><span data-stu-id="4d75d-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="4d75d-118">将使用的 RCSU。</span><span class="sxs-lookup"><span data-stu-id="4d75d-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="4d75d-119">将用于电子商务系统管理员的 Microsoft Azure Active Directory 安全组。</span><span class="sxs-lookup"><span data-stu-id="4d75d-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="4d75d-120">将用于评分和评价审查者的 Microsoft Azure Active Directory 安全组。</span><span class="sxs-lookup"><span data-stu-id="4d75d-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="4d75d-121">将与环境关联的域。</span><span class="sxs-lookup"><span data-stu-id="4d75d-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="4d75d-122">此外，还可以收集以下可选信息：</span><span class="sxs-lookup"><span data-stu-id="4d75d-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="4d75d-123">Azure AD 企业对消费者 (B2C) 信息：</span><span class="sxs-lookup"><span data-stu-id="4d75d-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="4d75d-124">租户名称。</span><span class="sxs-lookup"><span data-stu-id="4d75d-124">Tenant Name.</span></span>
    - <span data-ttu-id="4d75d-125">客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="4d75d-125">Client ID.</span></span>
    - <span data-ttu-id="4d75d-126">登录自定义域。</span><span class="sxs-lookup"><span data-stu-id="4d75d-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="4d75d-127">回复 URL。</span><span class="sxs-lookup"><span data-stu-id="4d75d-127">Reply URL.</span></span>
    - <span data-ttu-id="4d75d-128">注册登录策略 ID。</span><span class="sxs-lookup"><span data-stu-id="4d75d-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="4d75d-129">重置密码策略 ID。</span><span class="sxs-lookup"><span data-stu-id="4d75d-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="4d75d-130">编辑个人资料策略 ID。</span><span class="sxs-lookup"><span data-stu-id="4d75d-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="4d75d-131">以后可通过服务请求添加此信息。</span><span class="sxs-lookup"><span data-stu-id="4d75d-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="4d75d-132">收集所需信息之后，请执行以下步骤初始化电子商务。</span><span class="sxs-lookup"><span data-stu-id="4d75d-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="4d75d-133">登录 [LCS](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="4d75d-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="4d75d-134">打开包含要在其中初始化电子商务的环境的项目。</span><span class="sxs-lookup"><span data-stu-id="4d75d-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="4d75d-135">在**环境**部分中，选择环境。</span><span class="sxs-lookup"><span data-stu-id="4d75d-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="4d75d-136">在**环境功能**下，选择**零售管理**链接。</span><span class="sxs-lookup"><span data-stu-id="4d75d-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="4d75d-137">在**电子商务**选项卡中，选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="4d75d-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="4d75d-138">将显示对话框，必须在其中输入预配所需信息。</span><span class="sxs-lookup"><span data-stu-id="4d75d-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="4d75d-139">填写必需信息，然后转到下一页。</span><span class="sxs-lookup"><span data-stu-id="4d75d-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="4d75d-140">在下一页，填写必需信息，然后提交表单。</span><span class="sxs-lookup"><span data-stu-id="4d75d-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="4d75d-141">将回到**电子商务**选项卡，在这里应该会看到已经开始初始化。</span><span class="sxs-lookup"><span data-stu-id="4d75d-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="4d75d-142">若要查看初始化状态，请**刷新**或以后回到**电子商务**选项卡。</span><span class="sxs-lookup"><span data-stu-id="4d75d-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="4d75d-143">从 LCS 初始化电子商务之后，系统将预配电子商务所需若干组件，并将其与环境关联。</span><span class="sxs-lookup"><span data-stu-id="4d75d-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="4d75d-144">预配完成后，将更新**零售管理**页中的**电子商务**选项卡以体现预配。</span><span class="sxs-lookup"><span data-stu-id="4d75d-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="4d75d-145">页面将显示最新自定义部署和其他任何进行中部署的状态。</span><span class="sxs-lookup"><span data-stu-id="4d75d-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="4d75d-146">还包含指向电子商务站点以及在其中创作站点的电子商务站点构建器的链接。</span><span class="sxs-lookup"><span data-stu-id="4d75d-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="4d75d-147">访问站点构建器</span><span class="sxs-lookup"><span data-stu-id="4d75d-147">Access site builder</span></span>

<span data-ttu-id="4d75d-148">要访问站点构建器，请转到 LCS 中**零售管理**页上的**电子商务**标签，然后选择**电子商务站点管理工具**链接。</span><span class="sxs-lookup"><span data-stu-id="4d75d-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="4d75d-149">站点构建器登录页面显示租户级别的视图。</span><span class="sxs-lookup"><span data-stu-id="4d75d-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="4d75d-150">从此页中，您可以：</span><span class="sxs-lookup"><span data-stu-id="4d75d-150">From this page, you can:</span></span>

- <span data-ttu-id="4d75d-151">修改租户级别设置。</span><span class="sxs-lookup"><span data-stu-id="4d75d-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="4d75d-152">导航到您创建并有权查看的任何站点。</span><span class="sxs-lookup"><span data-stu-id="4d75d-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="4d75d-153">访问审核功能，例如审查和报告。</span><span class="sxs-lookup"><span data-stu-id="4d75d-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="4d75d-154">创建新站点。</span><span class="sxs-lookup"><span data-stu-id="4d75d-154">Create a new site.</span></span> <span data-ttu-id="4d75d-155">有关如何创建新站点的详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。</span><span class="sxs-lookup"><span data-stu-id="4d75d-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4d75d-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="4d75d-156">Additional resources</span></span>

[<span data-ttu-id="4d75d-157">配置域名</span><span class="sxs-lookup"><span data-stu-id="4d75d-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4d75d-158">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="4d75d-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4d75d-159">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="4d75d-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4d75d-160">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="4d75d-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4d75d-161">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="4d75d-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4d75d-162">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="4d75d-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4d75d-163">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="4d75d-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4d75d-164">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="4d75d-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4d75d-165">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="4d75d-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4d75d-166">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="4d75d-166">Enable location-based store detection</span></span>](enable-store-detection.md)
