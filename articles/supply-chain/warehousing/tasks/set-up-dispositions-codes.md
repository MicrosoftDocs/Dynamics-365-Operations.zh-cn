---
title: 设置处置代码
description: 此过程在针对可以在移动设备上用于退货单接收流程的处置代码的设置。
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16458f709788e538d036cc4d3b3239f4ffa3c42e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830921"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="c72ff-103">设置处置代码</span><span class="sxs-lookup"><span data-stu-id="c72ff-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c72ff-104">此过程在针对可以在移动设备上用于退货单接收流程的处置代码的设置。</span><span class="sxs-lookup"><span data-stu-id="c72ff-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="c72ff-105">部署代码是收到物料时可以使用的规则集合。</span><span class="sxs-lookup"><span data-stu-id="c72ff-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="c72ff-106">例如，在工作用户使用设备接收损坏的物料时，用户必须扫描损坏物料的处置代码。</span><span class="sxs-lookup"><span data-stu-id="c72ff-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="c72ff-107">接收的货物的库存状态、工作模板和位置指令可以通过扫描的处置代码确定。</span><span class="sxs-lookup"><span data-stu-id="c72ff-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="c72ff-108">对于采购订单接收流程和生产订单完工入库流程，使用处置代码是可选的。</span><span class="sxs-lookup"><span data-stu-id="c72ff-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="c72ff-109">对于销售订单退货接收流程，如果使用移动设备登记物料，使用处置代码是强制的。</span><span class="sxs-lookup"><span data-stu-id="c72ff-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="c72ff-110">本指南使用演示数据公司 USMF 创建。</span><span class="sxs-lookup"><span data-stu-id="c72ff-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="c72ff-111">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="c72ff-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="c72ff-112">转到“仓库管理”>“设置”>“移动设备”>“处置码”。</span><span class="sxs-lookup"><span data-stu-id="c72ff-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="c72ff-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c72ff-113">Click New.</span></span>
    * <span data-ttu-id="c72ff-114">创建新的处置码以供客户退货使用。</span><span class="sxs-lookup"><span data-stu-id="c72ff-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="c72ff-115">在“处置码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c72ff-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="c72ff-116">在“库存状态”字段中，选择一个显示库存锁定的库存状态。</span><span class="sxs-lookup"><span data-stu-id="c72ff-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="c72ff-117">如果您正在使用 USMF，则选择“锁定”。</span><span class="sxs-lookup"><span data-stu-id="c72ff-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="c72ff-118">您可以将库存状态添加到处置码，以覆写订单行上显示的默认状态。</span><span class="sxs-lookup"><span data-stu-id="c72ff-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="c72ff-119">在“工作模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c72ff-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="c72ff-120">选项：选择与退货单相关的一个工作模板代码。</span><span class="sxs-lookup"><span data-stu-id="c72ff-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="c72ff-121">如果没有提供任何数值，请使用系统中配置的标准规则来解决工作模板问题。</span><span class="sxs-lookup"><span data-stu-id="c72ff-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="c72ff-122">选定工作模板将会限制此处置码的使用过程。</span><span class="sxs-lookup"><span data-stu-id="c72ff-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="c72ff-123">例如，如果处置码有一个带采购订单类型的工作指令的工作模板，则其不能用于登记被客户退回的物料。</span><span class="sxs-lookup"><span data-stu-id="c72ff-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="c72ff-124">在“退货处置码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c72ff-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="c72ff-125">退货处置码可以确定已登记物料的退货单流程的剩余部分。</span><span class="sxs-lookup"><span data-stu-id="c72ff-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="c72ff-126">在本示例中，客户应收到贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="c72ff-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="c72ff-127">添加包含信贷行为的退货处置码。</span><span class="sxs-lookup"><span data-stu-id="c72ff-127">Add a returns disposition code that contains an action Credit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]