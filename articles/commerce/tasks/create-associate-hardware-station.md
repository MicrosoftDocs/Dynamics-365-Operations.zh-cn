---
title: 创建和关联硬件工作站
description: 此程序会逐步演示如何创建新的硬件工作站。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 772ccc44c01d97a07796bd1ee443012448955f49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021744"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="c92c2-103">创建和关联硬件工作站</span><span class="sxs-lookup"><span data-stu-id="c92c2-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c92c2-104">此程序会逐步演示如何创建新的硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="c92c2-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="c92c2-105">新硬件配置文件将被创建和用于添加新的硬件工作站到预定义的商店（渠道）。</span><span class="sxs-lookup"><span data-stu-id="c92c2-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="c92c2-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="c92c2-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c92c2-107">转至“商业要素”>“渠道”></span><span class="sxs-lookup"><span data-stu-id="c92c2-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="c92c2-108">></span><span class="sxs-lookup"><span data-stu-id="c92c2-108">> ..</span></span> <span data-ttu-id="c92c2-109">></span><span class="sxs-lookup"><span data-stu-id="c92c2-109">> ..</span></span> <span data-ttu-id="c92c2-110">>”硬件工作站配置文件“。</span><span class="sxs-lookup"><span data-stu-id="c92c2-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="c92c2-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c92c2-111">Click New.</span></span>
3. <span data-ttu-id="c92c2-112">在“硬件工作站 ID”字段中，输入“TestHWProfile”。</span><span class="sxs-lookup"><span data-stu-id="c92c2-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="c92c2-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c92c2-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c92c2-114">在“端口编号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c92c2-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="c92c2-115">在“硬件配置文件”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="c92c2-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c92c2-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c92c2-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c92c2-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c92c2-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c92c2-118">在“包装名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="c92c2-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c92c2-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c92c2-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c92c2-120">这是随新环境提供的标准包装。</span><span class="sxs-lookup"><span data-stu-id="c92c2-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="c92c2-121">版本号可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="c92c2-121">The version number may vary.</span></span>  
11. <span data-ttu-id="c92c2-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c92c2-122">Click Save.</span></span>
12. <span data-ttu-id="c92c2-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c92c2-123">Close the page.</span></span>
13. <span data-ttu-id="c92c2-124">转至“Retail 和 Commerce”>“渠道”>“所有商店”。</span><span class="sxs-lookup"><span data-stu-id="c92c2-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="c92c2-125">在列表中，选择行 17。</span><span class="sxs-lookup"><span data-stu-id="c92c2-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="c92c2-126">如果您正使用 USRT 演示数据公司，则是休斯敦商店。</span><span class="sxs-lookup"><span data-stu-id="c92c2-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="c92c2-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c92c2-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c92c2-128">切换“硬件工作站”部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="c92c2-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="c92c2-129">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c92c2-129">Click Add.</span></span>
18. <span data-ttu-id="c92c2-130">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c92c2-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="c92c2-131">在“配置文件 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="c92c2-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="c92c2-132">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c92c2-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c92c2-133">这必须是前面步骤中创建的新硬件工作站配置文件。</span><span class="sxs-lookup"><span data-stu-id="c92c2-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="c92c2-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c92c2-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="c92c2-135">在“主机名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c92c2-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="c92c2-136">在“EFT 终端 ID”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c92c2-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="c92c2-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c92c2-137">Click Save.</span></span>

