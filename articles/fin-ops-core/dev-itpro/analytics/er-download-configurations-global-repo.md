---
title: 从 Configuration service 的全局知识库下载 ER 配置
description: 本主题说明如何从 Configuration service 的全局知识库下载电子申报 (ER) 配置。
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a96e78a64fe0559ae5f3bfddabf3fe1cad8a3dcb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679550"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="b74ff-103">从 Configuration service 的全局知识库下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="b74ff-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b74ff-104">本主题说明如何从 Configuration service 的全局知识库下载[电子申报 (ER) 配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="b74ff-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="b74ff-105">有关详细信息，请参阅 [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services、Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)。</span><span class="sxs-lookup"><span data-stu-id="b74ff-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="b74ff-106">打开配置库</span><span class="sxs-lookup"><span data-stu-id="b74ff-106">Open configurations repository</span></span>

1. <span data-ttu-id="b74ff-107">使用以下角色之一登录到 Dynamics 365 Finance 应用程序：</span><span class="sxs-lookup"><span data-stu-id="b74ff-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="b74ff-108">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="b74ff-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="b74ff-109">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="b74ff-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b74ff-110">系统管理员</span><span class="sxs-lookup"><span data-stu-id="b74ff-110">System administrator</span></span>

2. <span data-ttu-id="b74ff-111">转到 **组织管理 > 工作区 > 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="b74ff-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="b74ff-112">在 **配置提供程序** 部分中，选择 **Microsoft** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="b74ff-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="b74ff-113">在 **Microsoft** 磁贴上，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="b74ff-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![电子申报工作区](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="b74ff-115">在 **配置存储库** 页面，在网格中，选择 **全局** 类型的现有存储库。</span><span class="sxs-lookup"><span data-stu-id="b74ff-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="b74ff-116">如果此存储库没有显示在网格中，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="b74ff-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="b74ff-117">选择 **添加** 添加新存储库。</span><span class="sxs-lookup"><span data-stu-id="b74ff-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="b74ff-118">存储库类型选择 **全局**，然后选择 **创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="b74ff-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="b74ff-119">如果系统提示，请按照授权说明操作。</span><span class="sxs-lookup"><span data-stu-id="b74ff-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="b74ff-120">为存储库输入名称和描述，然后选择 **确定** 确认新的存储库条目。</span><span class="sxs-lookup"><span data-stu-id="b74ff-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="b74ff-121">在网格中，选择 **全局** 类型的新存储库。</span><span class="sxs-lookup"><span data-stu-id="b74ff-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="b74ff-122">选择 **打开** 查看选择的存储库的 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="b74ff-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![配置存储库页面](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="b74ff-124">导入单个配置</span><span class="sxs-lookup"><span data-stu-id="b74ff-124">Import a single configuration</span></span>

1. <span data-ttu-id="b74ff-125">在 **配置存储库** 页面上的配置树中，选择所需的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="b74ff-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="b74ff-126">在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。</span><span class="sxs-lookup"><span data-stu-id="b74ff-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="b74ff-127">选择 **导入** 将所选版本从全局知识库下载到当前 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="b74ff-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b74ff-128">**导入** 按钮对当前 Finance 实例中已呈现的 ER 配置版本不可用。</span><span class="sxs-lookup"><span data-stu-id="b74ff-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![配置存储库页面](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="b74ff-130">导入筛选的配置</span><span class="sxs-lookup"><span data-stu-id="b74ff-130">Import filtered configurations</span></span>

1. <span data-ttu-id="b74ff-131">在 **配置存储库** 页面的配置树中，展开 **筛选器** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b74ff-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="b74ff-132">在 **标记** 网格中，添加所需的任何标记。</span><span class="sxs-lookup"><span data-stu-id="b74ff-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="b74ff-133">在 **国家/地区适用性** 字段中，选择适当的国家/地区代码，然后选择 **应用筛选器**。</span><span class="sxs-lookup"><span data-stu-id="b74ff-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b74ff-134">**配置** 快速选项卡显示满足指定选择条件的所有配置。</span><span class="sxs-lookup"><span data-stu-id="b74ff-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="b74ff-135">在 **配置** 快速选项卡上，选择 **导入** 将筛选出的配置从全局知识库下载到当前实例。</span><span class="sxs-lookup"><span data-stu-id="b74ff-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="b74ff-136">在 **配置** 快速选项卡上，选择 **重置筛选器** 清理指定的选择条件。</span><span class="sxs-lookup"><span data-stu-id="b74ff-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![配置存储库页面](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="b74ff-138">根据 ER 设置，配置在导入后进行验证。</span><span class="sxs-lookup"><span data-stu-id="b74ff-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="b74ff-139">您可能会收到发现的任何不一致问题。</span><span class="sxs-lookup"><span data-stu-id="b74ff-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="b74ff-140">必须先解决这些问题，然后才可以使用导入的配置版本。</span><span class="sxs-lookup"><span data-stu-id="b74ff-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="b74ff-141">有关详细信息，请参阅本主题的相关资源列表。</span><span class="sxs-lookup"><span data-stu-id="b74ff-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="b74ff-142">ER 配置可以配置为依赖于其他配置。</span><span class="sxs-lookup"><span data-stu-id="b74ff-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="b74ff-143">因此，连同所选配置一起，其他配置可能会自动导入。</span><span class="sxs-lookup"><span data-stu-id="b74ff-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="b74ff-144">有关配置依赖关系的详细信息，请参阅[定义 ER 配置与其他组件之间的依赖关系](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)。</span><span class="sxs-lookup"><span data-stu-id="b74ff-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b74ff-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="b74ff-145">Additional resources</span></span>

[<span data-ttu-id="b74ff-146">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="b74ff-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
