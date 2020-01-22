---
title: 部署新的电子商务租户
description: 此主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的电子商务租户。
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945505"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="6156e-103">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="6156e-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6156e-104">此主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="6156e-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="6156e-105">概览</span><span class="sxs-lookup"><span data-stu-id="6156e-105">Overview</span></span>
    
<span data-ttu-id="6156e-106">Microsoft Dynamics Lifecycle Services (LCS) 是基于云的协作工作空间，合作伙伴和客户可将其用于管理自己的项目和环境，查看有关 Microsoft Dynamics 产品和功能的最新信息，以及创建，跟踪和浏览支持事件。</span><span class="sxs-lookup"><span data-stu-id="6156e-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="6156e-107">电子商务管理功能集成到 LCS 中。</span><span class="sxs-lookup"><span data-stu-id="6156e-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="6156e-108">若要详细了解 LCS，请参阅 [Lifecycle Services 用户指南](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)。</span><span class="sxs-lookup"><span data-stu-id="6156e-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="6156e-109">入门</span><span class="sxs-lookup"><span data-stu-id="6156e-109">Get started</span></span>

<span data-ttu-id="6156e-110">必须先初始化项目、环境和 Retail Cloud Scale Unit (RCSU)，才能初始化电子商务。</span><span class="sxs-lookup"><span data-stu-id="6156e-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="6156e-111">若要在 LCS 中执行初始化，必须具有项目负责人或环境管理员角色的权限。</span><span class="sxs-lookup"><span data-stu-id="6156e-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="6156e-112">支持生产环境和沙盒环境拓扑。</span><span class="sxs-lookup"><span data-stu-id="6156e-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="6156e-113">有关环境的详细信息，请参阅[环境计划](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)。</span><span class="sxs-lookup"><span data-stu-id="6156e-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="6156e-114">有关 RCSU 的详细信息，请参阅[初始化 Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)。</span><span class="sxs-lookup"><span data-stu-id="6156e-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="6156e-115">初始化电子商务</span><span class="sxs-lookup"><span data-stu-id="6156e-115">Initialize e-Commerce</span></span>

<span data-ttu-id="6156e-116">此过程用于初始化现有环境中的电子商务功能。</span><span class="sxs-lookup"><span data-stu-id="6156e-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="6156e-117">首先，确保具有以下必需信息：</span><span class="sxs-lookup"><span data-stu-id="6156e-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="6156e-118">将使用的 RCSU。</span><span class="sxs-lookup"><span data-stu-id="6156e-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="6156e-119">将用于电子商务系统管理员的 Microsoft Azure Active Directory 安全组。</span><span class="sxs-lookup"><span data-stu-id="6156e-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="6156e-120">将用于评分和评价审查者的 Microsoft Azure Active Directory 安全组。</span><span class="sxs-lookup"><span data-stu-id="6156e-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="6156e-121">将与环境关联的域。</span><span class="sxs-lookup"><span data-stu-id="6156e-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="6156e-122">此外，还可以收集以下可选信息：</span><span class="sxs-lookup"><span data-stu-id="6156e-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="6156e-123">Azure AD 企业对消费者 (B2C) 信息：</span><span class="sxs-lookup"><span data-stu-id="6156e-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="6156e-124">租户名称。</span><span class="sxs-lookup"><span data-stu-id="6156e-124">Tenant Name.</span></span>
    - <span data-ttu-id="6156e-125">客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="6156e-125">Client ID.</span></span>
    - <span data-ttu-id="6156e-126">登录自定义域。</span><span class="sxs-lookup"><span data-stu-id="6156e-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="6156e-127">回复 URL。</span><span class="sxs-lookup"><span data-stu-id="6156e-127">Reply URL.</span></span>
    - <span data-ttu-id="6156e-128">注册登录策略 ID。</span><span class="sxs-lookup"><span data-stu-id="6156e-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="6156e-129">重置密码策略 ID。</span><span class="sxs-lookup"><span data-stu-id="6156e-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="6156e-130">编辑个人资料策略 ID。</span><span class="sxs-lookup"><span data-stu-id="6156e-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="6156e-131">以后可通过服务请求添加此信息。</span><span class="sxs-lookup"><span data-stu-id="6156e-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="6156e-132">收集所需信息之后，请执行以下步骤初始化电子商务。</span><span class="sxs-lookup"><span data-stu-id="6156e-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="6156e-133">登录 [LCS](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="6156e-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="6156e-134">打开包含要在其中初始化电子商务的环境的项目。</span><span class="sxs-lookup"><span data-stu-id="6156e-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="6156e-135">在**环境**部分中，选择环境。</span><span class="sxs-lookup"><span data-stu-id="6156e-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="6156e-136">在**环境功能**下，选择**零售管理**链接。</span><span class="sxs-lookup"><span data-stu-id="6156e-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="6156e-137">在**电子商务**选项卡中，选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="6156e-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="6156e-138">将显示对话框，必须在其中输入预配所需信息。</span><span class="sxs-lookup"><span data-stu-id="6156e-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="6156e-139">填写必需信息，然后转到下一页。</span><span class="sxs-lookup"><span data-stu-id="6156e-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="6156e-140">在下一页，填写必需信息，然后提交表单。</span><span class="sxs-lookup"><span data-stu-id="6156e-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="6156e-141">将回到**电子商务**选项卡，在这里应该会看到已经开始初始化。</span><span class="sxs-lookup"><span data-stu-id="6156e-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="6156e-142">若要查看初始化状态，请**刷新**或以后回到**电子商务**选项卡。</span><span class="sxs-lookup"><span data-stu-id="6156e-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="6156e-143">从 LCS 初始化电子商务之后，系统将预配电子商务所需若干组件，并将其与环境关联。</span><span class="sxs-lookup"><span data-stu-id="6156e-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="6156e-144">预配完成后，将更新**零售管理**页中的**电子商务**选项卡以体现预配。</span><span class="sxs-lookup"><span data-stu-id="6156e-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="6156e-145">页面将显示最新自定义部署和其他任何进行中部署的状态。</span><span class="sxs-lookup"><span data-stu-id="6156e-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="6156e-146">还包含电子商务站点和电子商务站点管理工具（创作工具）的链接。</span><span class="sxs-lookup"><span data-stu-id="6156e-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="6156e-147">访问创作环境</span><span class="sxs-lookup"><span data-stu-id="6156e-147">Access the authoring environment</span></span>

<span data-ttu-id="6156e-148">若要访问创作环境，请转到**零售管理**页中的**电子商务**选项卡。</span><span class="sxs-lookup"><span data-stu-id="6156e-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="6156e-149">可在这里找到电子商务站点和站点管理工具的链接。</span><span class="sxs-lookup"><span data-stu-id="6156e-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6156e-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="6156e-150">Additional resources</span></span>

[<span data-ttu-id="6156e-151">配置域名</span><span class="sxs-lookup"><span data-stu-id="6156e-151">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6156e-152">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="6156e-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6156e-153">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="6156e-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6156e-154">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="6156e-154">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6156e-155">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="6156e-155">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6156e-156">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="6156e-156">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6156e-157">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="6156e-157">Enable location-based store detection</span></span>](enable-store-detection.md)
