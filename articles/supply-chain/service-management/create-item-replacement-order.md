---
title: 创建物料更换单
description: 在退回和检查产品后，通常创建物料更换单。
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63c175d12cac91648cb57a3f41d1769e81d57af
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830091"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="8624d-103">创建物料更换单</span><span class="sxs-lookup"><span data-stu-id="8624d-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8624d-104">在退回和检查产品后，通常创建物料更换单。</span><span class="sxs-lookup"><span data-stu-id="8624d-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="8624d-105">但是，当物料必须在退回前更换或将不退回原始物料时，可以在创建退货单后立即创建物料更换单。</span><span class="sxs-lookup"><span data-stu-id="8624d-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="8624d-106">收到退回的物料后，创建更换单。</span><span class="sxs-lookup"><span data-stu-id="8624d-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="8624d-107">单击**销售和市场营销** \> **通用** \> **退货单** \> **所有退货单**。</span><span class="sxs-lookup"><span data-stu-id="8624d-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="8624d-108">创建新的退货单，或从列表中选择已退货的订单以打开**退货单 - 物料退回授权号: %1、%2** 窗体。</span><span class="sxs-lookup"><span data-stu-id="8624d-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="8624d-109">单击**退货行**，然后选择**更换物料**。</span><span class="sxs-lookup"><span data-stu-id="8624d-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="8624d-110">选择要替换退回的物料的物料。</span><span class="sxs-lookup"><span data-stu-id="8624d-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="8624d-111">输入物料描述，然后单击**应用**。</span><span class="sxs-lookup"><span data-stu-id="8624d-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="8624d-112">单击**装箱单**以便为退货单生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="8624d-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="8624d-113">已为您选择的更换物料生成销售订单。</span><span class="sxs-lookup"><span data-stu-id="8624d-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="8624d-114">为更换物料创建销售订单后，将自动搜索销售协议，如果有适用的销售协议，系统会将其应用到销售订单。</span><span class="sxs-lookup"><span data-stu-id="8624d-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="8624d-115">在接收到将退回的物料前，创建更换单。</span><span class="sxs-lookup"><span data-stu-id="8624d-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="8624d-116">单击**销售和市场营销** \> **通用** \> **退货单** \> **所有退货单**。</span><span class="sxs-lookup"><span data-stu-id="8624d-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="8624d-117">创建新的退货单，或从列表中选择退货订单以打开**退货单 - 物料退回授权号: %1、%2** 窗体。</span><span class="sxs-lookup"><span data-stu-id="8624d-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="8624d-118">如果您要标识已退回物料的销售订单，请单击**查找销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8624d-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="8624d-119">完成**查找销售订单**窗体，然后单击**确定**以关闭该窗体并回到**退货单 - 物料退回授权号: %1、%2** 窗体。</span><span class="sxs-lookup"><span data-stu-id="8624d-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="8624d-120">已退回物料的销售订单行复制到退货单。</span><span class="sxs-lookup"><span data-stu-id="8624d-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="8624d-121">单击**更换单**以打开**创建销售订单**窗体。</span><span class="sxs-lookup"><span data-stu-id="8624d-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="8624d-122">选中**复制退货单行**复选框以将您在**退货单 - 物料退回授权号: %1、%2** 窗体上选择的退货单的详细信息转移到此销售订单。</span><span class="sxs-lookup"><span data-stu-id="8624d-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="8624d-123">必要时输入或修改详细信息。</span><span class="sxs-lookup"><span data-stu-id="8624d-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="8624d-124">如果您在步骤 3 标识销售订单，以及如果已退回物料的销售订单行与销售协议关联，物料更换单的适用销售协议的标识符将自动显示在**销售协议 ID** 字段中。</span><span class="sxs-lookup"><span data-stu-id="8624d-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="8624d-125">单击**确定**以关闭**创建销售订单**窗体并打开**销售订单**窗体，其中您可以继续为新的销售订单输入信息。</span><span class="sxs-lookup"><span data-stu-id="8624d-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="8624d-126">所有适用的退货单行将复制到新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="8624d-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="8624d-127">如果销售协议的标识符将自动显示在**销售协议 ID** 字段中，则销售协议已与物料更换单的销售订单标题关联。</span><span class="sxs-lookup"><span data-stu-id="8624d-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="8624d-128">如果销售协议中存在尚未履行的承诺，并且销售订单在销售协议过期之前创建，则关联在销售协议行和销售订单行之间建立。</span><span class="sxs-lookup"><span data-stu-id="8624d-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="8624d-129">因此，销售协议中的信息（如，物料价格）复制到新的销售订单行。</span><span class="sxs-lookup"><span data-stu-id="8624d-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


