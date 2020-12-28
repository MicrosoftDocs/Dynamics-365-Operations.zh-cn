---
title: 从 Attract 和 Onboard 中导出数据
description: 从 Dynamics 365 Talent Attract 和 Onboard 中导出数据。
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460393"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="d4c56-103">从 Attract 和 Onboard 中导出数据</span><span class="sxs-lookup"><span data-stu-id="d4c56-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4c56-104">正如[停用 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard 应用](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)中宣布的那样，我们将在 2022 年 2 月 1 日停用 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard。</span><span class="sxs-lookup"><span data-stu-id="d4c56-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="d4c56-105">为了帮助您迁移到另一产品，这两款应用现在都提供了数据导出功能。</span><span class="sxs-lookup"><span data-stu-id="d4c56-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="d4c56-106">从 Attract 中导出数据</span><span class="sxs-lookup"><span data-stu-id="d4c56-106">Export data from Attract</span></span>

<span data-ttu-id="d4c56-107">您可以在环境访问权限不受限制的情况下导出数据。</span><span class="sxs-lookup"><span data-stu-id="d4c56-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="d4c56-108">出于测试目的或者是为了了解我们的数据结构，您可能需要执行此操作。</span><span class="sxs-lookup"><span data-stu-id="d4c56-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="d4c56-109">准备迁移时，请按照此过程之后的说明限制 Attract 环境的访问权限。</span><span class="sxs-lookup"><span data-stu-id="d4c56-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="d4c56-110">确保再次导出数据。</span><span class="sxs-lookup"><span data-stu-id="d4c56-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="d4c56-111">转到 [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport)。</span><span class="sxs-lookup"><span data-stu-id="d4c56-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="d4c56-112">在 **数据导出** 下面，选择 **请求数据导出**。</span><span class="sxs-lookup"><span data-stu-id="d4c56-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="d4c56-113">请求从 Attract 中导出数据</span><span class="sxs-lookup"><span data-stu-id="d4c56-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="d4c56-114">当出现 **正在处理您的请求** 消息框时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d4c56-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="d4c56-115">数据导出最多可能需要 20 分钟，具体取决于导出的大小。</span><span class="sxs-lookup"><span data-stu-id="d4c56-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="d4c56-116">导出完成后，选择旁边的 **下载** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d4c56-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="d4c56-117">所有数据导出都可以使用 7 天，到时 **下载** 链接会过期。</span><span class="sxs-lookup"><span data-stu-id="d4c56-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="d4c56-118">下载内容包含带有 Attract 数据的 .zip 文件，其中包括以下文件夹：</span><span class="sxs-lookup"><span data-stu-id="d4c56-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="d4c56-119">文件夹名称</span><span class="sxs-lookup"><span data-stu-id="d4c56-119">Folder name</span></span> | <span data-ttu-id="d4c56-120">说明</span><span class="sxs-lookup"><span data-stu-id="d4c56-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d4c56-121">管理员设置</span><span class="sxs-lookup"><span data-stu-id="d4c56-121">Admin settings</span></span> | <span data-ttu-id="d4c56-122">Attract 管理中心配置。</span><span class="sxs-lookup"><span data-stu-id="d4c56-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="d4c56-123">应聘者</span><span class="sxs-lookup"><span data-stu-id="d4c56-123">Candidates</span></span> | <span data-ttu-id="d4c56-124">已添加到工作或人才库的所有应聘者。</span><span class="sxs-lookup"><span data-stu-id="d4c56-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="d4c56-125">电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="d4c56-125">Email templates</span></span> | <span data-ttu-id="d4c56-126">为环境配置的所有电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="d4c56-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="d4c56-127">职位聘约包模板</span><span class="sxs-lookup"><span data-stu-id="d4c56-127">Job offer package templates</span></span> | <span data-ttu-id="d4c56-128">已创建的所有职位聘约包模板及其关联的配置。</span><span class="sxs-lookup"><span data-stu-id="d4c56-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="d4c56-129">职位聘约规则集</span><span class="sxs-lookup"><span data-stu-id="d4c56-129">Job offer rule sets</span></span> |  <span data-ttu-id="d4c56-130">为管理聘约而上载的所有规则集文件。</span><span class="sxs-lookup"><span data-stu-id="d4c56-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="d4c56-131">职位聘约模板</span><span class="sxs-lookup"><span data-stu-id="d4c56-131">Job offer templates</span></span> | <span data-ttu-id="d4c56-132">为环境创建的所有职位聘约文档模板。</span><span class="sxs-lookup"><span data-stu-id="d4c56-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="d4c56-133">空缺职位</span><span class="sxs-lookup"><span data-stu-id="d4c56-133">Job openings</span></span> | <span data-ttu-id="d4c56-134">所有创建的职位</span><span class="sxs-lookup"><span data-stu-id="d4c56-134">All created jobs.</span></span> <span data-ttu-id="d4c56-135">已删除的职位不会导出。</span><span class="sxs-lookup"><span data-stu-id="d4c56-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="d4c56-136">子文件夹包含应聘者申请，以及应聘者申请附件和聘约包的子文件夹（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d4c56-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="d4c56-137">空缺职位模板</span><span class="sxs-lookup"><span data-stu-id="d4c56-137">Job opening templates</span></span> | <span data-ttu-id="d4c56-138">在环境中配置的工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d4c56-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="d4c56-139">人才池</span><span class="sxs-lookup"><span data-stu-id="d4c56-139">Talent pools</span></span> | <span data-ttu-id="d4c56-140">所有已创建的人才池，其要素列表以及人才池的候选人列表。</span><span class="sxs-lookup"><span data-stu-id="d4c56-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="d4c56-141">工作人员</span><span class="sxs-lookup"><span data-stu-id="d4c56-141">Workers</span></span> | <span data-ttu-id="d4c56-142">环境中存在的所有工作人员及其角色的列表。</span><span class="sxs-lookup"><span data-stu-id="d4c56-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="d4c56-143">（根文件夹）</span><span class="sxs-lookup"><span data-stu-id="d4c56-143">(root folder)</span></span> | <span data-ttu-id="d4c56-144">一个描述数据结构字段的 JSON 架构文件。</span><span class="sxs-lookup"><span data-stu-id="d4c56-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="d4c56-145">限制访问 Attract</span><span class="sxs-lookup"><span data-stu-id="d4c56-145">Restrict access to Attract</span></span>

<span data-ttu-id="d4c56-146">当您准备好迁移时，请限制非管理员访问您的 Attract 环境并导出数据。</span><span class="sxs-lookup"><span data-stu-id="d4c56-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="d4c56-147">限制访问 Attract 是永久性限制，不能撤消。</span><span class="sxs-lookup"><span data-stu-id="d4c56-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="d4c56-148">如果希望非管理员用户继续访问您的环境，请跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="d4c56-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="d4c56-149">转到 [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport)。</span><span class="sxs-lookup"><span data-stu-id="d4c56-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="d4c56-150">要限制非管理员访问您的 Attract 环境，请在 **限制访问此应用** 下面选择 **立即限制访问**。</span><span class="sxs-lookup"><span data-stu-id="d4c56-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="d4c56-151">限制访问还会取消发布任何已发布的有效职位。</span><span class="sxs-lookup"><span data-stu-id="d4c56-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="d4c56-152">限制非管理员访问 Attract</span><span class="sxs-lookup"><span data-stu-id="d4c56-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="d4c56-153">当您看到 **这是永久性更改** 警告时，选择 **限制访问** 以永久限制非管理员用户进入此环境。</span><span class="sxs-lookup"><span data-stu-id="d4c56-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="d4c56-154">如果您尚未准备好完成此步骤，请选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="d4c56-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="d4c56-155">警告限制访问是永久性更改</span><span class="sxs-lookup"><span data-stu-id="d4c56-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="d4c56-156">在您限制访问 Attract 环境后，管理员可以继续访问数据导出和人员报告页面。</span><span class="sxs-lookup"><span data-stu-id="d4c56-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="d4c56-157">从 Onboard 中导出数据</span><span class="sxs-lookup"><span data-stu-id="d4c56-157">Export data from Onboard</span></span>

<span data-ttu-id="d4c56-158">准备就绪后，您可以从 Onboard 中下载模板、指南和应聘者数据。</span><span class="sxs-lookup"><span data-stu-id="d4c56-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="d4c56-159">转到 [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport)。</span><span class="sxs-lookup"><span data-stu-id="d4c56-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="d4c56-160">在 **数据导出** 下面，选择 **请求数据导出**。</span><span class="sxs-lookup"><span data-stu-id="d4c56-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="d4c56-161">请求从 Onboard 中导出数据</span><span class="sxs-lookup"><span data-stu-id="d4c56-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="d4c56-162">当出现 **正在处理您的请求** 消息框时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d4c56-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="d4c56-163">数据导出最多可能需要 20 分钟，具体取决于导出的大小。</span><span class="sxs-lookup"><span data-stu-id="d4c56-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="d4c56-164">导出完成后，选择旁边的 **下载** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d4c56-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="d4c56-165">从 Onboard 中下载导出数据</span><span class="sxs-lookup"><span data-stu-id="d4c56-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="d4c56-166">您的数据导出可以使用 7 天。</span><span class="sxs-lookup"><span data-stu-id="d4c56-166">Your data export is available for seven days.</span></span> <span data-ttu-id="d4c56-167">七天后，**下载** 链接过期，如果您需要再次下载数据，则必须请求新的导出。</span><span class="sxs-lookup"><span data-stu-id="d4c56-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="d4c56-168">当您开始新的数据导出时，新导出成功后，所有现有下载都将过期。</span><span class="sxs-lookup"><span data-stu-id="d4c56-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="d4c56-169">下载是一个 .zip 文件，其中包含：</span><span class="sxs-lookup"><span data-stu-id="d4c56-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="d4c56-170">一个 **Templates** 文件夹，其中包含 Word 文档格式的 Onboard 模板。</span><span class="sxs-lookup"><span data-stu-id="d4c56-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="d4c56-171">一个 **Guides** 文件夹，其中包含 Word 文档格式的 Onboard 指南。</span><span class="sxs-lookup"><span data-stu-id="d4c56-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4c56-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="d4c56-172">See also</span></span>

[<span data-ttu-id="d4c56-173">停用 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard 应用</span><span class="sxs-lookup"><span data-stu-id="d4c56-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)