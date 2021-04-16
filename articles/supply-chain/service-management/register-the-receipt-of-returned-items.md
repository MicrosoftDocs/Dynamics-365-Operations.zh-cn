---
title: 登记退回物料的接收
description: 可使用“到达概览”窗体或“登记”窗体登记退回物料的接收。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96532173c003621271f768dcdc64d67b6948ab6c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836030"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="f2fc8-103">登记退回物料的接收</span><span class="sxs-lookup"><span data-stu-id="f2fc8-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f2fc8-104">可通过两种方法来登记退回物料的接收。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="f2fc8-105">第一种方法是仓库接收使用 **到达概览** 窗体的流程。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="f2fc8-106">第二种方法是使用 **登记** 窗体。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="f2fc8-107">在“到达概览”窗体中登记退回物料的接收</span><span class="sxs-lookup"><span data-stu-id="f2fc8-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="f2fc8-108">您可以使用 **到达概览** 窗体，以通过其 Return Materials Authorization (RMA) 编号标识退货装运。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="f2fc8-109">如果日志名称在 **设置** 选项卡上定义，且对应于 **到达概览** 窗体上选择的行的日志行存在，则，您单击 **开始到达** 时，创建新的日志标题。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="f2fc8-110">单击 **库存管理** \> **定期** \> **到达概览**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="f2fc8-111">在 **设置名称** 字段中，选择 **退货单**，然后单击 **更新**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="f2fc8-112">可以使用<STRONG>范围</STRONG>字段使搜索范围变窄。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="f2fc8-113">在<STRONG>物料退回授权号</STRONG>字段中键入或选择物料退回授权号则可以得到精确的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="f2fc8-114">若要定义和保存一组用于限制显示哪些传入到达的筛选器，请单击<STRONG>设置</STRONG>选项卡。可用筛选器包括类型、仓库和货台。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="f2fc8-115">退货单不能与<STRONG>到达概览</STRONG>窗体中的其他到达类型混合。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="f2fc8-116">因此，该参考将始终为销售订单，但是不会在日志标题中指定销售订单 ID。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="f2fc8-117">在 **收货** 网格中查找与要退回的物料匹配的行，然后在 **选择用于到达** 列中选中该复选框。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="f2fc8-118">若要从退货接收中排除某些行，如不包括在退回装运货物的原始订单中的物料，请在窗体下半部分的 **行** 表中清除关联的 **选择用于到达** 复选框。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="f2fc8-119">单击 **开始到达** 按钮创建到达日志。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="f2fc8-120">可以选择多个退货单并将它们全部包括在一个到达流程中。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="f2fc8-121">每个退货单行将复制到相应的物料到达日志行。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="f2fc8-122">通过使用<STRONG>物料到达</STRONG>窗体，也可以手动创建到达日志。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="f2fc8-123">单击 **库存管理** \> **日记帐** \> **物料到达** \> **物料到达**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="f2fc8-124">选择您刚创建的到达日志，然后单击 **行** 打开 **日记帐行、库位** 窗体。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="f2fc8-125">如果需要，在 **常规** 选项卡上，调整 **数量** 字段中的编号，然后在 **处置代码** 字段中分配处置代码。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="f2fc8-126">或者，您可以选中 **检验管理** 复选框将退回的物料通过检验单上下文中的检查流程发送。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="f2fc8-127">如果您通过检验发送退回物料，则您不能指定处置代码。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="f2fc8-128">单击 **验证** 按钮。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="f2fc8-129">如果验证过程中没有出错，则单击 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="f2fc8-130">在“登记”窗体中登记退回物料的接收</span><span class="sxs-lookup"><span data-stu-id="f2fc8-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="f2fc8-131">作为使用 **到达概览** 窗体的备选方案，您可以使用 **登记** 窗体登记退回物料的到达。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="f2fc8-132">单击 **销售和市场营销** \> **通用** \> **退货单** \> **所有退货单**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="f2fc8-133">创建新退货单或从该列表中打开退货单。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="f2fc8-134">在 **行** 快速选项卡上，选择该退货单行。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="f2fc8-135">单击 **更新行**，然后单击 **登记**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="f2fc8-136">在 **处置代码** 字段中分配某一处置代码，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="f2fc8-137">无法使用<STRONG>登记</STRONG>窗体为检查发送物料作为检验单。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="f2fc8-138">在 **交易记录** 网格中，选择要登记的交易记录。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="f2fc8-139">在 **立即登记** 网格中，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="f2fc8-140">在所有退回物料出现在 **立即登记** 网格中前，重复前两个步骤。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="f2fc8-141">单击 **全部过帐**。</span><span class="sxs-lookup"><span data-stu-id="f2fc8-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2fc8-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="f2fc8-142">See also</span></span>

<span data-ttu-id="f2fc8-143">[到达概览（窗体）](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="f2fc8-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]