---
title: 通过 Attract 将工作发布到外部求职站点
description: 本主题介绍如何使用 Dynamics 365 for Talent - Attract 将工作发布到外部招聘站点。
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590474"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="1ab2a-103">通过 Attract 将工作发布到外部求职站点</span><span class="sxs-lookup"><span data-stu-id="1ab2a-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ab2a-104">您可能希望尽可能多的合格应聘者可以看到您的开放职位。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="1ab2a-105">Broadbean 之类招聘站点可以帮助您达成这个目标。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="1ab2a-106">Microsoft Dynamics 365 Talent: Attract 现在允许您将工作发布到 Broadbean，而 Microsoft 将继续提供此领域中的新功能。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="1ab2a-107">将工作发布到 Broadbean</span><span class="sxs-lookup"><span data-stu-id="1ab2a-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="1ab2a-108">必须先配置 Broadbean 集成，才能将工作发布到 Broadbean。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="1ab2a-109">若要将工作发布到外部站点，必须安装[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="1ab2a-110">要通过 Attract 向 Broadbean 发布工作，必须订阅 Broadbean。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="1ab2a-111">此功能现在处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-111">This feature is currently in preview.</span></span> <span data-ttu-id="1ab2a-112">如果要尝试，必须[在 Attract 管理员设置中开启](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="1ab2a-113">配置 Broadbean 集成</span><span class="sxs-lookup"><span data-stu-id="1ab2a-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="1ab2a-114">以管理员身份登录 Attract。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="1ab2a-115">选择页面右上角的**设置**按钮（齿轮符号），然后选择**管理员中心**。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="1ab2a-116">在**招聘公告设置**选项卡的**启用 Broadbean 集成**部分中，开启集成。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="1ab2a-117">联系 Broadbean，然后在**用户名、客户端 ID 和加密令牌**中输入您的信息。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="1ab2a-118">您的 Broadbean 凭证是敏感的机密信息。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="1ab2a-119">因此，请妥善保存和共享。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="1ab2a-120">Attract 中的所有拥有管理员角色的人员都可以查看这些凭证。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="1ab2a-121">Microsoft 和 Attract 不会参与这些值的创建和维护。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="1ab2a-122">您负责使其在 Attract 中保持最新并与 Broadbean 合作解决涉及您的配置的所有问题。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="1ab2a-123">将工作发布到 Broadbean</span><span class="sxs-lookup"><span data-stu-id="1ab2a-123">Post a job to Broadbean</span></span>

<span data-ttu-id="1ab2a-124">开启 Broadbean 之后，招聘人员和管理员可以向其发布工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="1ab2a-125">您必须有该工作的申请 URL。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="1ab2a-126">在 Attract 中，打开要发布到 Broadbean 的工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="1ab2a-127">在**发布**部分中，选择与 Broadbean 对应的**立即发布**按钮。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="1ab2a-128">按照 Broadbean 窗口中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="1ab2a-129">Attract 将把以下信息传递到 Broadbean：</span><span class="sxs-lookup"><span data-stu-id="1ab2a-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="1ab2a-130">请求 ID</span><span class="sxs-lookup"><span data-stu-id="1ab2a-130">Request ID</span></span>
- <span data-ttu-id="1ab2a-131">职位</span><span class="sxs-lookup"><span data-stu-id="1ab2a-131">Job title</span></span>
- <span data-ttu-id="1ab2a-132">工作描述</span><span class="sxs-lookup"><span data-stu-id="1ab2a-132">Job description</span></span>
- <span data-ttu-id="1ab2a-133">工作地点</span><span class="sxs-lookup"><span data-stu-id="1ab2a-133">Job location</span></span>
- <span data-ttu-id="1ab2a-134">申请 URL</span><span class="sxs-lookup"><span data-stu-id="1ab2a-134">Apply URL</span></span>
- <span data-ttu-id="1ab2a-135">招聘人员信息</span><span class="sxs-lookup"><span data-stu-id="1ab2a-135">Recruiter information</span></span>

<span data-ttu-id="1ab2a-136">Broadbean 成功完成发布之后，Attract 中工作的**发布**部分将把 Broadbean 状态显示为**已发布**。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="1ab2a-137">Broadbean 需要**行业**字段。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="1ab2a-138">目前，此字段默认设置为 **IT**。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="1ab2a-139">但是，您可以在 Broadbean 作业发布的窗口中将该值更改为正确的行业。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="1ab2a-140">Broadbean 需要一些时间才能将您的工作发布到您选择所有招聘公告中。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="1ab2a-141">因此，可能在稍微延迟后 Attract 才会提供工作的状态更新。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="1ab2a-142">查看 Broadbean 工作发布</span><span class="sxs-lookup"><span data-stu-id="1ab2a-142">View a Broadbean job posting</span></span>

<span data-ttu-id="1ab2a-143">将工作发布到 Broadbean 会话，可以通过 Attract 查看。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="1ab2a-144">在 Attract 中，打开要在 Broadbean 中查看的工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="1ab2a-145">在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**查看**。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="1ab2a-146">将在新窗口中显示 Broadbean 工作发布。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="1ab2a-147">更新 Broadbean 工作发布</span><span class="sxs-lookup"><span data-stu-id="1ab2a-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="1ab2a-148">可以通过两种方法更新 Broadbean 工作发布。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="1ab2a-149">在 Attract 中，打开要更新的工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="1ab2a-150">在**发布**部分中，选择与 Broadbean 对应的**更新发布**按钮。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="1ab2a-151">在 Broadbean 窗口中编辑发布。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="1ab2a-152">–或者–</span><span class="sxs-lookup"><span data-stu-id="1ab2a-152">–or–</span></span>

1. <span data-ttu-id="1ab2a-153">在 Attract 中，打开要在 Broadbean 中查看的工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="1ab2a-154">在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**查看**。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="1ab2a-155">在 Broadbean 窗口中，编辑工作详细信息，然后重新发布工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="1ab2a-156">将不更改 Attract 中的工作详细信息。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="1ab2a-157">删除 Broadbean 工作发布</span><span class="sxs-lookup"><span data-stu-id="1ab2a-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="1ab2a-158">可以根据需要删除 Broadbean 中的工作发布。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="1ab2a-159">在 Attract 中，打开要删除的工作。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="1ab2a-160">在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**删除发布**。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="1ab2a-161">Broadbean 删除工作之后，Attract 中的 Broadbean 项将带有**立即发布**按钮。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="1ab2a-162">存在此按钮说明工作已删除，可以重新发布。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="1ab2a-163">Broadbean 集成故障排除</span><span class="sxs-lookup"><span data-stu-id="1ab2a-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="1ab2a-164">如果将工作发布到 Broadbean 时遇到问题，请尝试以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="1ab2a-165">验证在 Attract 中输入的 Broadbean 配置是否有效且正确。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="1ab2a-166">如果这些凭证有效且正确，请联系 [Broadbean 支持](https://www.broadbean.com/resources/support/)。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="1ab2a-167">如果问题仍然存在，请联系 [Microsoft 支持](./talent-support.md)。</span><span class="sxs-lookup"><span data-stu-id="1ab2a-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
