--- 
title: "创建可配置产品的销售订单"
description: "此过程显示如何将配置模板应用于销售订单中的一个产品。"
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7084c3749f18e4fbe90fe4e04bdeac320cefeafa
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="b46d1-103">创建可配置产品的销售订单</span><span class="sxs-lookup"><span data-stu-id="b46d1-103">Create a sales order for a configurable product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b46d1-104">此过程显示如何将配置模板应用于销售订单中的一个产品。</span><span class="sxs-lookup"><span data-stu-id="b46d1-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="b46d1-105">此示例使用 USMF 演示数据公司中的 D0006 扬声器模型。</span><span class="sxs-lookup"><span data-stu-id="b46d1-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="b46d1-106">通常，销售订单处理人员使用此过程。</span><span class="sxs-lookup"><span data-stu-id="b46d1-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="b46d1-107">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="b46d1-107">Create a sales order</span></span>
1. <span data-ttu-id="b46d1-108">点击“销售订单处理和查询”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="b46d1-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-109">Click New.</span></span>
3. <span data-ttu-id="b46d1-110">单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-110">Click Sales order.</span></span>
4. <span data-ttu-id="b46d1-111">在“客户帐户”字段中选择“US-001”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="b46d1-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-112">Click OK.</span></span>
6. <span data-ttu-id="b46d1-113">在“物料编号”字段中，选择 D0006。</span><span class="sxs-lookup"><span data-stu-id="b46d1-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="b46d1-114">对于此任务，必须选择一个可配置产品。</span><span class="sxs-lookup"><span data-stu-id="b46d1-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="b46d1-115">单击“产品和供应”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-115">Click Product and supply.</span></span>
8. <span data-ttu-id="b46d1-116">单击“配置行”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-116">Click Configure line.</span></span>
    * <span data-ttu-id="b46d1-117">请注意，已根据选择的配置更改了价格，并且“含电缆”字段现在已设置为 True。</span><span class="sxs-lookup"><span data-stu-id="b46d1-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="b46d1-118">记下为电缆选择的默认价格和设置。</span><span class="sxs-lookup"><span data-stu-id="b46d1-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="b46d1-119">单击“加载模板”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-119">Click Load template.</span></span>
    * <span data-ttu-id="b46d1-120">此示例显示如何应用模板以选择预定义的配置。</span><span class="sxs-lookup"><span data-stu-id="b46d1-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="b46d1-121">如果将此过程用作任务指南并希望查看可用的其他属性值，必须单击“解锁”按钮。</span><span class="sxs-lookup"><span data-stu-id="b46d1-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="b46d1-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-122">Click OK.</span></span>
11. <span data-ttu-id="b46d1-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b46d1-123">Click OK.</span></span>
12. <span data-ttu-id="b46d1-124">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="b46d1-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="b46d1-125">单击“产品”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b46d1-125">Click the Product tab.</span></span>
    * <span data-ttu-id="b46d1-126">此物料的配置现在在产品维度下列出。</span><span class="sxs-lookup"><span data-stu-id="b46d1-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="b46d1-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b46d1-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="b46d1-128">选择产品配置</span><span class="sxs-lookup"><span data-stu-id="b46d1-128">Select the product configuration</span></span>


