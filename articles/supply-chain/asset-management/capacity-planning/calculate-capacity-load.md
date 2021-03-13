---
title: 计算产能负荷
description: 本主题介绍如何在资产管理中计算产能负荷。
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3aa87f5594be079144142296cac977b0bfdd125e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022575"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="cd953-103">计算产能负荷</span><span class="sxs-lookup"><span data-stu-id="cd953-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="cd953-104">在资产管理中，可计算以下对象的产能负荷：</span><span class="sxs-lookup"><span data-stu-id="cd953-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="cd953-105">维护安排行</span><span class="sxs-lookup"><span data-stu-id="cd953-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="cd953-106">尚未安排的工作订单</span><span class="sxs-lookup"><span data-stu-id="cd953-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="cd953-107">已计划的工作订单</span><span class="sxs-lookup"><span data-stu-id="cd953-107">scheduled work orders</span></span>

<span data-ttu-id="cd953-108">如果要获取特定期间的预计产能负荷的概览，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="cd953-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="cd953-109">可以计算所有资产或所选资产的产能负荷。</span><span class="sxs-lookup"><span data-stu-id="cd953-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="cd953-110">也可以对维护停机时间活动或工作订单池进行计算。</span><span class="sxs-lookup"><span data-stu-id="cd953-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="cd953-111">单击 **资产管理** > **查询** > **产能负荷**，或 **资产管理** > **常用** > **工作订单池** > **所有工作订单池** / **有效的工作订单池** > 在列表中选择工作订单池 > **产能负荷** 按钮，或 **资产管理** > **常用** > **维护停机时间活动** > **所有维护停机时间活动** / **有效的维护停机时间活动** > 在列表中选择维护活动 > **产能负荷** 按钮。</span><span class="sxs-lookup"><span data-stu-id="cd953-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="cd953-112">在 **计算产能负荷** 对话框的 **开始日期/时间** 和 **结束日期/时间** 字段中，为计算选择期间。</span><span class="sxs-lookup"><span data-stu-id="cd953-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="cd953-113">如果要在计算中包括维护安排行，请在 **包括维护安排** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cd953-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="cd953-114">如果要在计算中包括工作订单作业，请在 **包括工作订单** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cd953-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="cd953-115">可使用 **级别** 字段指示要与功能位置有关的产能负荷行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="cd953-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="cd953-116">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行和工作订单，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="cd953-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="cd953-117">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护安排行和所有工作订单行。</span><span class="sxs-lookup"><span data-stu-id="cd953-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="cd953-118">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="cd953-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="cd953-119">在 **分组依据...** 组中，单击相关按钮显示所需成本计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="cd953-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="cd953-120">在下面的屏幕截图中，选中的 **分组依据** 按钮以蓝色突出显示。</span><span class="sxs-lookup"><span data-stu-id="cd953-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="cd953-121">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="cd953-121">Click on a button to activate or deactivate it.</span></span>

    ![图 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="cd953-123">如果要仅侧重有关计划的工作订单的产能计划，请参阅[对计划的工作订单计算产能负荷](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md)。</span><span class="sxs-lookup"><span data-stu-id="cd953-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

