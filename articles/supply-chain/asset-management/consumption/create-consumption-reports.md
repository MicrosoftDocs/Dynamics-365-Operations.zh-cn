---
title: 创建消耗报表
description: 本主题说明如何在资产管理中创建消耗报表。
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: eecfb101af9a91f515aab221181c54d53e358a68
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652417"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="b6ab1-103">创建消耗报表</span><span class="sxs-lookup"><span data-stu-id="b6ab1-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b6ab1-104">在资产管理中为工作订单创建和过帐消耗登记之后，将提供两个报告来显示消耗详细信息。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="b6ab1-105">资产消耗报表</span><span class="sxs-lookup"><span data-stu-id="b6ab1-105">Asset consumption report</span></span>

<span data-ttu-id="b6ab1-106">过帐工作订单的消耗后，可打印资产消耗报表。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="b6ab1-107">该报告显示为资产过帐的工时、工时成本、物料成本和费用。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="b6ab1-108">单击**资产管理** > **报表** > **资产** > **资产消耗**。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="b6ab1-109">在**资产消耗**对话框中，选择要查看的参数和详细程度，方法是在相关切换按钮上选择**是**，然后在**显示**部分中插入功能位置级别。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="b6ab1-110">可使用**级别**字段指示要与功能位置有关的资产行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="b6ab1-111">例如，如果在字段中输入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产行，因此，可以从较低级别的功能位置叠加行。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="b6ab1-112">如果在**级别**字段中输入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有资产。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="b6ab1-113">在**所有子资产之和**切换按钮上选择**是**可在报表中查看每个子资产之和。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="b6ab1-114">在**日期**部分中选择日期期间。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="b6ab1-115">在**目标**快速选项卡上，选择要在屏幕上显示报表，打印报表还是另存为文件或电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="b6ab1-116">如果需要，可选择在报表中显示特定资产。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="b6ab1-117">在**要包括的记录**快速选项卡上，单击**筛选**，然后添加报表中要包括的资产。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="b6ab1-118">单击**确定**以生成报表。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="b6ab1-119">工作订单消耗报表</span><span class="sxs-lookup"><span data-stu-id="b6ab1-119">Work order consumption report</span></span>

<span data-ttu-id="b6ab1-120">过帐工作订单的消耗后，可打印工作订单消耗报表。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="b6ab1-121">该报告显示为工作订单过帐的工时、工时成本、物料成本和费用。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="b6ab1-122">单击**资产管理** > **报告** > **工作订单报告** > **工作订单消耗**。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="b6ab1-123">在**工作订单消耗**对话框中，显示报表中要包含的参数，方法是在**显示**部分中的相关切换按钮上选择**是**。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="b6ab1-124">在**日期**部分中选择日期期间。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="b6ab1-125">在**目标**快速选项卡上，选择要在屏幕上显示报表，打印报表还是另存为文件或电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="b6ab1-126">如果需要，可选择在报表中显示特定工作订单。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="b6ab1-127">在**要包括的记录**快速选项卡上，单击**筛选**，然后添加报表中要包括的工作订单。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="b6ab1-128">单击**确定**以生成报表。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="b6ab1-129">也可以生成[工作订单报表](../work-orders/work-order-report.md)，其中包含更多工作订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="b6ab1-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

