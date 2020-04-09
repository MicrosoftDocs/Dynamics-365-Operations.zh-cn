---
title: 创建配置规则
description: 该过程创建配置规则，以用于基于维度的配置，从而执行或防止物料清单行的某些组合。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d5758b2903cd0a269f3e03e44b618c26e8b2310
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147863"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="1de0c-103">创建配置规则</span><span class="sxs-lookup"><span data-stu-id="1de0c-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1de0c-104">该过程创建配置规则，以用于基于维度的配置，从而执行或防止物料清单行的某些组合。</span><span class="sxs-lookup"><span data-stu-id="1de0c-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="1de0c-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="1de0c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1de0c-106">这是八个过程中第七个说明如何构建基于维度的配置组合的过程。</span><span class="sxs-lookup"><span data-stu-id="1de0c-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="1de0c-107">转到“产品信息管理”>“物料清单和配方”>“物料清单”。</span><span class="sxs-lookup"><span data-stu-id="1de0c-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="1de0c-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="1de0c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1de0c-109">查找和选择适用于基于维度的配置技术的物料清单。</span><span class="sxs-lookup"><span data-stu-id="1de0c-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="1de0c-110">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="1de0c-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="1de0c-111">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="1de0c-111">Click Change view.</span></span>
5. <span data-ttu-id="1de0c-112">单击“标题”视图。</span><span class="sxs-lookup"><span data-stu-id="1de0c-112">Click Header view.</span></span>
    * <span data-ttu-id="1de0c-113">打开标题视图以访问“配置流程”快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="1de0c-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="1de0c-114">展开或折叠“配置流程”部分。</span><span class="sxs-lookup"><span data-stu-id="1de0c-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="1de0c-115">“配置流程”快速选项卡必须处于展开模式。</span><span class="sxs-lookup"><span data-stu-id="1de0c-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="1de0c-116">单击“配置规则”。</span><span class="sxs-lookup"><span data-stu-id="1de0c-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="1de0c-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1de0c-117">Click New.</span></span>
9. <span data-ttu-id="1de0c-118">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1de0c-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="1de0c-119">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="1de0c-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1de0c-120">当前配置组中的物料会显示。</span><span class="sxs-lookup"><span data-stu-id="1de0c-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="1de0c-121">选择代表该规则中的条件的那个。</span><span class="sxs-lookup"><span data-stu-id="1de0c-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="1de0c-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1de0c-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1de0c-123">在“方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="1de0c-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="1de0c-124">可能强制从另一配置组选择或取消选择某一物料。</span><span class="sxs-lookup"><span data-stu-id="1de0c-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="1de0c-125">在“派生组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="1de0c-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="1de0c-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="1de0c-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="1de0c-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1de0c-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1de0c-128">选择所需的配置组。</span><span class="sxs-lookup"><span data-stu-id="1de0c-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="1de0c-129">在“派生物料”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="1de0c-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="1de0c-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1de0c-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1de0c-131">选择将被选择或取消选择的物料编号，选择与否取决于所选的方法。</span><span class="sxs-lookup"><span data-stu-id="1de0c-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="1de0c-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1de0c-132">Close the page.</span></span>

