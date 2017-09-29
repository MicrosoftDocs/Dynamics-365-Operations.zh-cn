---
title: "从 Lifecycle Services 下载电子申报配置"
description: "本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载电子申报 (ER) 配置。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a4411b25285128c849a715fdc7a2f5fe51580a3b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="704fc-103">从 Lifecycle Services 下载电子申报配置</span><span class="sxs-lookup"><span data-stu-id="704fc-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="704fc-104">本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载电子申报 (ER) 配置。</span><span class="sxs-lookup"><span data-stu-id="704fc-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="704fc-105">本教程指导您如何从 Microsoft Dynamics Lifecycle Services (LCS) 下载最新版本的电子申报 (ER) 配置的整个流程。</span><span class="sxs-lookup"><span data-stu-id="704fc-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="704fc-106">通过使用以下角色之一登录到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="704fc-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="704fc-107">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="704fc-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="704fc-108">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="704fc-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="704fc-109">系统管理员</span><span class="sxs-lookup"><span data-stu-id="704fc-109">System administrator</span></span>

2.  <span data-ttu-id="704fc-110">转到**组织管理** &gt; **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="704fc-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="704fc-111">在**配置提供程序**部分中，选择 **Microsoft** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="704fc-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="704fc-112">在 **Microsoft** 磁贴上，单击**存储库**。</span><span class="sxs-lookup"><span data-stu-id="704fc-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="704fc-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="704fc-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="704fc-114">在**配置存储库**页面，在网格中，选择 **LCS** 类型的现有存储库。</span><span class="sxs-lookup"><span data-stu-id="704fc-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="704fc-115">如果此存储库没有显示在网格中，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="704fc-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="704fc-116">单击**添加**添加新存储库。</span><span class="sxs-lookup"><span data-stu-id="704fc-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="704fc-117">选择 **LCS** 作为存储库类型。</span><span class="sxs-lookup"><span data-stu-id="704fc-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="704fc-118">单击**创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="704fc-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="704fc-119">如果系统提示，请按照授权说明操作。</span><span class="sxs-lookup"><span data-stu-id="704fc-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="704fc-120">输入存储库的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="704fc-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="704fc-121">单击**确定**确认新存储库条目。</span><span class="sxs-lookup"><span data-stu-id="704fc-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="704fc-122">在网格中，选择 **LCS** 类型的新存储库。</span><span class="sxs-lookup"><span data-stu-id="704fc-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="704fc-123">单击**打开**查看选择的存储库的 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="704fc-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="704fc-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="704fc-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="704fc-125">在左侧窗格的配置树中，选择您所需的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="704fc-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="704fc-126">在**版本**快速选项卡上，选择所选 ER 配置所需的版本。</span><span class="sxs-lookup"><span data-stu-id="704fc-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="704fc-127">单击**导入**将所选版本从 LCS 下载到当前 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="704fc-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="704fc-128">**注意：****导入**按钮对当前 Finance and Operations 实例中已呈现的 ER 配置版本不可用。</span><span class="sxs-lookup"><span data-stu-id="704fc-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="704fc-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="704fc-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="704fc-130">**注意：**根据 ER 设置，配置在导入后进行验证。</span><span class="sxs-lookup"><span data-stu-id="704fc-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="704fc-131">您可能会收到发现的任何不一致问题。</span><span class="sxs-lookup"><span data-stu-id="704fc-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="704fc-132">在可以使用导入的配置版本之前，必须解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="704fc-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="704fc-133">有关详细信息，请参阅本主题的相关文章列表。</span><span class="sxs-lookup"><span data-stu-id="704fc-133">For more information, see the list of related articles for this topic.</span></span>

<a name="see-also"></a><span data-ttu-id="704fc-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="704fc-134">See also</span></span>
--------

[<span data-ttu-id="704fc-135">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="704fc-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




