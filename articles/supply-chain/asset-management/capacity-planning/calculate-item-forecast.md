---
title: 计算物料预测
description: 本主题介绍如何在资产管理中计算物料预测。
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1cea3b6cfd42348285985122ae905f8ea9f3facb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260026"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="af63c-103">计算物料预测</span><span class="sxs-lookup"><span data-stu-id="af63c-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="af63c-104">就像可以创建上一部分中介绍的产能负荷计算，也可以为以下对象创建物料预测计算：</span><span class="sxs-lookup"><span data-stu-id="af63c-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="af63c-105">维护安排行</span><span class="sxs-lookup"><span data-stu-id="af63c-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="af63c-106">尚未安排的工作订单</span><span class="sxs-lookup"><span data-stu-id="af63c-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="af63c-107">已计划的工作订单</span><span class="sxs-lookup"><span data-stu-id="af63c-107">scheduled work orders</span></span>

<span data-ttu-id="af63c-108">如果要获取特定期间的预计物料消耗（为了完成工作订单需要的备件和其他物料）的概览，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="af63c-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="af63c-109">可以计算所有资产或所选资产的物料预测。</span><span class="sxs-lookup"><span data-stu-id="af63c-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="af63c-110">也可以为维护停机时间活动（**所有维护停机时间活动** 或 **有效维护停机时间活动**）或工作订单池（**所有工作订单池** 或 **有效工作订单池**）创建计算。</span><span class="sxs-lookup"><span data-stu-id="af63c-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="af63c-111">单击 **资产管理** > **查询** > **物料预测**，或 **资产管理** > **常用** > **工作订单池** > **所有工作订单池** / **有效的工作订单池** > 在列表中选择工作订单池 > **物料预测** 按钮，或 **资产管理** > **常用** > **维护停机时间活动** > **所有维护停机时间活动** / **有效的维护停机时间活动** > 在列表中选择维护停机时间活动 > **物料预测** 按钮。</span><span class="sxs-lookup"><span data-stu-id="af63c-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="af63c-112">在 **计算物料预测** 对话框的 **开始日期/时间** 和 **结束日期/时间** 字段中，为计算选择期间。</span><span class="sxs-lookup"><span data-stu-id="af63c-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="af63c-113">如果要在预测计算中包括维护安排行，请在 **包括维护安排** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="af63c-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="af63c-114">如果要在预测计算中包括工作订单作业，请在 **包括工作订单** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="af63c-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="af63c-115">可使用 **级别** 字段指示要与功能位置有关的物料预测行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="af63c-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="af63c-116">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行和工作订单，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="af63c-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="af63c-117">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护安排行和所有工作订单行。</span><span class="sxs-lookup"><span data-stu-id="af63c-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="af63c-118">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="af63c-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="af63c-119">在 **分组依据...** 组中，单击相关按钮显示所需成本计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="af63c-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="af63c-120">在下面的屏幕截图中，选中的 **分组依据** 按钮以蓝色突出显示。</span><span class="sxs-lookup"><span data-stu-id="af63c-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="af63c-121">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="af63c-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="af63c-122">如果要查看与物料关联的产品、存储或跟踪维度，请单击 **显示维度** 按钮。</span><span class="sxs-lookup"><span data-stu-id="af63c-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="af63c-123">选中相关复选框，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="af63c-123">Select the relevant check boxes, and click **OK**.</span></span>

![图 1](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]