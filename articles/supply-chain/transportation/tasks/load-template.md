---
title: 负荷模板
description: 本主题介绍如何设置负荷模板以及如何将负荷模板与新负荷关联。
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 175c8017b14cc298cdaa00031f8450015a747786
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831498"
---
# <a name="load-templates"></a><span data-ttu-id="360f7-103">负荷模板</span><span class="sxs-lookup"><span data-stu-id="360f7-103">Load templates</span></span>

<span data-ttu-id="360f7-104">创建新负荷时，您可以分配负荷模板。</span><span class="sxs-lookup"><span data-stu-id="360f7-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="360f7-105">负荷模板包含有关设备以及度量（例如负荷的高度、宽度、深度和体积）的信息。</span><span class="sxs-lookup"><span data-stu-id="360f7-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="360f7-106">本主题介绍如何设置负荷模板以及如何将负荷模板与新负荷关联。</span><span class="sxs-lookup"><span data-stu-id="360f7-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="360f7-107">设置负荷模板</span><span class="sxs-lookup"><span data-stu-id="360f7-107">Set up a load template</span></span>

1. <span data-ttu-id="360f7-108">转到 **运输管理 \> 设置 \> 负荷构建 \> 负荷模板**。</span><span class="sxs-lookup"><span data-stu-id="360f7-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="360f7-109">在操作窗格上，选择 **新建** 以添加新模板，或选择 **编辑** 以编辑现有模板。</span><span class="sxs-lookup"><span data-stu-id="360f7-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="360f7-110">在新模板或现有模板的行中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="360f7-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="360f7-111">**负荷模板 ID** – 输入负荷模板的唯一标识符 (ID)。</span><span class="sxs-lookup"><span data-stu-id="360f7-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="360f7-112">**设备** – 选择应该用于装运负荷的设备。</span><span class="sxs-lookup"><span data-stu-id="360f7-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="360f7-113">**负荷高度**、**负荷宽度** 和 **负荷深度** – 输入负荷的维度。</span><span class="sxs-lookup"><span data-stu-id="360f7-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="360f7-114">**允许的最大负荷体积** 和 **允许的最大负荷重量** – 输入允许的最大负荷体积和重量。</span><span class="sxs-lookup"><span data-stu-id="360f7-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="360f7-115">**允许的最大毛重** – 输入允许的最大负荷毛重。</span><span class="sxs-lookup"><span data-stu-id="360f7-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="360f7-116">负荷的毛重包括其皮重和负荷重量。</span><span class="sxs-lookup"><span data-stu-id="360f7-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="360f7-117">**允许的最大货运件数** – 输入负荷可包含的最大货运件数。</span><span class="sxs-lookup"><span data-stu-id="360f7-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="360f7-118">**地面堆叠负荷** – 选中此复选框以使用地面负荷。</span><span class="sxs-lookup"><span data-stu-id="360f7-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="360f7-119">在地面负荷方案中，箱子从地面到天花板，从一面墙到另一面墙堆叠在集装箱内，以最大化容量。</span><span class="sxs-lookup"><span data-stu-id="360f7-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="360f7-120">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="360f7-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="360f7-121">将负荷模板与新负荷关联</span><span class="sxs-lookup"><span data-stu-id="360f7-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="360f7-122">转到 **运输管理 \> 计划 \> 负荷计划工作台**。</span><span class="sxs-lookup"><span data-stu-id="360f7-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="360f7-123">在页面的上部，根据要为其创建负荷的源单据的类型，选择以下选项卡之一：**装运**、**销售行**、**转移行** 或 **采购订单行**。</span><span class="sxs-lookup"><span data-stu-id="360f7-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="360f7-124">选择要为其计划负荷的特定单据。</span><span class="sxs-lookup"><span data-stu-id="360f7-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="360f7-125">在操作窗格上 **供应与需求** 选项卡上 **添加** 组中，选择 **至新负荷**。</span><span class="sxs-lookup"><span data-stu-id="360f7-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="360f7-126">在 **负荷模板** 对话框中，在 **负荷模板 ID** 字段中，选择要应用的模板。</span><span class="sxs-lookup"><span data-stu-id="360f7-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="360f7-127">选择 **确定** 以应用模板。</span><span class="sxs-lookup"><span data-stu-id="360f7-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]