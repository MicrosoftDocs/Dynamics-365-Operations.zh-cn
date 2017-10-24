--- 
title: "销售税分配和覆盖"
description: "此过程演示如何为零售渠道分配增值税组。"
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="067af-103">销售税分配和覆盖</span><span class="sxs-lookup"><span data-stu-id="067af-103">Sales tax assignment and overrides</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="067af-104">此过程演示如何为零售渠道分配增值税组。</span><span class="sxs-lookup"><span data-stu-id="067af-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="067af-105">还逐步演示了新建增值税覆盖并分配给现有增值税覆盖组的过程。</span><span class="sxs-lookup"><span data-stu-id="067af-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="067af-106">此过程</span><span class="sxs-lookup"><span data-stu-id="067af-106">This procedure</span></span>

<span data-ttu-id="067af-107">在演示数据中使用 USRT 公司。</span><span class="sxs-lookup"><span data-stu-id="067af-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="067af-108">转至“零售和商业”>“渠道”>“零售商店”>“所有零售商店”。</span><span class="sxs-lookup"><span data-stu-id="067af-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="067af-109">在列表中，单击“休斯敦”的“零售渠道 ID”链接。</span><span class="sxs-lookup"><span data-stu-id="067af-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="067af-110">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="067af-110">Click Edit.</span></span>
    * <span data-ttu-id="067af-111">“增值税组”字段中包含当前公司的增值税组列表。</span><span class="sxs-lookup"><span data-stu-id="067af-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="067af-112">当前分配的组是普通的“德克萨斯”增值税组。</span><span class="sxs-lookup"><span data-stu-id="067af-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="067af-113">“华盛顿”和“华盛顿，金县”也有增值税组。</span><span class="sxs-lookup"><span data-stu-id="067af-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="067af-114">增值税组中可以包含多个城市的适用税。</span><span class="sxs-lookup"><span data-stu-id="067af-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="067af-115">可以在“增值税覆盖”字段中将增值税覆盖组映射到渠道。</span><span class="sxs-lookup"><span data-stu-id="067af-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="067af-116">增值税覆盖组可用于将多个商店适用的增值税覆盖组合在一起。</span><span class="sxs-lookup"><span data-stu-id="067af-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="067af-117">可以创建该组并直接分配给渠道来节约时间，而不是手动逐一分配增值税覆盖。</span><span class="sxs-lookup"><span data-stu-id="067af-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="067af-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="067af-118">Click Save.</span></span>
5. <span data-ttu-id="067af-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="067af-119">Close the page.</span></span>
6. <span data-ttu-id="067af-120">转到“零售和商业”>“渠道设置”>“增值税”>“增值税覆盖”。</span><span class="sxs-lookup"><span data-stu-id="067af-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="067af-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="067af-121">Click New.</span></span>
8. <span data-ttu-id="067af-122">在“增值税覆盖”字段中，为新覆盖提供名称。</span><span class="sxs-lookup"><span data-stu-id="067af-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="067af-123">在“描述”字段中，提供该覆盖的描述。</span><span class="sxs-lookup"><span data-stu-id="067af-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="067af-124">将状态设置为“启用”。</span><span class="sxs-lookup"><span data-stu-id="067af-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="067af-125">展开或折叠“覆盖”部分。</span><span class="sxs-lookup"><span data-stu-id="067af-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="067af-126">在“类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="067af-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="067af-127">物料增值税组可用于覆盖属于该组的具体物料的税。</span><span class="sxs-lookup"><span data-stu-id="067af-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="067af-128">例如，食品物料的征税通常与耐用品的征税不同，所以可能有自己的增值税组。</span><span class="sxs-lookup"><span data-stu-id="067af-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="067af-129">增值税组是适用于特定渠道的税的组合。</span><span class="sxs-lookup"><span data-stu-id="067af-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="067af-130">例如，如果某个渠道同时开展零售和批发业务，则可以使用不同的物料增值税组。</span><span class="sxs-lookup"><span data-stu-id="067af-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="067af-131">将把所有适用的税映射到该增值税组。</span><span class="sxs-lookup"><span data-stu-id="067af-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="067af-132">现在可以选择“源”和“目标”税或“源税组”和“目标税组”来创建增值税覆盖。</span><span class="sxs-lookup"><span data-stu-id="067af-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="067af-133">“源”字段指示要覆盖的税或税组。</span><span class="sxs-lookup"><span data-stu-id="067af-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="067af-134">通过物料增值税组覆盖提供的选项比通过增值税组覆盖提供的选择多。</span><span class="sxs-lookup"><span data-stu-id="067af-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="067af-135">可以将增值税覆盖设置为覆盖整个交易记录中的税，或覆盖交易记录的特定行中的税。</span><span class="sxs-lookup"><span data-stu-id="067af-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="067af-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="067af-136">Click Save.</span></span>
14. <span data-ttu-id="067af-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="067af-137">Close the page.</span></span>
15. <span data-ttu-id="067af-138">转到“零售和商业”>“渠道设置”>“增值税”>“增值税覆盖组”。</span><span class="sxs-lookup"><span data-stu-id="067af-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="067af-139">此步骤，您将把新建的增值税覆盖分配给为休斯敦渠道分配的增值税覆盖组。</span><span class="sxs-lookup"><span data-stu-id="067af-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="067af-140">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="067af-140">Click Edit.</span></span>
17. <span data-ttu-id="067af-141">展开或折叠“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="067af-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="067af-142">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="067af-142">Click Add.</span></span>
19. <span data-ttu-id="067af-143">在“增值税覆盖”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="067af-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="067af-144">在列表中选择前面创建的增值税覆盖。</span><span class="sxs-lookup"><span data-stu-id="067af-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="067af-145">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="067af-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="067af-146">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="067af-146">Click Save.</span></span>

