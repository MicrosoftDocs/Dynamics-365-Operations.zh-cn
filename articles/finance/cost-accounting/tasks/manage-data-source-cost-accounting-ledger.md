---
title: 管理成本核算分类帐的数据源
description: 此过程用于管理成本核算分类帐的总帐数据源。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48d92a634a08f686e29260a71782bbacf7215f2f
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759152"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="09563-103">管理成本核算分类帐的数据源</span><span class="sxs-lookup"><span data-stu-id="09563-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09563-104">此过程用于管理成本核算分类帐的总帐数据源。</span><span class="sxs-lookup"><span data-stu-id="09563-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="09563-105">完成此任务之前，确保播放“创建成本核算分类帐”和“定义成本控制单元”任务指南。</span><span class="sxs-lookup"><span data-stu-id="09563-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="09563-106">此录制使用 USP2 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="09563-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="09563-107">转到“成本核算”>“分类帐设置”>“成本核算分类帐”。</span><span class="sxs-lookup"><span data-stu-id="09563-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="09563-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="09563-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="09563-109">单击“实际版本”。</span><span class="sxs-lookup"><span data-stu-id="09563-109">Click Actual versions.</span></span>
4. <span data-ttu-id="09563-110">在“操作窗格”上单击“管理”。</span><span class="sxs-lookup"><span data-stu-id="09563-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="09563-111">单击“总帐”。</span><span class="sxs-lookup"><span data-stu-id="09563-111">Click General ledger.</span></span>
6. <span data-ttu-id="09563-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="09563-112">Click New.</span></span>
7. <span data-ttu-id="09563-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="09563-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="09563-114">在“数据提供方”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="09563-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="09563-115">在此示例中，选择“Dynamics 365 Finance - 总帐条目”。</span><span class="sxs-lookup"><span data-stu-id="09563-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="09563-116">在“成本元素维度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="09563-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="09563-117">在此示例中，选择“成本元素”。</span><span class="sxs-lookup"><span data-stu-id="09563-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="09563-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="09563-118">Click Save.</span></span>
11. <span data-ttu-id="09563-119">单击“配置数据提供方”。</span><span class="sxs-lookup"><span data-stu-id="09563-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="09563-120">在“法人”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="09563-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="09563-121">在此示例中，选择“USP2”。</span><span class="sxs-lookup"><span data-stu-id="09563-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="09563-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="09563-122">Click New.</span></span>
14. <span data-ttu-id="09563-123">在“过帐层”字段中，选择“当前”。</span><span class="sxs-lookup"><span data-stu-id="09563-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="09563-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="09563-124">Click OK.</span></span>

