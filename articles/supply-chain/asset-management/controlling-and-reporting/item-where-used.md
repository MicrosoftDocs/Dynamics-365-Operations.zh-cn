---
title: 物料的使用位置
description: 本主题介绍如何在资产管理中获取有关物料使用位置的概览。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511108e689c10e27a42253d95b02e5394f9eb713
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652348"
---
# <a name="item-where-used"></a><span data-ttu-id="623e1-103">物料的使用位置</span><span class="sxs-lookup"><span data-stu-id="623e1-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="623e1-104">可对特定物料进行计算，以便在资产管理中获取有关物料使用位置的概览。</span><span class="sxs-lookup"><span data-stu-id="623e1-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="623e1-105">结果显示物料在其生命周期内的使用上下文。</span><span class="sxs-lookup"><span data-stu-id="623e1-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="623e1-106">**物料使用位置**页可以从资产管理主菜单打开，也可以从以下页访问：</span><span class="sxs-lookup"><span data-stu-id="623e1-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="623e1-107">资产物料清单</span><span class="sxs-lookup"><span data-stu-id="623e1-107">Asset BOM</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="623e1-108">资产类型默认的备件</span><span class="sxs-lookup"><span data-stu-id="623e1-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

- [<span data-ttu-id="623e1-109">维护作业类型默认预测的物料预测</span><span class="sxs-lookup"><span data-stu-id="623e1-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="623e1-110">工作订单维护预告</span><span class="sxs-lookup"><span data-stu-id="623e1-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="623e1-111">工作订单采购申请</span><span class="sxs-lookup"><span data-stu-id="623e1-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="623e1-112">工作订单采购</span><span class="sxs-lookup"><span data-stu-id="623e1-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="623e1-113">创建物料使用位置计算</span><span class="sxs-lookup"><span data-stu-id="623e1-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="623e1-114">单击**资产管理** > **查询** > **物料使用位置**，或在上面介绍的页面之一中选择**物料使用位置**按钮。</span><span class="sxs-lookup"><span data-stu-id="623e1-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="623e1-115">在**物料使用位置**对话框的**物料编号**字段中，选择要为其创建计算的物料。</span><span class="sxs-lookup"><span data-stu-id="623e1-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="623e1-116">可使用**级别**字段指示要与功能位置有关的物料行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="623e1-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="623e1-117">例如，如果在此字段中插入数字“1”，并且采用了多级别功能位置结构，则在最上级别显示功能位置的所有物料行。</span><span class="sxs-lookup"><span data-stu-id="623e1-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="623e1-118">因此，可以从较低级别的功能位置开始叠加行中的关联/数量。</span><span class="sxs-lookup"><span data-stu-id="623e1-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="623e1-119">如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有物料行。</span><span class="sxs-lookup"><span data-stu-id="623e1-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="623e1-120">在**包括**部分中，在要包括到计算中的切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="623e1-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="623e1-121">单击**确定**开始计算。</span><span class="sxs-lookup"><span data-stu-id="623e1-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="623e1-122">在**物料使用位置**选项卡上，选择**分组依据**按钮可以显示所需计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="623e1-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="623e1-123">将突出显示所选**分组依据**按钮。</span><span class="sxs-lookup"><span data-stu-id="623e1-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="623e1-124">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="623e1-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="623e1-125">如果要显示与物料关联的维度，请单击**显示维度**，然后选择要显示的维度。</span><span class="sxs-lookup"><span data-stu-id="623e1-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="623e1-126">示例</span><span class="sxs-lookup"><span data-stu-id="623e1-126">Example</span></span>

<span data-ttu-id="623e1-127">在下面的屏幕截图中，可以看到编号为“1000”的物料的物料使用位置计算的示例。</span><span class="sxs-lookup"><span data-stu-id="623e1-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![使用位置计算的物料的示例](media/12-controlling-and-reporting.png)

