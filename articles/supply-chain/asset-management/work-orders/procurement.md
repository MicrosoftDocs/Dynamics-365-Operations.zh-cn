---
title: 采购
description: 本主题介绍资产管理中的采购。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875523"
---
# <a name="procurement"></a><span data-ttu-id="03039-103">采购</span><span class="sxs-lookup"><span data-stu-id="03039-103">Procurement</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="03039-104">在资产管理中，可获取与工作订单关联的采购申请和采购订单的概览。</span><span class="sxs-lookup"><span data-stu-id="03039-104">In Asset Management, you can get an overview of purchase requisitions and purchase orders related to work orders.</span></span> <span data-ttu-id="03039-105">还可以基于工作订单创建采购订单或采购申请。</span><span class="sxs-lookup"><span data-stu-id="03039-105">It is also possible to create a purchase order or a purchase requisition from a work order.</span></span>

<span data-ttu-id="03039-106">在**工作订单采购申请**列表（**资产管理** > **常用** > **采购** > **工作订单采购申请**）中，可查看与工作订单关联的采购申请的列表。</span><span class="sxs-lookup"><span data-stu-id="03039-106">In the **Work order purchase requisition** list (**Asset management** > **Common** > **Procurement** > **Work order purchase requisition**), you see a list of purchase requisitions related to work orders.</span></span>

- <span data-ttu-id="03039-107">在**工作订单采购申请**列表中选择一个工作订单作业，然后单击**采购申请**可打开关联的采购申请。</span><span class="sxs-lookup"><span data-stu-id="03039-107">Select a work order job in the **Work order purchase requisition** list, and click the **Purchase requisition** button to open the related purchase requisition.</span></span>  
- <span data-ttu-id="03039-108">在**工作订单采购申请**列表中选择一个工作订单作业，然后单击**工作订单**可打开关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="03039-108">Select a work order job in the **Work order purchase requisition** list, and click the **Work order** button to open the related work order.</span></span>  
- <span data-ttu-id="03039-109">如果要获取有关在与资产、维护作业类型默认、备件和工作订单关联时，所选行的物料在资产管理中何处使用的概览，请在**工作订单采购申请**列表中选择一个工作订单作业，然后单击**物料的使用位置**按钮。</span><span class="sxs-lookup"><span data-stu-id="03039-109">Select a work order job in the **Work order purchase requisition** list, and click the **Item where used** button if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 

![图 1](media/08-work-orders.png)


<span data-ttu-id="03039-111">在**工作订单采购申请**列表（**企业资产管理** > **常用** > **采购** > **工作订单采购**）中，可查看与工作订单关联的采购订单的列表。</span><span class="sxs-lookup"><span data-stu-id="03039-111">In the **Work order purchase** list (**Enterprise asset management** > **Common** > **Procurement** > **Work order purchase**), you can see a list of purchase orders related to work orders.</span></span>

- <span data-ttu-id="03039-112">在**工作订单采购申请**列表中选择一个工作订单作业，然后单击**采购订单**可打开关联的采购订单。</span><span class="sxs-lookup"><span data-stu-id="03039-112">Select a work order job in the **Work order purchase** list, and click the **Purchase order** button to open the related purchase order.</span></span>  
- <span data-ttu-id="03039-113">在**工作订单采购**列表中选择一个工作订单作业，然后单击**工作订单**可打开关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="03039-113">Select a work order job in the **Work order purchase** list, and click the **Work order** button to open the related work order.</span></span>  
- <span data-ttu-id="03039-114">如果要获取有关在与资产、维护作业类型默认、备件和工作订单关联时，所选行的物料在资产管理中何处使用的概览，请在**工作订单**采购列表中选择一个工作订单作业，然后单击**物料的使用位置**按钮。</span><span class="sxs-lookup"><span data-stu-id="03039-114">Select a work order job in the **Work order** purchase list, and click the **Item where used** button if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 

![图 2](media/09-work-orders.png)


<span data-ttu-id="03039-116">在上面显示的列表中，将在每行右侧放置一个与交货日期控制有关的图标。</span><span class="sxs-lookup"><span data-stu-id="03039-116">In the lists shown above, an icon regarding delivery date control is placed to the right on each line.</span></span> <span data-ttu-id="03039-117">如果此图标显示红色圆圈包起来的感叹号，则表示关联采购申请或采购订单的交货可能延迟。</span><span class="sxs-lookup"><span data-stu-id="03039-117">If the icon shows an exclamation mark in a red circle, it means that delivery on the related purchase requisition or purchase order may be delayed.</span></span>

<span data-ttu-id="03039-118">在采购申请中，**采购申请**窗体 > **采购申请标题**快速选项卡 > **请求日期**字段中显示用于计算可能的延迟的日期。</span><span class="sxs-lookup"><span data-stu-id="03039-118">On a purchase requisition, the date used to calculate possible delay is found in the **Purchase requisitions** form > **Purchase requisition header** FastTab > **Requested date** field.</span></span> <span data-ttu-id="03039-119">将按照与采购订单日期相同的方式把该日期与工作订单或工作订单作业的可用日期进行比较。</span><span class="sxs-lookup"><span data-stu-id="03039-119">That date is compared to the available date on the work order or work order job in the same way as the purchase order date.</span></span>

<span data-ttu-id="03039-120">在采购订单中，用于计算可能的延迟的日期是与采购订单行关联的日期，其在**采购订单**窗体中 > 选择采购订单行 > **行详细信息**快速选项卡 > **设置**选项卡 > **确认的交货日期**字段中显示。</span><span class="sxs-lookup"><span data-stu-id="03039-120">On a purchase order, the date used to calculate possible delay is the date related to the purchase order line, which shown in the **Purchase order** form > select purchase order line > **Line details** FastTab > **Setup** tab > **Confirmed delivery date** field.</span></span> <span data-ttu-id="03039-121">如果不填写该字段，将使用**采购订单标题**快速选项卡上**交货日期**字段中的日期。</span><span class="sxs-lookup"><span data-stu-id="03039-121">If that field is not filled out, the date in the **Delivery date** field on the **Purchase order header** FastTab is used.</span></span> <span data-ttu-id="03039-122">将按照以下顺序把这些日期之一与工作订单或工作订单作业的可用日期进行比较：</span><span class="sxs-lookup"><span data-stu-id="03039-122">One of those dates is compared to the available date on the work order or work order job in the following order:</span></span>

- <span data-ttu-id="03039-123">工作订单的实际开始日期，或</span><span class="sxs-lookup"><span data-stu-id="03039-123">Actual start date on the work order, or</span></span>  

- <span data-ttu-id="03039-124">关联的工作订单作业的计划开始日期，或</span><span class="sxs-lookup"><span data-stu-id="03039-124">Scheduled start date on the related work order job, or</span></span>  

- <span data-ttu-id="03039-125">工作订单的计划开始日期，或</span><span class="sxs-lookup"><span data-stu-id="03039-125">Scheduled start date on the work order, or</span></span>  

- <span data-ttu-id="03039-126">工作订单的预计开始日期</span><span class="sxs-lookup"><span data-stu-id="03039-126">Expected start date on the work order</span></span>  


## <a name="create-purchase-order-from-a-work-order"></a><span data-ttu-id="03039-127">基于工作订单创建采购订单</span><span class="sxs-lookup"><span data-stu-id="03039-127">Create purchase order from a work order</span></span>

<span data-ttu-id="03039-128">在**所有工作订单**中，选择一个工作订单作业，然后创建关联的采购订单或采购申请。</span><span class="sxs-lookup"><span data-stu-id="03039-128">In **All Work orders**, you select a work order job and create a related purchase order or a purchase requisition.</span></span> <span data-ttu-id="03039-129">目的是确保采购订单或采购申请与工作订单之间的项目关联。</span><span class="sxs-lookup"><span data-stu-id="03039-129">This is done to ensure project relations between the purchase order or purchase requisition and the work order.</span></span>

1. <span data-ttu-id="03039-130">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="03039-130">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="03039-131">在**所有工作订单**或**有效工作订单**列表中，选择要为其创建采购订单的工作订单，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="03039-131">In the **All work orders** or **Active work orders** list, select the work order for which you want to create a purchase order, and click **Edit**.</span></span>

3. <span data-ttu-id="03039-132">在**工作订单**窗体 > **工作订单维护作业**快速选项卡上，选择要为其创建采购订单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="03039-132">In the **Work order** form > **Work order maintenance jobs** FastTab, select the work order job for which you want to create the purchase order.</span></span>

4. <span data-ttu-id="03039-133">单击**物料任务** > **基于工作订单作业创建采购订单**。</span><span class="sxs-lookup"><span data-stu-id="03039-133">Click **Item tasks** > **Purchase order from work order job**.</span></span>

5. <span data-ttu-id="03039-134">在**项目采购订单**列表页中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="03039-134">In the **Project purchase orders** list page, click **New**.</span></span>

6. <span data-ttu-id="03039-135">创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="03039-135">Create the purchase order.</span></span>

>[!NOTE]
><span data-ttu-id="03039-136">创建采购申请与创建采购订单几乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="03039-136">Creating a purchase requisition is almost identical to creating a purchase order.</span></span> <span data-ttu-id="03039-137">唯一区别是，在上面的过程中，在步骤 2 中单击的是**物料任务** > **基于工作订单作业创建采购申请**。</span><span class="sxs-lookup"><span data-stu-id="03039-137">The only difference is that in the above procedure, you click **Item tasks** > **Purchase requisition from work order job** in step 2.</span></span>

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a><span data-ttu-id="03039-138">工作订单与采购订单或采购申请之间的项目关联</span><span class="sxs-lookup"><span data-stu-id="03039-138">Project relation between work order and purchase order or purchase requisition</span></span>

<span data-ttu-id="03039-139">采购订单行或采购申请行通过工作订单项目和关联的项目活动编号与工作订单作业关联。</span><span class="sxs-lookup"><span data-stu-id="03039-139">A purchase order line or purchase requisition line is related to a work order job via the work order project and the related project activity number.</span></span> <span data-ttu-id="03039-140">基于工作订单作业创建采购订单或采购申请时，必须指定关联的项目活动编号。</span><span class="sxs-lookup"><span data-stu-id="03039-140">When you create a purchase order or purchase requisition from a work order job, the related project activity number is mandatory.</span></span> <span data-ttu-id="03039-141">如果关联的工作订单中包含全部使用相同维护作业类型的工作订单作业，则在采购订单或采购申请中自动插入项目活动编号。</span><span class="sxs-lookup"><span data-stu-id="03039-141">The project activity number is automatically inserted on a purchase order or purchase requisition if the related work order contains work order jobs that all use the same maintenance job type.</span></span> <span data-ttu-id="03039-142">如果工作订单作业中包含不同维护作业类型，则必须手动插入项目活动编号。</span><span class="sxs-lookup"><span data-stu-id="03039-142">If the work order jobs contain different maintenance job types, the project activity number must be inserted manually.</span></span>

<span data-ttu-id="03039-143">若要查看或插入与采购订单行关联的活动编号，请打开**工作订单采购** > 选择采购订单记录 > 在**采购订单**列中单击采购订单 > **行详细信息**快速选项卡 > **项目**选项卡 > **活动编号**字段。</span><span class="sxs-lookup"><span data-stu-id="03039-143">To see or insert the activity number related to a purchase order line, open **Work order purchase** > select the purchase order record > click on the purchase order in the **Purchase order** column > **Line details** FastTab > **Project** tab > **Activity number** field.</span></span>


![图 3](media/10-work-orders.png)


<span data-ttu-id="03039-145">同样，若要查看或插入与工作订单采购申请行关联的活动编号，请打开**工作订单采购申请** > 选择采购申请记录 > 在**采购申请**列中单击采购申请 > **行详细信息**快速选项卡 > **项目**选项卡 > **活动编号**字段。</span><span class="sxs-lookup"><span data-stu-id="03039-145">Likewise, to see or insert the activity number related to a work order purchase requisition line, open **Work order purchase requisition** > select the purchase requisition record > click on the purchase requisition in the **Purchase requisition** column > **Line details** FastTab > **Project** tab > **Activity number** field.</span></span>

