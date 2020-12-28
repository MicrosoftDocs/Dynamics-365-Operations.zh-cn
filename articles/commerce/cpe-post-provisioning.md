---
title: 配置 Dynamics 365 Commerce 评估环境
description: 本主题说明如何在预配后配置 Microsoft Dynamics 365 Commerce 评估环境。
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410379"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="be826-103">配置 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="be826-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be826-104">本主题说明如何在预配后配置 Microsoft Dynamics 365 Commerce 评估环境。</span><span class="sxs-lookup"><span data-stu-id="be826-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="be826-105">概览</span><span class="sxs-lookup"><span data-stu-id="be826-105">Overview</span></span>

<span data-ttu-id="be826-106">请仅在预配了 Commerce 评估环境之后，再完成本主题中的过程。</span><span class="sxs-lookup"><span data-stu-id="be826-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="be826-107">有关如何预配 Commerce 评估环境的信息，请参阅[预配 Commerce 评估环境](provisioning-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="be826-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="be826-108">端到端预配 Commerce 评估环境后，必须先完成其他预配后配置步骤，然后才能开始评估环境。</span><span class="sxs-lookup"><span data-stu-id="be826-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="be826-109">要完成这些步骤，您必须使用 Microsoft Dynamics Lifecycle Services (LCS) 和 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="be826-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="be826-110">开始之前</span><span class="sxs-lookup"><span data-stu-id="be826-110">Before you start</span></span>

1. <span data-ttu-id="be826-111">登录 [LCS 门户](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="be826-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="be826-112">转到您的项目。</span><span class="sxs-lookup"><span data-stu-id="be826-112">Go to your project.</span></span>
1. <span data-ttu-id="be826-113">在顶级菜单上，选择 **云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="be826-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="be826-114">在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="be826-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="be826-115">在右侧的环境信息中，选择 **登录到环境**。</span><span class="sxs-lookup"><span data-stu-id="be826-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="be826-116">您将被送到 Commerce headquarters。</span><span class="sxs-lookup"><span data-stu-id="be826-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="be826-117">确保选择了右上角的 **USRT** 法人。</span><span class="sxs-lookup"><span data-stu-id="be826-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="be826-118">在 Commerce headquarters 进行预配后活动期间，请确保 **USRT** 法人始终处于选中状态。</span><span class="sxs-lookup"><span data-stu-id="be826-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="be826-119">配置销售点</span><span class="sxs-lookup"><span data-stu-id="be826-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="be826-120">将工作人员与您的标识关联</span><span class="sxs-lookup"><span data-stu-id="be826-120">Associate a worker with your identity</span></span>

<span data-ttu-id="be826-121">要将工作人员与您的标识关联，请在 Commerce headquarters 中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="be826-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="be826-122">使用左侧菜单转到 **模块 \> Retail 和 Commerce \> 员工 \> 工作人员**。</span><span class="sxs-lookup"><span data-stu-id="be826-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="be826-123">在列表中，找到并选择以下记录：**000713 - Andrew Collette**。</span><span class="sxs-lookup"><span data-stu-id="be826-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="be826-124">在“操作窗格”上，选择 **Commerce**。</span><span class="sxs-lookup"><span data-stu-id="be826-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="be826-125">选择 **关联现有标识**。</span><span class="sxs-lookup"><span data-stu-id="be826-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="be826-126">在（**使用电子邮件搜索** 右侧的）**电子邮件** 字段中，输入您的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="be826-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="be826-127">选择 **搜索**。</span><span class="sxs-lookup"><span data-stu-id="be826-127">Select **Search**.</span></span>
1. <span data-ttu-id="be826-128">选择包含您的姓名的记录。</span><span class="sxs-lookup"><span data-stu-id="be826-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="be826-129">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="be826-129">Select **OK**.</span></span>
1. <span data-ttu-id="be826-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="be826-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="be826-131">激活 Cloud POS</span><span class="sxs-lookup"><span data-stu-id="be826-131">Activate Cloud POS</span></span>

<span data-ttu-id="be826-132">要激活 Cloud POS，请在 LCS 中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="be826-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="be826-133">在顶级菜单上，选择 **云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="be826-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="be826-134">在列表中选择您的环境。</span><span class="sxs-lookup"><span data-stu-id="be826-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="be826-135">在右侧的环境信息中，选择 **登录到云销售点**。</span><span class="sxs-lookup"><span data-stu-id="be826-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="be826-136">选择 **下一步** 打开 **开始之前** 对话框。</span><span class="sxs-lookup"><span data-stu-id="be826-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="be826-137">保留 **服务器 URL** 字段不变。</span><span class="sxs-lookup"><span data-stu-id="be826-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="be826-138">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="be826-138">Select **Next**.</span></span>
1. <span data-ttu-id="be826-139">使用您的 Microsoft Azure Active Directory (Azure AD) 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="be826-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="be826-140">在 **商店名称** 下，选择 **旧金山**，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="be826-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="be826-141">在 **收银机和设备** 下，选择 **SANFRAN-1**。</span><span class="sxs-lookup"><span data-stu-id="be826-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="be826-142">选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="be826-142">Select **Activate**.</span></span> <span data-ttu-id="be826-143">您已注销并进入 POS 登录页面。</span><span class="sxs-lookup"><span data-stu-id="be826-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="be826-144">现在可使用操作员 ID **000713** 和密码 **123** 登录到云 POS 体验。</span><span class="sxs-lookup"><span data-stu-id="be826-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="be826-145">在 Commerce 中设置站点</span><span class="sxs-lookup"><span data-stu-id="be826-145">Set up your site in Commerce</span></span>

<span data-ttu-id="be826-146">要开始在 Commerce 中设置评估站点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="be826-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="be826-147">使用您在预配期间初始化电子商务时记下的 URL 登录站点构建器（请参阅[初始化电子商务](provisioning-guide.md#initialize-e-commerce)）。</span><span class="sxs-lookup"><span data-stu-id="be826-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="be826-148">选择 **Fabrikam** 站点打开站点设置对话框。</span><span class="sxs-lookup"><span data-stu-id="be826-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="be826-149">选择初始化电子商务时输入的域。</span><span class="sxs-lookup"><span data-stu-id="be826-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="be826-150">选择 **Fabrikam 扩展的在线商店** 作为默认渠道。</span><span class="sxs-lookup"><span data-stu-id="be826-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="be826-151">（请务必选择 **扩展的** 在线商店。）</span><span class="sxs-lookup"><span data-stu-id="be826-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="be826-152">选择 **en-us** 作为默认语言。</span><span class="sxs-lookup"><span data-stu-id="be826-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="be826-153">保留 **路径** 的值不变。</span><span class="sxs-lookup"><span data-stu-id="be826-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="be826-154">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="be826-154">Select **OK**.</span></span> <span data-ttu-id="be826-155">将出现站点上的页面的列表。</span><span class="sxs-lookup"><span data-stu-id="be826-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="be826-156">启用作业</span><span class="sxs-lookup"><span data-stu-id="be826-156">Enable jobs</span></span>

<span data-ttu-id="be826-157">要在 Commerce 中启用作业，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="be826-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="be826-158">登录到环境（总部）。</span><span class="sxs-lookup"><span data-stu-id="be826-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="be826-159">使用左侧菜单转到 **Retail 和 Commerce \> 查询和报表 \> 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="be826-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="be826-160">必须为以下每个作业完成此过程的其余步骤：</span><span class="sxs-lookup"><span data-stu-id="be826-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="be826-161">处理零售订单电子邮件通知</span><span class="sxs-lookup"><span data-stu-id="be826-161">Process retail order email notification</span></span>
    * <span data-ttu-id="be826-162">产品可用性</span><span class="sxs-lookup"><span data-stu-id="be826-162">Product availability</span></span>
    * <span data-ttu-id="be826-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="be826-163">P-0001</span></span>
    * <span data-ttu-id="be826-164">同步订单作业</span><span class="sxs-lookup"><span data-stu-id="be826-164">Synchronize orders job</span></span>

1. <span data-ttu-id="be826-165">使用快速筛选器按名称搜索作业。</span><span class="sxs-lookup"><span data-stu-id="be826-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="be826-166">如果作业的状态为 **正在执行**，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="be826-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="be826-167">选择记录。</span><span class="sxs-lookup"><span data-stu-id="be826-167">Select the record.</span></span>
    1. <span data-ttu-id="be826-168">在操作窗格上，在 **批处理作业** 选项卡上，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="be826-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="be826-169">选择 **取消**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="be826-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="be826-170">（可选）您还可以将以下作业的重复执行间隔设置为一 (1) 分钟：</span><span class="sxs-lookup"><span data-stu-id="be826-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="be826-171">处理零售订单电子邮件通知作业</span><span class="sxs-lookup"><span data-stu-id="be826-171">Process retail order email notification job</span></span>
* <span data-ttu-id="be826-172">P-0001 作业</span><span class="sxs-lookup"><span data-stu-id="be826-172">P-0001 job</span></span>
* <span data-ttu-id="be826-173">同步订单作业</span><span class="sxs-lookup"><span data-stu-id="be826-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="be826-174">运行完全数据同步</span><span class="sxs-lookup"><span data-stu-id="be826-174">Run full data synchronization</span></span>

<span data-ttu-id="be826-175">要在 Commerce 中运行完整的数据同步，请在 Commerce headquarters 中按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="be826-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="be826-176">使用左侧菜单转到 **模块 \> Retail 和 Commerce \> 总部设置 \> 商业调度程序 \> 渠道数据库**。</span><span class="sxs-lookup"><span data-stu-id="be826-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="be826-177">选择名为 **scXXXXXXXXX** 的渠道。</span><span class="sxs-lookup"><span data-stu-id="be826-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="be826-178">在操作窗格中，选择 **完全数据同步**。</span><span class="sxs-lookup"><span data-stu-id="be826-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="be826-179">输入 **9999** 作为配送计划。</span><span class="sxs-lookup"><span data-stu-id="be826-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="be826-180">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="be826-180">Select **OK**.</span></span>
1. <span data-ttu-id="be826-181">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="be826-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="be826-182">测试信用卡信息以执行测试性购买</span><span class="sxs-lookup"><span data-stu-id="be826-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="be826-183">若要在站点中执行测试交易，可使用以下测试信用卡信息：</span><span class="sxs-lookup"><span data-stu-id="be826-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="be826-184">**卡号：** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="be826-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="be826-185">**到期日期：** 10/20</span><span class="sxs-lookup"><span data-stu-id="be826-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="be826-186">**卡验证值 (CVV) 代码：** 737</span><span class="sxs-lookup"><span data-stu-id="be826-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be826-187">在任何情况下，都不要尝试在测试站点上使用实际的信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="be826-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="be826-188">后续步骤</span><span class="sxs-lookup"><span data-stu-id="be826-188">Next steps</span></span>

<span data-ttu-id="be826-189">在预配和配置步骤完成之后，您就可以开始使用评估环境了。</span><span class="sxs-lookup"><span data-stu-id="be826-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="be826-190">使用 Commerce 站点构建器 URL 可以转到创作体验。</span><span class="sxs-lookup"><span data-stu-id="be826-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="be826-191">使用 Commerce 站点 URL 可以转到零售客户站点体验。</span><span class="sxs-lookup"><span data-stu-id="be826-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="be826-192">要为 Commerce 评估环境配置可选功能，请参阅[为 Commerce 评估环境配置可选功能](cpe-optional-features.md)。</span><span class="sxs-lookup"><span data-stu-id="be826-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be826-193">其他资源</span><span class="sxs-lookup"><span data-stu-id="be826-193">Additional resources</span></span>

[<span data-ttu-id="be826-194">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="be826-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="be826-195">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="be826-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="be826-196">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="be826-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="be826-197">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="be826-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="be826-198">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="be826-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="be826-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="be826-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="be826-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="be826-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="be826-201">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="be826-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="be826-202">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="be826-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
