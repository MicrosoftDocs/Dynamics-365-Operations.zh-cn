---
title: 导入更新后的 ER 配置版本
description: 本主题说明如何从 Configuration service 的全局存储库导入更新后的电子申报 (ER) 配置版本。
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 724048991fc8864ef72a5155af66b9c709f4b875
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893948"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="58428-103">导入更新后的 ER 配置版本</span><span class="sxs-lookup"><span data-stu-id="58428-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58428-104">电子申报 (ER) [存储库](general-electronic-reporting.md#Repository)用于共享 [ER 配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="58428-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="58428-105">可以将不同存储库中的 ER 配置[导入](download-electronic-reporting-configuration-lcs.md)到您的 Microsoft Dynamics 365 Finance 实例中。</span><span class="sxs-lookup"><span data-stu-id="58428-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="58428-106">导入 ER 配置时，[配置提供程序](general-electronic-reporting.md#Provider)可以发布新[版本](general-electronic-reporting.md#component-versioning)存储库，以使其可共享。</span><span class="sxs-lookup"><span data-stu-id="58428-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="58428-107">本主题说明如何从 Configuration service 的全局存储库导入更新后的 ER 配置版本。</span><span class="sxs-lookup"><span data-stu-id="58428-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="58428-108">有关详细信息，请参阅 [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services、Configuration service](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)。</span><span class="sxs-lookup"><span data-stu-id="58428-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="58428-109">检查可用的更新后版本</span><span class="sxs-lookup"><span data-stu-id="58428-109">Review the available updated versions</span></span>

1. <span data-ttu-id="58428-110">通过使用以下角色之一登录到 Finance：</span><span class="sxs-lookup"><span data-stu-id="58428-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="58428-111">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="58428-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="58428-112">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="58428-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="58428-113">系统管理员</span><span class="sxs-lookup"><span data-stu-id="58428-113">System administrator</span></span>

2. <span data-ttu-id="58428-114">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="58428-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="58428-115">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **导入配置版本更新**。</span><span class="sxs-lookup"><span data-stu-id="58428-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![本地化配置页面](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="58428-117">在 **导入电子申报配置版本更新** 对话框的 **运行模式** 字段中，选择 **仅显示可用更新**。</span><span class="sxs-lookup"><span data-stu-id="58428-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="58428-118">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="58428-118">Then select **OK**.</span></span> 

    ![“运行模式”字段设置为“仅显示可用更新”](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="58428-120">查看收到的消息。</span><span class="sxs-lookup"><span data-stu-id="58428-120">Review the messages that you receive.</span></span> <span data-ttu-id="58428-121">这些消息提供有关当前 Finance 实例中的 ER 配置和有关其与全球存储库内容的比较的以下信息：</span><span class="sxs-lookup"><span data-stu-id="58428-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="58428-122">ER 配置总数</span><span class="sxs-lookup"><span data-stu-id="58428-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="58428-123">全球存储库中不存在的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="58428-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="58428-124">当前 Finance 实例中已有其最新版本的 ER 配置（若要查看这些 ER 配置的完整列表，请选择 **消息详细信息** 链接。）</span><span class="sxs-lookup"><span data-stu-id="58428-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![“已导入了以下配置的最新版本”消息和消息详细信息](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="58428-126">全球存储库中有其最新版本且可导入到当前 Finance 实例的 ER 配置（若要查看这些 ER 配置的完整列表，请选择 **消息详细信息** 链接。）</span><span class="sxs-lookup"><span data-stu-id="58428-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![“可用更新”消息和消息详细信息](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="58428-128">导入可用的更新后版本</span><span class="sxs-lookup"><span data-stu-id="58428-128">Import available updated versions</span></span>

1. <span data-ttu-id="58428-129">通过使用以下角色之一登录到 Finance：</span><span class="sxs-lookup"><span data-stu-id="58428-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="58428-130">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="58428-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="58428-131">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="58428-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="58428-132">系统管理员</span><span class="sxs-lookup"><span data-stu-id="58428-132">System administrator</span></span>

2. <span data-ttu-id="58428-133">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="58428-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="58428-134">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **导入配置版本更新**。</span><span class="sxs-lookup"><span data-stu-id="58428-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="58428-135">在 **导入电子申报配置版本更新** 对话框的 **运行模式** 字段中，选择 **导入最新更新** 将最新的 ER 配置版本从全球存储库导入到当前 Finance 实例中。</span><span class="sxs-lookup"><span data-stu-id="58428-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="58428-136">若要为导入计划批处理作业，请在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="58428-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="58428-137">如果要定期重复导入，请配置所需重复周期。</span><span class="sxs-lookup"><span data-stu-id="58428-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![“运行模式”字段设置为“导入最新更新”](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="58428-139">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="58428-139">Select **OK**.</span></span>
7. <span data-ttu-id="58428-140">若要了解已导入了哪些配置版本，请执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="58428-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="58428-141">如果以交互方式运行导入，而不是使用批处理作业运行导入，请查看收到的消息。</span><span class="sxs-lookup"><span data-stu-id="58428-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![以交互方式运行导入期间收到的消息](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="58428-143">如果以批处理方式运行导入，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="58428-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="58428-144">转到 **通用** \> **查询** \> **批处理作业** \> **我的批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="58428-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="58428-145">找到并选择 **导入电子申报配置版本更新** 作业，然后在操作窗格的 **批处理作业** 选项卡上，选择 **批处理作业历史记录** 查看作业历史记录。</span><span class="sxs-lookup"><span data-stu-id="58428-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="58428-146">在 **批处理作业历史** 页面上，选择 **日志**。</span><span class="sxs-lookup"><span data-stu-id="58428-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="58428-147">然后，在收到的消息中，选择 **消息详细信息** 链接查看作业日志。</span><span class="sxs-lookup"><span data-stu-id="58428-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![作业日志](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="58428-149">建议不要计划定期批处理作业来将更新后的 ER 配置版本直接从全球存储库导入到生产环境中，因为导入的版本将立即可用。</span><span class="sxs-lookup"><span data-stu-id="58428-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="58428-150">而是改用这种方法将 ER 配置版本部署到沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="58428-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="58428-151">然后可以先在沙盒环境中评估它们，之后才将其部署到生产环境。</span><span class="sxs-lookup"><span data-stu-id="58428-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58428-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="58428-152">Additional resources</span></span>

- [<span data-ttu-id="58428-153">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="58428-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="58428-154">从 Configuration service 的全局知识库下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="58428-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]