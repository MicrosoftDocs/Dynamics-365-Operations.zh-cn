---
title: 航行状态设置
description: 本主题介绍如何建立用户可以分配给航行的状态值。
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022100"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="ebcd5-103">航行状态设置</span><span class="sxs-lookup"><span data-stu-id="ebcd5-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebcd5-104">在 **航行状态** 页上，建立用户可以分配给航行的状态值集。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="ebcd5-105">用户可以将航行状态值分配给航行的所有级别：航行、装运集装箱、帐页、采购订单和物料（采购订单行和转移单行）。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="ebcd5-106">它们用于两个目的：</span><span class="sxs-lookup"><span data-stu-id="ebcd5-106">They are used for two purposes:</span></span>

- <span data-ttu-id="ebcd5-107">通知用户航行、装运集装箱、帐页、采购订单或物料（采购订单行和转移单行）的状态。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="ebcd5-108">通过阻止修改或删除限制成本区域的使用。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="ebcd5-109">要设置航行状态，转到 **登陆成本 \> 设置 \> 航行状态**。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="ebcd5-110">在那里，您可以使用操作窗格上的按钮添加、删除和编辑状态。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="ebcd5-111">每个成本区域有自己的航行状态集和层次结构。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="ebcd5-112">因此，在 **航行状态** 页上，在 **成本区域** 字段中，您必须首先选择要查看或为其创建航行状态的成本区域。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="ebcd5-113">然后，对于每个航行状态，根据需要设置下表中所述的字段。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="ebcd5-114">请注意，航行状态还可以由系统事件自动更改，如使用跟踪控制中心建立的规则。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="ebcd5-115">字段</span><span class="sxs-lookup"><span data-stu-id="ebcd5-115">Field</span></span> | <span data-ttu-id="ebcd5-116">说明</span><span class="sxs-lookup"><span data-stu-id="ebcd5-116">Description</span></span> |
|---|---|
| <span data-ttu-id="ebcd5-117">航行状态</span><span class="sxs-lookup"><span data-stu-id="ebcd5-117">Voyage status</span></span> | <span data-ttu-id="ebcd5-118">输入航行状态的名称。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="ebcd5-119">说明</span><span class="sxs-lookup"><span data-stu-id="ebcd5-119">Description</span></span> | <span data-ttu-id="ebcd5-120">输入航行状态的描述。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="ebcd5-121">修改</span><span class="sxs-lookup"><span data-stu-id="ebcd5-121">Modify</span></span> | <span data-ttu-id="ebcd5-122">如果允许用户修改具有此状态的航行，选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="ebcd5-123">Delete</span><span class="sxs-lookup"><span data-stu-id="ebcd5-123">Delete</span></span> | <span data-ttu-id="ebcd5-124">如果允许用户删除具有此状态的航行，选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="ebcd5-125">强制</span><span class="sxs-lookup"><span data-stu-id="ebcd5-125">Mandatory</span></span> | <span data-ttu-id="ebcd5-126">选中此复选框可以让航行状态变为强制信息，这样不会被跳过。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="ebcd5-127">父对象</span><span class="sxs-lookup"><span data-stu-id="ebcd5-127">Parent</span></span> | <span data-ttu-id="ebcd5-128">使用此字段可以在状态值之间建立层次结构。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="ebcd5-129">航行状态只能在层次结构中从父状态向下更改为子状态之一（手动或自动）。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="ebcd5-130">您只需要设置组织使用的特定航行状态。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="ebcd5-131">典型的航行状态包括 *已确认*、*在途货物*、*已接收*、*成本计算就绪* 和 *已计算成本*。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="ebcd5-132">但是，其他状态可能会显示。</span><span class="sxs-lookup"><span data-stu-id="ebcd5-132">However, other statuses might be present.</span></span>
