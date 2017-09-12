--- 
title: "设置附属分配"
description: "此过程显示如何设置附属分配。"
author: BibiSp
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
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31787aa180639b934b837b98dc170070d33fd56f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="0f6c8-103">设置附属分配</span><span class="sxs-lookup"><span data-stu-id="0f6c8-103">Set up accessorial assignments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f6c8-104">此过程显示如何设置附属分配。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="0f6c8-105">这通常由运输协调员完成。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="0f6c8-106">您需要运行“设置运输中心附加费用和附属主数据”指南才能使用该指南。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="0f6c8-107">设置附属分配</span><span class="sxs-lookup"><span data-stu-id="0f6c8-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="0f6c8-108">转到“运输管理”>“设置”>“分级”>“附属分配”。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="0f6c8-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-109">Click New.</span></span>
3. <span data-ttu-id="0f6c8-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0f6c8-111">切换“详细信息”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="0f6c8-112">在“中心”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0f6c8-113">在列表中，选择您在“设置中心附加费用和附属主数据”指南中为附属主数据创建的中心。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="0f6c8-114">在“中心附属 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0f6c8-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0f6c8-116">切换“标准”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="0f6c8-117">在“条件”部分，您可以根据所提供的不同值，选择费用适用时的确切标准。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="0f6c8-118">将“始终应用”选项设为“是”。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="0f6c8-119">在“附属分配水平”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="0f6c8-120">切换“计算”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="0f6c8-121">在“附加费用类型”字段中，选择“统一”。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="0f6c8-122">附加费用类型确定如何计算实际成本。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="0f6c8-123">在此示例中，此为统一收费。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="0f6c8-124">在“附加费用”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="0f6c8-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0f6c8-125">Click Save.</span></span>


