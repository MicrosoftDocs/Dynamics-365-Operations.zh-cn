---
title: 配置跨公司财务数据共享
description: 此过程显示在公司间共享数据时，如何配置、启用、验证和解决冲突。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 049ffeee7db95cc2e5a31526d5d99026303456be
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848247"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="998f4-103">配置跨公司财务数据共享</span><span class="sxs-lookup"><span data-stu-id="998f4-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="998f4-104">此过程显示在公司间共享数据时，如何配置、启用、验证和解决冲突。</span><span class="sxs-lookup"><span data-stu-id="998f4-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="998f4-105">它使用 USMF 公司和共享模板的财务数据。</span><span class="sxs-lookup"><span data-stu-id="998f4-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="998f4-106">此任务指南需要 Dynamics AX 平台 7.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="998f4-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="998f4-107">转到“系统管理”>“工作区”>“数据管理”。</span><span class="sxs-lookup"><span data-stu-id="998f4-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="998f4-108">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="998f4-108">Click Import.</span></span>
3. <span data-ttu-id="998f4-109">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="998f4-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="998f4-110">在“源数据格式”字段中，选择包装类型。</span><span class="sxs-lookup"><span data-stu-id="998f4-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="998f4-111">单击“上载”。</span><span class="sxs-lookup"><span data-stu-id="998f4-111">Click Upload.</span></span> <span data-ttu-id="998f4-112">导航到共享模板包装文件的财务数据的位置并选择该文档。</span><span class="sxs-lookup"><span data-stu-id="998f4-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="998f4-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="998f4-113">Click Save.</span></span>
6. <span data-ttu-id="998f4-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="998f4-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="998f4-115">选择共享刚才创建的策略的数据。</span><span class="sxs-lookup"><span data-stu-id="998f4-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="998f4-116">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="998f4-116">Click Import.</span></span>
8. <span data-ttu-id="998f4-117">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="998f4-117">Click Close.</span></span>
9. <span data-ttu-id="998f4-118">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="998f4-118">Refresh the page.</span></span>
10. <span data-ttu-id="998f4-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="998f4-119">Close the page.</span></span>
11. <span data-ttu-id="998f4-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="998f4-120">Close the page.</span></span>
12. <span data-ttu-id="998f4-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="998f4-121">Close the page.</span></span>
13. <span data-ttu-id="998f4-122">转到“系统管理”>“设置”>“配置跨公司数据共享”。</span><span class="sxs-lookup"><span data-stu-id="998f4-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="998f4-123">在列表中，找到并选择付款日。</span><span class="sxs-lookup"><span data-stu-id="998f4-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="998f4-124">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="998f4-124">Click Add.</span></span>
16. <span data-ttu-id="998f4-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="998f4-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="998f4-126">在“公司”字段中，键入 'USSI'。</span><span class="sxs-lookup"><span data-stu-id="998f4-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="998f4-127">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="998f4-127">Click Add.</span></span>
19. <span data-ttu-id="998f4-128">在“公司”字段中，键入 'USMF'。</span><span class="sxs-lookup"><span data-stu-id="998f4-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="998f4-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="998f4-129">Click Save.</span></span>
21. <span data-ttu-id="998f4-130">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="998f4-130">Click Enable.</span></span>
22. <span data-ttu-id="998f4-131">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="998f4-131">Click Yes.</span></span>
23. <span data-ttu-id="998f4-132">单击“查找共享问题”。</span><span class="sxs-lookup"><span data-stu-id="998f4-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="998f4-133">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="998f4-133">Click Yes.</span></span>
25. <span data-ttu-id="998f4-134">单击“更新字段值”。</span><span class="sxs-lookup"><span data-stu-id="998f4-134">Click Update field value.</span></span>
26. <span data-ttu-id="998f4-135">单击“使用公司 1 的值”。</span><span class="sxs-lookup"><span data-stu-id="998f4-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="998f4-136">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="998f4-136">Refresh the page.</span></span>
28. <span data-ttu-id="998f4-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="998f4-137">Close the page.</span></span>

