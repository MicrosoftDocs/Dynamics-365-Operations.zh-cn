---
title: 配置 Commerce 预览环境
description: 本主题说明如何在预配后配置 Microsoft Dynamics 365 Commerce 预览环境。
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906131"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="db622-103">配置 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="db622-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="db622-104">本主题说明如何在预配后配置 Microsoft Dynamics 365 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="db622-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="db622-105">概览</span><span class="sxs-lookup"><span data-stu-id="db622-105">Overview</span></span>

<span data-ttu-id="db622-106">请仅在预配了 Commerce 预览环境之后，再完成本主题中的过程。</span><span class="sxs-lookup"><span data-stu-id="db622-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="db622-107">有关如何预配 Commerce 预览环境的信息，请参阅[预配 Commerce 预览环境](provisioning-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="db622-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="db622-108">端到端预配 Commerce 预览环境后，必须先完成其他预配后配置步骤，然后才能开始评估环境。</span><span class="sxs-lookup"><span data-stu-id="db622-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="db622-109">要完成这些步骤，您必须使用 Microsoft Dynamics Lifecycle Services (LCS)、Dynamics 365 Commerce 和 Dynamics 365 Retail。</span><span class="sxs-lookup"><span data-stu-id="db622-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="db622-110">开始之前</span><span class="sxs-lookup"><span data-stu-id="db622-110">Before you start</span></span>

1. <span data-ttu-id="db622-111">登录 [LCS 门户](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="db622-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="db622-112">转到您的项目。</span><span class="sxs-lookup"><span data-stu-id="db622-112">Go to your project.</span></span>
1. <span data-ttu-id="db622-113">在顶级菜单上，选择**云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="db622-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="db622-114">在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="db622-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="db622-115">在右侧的环境信息中，选择**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="db622-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="db622-116">选择**登录**打开菜单，然后选择**登录到环境**。</span><span class="sxs-lookup"><span data-stu-id="db622-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="db622-117">确保选择了右上角的 **USRT** 法人。</span><span class="sxs-lookup"><span data-stu-id="db622-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="db622-118">在 LCS 中配置销售点</span><span class="sxs-lookup"><span data-stu-id="db622-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="db622-119">将工作人员与您的标识关联</span><span class="sxs-lookup"><span data-stu-id="db622-119">Associate a worker with your identity</span></span>

<span data-ttu-id="db622-120">要在 LCS 中将工作人员与您的标识关联，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="db622-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="db622-121">使用左侧菜单转到**模块 \> Retail \> 员工 \> 工作人员**。</span><span class="sxs-lookup"><span data-stu-id="db622-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="db622-122">在列表中，找到并选择以下记录：**000713 - Andrew Collette**。</span><span class="sxs-lookup"><span data-stu-id="db622-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="db622-123">在操作窗格上，选择 **Retail**。</span><span class="sxs-lookup"><span data-stu-id="db622-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="db622-124">选择**关联现有标识**。</span><span class="sxs-lookup"><span data-stu-id="db622-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="db622-125">在（**使用电子邮件搜索**右侧的）**电子邮件**字段中，输入您的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="db622-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="db622-126">选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="db622-126">Select **Search**.</span></span>
1. <span data-ttu-id="db622-127">选择包含您的姓名的记录。</span><span class="sxs-lookup"><span data-stu-id="db622-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="db622-128">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="db622-128">Select **OK**.</span></span>
1. <span data-ttu-id="db622-129">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="db622-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="db622-130">激活 Cloud POS</span><span class="sxs-lookup"><span data-stu-id="db622-130">Activate Cloud POS</span></span>

<span data-ttu-id="db622-131">要在 LCS 中激活 Cloud POS，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="db622-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="db622-132">在顶级菜单上，选择**云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="db622-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="db622-133">在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="db622-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="db622-134">在右侧的环境信息中，选择**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="db622-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="db622-135">选择**登录**打开菜单，然后选择**登录到云销售点**打开销售点 (POS)。</span><span class="sxs-lookup"><span data-stu-id="db622-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="db622-136">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="db622-136">Select **Next**.</span></span>
1. <span data-ttu-id="db622-137">使用您的 Microsoft Azure Active Directory (Azure AD) 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="db622-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="db622-138">在**商店名称**下，选择**旧金山**。</span><span class="sxs-lookup"><span data-stu-id="db622-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="db622-139">选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="db622-139">Select **Next**.</span></span>
1. <span data-ttu-id="db622-140">在**收银机和设备**下，选择 **SANFRAN-1**。</span><span class="sxs-lookup"><span data-stu-id="db622-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="db622-141">选择**激活**。</span><span class="sxs-lookup"><span data-stu-id="db622-141">Select **Activate**.</span></span> <span data-ttu-id="db622-142">您已注销并进入 POS 登录页面。</span><span class="sxs-lookup"><span data-stu-id="db622-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="db622-143">现在可使用操作员 ID **000713** 和密码 **123** 登录到云 POS 体验。</span><span class="sxs-lookup"><span data-stu-id="db622-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="db622-144">在 Commerce 中设置站点</span><span class="sxs-lookup"><span data-stu-id="db622-144">Set up your site in Commerce</span></span>

<span data-ttu-id="db622-145">要开始在 Commerce 中设置预览站点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="db622-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="db622-146">使用您在预配期间初始化电子商务时记下的 URL 登录站点管理工具（请参阅[初始化电子商务](provisioning-guide.md#initialize-e-commerce)）。</span><span class="sxs-lookup"><span data-stu-id="db622-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="db622-147">选择 **Fabrikam** 站点打开站点设置对话框。</span><span class="sxs-lookup"><span data-stu-id="db622-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="db622-148">选择初始化电子商务时输入的域。</span><span class="sxs-lookup"><span data-stu-id="db622-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="db622-149">选择 **Fabrikam 扩展的在线商店**作为默认渠道。</span><span class="sxs-lookup"><span data-stu-id="db622-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="db622-150">（请务必选择**扩展的**在线商店。）</span><span class="sxs-lookup"><span data-stu-id="db622-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="db622-151">选择 **en-us** 作为默认语言。</span><span class="sxs-lookup"><span data-stu-id="db622-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="db622-152">保留**路径**的值不变。</span><span class="sxs-lookup"><span data-stu-id="db622-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="db622-153">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="db622-153">Select **OK**.</span></span> <span data-ttu-id="db622-154">将出现站点上的页面的列表。</span><span class="sxs-lookup"><span data-stu-id="db622-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="db622-155">在 Retail 中启用作业</span><span class="sxs-lookup"><span data-stu-id="db622-155">Enable jobs in Retail</span></span>

<span data-ttu-id="db622-156">要在 Retail 中启用作业，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="db622-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="db622-157">登录到环境（总部）。</span><span class="sxs-lookup"><span data-stu-id="db622-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="db622-158">使用左侧菜单转到 **Retail \> 查询和报表 \> 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="db622-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="db622-159">必须为以下每个作业完成此过程的其余步骤：</span><span class="sxs-lookup"><span data-stu-id="db622-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="db622-160">处理零售订单电子邮件通知</span><span class="sxs-lookup"><span data-stu-id="db622-160">Process retail order email notification</span></span>
    * <span data-ttu-id="db622-161">产品可用性</span><span class="sxs-lookup"><span data-stu-id="db622-161">Product availability</span></span>
    * <span data-ttu-id="db622-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="db622-162">P-0001</span></span>
    * <span data-ttu-id="db622-163">同步订单作业</span><span class="sxs-lookup"><span data-stu-id="db622-163">Synchronize orders job</span></span>

1. <span data-ttu-id="db622-164">使用快速筛选器按名称搜索作业。</span><span class="sxs-lookup"><span data-stu-id="db622-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="db622-165">如果作业的状态为**预扣**，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="db622-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="db622-166">选择记录。</span><span class="sxs-lookup"><span data-stu-id="db622-166">Select the record.</span></span>
    1. <span data-ttu-id="db622-167">在操作窗格上，在**批处理作业**选项卡上，选择**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="db622-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="db622-168">选择**等待**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="db622-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="db622-169">在 Retail 中运行完整的数据同步</span><span class="sxs-lookup"><span data-stu-id="db622-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="db622-170">要在 Retail 中运行完整的数据同步，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="db622-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="db622-171">使用左侧菜单转到**模块 \> Retail \> 总部设置 \> 零售调度 \> 渠道数据库**。</span><span class="sxs-lookup"><span data-stu-id="db622-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="db622-172">在左侧的列表中，已选择了**默认**渠道。</span><span class="sxs-lookup"><span data-stu-id="db622-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="db622-173">选择其他可用渠道。</span><span class="sxs-lookup"><span data-stu-id="db622-173">Select the other available channel.</span></span> <span data-ttu-id="db622-174">此渠道名为 **scXXXXXXXXX**。</span><span class="sxs-lookup"><span data-stu-id="db622-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="db622-175">在操作窗格中，选择**完全数据同步**。</span><span class="sxs-lookup"><span data-stu-id="db622-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="db622-176">输入 **9999** 作为配送计划。</span><span class="sxs-lookup"><span data-stu-id="db622-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="db622-177">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="db622-177">Select **OK**.</span></span>
1. <span data-ttu-id="db622-178">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="db622-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="db622-179">测试信用卡信息以执行测试性购买</span><span class="sxs-lookup"><span data-stu-id="db622-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="db622-180">若要在站点中执行测试交易，可使用以下测试信用卡信息：</span><span class="sxs-lookup"><span data-stu-id="db622-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="db622-181">**卡号：** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="db622-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="db622-182">**到期日期：** 10/20</span><span class="sxs-lookup"><span data-stu-id="db622-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="db622-183">**卡验证值 (CVV) 代码：** 737</span><span class="sxs-lookup"><span data-stu-id="db622-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db622-184">在任何情况下，都不要尝试在测试站点上使用实际的信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="db622-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="db622-185">后续步骤</span><span class="sxs-lookup"><span data-stu-id="db622-185">Next steps</span></span>

<span data-ttu-id="db622-186">在预配和配置步骤完成之后，您就可以评估预览环境了。</span><span class="sxs-lookup"><span data-stu-id="db622-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="db622-187">使用 Commerce 站点管理工具的 URL 可以转到创作体验。</span><span class="sxs-lookup"><span data-stu-id="db622-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="db622-188">使用 Commerce 站点的 URL 可以转到零售客户站点体验。</span><span class="sxs-lookup"><span data-stu-id="db622-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="db622-189">要为 Commerce 预览环境配置可选功能，请参阅[为 Commerce 预览环境配置可选功能](cpe-optional-features.md)。</span><span class="sxs-lookup"><span data-stu-id="db622-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db622-190">其他资源</span><span class="sxs-lookup"><span data-stu-id="db622-190">Additional resources</span></span>

[<span data-ttu-id="db622-191">Commerce 预览环境概述</span><span class="sxs-lookup"><span data-stu-id="db622-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="db622-192">预配 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="db622-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="db622-193">为 Commerce 预览环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="db622-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="db622-194">Commerce 预览环境常见问题</span><span class="sxs-lookup"><span data-stu-id="db622-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="db622-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="db622-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="db622-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="db622-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="db622-197">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="db622-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="db622-198">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="db622-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="db622-199">Dynamics 365 Retail 的帮助资源</span><span class="sxs-lookup"><span data-stu-id="db622-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
