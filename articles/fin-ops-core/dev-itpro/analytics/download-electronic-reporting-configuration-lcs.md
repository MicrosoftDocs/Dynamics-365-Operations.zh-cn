---
title: 从 Lifecycle Services 下载电子申报配置
description: 本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载电子申报 (ER) 配置。
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 719b277fb828ea2085ea80bc4a36c2af3412f66b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683297"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="12cc6-103">从 Lifecycle Services 下载电子报告配置</span><span class="sxs-lookup"><span data-stu-id="12cc6-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12cc6-104">此主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 中的[共享资产库](../lifecycle-services/asset-library.md)下载最新版本的[电子申报 (ER) 配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="12cc6-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="12cc6-105">通过使用以下角色之一登录到应用程序：</span><span class="sxs-lookup"><span data-stu-id="12cc6-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="12cc6-106">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="12cc6-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="12cc6-107">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="12cc6-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="12cc6-108">系统管理员</span><span class="sxs-lookup"><span data-stu-id="12cc6-108">System administrator</span></span>

2. <span data-ttu-id="12cc6-109">转到 **组织管理** &gt; **工作区** &gt; **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="12cc6-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="12cc6-110">在 **配置提供程序** 部分中，选择 **Microsoft** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="12cc6-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="12cc6-111">在 **Microsoft** 磁贴上，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="12cc6-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="12cc6-112">[“本地化配置”页面中的 ![Microsoft 磁贴](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="12cc6-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="12cc6-113">在 **配置存储库** 页面，在网格中，选择 **LCS** 类型的现有存储库。</span><span class="sxs-lookup"><span data-stu-id="12cc6-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="12cc6-114">如果此存储库没有显示在网格中，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="12cc6-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="12cc6-115">选择 **添加** 添加存储库。</span><span class="sxs-lookup"><span data-stu-id="12cc6-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="12cc6-116">选择 **LCS** 作为存储库类型。</span><span class="sxs-lookup"><span data-stu-id="12cc6-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="12cc6-117">选择 **创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="12cc6-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="12cc6-118">如果系统提示您提供授权信息，请按照屏幕上的说明操作。</span><span class="sxs-lookup"><span data-stu-id="12cc6-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="12cc6-119">输入存储库的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="12cc6-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="12cc6-120">选择 **确定** 确认新存储库条目。</span><span class="sxs-lookup"><span data-stu-id="12cc6-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="12cc6-121">在网格中，选择 **LCS** 类型的新存储库。</span><span class="sxs-lookup"><span data-stu-id="12cc6-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="12cc6-122">选择 **打开** 查看选择的存储库的 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="12cc6-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="12cc6-123">[![配置存储库页面](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="12cc6-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="12cc6-124">如果访问 LCS 存储库以从 LCS 中的共享资产库下载配置时遇到问题，可以改为从[全局存储库](er-download-configurations-global-repo.md)下载配置。</span><span class="sxs-lookup"><span data-stu-id="12cc6-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="12cc6-125">在左侧窗格的配置树中，选择所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="12cc6-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="12cc6-126">在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。</span><span class="sxs-lookup"><span data-stu-id="12cc6-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="12cc6-127">选择 **导入** 将所选版本从 LCS 下载到当前实例。</span><span class="sxs-lookup"><span data-stu-id="12cc6-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12cc6-128">**导入** 按钮对当前实例中已呈现的 ER 配置版本不可用。</span><span class="sxs-lookup"><span data-stu-id="12cc6-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="12cc6-129">[![配置存储库页面](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="12cc6-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="12cc6-130">根据 ER 设置，配置在导入后进行验证。</span><span class="sxs-lookup"><span data-stu-id="12cc6-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="12cc6-131">您可能会收到发现的任何不一致问题。</span><span class="sxs-lookup"><span data-stu-id="12cc6-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="12cc6-132">在可以使用导入的配置版本之前，必须解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="12cc6-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="12cc6-133">有关详细信息，请参阅本主题的相关主题列表。</span><span class="sxs-lookup"><span data-stu-id="12cc6-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12cc6-134">其他资源</span><span class="sxs-lookup"><span data-stu-id="12cc6-134">Additional resources</span></span>

[<span data-ttu-id="12cc6-135">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="12cc6-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="12cc6-136">从 Configuration service 的全局知识库下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="12cc6-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
