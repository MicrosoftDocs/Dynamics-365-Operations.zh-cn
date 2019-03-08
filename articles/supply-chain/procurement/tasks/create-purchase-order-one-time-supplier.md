---
title: 创建零星供应商的采购订单
description: 此过程演示如何为零星供应商创建采购订单。
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beaf6bcbc870e11e74289375611c631306545633
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "312868"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="5f425-103">创建零星供应商的采购订单</span><span class="sxs-lookup"><span data-stu-id="5f425-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f425-104">此过程演示如何为零星供应商创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="5f425-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="5f425-105">供应商随采购订单自动创建，而不必手动创建供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="5f425-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="5f425-106">采购订单通常由采购代理创建。</span><span class="sxs-lookup"><span data-stu-id="5f425-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="5f425-107">可以在 USMF 演示数据公司中使用本指南中的示例。</span><span class="sxs-lookup"><span data-stu-id="5f425-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="5f425-108">前提是已在“应付账款参数”页中设置了零星供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="5f425-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="5f425-109">创建零星供应商的采购订单</span><span class="sxs-lookup"><span data-stu-id="5f425-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="5f425-110">转到“采购”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="5f425-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5f425-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5f425-111">Click New.</span></span>
3. <span data-ttu-id="5f425-112">在“零星供应商”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5f425-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="5f425-113">将自动创建供应商帐户并分配给采购订单。</span><span class="sxs-lookup"><span data-stu-id="5f425-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="5f425-114">供应商帐户基于“应付账款参数”页中“常规”选项卡上指定的模板创建供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="5f425-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="5f425-115">在“名称”字段中，键入该供应商的名称。</span><span class="sxs-lookup"><span data-stu-id="5f425-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="5f425-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5f425-116">Click OK.</span></span>
    * <span data-ttu-id="5f425-117">采购订单现在可以和其他任何订单一样完成和处理。</span><span class="sxs-lookup"><span data-stu-id="5f425-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="5f425-118">方法没有任何特别特征。</span><span class="sxs-lookup"><span data-stu-id="5f425-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="5f425-119">发票将记录供应商帐户中随订单创建的到期交易，然后处理付款。</span><span class="sxs-lookup"><span data-stu-id="5f425-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="5f425-120">此操作完成后，可以删除供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="5f425-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="5f425-121">这通常由应付账款部门完成。</span><span class="sxs-lookup"><span data-stu-id="5f425-121">This is typically done by the accounts payable department.</span></span>  

