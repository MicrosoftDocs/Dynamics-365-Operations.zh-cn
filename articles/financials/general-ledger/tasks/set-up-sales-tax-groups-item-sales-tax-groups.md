--- 
title: "设置销售税组和物料销售税组"
description: "此任务记录向您介绍销售税和物料销售税组的设置。"
author: twheeloc
manager: AnnBe
ms.date: 11/10/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4d7f1093edcfff65fd466fa8138b1bb5203648b3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="82115-103">设置销售税组和物料销售税组</span><span class="sxs-lookup"><span data-stu-id="82115-103">Set up sales tax groups and item sales tax groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82115-104">此任务记录向您介绍销售税和物料销售税组的设置。</span><span class="sxs-lookup"><span data-stu-id="82115-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="82115-105">增值税组是附加到客户和供应商的增值税代码组。</span><span class="sxs-lookup"><span data-stu-id="82115-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="82115-106">它们也附加到了交易记录的会计科目，这些会计科目没有过账到某个特定的供应商或客户。</span><span class="sxs-lookup"><span data-stu-id="82115-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="82115-107">物料销售税组是附到产品等资源中的销售税代码组。</span><span class="sxs-lookup"><span data-stu-id="82115-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="82115-108">应用到特定交易记录的增值税由该交易记录的增值税组及增值税（物料）组中包括的增值税代码决定。</span><span class="sxs-lookup"><span data-stu-id="82115-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="82115-109">仅当为必须及时或记录增值税的每个交易记录选择了增值税组合物料增值税组，才能计算增值税。</span><span class="sxs-lookup"><span data-stu-id="82115-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="82115-110">转到报税>间接税>销售税》销售税组。</span><span class="sxs-lookup"><span data-stu-id="82115-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="82115-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="82115-111">Click New.</span></span>
3. <span data-ttu-id="82115-112">在“销售税组”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="82115-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="82115-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="82115-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82115-114">切换“设置”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="82115-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="82115-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="82115-115">Click Add.</span></span>
7. <span data-ttu-id="82115-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="82115-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="82115-117">在“销售税代码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="82115-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="82115-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="82115-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="82115-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="82115-119">Click Save.</span></span>
11. <span data-ttu-id="82115-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="82115-120">Close the page.</span></span>
12. <span data-ttu-id="82115-121">转到报税>间接税>销售税>物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="82115-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="82115-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="82115-122">Click New.</span></span>
14. <span data-ttu-id="82115-123">在“物料销售税组”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="82115-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="82115-124">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="82115-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="82115-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="82115-125">Click Add.</span></span>
17. <span data-ttu-id="82115-126">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="82115-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="82115-127">在“销售税代码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="82115-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="82115-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="82115-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="82115-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="82115-129">Click Save.</span></span>


