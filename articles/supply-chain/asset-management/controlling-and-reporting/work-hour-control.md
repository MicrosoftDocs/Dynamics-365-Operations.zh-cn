---
title: 工时控制
description: 本主题介绍资产管理中的工时控制。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ac64b0e40662f30cc615dfbd3f05aba5b37d862
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838650"
---
# <a name="work-hour-control"></a><span data-ttu-id="58cd3-103">工时控制</span><span class="sxs-lookup"><span data-stu-id="58cd3-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="58cd3-104">在资产管理中，可计算工时，以便获取资产、功能位置或工作订单的实际工时与预算工时的比较概览。</span><span class="sxs-lookup"><span data-stu-id="58cd3-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="58cd3-105">实际工时基于过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="58cd3-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="58cd3-106">资产、功能位置和工作订单的工时控制</span><span class="sxs-lookup"><span data-stu-id="58cd3-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="58cd3-107">为资产、功能位置和工作订单创建的计算几乎相同。</span><span class="sxs-lookup"><span data-stu-id="58cd3-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="58cd3-108">唯一区别是，对于资产和功能位置，还可以在计算中包括子资产和子位置。</span><span class="sxs-lookup"><span data-stu-id="58cd3-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="58cd3-109">日期是记录登记时的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="58cd3-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="58cd3-110">单击 **资产管理** > **查询** > **资产** > **资产工时控制** 或 **功能位置工时控制**，或 **资产管理** > **查询** > **工作订单** > **工作订单工时控制**。</span><span class="sxs-lookup"><span data-stu-id="58cd3-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="58cd3-111">在 **资产工时控制** 对话框中，</span><span class="sxs-lookup"><span data-stu-id="58cd3-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="58cd3-112">在 **资产工时控制** / **功能位置工时控制** / **工作订单工时控制** 对话框中的 **开始日期** 和 **结束日期** 字段中，选择要计算的期间。</span><span class="sxs-lookup"><span data-stu-id="58cd3-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="58cd3-113">如果需要，选择计算中要包括的 **财务维度集**。</span><span class="sxs-lookup"><span data-stu-id="58cd3-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="58cd3-114">如果不希望显示包含零工时的结果，请在 **忽略零** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="58cd3-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="58cd3-115">可使用 **级别** 字段指示要与功能位置有关的工时控制行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="58cd3-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="58cd3-116">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置层次结构，则将在最上级别显示某个功能位置的所有工时控制行，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="58cd3-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="58cd3-117">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有工时控制行。</span><span class="sxs-lookup"><span data-stu-id="58cd3-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="58cd3-118">若要将与子资产关联的成本显示为单独行，请在 **包括子资产** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="58cd3-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="58cd3-119">如果要限制搜索，可在 **要包括的记录** 快速选项卡上选择特定资产/功能位置/工作订单。</span><span class="sxs-lookup"><span data-stu-id="58cd3-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="58cd3-120">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="58cd3-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="58cd3-121">在 **资产工时控制** 页面上，单击 **分组依据** 按钮显示所需的计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="58cd3-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="58cd3-122">将突出显示所选 **分组依据** 按钮。</span><span class="sxs-lookup"><span data-stu-id="58cd3-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="58cd3-123">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="58cd3-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="58cd3-124">示例</span><span class="sxs-lookup"><span data-stu-id="58cd3-124">Example</span></span>

<span data-ttu-id="58cd3-125">下面的屏幕截图显示 **资产工时控制** 计算的示例。</span><span class="sxs-lookup"><span data-stu-id="58cd3-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="58cd3-126">**原始预算** 字段显示工作订单预测中的预算工时。</span><span class="sxs-lookup"><span data-stu-id="58cd3-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="58cd3-127">**实际工时** 字段显示工作订单中的已过帐工时。</span><span class="sxs-lookup"><span data-stu-id="58cd3-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="58cd3-128">**承诺工时** 字段显示在与工作订单关联时，公司承诺的工时总量。</span><span class="sxs-lookup"><span data-stu-id="58cd3-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![资产工时控制计算示例](media/04-controlling-and-reporting.png)

<span data-ttu-id="58cd3-130">另外一种创建工时计算的方法是在 **所有资产** 或 **有效资产** 中选择多个资产。</span><span class="sxs-lookup"><span data-stu-id="58cd3-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="58cd3-131">然后单击 **常规** 快速选项卡上的 **工时控制** 按钮。</span><span class="sxs-lookup"><span data-stu-id="58cd3-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="58cd3-132">将在 **要包括的记录** 快速选项卡上的 **资产** 字段中自动插入所选资产。</span><span class="sxs-lookup"><span data-stu-id="58cd3-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="58cd3-133">单击 **资产工时控制** 对话框中的 **确定**，然后将显示所选资产的计算。</span><span class="sxs-lookup"><span data-stu-id="58cd3-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="58cd3-134">可以在 **所有功能位置** 或 **有效功能位置** 中对功能位置执行同样的过程，也可以在 **所有工作订单** 或 **有效工作订单** 中对工作订单执行同样的过程。</span><span class="sxs-lookup"><span data-stu-id="58cd3-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]