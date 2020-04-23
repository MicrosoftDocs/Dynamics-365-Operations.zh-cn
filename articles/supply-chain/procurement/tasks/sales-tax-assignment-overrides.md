---
title: 销售税分配和覆盖
description: 此过程演示如何为商业渠道分配增值税组。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207578"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="75048-103"> 销售税分配和覆盖</span><span class="sxs-lookup"><span data-stu-id="75048-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75048-104">此过程演示如何为商业渠道分配增值税组。</span><span class="sxs-lookup"><span data-stu-id="75048-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="75048-105">还逐步演示了新建增值税覆盖并分配给现有增值税覆盖组的过程。</span><span class="sxs-lookup"><span data-stu-id="75048-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="75048-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="75048-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="75048-107">转至“Retail 和 Commerce”>“渠道”>“商店”>“所有商店”。</span><span class="sxs-lookup"><span data-stu-id="75048-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="75048-108">在列表中，单击“休斯敦”的“渠道 ID”链接。</span><span class="sxs-lookup"><span data-stu-id="75048-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="75048-109">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="75048-109">Click Edit.</span></span>
    * <span data-ttu-id="75048-110">“增值税组”字段中包含当前公司的增值税组列表。</span><span class="sxs-lookup"><span data-stu-id="75048-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="75048-111">当前分配的组是普通的“德克萨斯”增值税组。</span><span class="sxs-lookup"><span data-stu-id="75048-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="75048-112">“华盛顿”和“华盛顿，金县”也有增值税组。</span><span class="sxs-lookup"><span data-stu-id="75048-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="75048-113">增值税组中可以包含多个城市的适用税。</span><span class="sxs-lookup"><span data-stu-id="75048-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="75048-114">可以在“增值税覆盖”字段中将增值税覆盖组映射到渠道。</span><span class="sxs-lookup"><span data-stu-id="75048-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="75048-115">增值税覆盖组可用于将多个商店适用的增值税覆盖组合在一起。</span><span class="sxs-lookup"><span data-stu-id="75048-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="75048-116">可以创建该组并直接分配给渠道来节约时间，而不是手动逐一分配增值税覆盖。</span><span class="sxs-lookup"><span data-stu-id="75048-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="75048-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="75048-117">Click Save.</span></span>
5. <span data-ttu-id="75048-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="75048-118">Close the page.</span></span>
6. <span data-ttu-id="75048-119">转到“Retail 和 Commerce”>“渠道设置”>“增值税”>“增值税覆盖”。</span><span class="sxs-lookup"><span data-stu-id="75048-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="75048-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="75048-120">Click New.</span></span>
8. <span data-ttu-id="75048-121">在“增值税覆盖”字段中，为新覆盖提供名称。</span><span class="sxs-lookup"><span data-stu-id="75048-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="75048-122">在“描述”字段中，提供该覆盖的描述。</span><span class="sxs-lookup"><span data-stu-id="75048-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="75048-123">将状态设置为“启用”。</span><span class="sxs-lookup"><span data-stu-id="75048-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="75048-124">展开或折叠“覆盖”部分。</span><span class="sxs-lookup"><span data-stu-id="75048-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="75048-125">在“类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="75048-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="75048-126">物料增值税组可用于覆盖属于该组的具体物料的税。</span><span class="sxs-lookup"><span data-stu-id="75048-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="75048-127">例如，食品物料的征税通常与耐用品的征税不同，所以可能有自己的增值税组。</span><span class="sxs-lookup"><span data-stu-id="75048-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="75048-128">增值税组是适用于特定渠道的税的组合。</span><span class="sxs-lookup"><span data-stu-id="75048-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="75048-129">例如，如果某个渠道同时开展零售和批发业务，则可以使用不同的物料增值税组。</span><span class="sxs-lookup"><span data-stu-id="75048-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="75048-130">将把所有适用的税映射到该增值税组。</span><span class="sxs-lookup"><span data-stu-id="75048-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="75048-131">现在可以选择“源”和“目标”税或“源税组”和“目标税组”来创建增值税覆盖。</span><span class="sxs-lookup"><span data-stu-id="75048-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="75048-132">“源”字段指示要覆盖的税或税组。</span><span class="sxs-lookup"><span data-stu-id="75048-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="75048-133">通过物料增值税组覆盖提供的选项比通过增值税组覆盖提供的选择多。</span><span class="sxs-lookup"><span data-stu-id="75048-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="75048-134">可以将增值税覆盖设置为覆盖整个交易记录中的税，或覆盖交易记录的特定行中的税。</span><span class="sxs-lookup"><span data-stu-id="75048-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="75048-135">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="75048-135">Click Save.</span></span>
14. <span data-ttu-id="75048-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="75048-136">Close the page.</span></span>
15. <span data-ttu-id="75048-137">转到“Retail 和 Commerce”>“渠道设置”>“增值税”>“增值税覆盖组”。</span><span class="sxs-lookup"><span data-stu-id="75048-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="75048-138">此步骤，您将把新建的增值税覆盖分配给为休斯敦渠道分配的增值税覆盖组。</span><span class="sxs-lookup"><span data-stu-id="75048-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="75048-139">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="75048-139">Click Edit.</span></span>
17. <span data-ttu-id="75048-140">展开或折叠“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="75048-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="75048-141">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="75048-141">Click Add.</span></span>
19. <span data-ttu-id="75048-142">在“增值税覆盖”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="75048-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="75048-143">在列表中选择前面创建的增值税覆盖。</span><span class="sxs-lookup"><span data-stu-id="75048-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="75048-144">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="75048-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="75048-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="75048-145">Click Save.</span></span>

