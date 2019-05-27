---
title: 通过 Attract 将工作发布到外部求职站点
description: 本主题介绍如何使用 Dynamics 365 for Talent - Attract 将工作发布到外部招聘站点。
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517435"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="37297-103">通过 Attract 将工作发布到外部求职站点</span><span class="sxs-lookup"><span data-stu-id="37297-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37297-104">您可能希望尽可能多的合格应聘者可以看到您的开放职位。</span><span class="sxs-lookup"><span data-stu-id="37297-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="37297-105">Broadbean 之类招聘站点可以帮助您达成这个目标。</span><span class="sxs-lookup"><span data-stu-id="37297-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="37297-106">Microsoft Dynamics 365 Talent: Attract 现在允许您将工作发布到 Broadbean，而 Microsoft 将继续提供此领域中的新功能。</span><span class="sxs-lookup"><span data-stu-id="37297-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="37297-107">将工作发布到 Broadbean</span><span class="sxs-lookup"><span data-stu-id="37297-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="37297-108">必须先配置 Broadbean 集成，才能将工作发布到 Broadbean。</span><span class="sxs-lookup"><span data-stu-id="37297-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="37297-109">若要将工作发布到外部站点，必须安装[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)。</span><span class="sxs-lookup"><span data-stu-id="37297-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="37297-110">此功能现在处于预览阶段。</span><span class="sxs-lookup"><span data-stu-id="37297-110">This feature is currently in preview.</span></span> <span data-ttu-id="37297-111">如果要尝试，必须[在 Attract 管理员设置中开启](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)。</span><span class="sxs-lookup"><span data-stu-id="37297-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="37297-112">配置 Broadbean 集成</span><span class="sxs-lookup"><span data-stu-id="37297-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="37297-113">以管理员身份登录 Attract。</span><span class="sxs-lookup"><span data-stu-id="37297-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="37297-114">选择页面右上角的**设置**按钮（齿轮符号），然后选择**管理员中心**。</span><span class="sxs-lookup"><span data-stu-id="37297-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="37297-115">在**招聘公告设置**选项卡的**启用 Broadbean 集成**部分中，开启集成。</span><span class="sxs-lookup"><span data-stu-id="37297-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="37297-116">联系 Broadbean，然后在**用户名、客户端 ID 和加密令牌**中输入您的信息。</span><span class="sxs-lookup"><span data-stu-id="37297-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="37297-117">您的 Broadbean 凭证是敏感的机密信息。</span><span class="sxs-lookup"><span data-stu-id="37297-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="37297-118">因此，请妥善保存和共享。</span><span class="sxs-lookup"><span data-stu-id="37297-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="37297-119">Attract 中的所有拥有管理员角色的人员都可以查看这些凭证。</span><span class="sxs-lookup"><span data-stu-id="37297-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="37297-120">Microsoft 和 Attract 不会参与这些值的创建和维护。</span><span class="sxs-lookup"><span data-stu-id="37297-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="37297-121">您负责使其在 Attract 中保持最新并与 Broadbean 合作解决涉及您的配置的所有问题。</span><span class="sxs-lookup"><span data-stu-id="37297-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="37297-122">将工作发布到 Broadbean</span><span class="sxs-lookup"><span data-stu-id="37297-122">Post a job to Broadbean</span></span>

<span data-ttu-id="37297-123">开启 Broadbean 之后，招聘人员和管理员可以向其发布工作。</span><span class="sxs-lookup"><span data-stu-id="37297-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="37297-124">您必须有该工作的申请 URL。</span><span class="sxs-lookup"><span data-stu-id="37297-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="37297-125">在 Attract 中，打开要发布到 Broadbean 的工作。</span><span class="sxs-lookup"><span data-stu-id="37297-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="37297-126">在**发布**部分中，选择与 Broadbean 对应的**立即发布**按钮。</span><span class="sxs-lookup"><span data-stu-id="37297-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="37297-127">按照 Broadbean 窗口中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="37297-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="37297-128">Attract 将把以下信息传递到 Broadbean：</span><span class="sxs-lookup"><span data-stu-id="37297-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="37297-129">请求 ID</span><span class="sxs-lookup"><span data-stu-id="37297-129">Request ID</span></span>
- <span data-ttu-id="37297-130">职位</span><span class="sxs-lookup"><span data-stu-id="37297-130">Job title</span></span>
- <span data-ttu-id="37297-131">工作描述</span><span class="sxs-lookup"><span data-stu-id="37297-131">Job description</span></span>
- <span data-ttu-id="37297-132">工作地点</span><span class="sxs-lookup"><span data-stu-id="37297-132">Job location</span></span>
- <span data-ttu-id="37297-133">申请 URL</span><span class="sxs-lookup"><span data-stu-id="37297-133">Apply URL</span></span>
- <span data-ttu-id="37297-134">招聘人员信息</span><span class="sxs-lookup"><span data-stu-id="37297-134">Recruiter information</span></span>

<span data-ttu-id="37297-135">Broadbean 成功完成发布之后，Attract 中工作的**发布**部分将把 Broadbean 状态显示为**已发布**。</span><span class="sxs-lookup"><span data-stu-id="37297-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="37297-136">Broadbean 需要**行业**字段。</span><span class="sxs-lookup"><span data-stu-id="37297-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="37297-137">目前，此字段默认设置为 **IT**。</span><span class="sxs-lookup"><span data-stu-id="37297-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="37297-138">但是，您可以在 Broadbean 作业发布的窗口中将该值更改为正确的行业。</span><span class="sxs-lookup"><span data-stu-id="37297-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="37297-139">Broadbean 需要一些时间才能将您的工作发布到您选择所有招聘公告中。</span><span class="sxs-lookup"><span data-stu-id="37297-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="37297-140">因此，可能在稍微延迟后 Attract 才会提供工作的状态更新。</span><span class="sxs-lookup"><span data-stu-id="37297-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="37297-141">查看 Broadbean 工作发布</span><span class="sxs-lookup"><span data-stu-id="37297-141">View a Broadbean job posting</span></span>

<span data-ttu-id="37297-142">将工作发布到 Broadbean 会话，可以通过 Attract 查看。</span><span class="sxs-lookup"><span data-stu-id="37297-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="37297-143">在 Attract 中，打开要在 Broadbean 中查看的工作。</span><span class="sxs-lookup"><span data-stu-id="37297-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="37297-144">在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**查看**。</span><span class="sxs-lookup"><span data-stu-id="37297-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="37297-145">将在新窗口中显示 Broadbean 工作发布。</span><span class="sxs-lookup"><span data-stu-id="37297-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="37297-146">更新 Broadbean 工作发布</span><span class="sxs-lookup"><span data-stu-id="37297-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="37297-147">可以通过两种方法更新 Broadbean 工作发布。</span><span class="sxs-lookup"><span data-stu-id="37297-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="37297-148">在 Attract 中，打开要更新的工作。</span><span class="sxs-lookup"><span data-stu-id="37297-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="37297-149">在**发布**部分中，选择与 Broadbean 对应的**更新发布**按钮。</span><span class="sxs-lookup"><span data-stu-id="37297-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="37297-150">在 Broadbean 窗口中编辑发布。</span><span class="sxs-lookup"><span data-stu-id="37297-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="37297-151">–或者–</span><span class="sxs-lookup"><span data-stu-id="37297-151">–or–</span></span>

1. <span data-ttu-id="37297-152">在 Attract 中，打开要在 Broadbean 中查看的工作。</span><span class="sxs-lookup"><span data-stu-id="37297-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="37297-153">在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**查看**。</span><span class="sxs-lookup"><span data-stu-id="37297-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="37297-154">在 Broadbean 窗口中，编辑工作详细信息，然后重新发布工作。</span><span class="sxs-lookup"><span data-stu-id="37297-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="37297-155">将不更改 Attract 中的工作详细信息。</span><span class="sxs-lookup"><span data-stu-id="37297-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="37297-156">删除 Broadbean 工作发布</span><span class="sxs-lookup"><span data-stu-id="37297-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="37297-157">可以根据需要删除 Broadbean 中的工作发布。</span><span class="sxs-lookup"><span data-stu-id="37297-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="37297-158">在 Attract 中，打开要删除的工作。</span><span class="sxs-lookup"><span data-stu-id="37297-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="37297-159">在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**删除发布**。</span><span class="sxs-lookup"><span data-stu-id="37297-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="37297-160">Broadbean 删除工作之后，Attract 中的 Broadbean 项将带有**立即发布**按钮。</span><span class="sxs-lookup"><span data-stu-id="37297-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="37297-161">存在此按钮说明工作已删除，可以重新发布。</span><span class="sxs-lookup"><span data-stu-id="37297-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="37297-162">Broadbean 集成故障排除</span><span class="sxs-lookup"><span data-stu-id="37297-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="37297-163">如果将工作发布到 Broadbean 时遇到问题，请尝试以下步骤。</span><span class="sxs-lookup"><span data-stu-id="37297-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="37297-164">验证在 Attract 中输入的 Broadbean 配置是否有效且正确。</span><span class="sxs-lookup"><span data-stu-id="37297-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="37297-165">如果这些凭证有效且正确，请联系 [Broadbean 支持](https://www.broadbean.com/resources/support/)。</span><span class="sxs-lookup"><span data-stu-id="37297-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="37297-166">如果问题仍然存在，请联系 [Microsoft 支持](./talent-support.md)。</span><span class="sxs-lookup"><span data-stu-id="37297-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
