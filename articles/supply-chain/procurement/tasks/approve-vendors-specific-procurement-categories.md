---
title: 审核特定采购类别的供应商
description: 本主题说明如何在 Dynamics 365 for Finance and Operations 中审核特定采购类别的供应商。
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867141"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="c1dea-103">审核特定采购类别的供应商</span><span class="sxs-lookup"><span data-stu-id="c1dea-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1dea-104">本主题说明如何在 Dynamics 365 for Finance and Operations 中审核特定采购类别的供应商。</span><span class="sxs-lookup"><span data-stu-id="c1dea-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c1dea-105">创建采购申请时，可能需要选择核准供应商或首选供应商，具体取决于制订的采购政策。</span><span class="sxs-lookup"><span data-stu-id="c1dea-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="c1dea-106">此过程演示如何指定供应商是特定采购类别的核准供应商或首选供应商。</span><span class="sxs-lookup"><span data-stu-id="c1dea-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="c1dea-107">此任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="c1dea-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="c1dea-108">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="c1dea-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="c1dea-109">在导航窗格中，转到**模块 > 采购 > 供应商 > 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c1dea-110">选择要设置为类别的核准供应商或首选供应商的供应商。</span><span class="sxs-lookup"><span data-stu-id="c1dea-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="c1dea-111">在操作窗格上，选择**常规**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c1dea-112">选择**类别**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-112">Select **Categories**.</span></span>
5. <span data-ttu-id="c1dea-113">选择**添加类别**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-113">Select **Add category**.</span></span>
6. <span data-ttu-id="c1dea-114">在**类别**字段中，选择**办公和桌面附件(办公和桌面附件)**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="c1dea-115">在**供应商类别状态**字段中，选择**首选**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="c1dea-116">可以为一个类别指定多家首选供应商。</span><span class="sxs-lookup"><span data-stu-id="c1dea-116">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="c1dea-117">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-117">Select **Save**.</span></span>
9. <span data-ttu-id="c1dea-118">在导航窗格中，转到**模块 > 采购 > 采购目录**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="c1dea-119">在树中，选择**企业采购类别\办公和桌面附件**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="c1dea-120">展开**供应商**部分。</span><span class="sxs-lookup"><span data-stu-id="c1dea-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="c1dea-121">检查所选供应商是否显示为办公室和桌面附件类别的首选供应商。</span><span class="sxs-lookup"><span data-stu-id="c1dea-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="c1dea-122">如果您要将此过程作为任务指南运行，可能必须选择**解锁**按钮才能向下滚动到供应商列表。</span><span class="sxs-lookup"><span data-stu-id="c1dea-122">If you’re running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="c1dea-123">还可以在此页中添加首选供应商和核准供应商。</span><span class="sxs-lookup"><span data-stu-id="c1dea-123">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="c1dea-124">在树中，展开**办公和桌面附件**，然后选择**剪刀**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="c1dea-125">在**从父类别继承供应商:** 字段中选择**否**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="c1dea-126">在**从父类别继承供应商:** 字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="c1dea-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

