---
title: 设置采购类别层次结构
description: 该过程会显示如何在采购类别层次结构中创建新节点，以及如何配置采购类别以用于采购流程。
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaab2093eb2531b63f27717d828f7064a8f9ed1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207500"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="39604-103">设置采购类别层次结构</span><span class="sxs-lookup"><span data-stu-id="39604-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39604-104">该过程会显示如何在采购类别层次结构中创建新节点，以及如何配置采购类别以用于采购流程。</span><span class="sxs-lookup"><span data-stu-id="39604-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="39604-105">这些任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="39604-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="39604-106">在您开始该过程之前，采购类型层次结构必须存在。</span><span class="sxs-lookup"><span data-stu-id="39604-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="39604-107">如果您正在使用公司演示数据，则您可以在 USMF 公司中执行该过程。</span><span class="sxs-lookup"><span data-stu-id="39604-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="39604-108">添加新采购类别</span><span class="sxs-lookup"><span data-stu-id="39604-108">Add a new procurement category</span></span>
1. <span data-ttu-id="39604-109">转到**导航窗格 > 模块 > 采购 > 托运 > 采购目录**。</span><span class="sxs-lookup"><span data-stu-id="39604-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="39604-110">在操作窗格上选择**编辑类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="39604-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="39604-111">当前采购类别层次结构会显示在页左侧。</span><span class="sxs-lookup"><span data-stu-id="39604-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="39604-112">您即将修改该层次结构。</span><span class="sxs-lookup"><span data-stu-id="39604-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="39604-113">在操作窗格上选择**新建类别模式**。</span><span class="sxs-lookup"><span data-stu-id="39604-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="39604-114">系统会默认选择顶端节点。</span><span class="sxs-lookup"><span data-stu-id="39604-114">The system selects the top node by default.</span></span> <span data-ttu-id="39604-115">如果您正在运行该过程以作为任务指南，您可以单击“解除锁定”按钮，并选择另一个父节点，以插入您的新节点。</span><span class="sxs-lookup"><span data-stu-id="39604-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="39604-116">一旦完成此项操作，再次锁定任务指南，然后单击“新类别节点”。</span><span class="sxs-lookup"><span data-stu-id="39604-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="39604-117">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="39604-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="39604-118">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="39604-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="39604-119">在**易记名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="39604-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="39604-120">易记名称是可选的。</span><span class="sxs-lookup"><span data-stu-id="39604-120">The friendly name is optional.</span></span> <span data-ttu-id="39604-121">它将连同类别名称一起显示在类别查找中。</span><span class="sxs-lookup"><span data-stu-id="39604-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="39604-122">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="39604-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="39604-123">添加产品到您的新采购类别</span><span class="sxs-lookup"><span data-stu-id="39604-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="39604-124">转到**采购和购置 > 托运 > 采购类别**。</span><span class="sxs-lookup"><span data-stu-id="39604-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="39604-125">选择您刚添加的节点。</span><span class="sxs-lookup"><span data-stu-id="39604-125">Select the node you just added.</span></span> <span data-ttu-id="39604-126">如果您正在运行该过程以作为任务指南，您可能需要解除任务指南锁定，以选择节点。</span><span class="sxs-lookup"><span data-stu-id="39604-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="39604-127">切换**产品**部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="39604-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="39604-128">选择**添加**以关联产品和采购类别。</span><span class="sxs-lookup"><span data-stu-id="39604-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="39604-129">选择您想要添加到采购类别的产品。</span><span class="sxs-lookup"><span data-stu-id="39604-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="39604-130">选择箭头以将产品添加到**所选**表中。</span><span class="sxs-lookup"><span data-stu-id="39604-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="39604-131">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="39604-131">Select **OK**.</span></span>
