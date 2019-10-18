---
title: 配置跨公司财务数据共享
description: 此过程显示在公司间共享数据时，如何配置、启用、验证和解决冲突。
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184362"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="ff7db-103">配置跨公司财务数据共享</span><span class="sxs-lookup"><span data-stu-id="ff7db-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff7db-104">此过程显示在公司间共享数据时，如何配置、启用、验证和解决冲突。</span><span class="sxs-lookup"><span data-stu-id="ff7db-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="ff7db-105">它使用 USMF 公司和共享模板的财务数据。</span><span class="sxs-lookup"><span data-stu-id="ff7db-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="ff7db-106">此任务指南需要 Dynamics AX 平台 7.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ff7db-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="ff7db-107">转到**导航窗格 > 模块 > 系统管理 > 工作区 > 数据管理**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="ff7db-108">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-108">Click **Import**.</span></span>
3. <span data-ttu-id="ff7db-109">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ff7db-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="ff7db-110">在**源数据格式**字段中，选择“包装”类型。</span><span class="sxs-lookup"><span data-stu-id="ff7db-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="ff7db-111">单击**上载**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-111">Click **Upload**.</span></span> <span data-ttu-id="ff7db-112">导航到共享模板包装文件的财务数据的位置并选择该文档。</span><span class="sxs-lookup"><span data-stu-id="ff7db-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="ff7db-113">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-113">Click **Save**.</span></span>
6. <span data-ttu-id="ff7db-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ff7db-114">In the list, mark the selected row.</span></span> <span data-ttu-id="ff7db-115">选择共享刚才创建的策略的数据。</span><span class="sxs-lookup"><span data-stu-id="ff7db-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="ff7db-116">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-116">Click **Import**.</span></span>
8. <span data-ttu-id="ff7db-117">单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-117">Click **Close**.</span></span>
9. <span data-ttu-id="ff7db-118">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="ff7db-118">Refresh the page.</span></span>
10. <span data-ttu-id="ff7db-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ff7db-119">Close the page.</span></span>
11. <span data-ttu-id="ff7db-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ff7db-120">Close the page.</span></span>
12. <span data-ttu-id="ff7db-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ff7db-121">Close the page.</span></span>
13. <span data-ttu-id="ff7db-122">转到**导航窗格 > 模块 > 系统管理 > 设置 > 配置跨公司数据共享**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="ff7db-123">在列表中，找到并选择**付款日**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="ff7db-124">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-124">Click **Add**.</span></span>
16. <span data-ttu-id="ff7db-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ff7db-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ff7db-126">在**公司**字段中，键入 'USSI'。</span><span class="sxs-lookup"><span data-stu-id="ff7db-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="ff7db-127">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-127">Click **Add**.</span></span>
19. <span data-ttu-id="ff7db-128">在**公司**字段中，键入 'USMF'。</span><span class="sxs-lookup"><span data-stu-id="ff7db-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="ff7db-129">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-129">Click **Save**.</span></span>
21. <span data-ttu-id="ff7db-130">单击**启用**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-130">Click **Enable**.</span></span>
22. <span data-ttu-id="ff7db-131">单击**是**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-131">Click **Yes**.</span></span>
23. <span data-ttu-id="ff7db-132">单击**查找共享问题**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="ff7db-133">单击**是**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-133">Click **Yes**.</span></span>
25. <span data-ttu-id="ff7db-134">单击**更新字段值**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="ff7db-135">单击**使用公司 1 的值**。</span><span class="sxs-lookup"><span data-stu-id="ff7db-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="ff7db-136">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="ff7db-136">Refresh the page.</span></span>
28. <span data-ttu-id="ff7db-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ff7db-137">Close the page.</span></span>

