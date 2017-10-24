--- 
title: "设置处置代码"
description: "此过程在针对可以在移动设备上用于退货单接收流程的处置代码的设置。"
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c004543188656dfd53d7539717cd6e93d0b9f47a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="9a3f2-103">设置处置代码</span><span class="sxs-lookup"><span data-stu-id="9a3f2-103">Set up dispositions codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a3f2-104">此过程在针对可以在移动设备上用于退货单接收流程的处置代码的设置。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="9a3f2-105">部署代码是收到物料时可以使用的规则集合。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="9a3f2-106">例如，在工作用户使用设备接收损坏的物料时，用户必须扫描损坏物料的处置代码。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="9a3f2-107">接收的货物的库存状态、工作模板和位置指令可以通过扫描的处置代码确定。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="9a3f2-108">对于采购订单接收流程和生产订单完工入库流程，使用处置代码是可选的。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="9a3f2-109">对于销售订单退货接收流程，如果使用移动设备登记物料，使用处置代码是强制的。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="9a3f2-110">本指南使用演示数据公司 USMF 创建。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="9a3f2-111">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="9a3f2-112">转到“仓库管理”>“设置”>“移动设备”>“处置码”。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="9a3f2-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-113">Click New.</span></span>
    * <span data-ttu-id="9a3f2-114">创建新的处置码以供客户退货使用。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="9a3f2-115">在“处置码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="9a3f2-116">在“库存状态”字段中，选择一个显示库存锁定的库存状态。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="9a3f2-117">如果您正在使用 USMF，则选择“锁定”。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="9a3f2-118">您可以将库存状态添加到处置码，以覆写订单行上显示的默认状态。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="9a3f2-119">在“工作模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="9a3f2-120">选项：选择与退货单相关的一个工作模板代码。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="9a3f2-121">如果没有提供任何数值，请使用系统中配置的标准规则来解决工作模板问题。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="9a3f2-122">选定工作模板将会限制此处置码的使用过程。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="9a3f2-123">例如，如果处置码有一个带采购订单类型的工作指令的工作模板，则其不能用于登记被客户退回的物料。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="9a3f2-124">在“退货处置码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="9a3f2-125">退货处置码可以确定已登记物料的退货单流程的剩余部分。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="9a3f2-126">在本示例中，客户应收到贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="9a3f2-127">添加包含信贷行为的退货处置码。</span><span class="sxs-lookup"><span data-stu-id="9a3f2-127">Add a returns disposition code that contains an action Credit.</span></span>  

