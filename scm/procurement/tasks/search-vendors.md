--- 
title: "搜索供应商"
description: "了解如何基于特定条件检索供应商。"
author: mkirknel
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa02b4fb6f309e55d0c74e477952e928ad8dfb12
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="search-for-vendors"></a><span data-ttu-id="8f843-103">搜索供应商</span><span class="sxs-lookup"><span data-stu-id="8f843-103">Search for vendors</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f843-104">了解如何基于特定条件检索供应商。</span><span class="sxs-lookup"><span data-stu-id="8f843-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="8f843-105">此示例显示了如何检索被批准用于特定采购类别，并拥有特定国家内首选地址的供应商。</span><span class="sxs-lookup"><span data-stu-id="8f843-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="8f843-106">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="8f843-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="8f843-107">此任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="8f843-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="8f843-108">转到“采购”>“供应商”>“供应商检索”。</span><span class="sxs-lookup"><span data-stu-id="8f843-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="8f843-109">单击“加号”图标以打开采购类别选择页。</span><span class="sxs-lookup"><span data-stu-id="8f843-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="8f843-110">在树形图中，选择“企业采购类别\办公设备“。</span><span class="sxs-lookup"><span data-stu-id="8f843-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="8f843-111">如果您正在运行该过程以作为任务指南，您可能必须单击“解除锁定”按钮，然后才可以选择正确的节点。</span><span class="sxs-lookup"><span data-stu-id="8f843-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="8f843-112">如果您没有使用 USMF，选择您拥有的某一类别。</span><span class="sxs-lookup"><span data-stu-id="8f843-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="8f843-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="8f843-113">Click Add.</span></span>
    * <span data-ttu-id="8f843-114">有可能在此选择多个类别。</span><span class="sxs-lookup"><span data-stu-id="8f843-114">It’s possible to select more than one category here.</span></span> <span data-ttu-id="8f843-115">如果您这样做，检索将会查找被核准用于至少一个类别的所有供应商。</span><span class="sxs-lookup"><span data-stu-id="8f843-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="8f843-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8f843-116">Click OK.</span></span>
6. <span data-ttu-id="8f843-117">在“国家/地区”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8f843-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="8f843-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8f843-118">Click OK.</span></span>

