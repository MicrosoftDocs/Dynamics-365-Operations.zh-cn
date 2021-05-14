---
title: 不符合项操作的费用
description: 本主题介绍如何创建可与不符合项的操作一起使用的质量费用。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956562"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="85cf8-103">不符合项操作的费用</span><span class="sxs-lookup"><span data-stu-id="85cf8-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85cf8-104">本主题介绍如何创建可与不符合项的操作一起使用的质量费用。</span><span class="sxs-lookup"><span data-stu-id="85cf8-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="85cf8-105">您可以使用 **质量费用** 页定义可以向不合格项的操作添加的费用类型。</span><span class="sxs-lookup"><span data-stu-id="85cf8-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="85cf8-106">费用让您可以跟踪您因未达标产品欠客户的费用，或供应商因您收到的未达标产品而欠您的费用的详细信息。</span><span class="sxs-lookup"><span data-stu-id="85cf8-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="85cf8-107">您还可以使用费用跟踪外部供应商或服务执行操作所需的成本。</span><span class="sxs-lookup"><span data-stu-id="85cf8-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="85cf8-108">质量费用示例</span><span class="sxs-lookup"><span data-stu-id="85cf8-108">Examples of quality charges</span></span>

<span data-ttu-id="85cf8-109">您在一家制造公司工作。</span><span class="sxs-lookup"><span data-stu-id="85cf8-109">You work for a manufacturing company.</span></span> <span data-ttu-id="85cf8-110">您的公司与多家供应商签订了合同。</span><span class="sxs-lookup"><span data-stu-id="85cf8-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="85cf8-111">这些合同概括了物料按时装运、损坏和产品质量的标准。</span><span class="sxs-lookup"><span data-stu-id="85cf8-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="85cf8-112">同样，您的一些客户与您的公司已就退货、损坏和产品质量达成协议。</span><span class="sxs-lookup"><span data-stu-id="85cf8-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="85cf8-113">每种情况都定义了费用结构，并在合同中加以指定。</span><span class="sxs-lookup"><span data-stu-id="85cf8-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="85cf8-114">您可以配置质量费用来概括各个费用类型，如 *损坏*、*延迟装运* 和 *质量*。</span><span class="sxs-lookup"><span data-stu-id="85cf8-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="85cf8-115">然后，当您创建不符合项时，您将添加一个或多个操作。</span><span class="sxs-lookup"><span data-stu-id="85cf8-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="85cf8-116">对于每个操作，您选择 **费用** 来定义有关费用的详细信息。</span><span class="sxs-lookup"><span data-stu-id="85cf8-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="85cf8-117">创建质量费用</span><span class="sxs-lookup"><span data-stu-id="85cf8-117">Create a quality charge</span></span>

1. <span data-ttu-id="85cf8-118">转到 **库存管理 \> 设置 \> 质量管理\> 质量费用**。</span><span class="sxs-lookup"><span data-stu-id="85cf8-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="85cf8-119">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="85cf8-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="85cf8-120">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="85cf8-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="85cf8-121">**费用代码** – 为质量费用输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="85cf8-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="85cf8-122">**描述** – 输入质量费用的详细描述。</span><span class="sxs-lookup"><span data-stu-id="85cf8-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="85cf8-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="85cf8-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="85cf8-124">向不符合项的操作添加质量费用</span><span class="sxs-lookup"><span data-stu-id="85cf8-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="85cf8-125">有关如何将操作添加到不符合项并向其应用费用的详细信息，请参阅[不符合项的操作](quality-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="85cf8-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85cf8-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="85cf8-126">Additional resources</span></span>

- [<span data-ttu-id="85cf8-127">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="85cf8-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="85cf8-128">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="85cf8-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="85cf8-129">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="85cf8-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="85cf8-130">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="85cf8-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="85cf8-131">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="85cf8-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="85cf8-132">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="85cf8-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="85cf8-133">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="85cf8-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="85cf8-134">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="85cf8-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
