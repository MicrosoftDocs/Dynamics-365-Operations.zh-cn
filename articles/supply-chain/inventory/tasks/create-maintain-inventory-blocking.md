---
title: 创建和维护库存锁定
description: 本主题介绍如何使用库存锁定防止实际现有库存量被其他出站源单据预留。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956150"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="acf9d-103">创建和维护库存锁定</span><span class="sxs-lookup"><span data-stu-id="acf9d-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acf9d-104">本主题介绍如何使用库存锁定防止实际现有库存量被其他出站源单据预留。</span><span class="sxs-lookup"><span data-stu-id="acf9d-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="acf9d-105">在开始本主题中的过程之前，您必须有可以达到实际现有库存量的物料。</span><span class="sxs-lookup"><span data-stu-id="acf9d-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="acf9d-106">锁定库存</span><span class="sxs-lookup"><span data-stu-id="acf9d-106">Block inventory</span></span>

<span data-ttu-id="acf9d-107">要创建库存锁定记录以锁定库存，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="acf9d-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="acf9d-108">转到 **库存管理 \> 定期任务 \> 库存锁定**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="acf9d-109">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="acf9d-110">在新锁定记录的标头上，将 **物料编号** 字段设置为要锁定的物料，然后输入描述。</span><span class="sxs-lookup"><span data-stu-id="acf9d-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="acf9d-111">在 **常规** 快速选项卡上，在 **数量** 字段中，输入要锁定的物料数量。</span><span class="sxs-lookup"><span data-stu-id="acf9d-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="acf9d-112">在 **库存维度** 快速选项卡上，指定您要锁定的物料当前所在的站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="acf9d-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="acf9d-113">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="acf9d-114">更新库存锁定的条件</span><span class="sxs-lookup"><span data-stu-id="acf9d-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="acf9d-115">要更新库存锁定记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="acf9d-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="acf9d-116">转到 **库存管理 \> 定期任务 \> 库存锁定**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="acf9d-117">在列表窗格中，选择相关的锁定记录。</span><span class="sxs-lookup"><span data-stu-id="acf9d-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="acf9d-118">根据需要编辑记录。</span><span class="sxs-lookup"><span data-stu-id="acf9d-118">Edit the record as required.</span></span> <span data-ttu-id="acf9d-119">例如，您可以更改 **预期日期** 字段的值，来指示被锁定的库存预计在何时可以预留。</span><span class="sxs-lookup"><span data-stu-id="acf9d-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="acf9d-120">如果选择了 **预期收货** 选项，此日期将出现在预期交易中。</span><span class="sxs-lookup"><span data-stu-id="acf9d-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="acf9d-121">（**预期收货** 选项在您手动创建锁定记录时默认选择。）</span><span class="sxs-lookup"><span data-stu-id="acf9d-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="acf9d-122">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="acf9d-123">解锁库存</span><span class="sxs-lookup"><span data-stu-id="acf9d-123">Unblock inventory</span></span>

<span data-ttu-id="acf9d-124">要删除库存锁定记录以解锁库存，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="acf9d-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="acf9d-125">转到 **库存管理 \> 定期任务 \> 库存锁定**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="acf9d-126">在列表窗格中，选择相关的锁定记录。</span><span class="sxs-lookup"><span data-stu-id="acf9d-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="acf9d-127">在操作窗格上，选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="acf9d-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="acf9d-128">系统将提示您确认操作。</span><span class="sxs-lookup"><span data-stu-id="acf9d-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="acf9d-129">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="acf9d-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="acf9d-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="acf9d-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
