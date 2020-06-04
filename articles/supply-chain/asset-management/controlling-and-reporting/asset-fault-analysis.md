---
title: 资产故障分析
description: 本主题介绍资产管理中的资产故障分析。
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32cd8fb55cd9245a9a7c426a7c956bb40c3fdb0e
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383542"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="3c910-103">资产故障分析</span><span class="sxs-lookup"><span data-stu-id="3c910-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3c910-104">在资产管理中，可以分析资产故障登记，以便获取特定期间登记的故障总数的概览。</span><span class="sxs-lookup"><span data-stu-id="3c910-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="3c910-105">可以从不同角度分析故障登记，例如，重点关注资产、资产类型、功能位置、故障特征或故障类型。</span><span class="sxs-lookup"><span data-stu-id="3c910-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="3c910-106">单击**资产管理** > **查询** > **资产故障** > **资产故障分析**。</span><span class="sxs-lookup"><span data-stu-id="3c910-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="3c910-107">在**资产故障分析计算**对话框中，可使用**级别**字段指示希望资产故障行与功能位置之间的关系的详细程度。</span><span class="sxs-lookup"><span data-stu-id="3c910-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="3c910-108">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产故障行，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="3c910-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="3c910-109">如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有资产故障行。</span><span class="sxs-lookup"><span data-stu-id="3c910-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="3c910-110">如果要限制搜索，可在**要包括的记录**快速选项卡上选择特定资产、故障日期、故障成因和故障补救措施。</span><span class="sxs-lookup"><span data-stu-id="3c910-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="3c910-111">单击**确定**开始计算。</span><span class="sxs-lookup"><span data-stu-id="3c910-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="3c910-112">在**资产故障分析**选项卡上，单击一个或多个**分组依据**按钮以显示要查看的详细程度。</span><span class="sxs-lookup"><span data-stu-id="3c910-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="3c910-113">将突出显示已激活的按钮。</span><span class="sxs-lookup"><span data-stu-id="3c910-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="3c910-114">通过单击按钮激活或停用这些按钮。</span><span class="sxs-lookup"><span data-stu-id="3c910-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="3c910-115">若要在屏幕上显示所选内容，请单击**更新计算**。</span><span class="sxs-lookup"><span data-stu-id="3c910-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="3c910-116">每次您激活或停用**分组依据**按钮时，请记住单击**更新计算**按钮。</span><span class="sxs-lookup"><span data-stu-id="3c910-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="3c910-117">之所以需要执行此操作，是因为重新计算故障概率时要处理大量数据。</span><span class="sxs-lookup"><span data-stu-id="3c910-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="3c910-118">示例</span><span class="sxs-lookup"><span data-stu-id="3c910-118">Examples</span></span>

<span data-ttu-id="3c910-119">可以通过多种方法分析故障登记。</span><span class="sxs-lookup"><span data-stu-id="3c910-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="3c910-120">本节有五个在分析资产故障登记时，不同数据选择如何提供更多见解和详细信息的示例。</span><span class="sxs-lookup"><span data-stu-id="3c910-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="3c910-121">按特征分组</span><span class="sxs-lookup"><span data-stu-id="3c910-121">Group by symptoms</span></span>

<span data-ttu-id="3c910-122">在下面的屏幕截图中，将仅选择**特征**按钮。</span><span class="sxs-lookup"><span data-stu-id="3c910-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="3c910-123">已对三种故障特征创建了故障登记：“漏气”、“保险丝熔断”和“设备卡住”。</span><span class="sxs-lookup"><span data-stu-id="3c910-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="3c910-124">在**概率 %** 列中，所有百分比之和为 100%。</span><span class="sxs-lookup"><span data-stu-id="3c910-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="3c910-125">在此故障分析中，概率基于所有**特征**登记。</span><span class="sxs-lookup"><span data-stu-id="3c910-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![图 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="3c910-127">按特征和时段分组</span><span class="sxs-lookup"><span data-stu-id="3c910-127">Group by symptoms and time period</span></span>

<span data-ttu-id="3c910-128">在下面的屏幕截图中，添加了**年**和**月**以显示如何查看所选期间内的故障登记。</span><span class="sxs-lookup"><span data-stu-id="3c910-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="3c910-129">故障特征现在显示为每年/月的登记。</span><span class="sxs-lookup"><span data-stu-id="3c910-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="3c910-130">在**概率 %** 列，如果将每月的所有百分比相加，则总和为 100%。</span><span class="sxs-lookup"><span data-stu-id="3c910-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="3c910-131">在此故障分析中，概率基于**特征**登记。</span><span class="sxs-lookup"><span data-stu-id="3c910-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="3c910-132">如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障特征以找到方法来限制该故障特征的登记数量。</span><span class="sxs-lookup"><span data-stu-id="3c910-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![图 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="3c910-134">按多个特征和资产分组</span><span class="sxs-lookup"><span data-stu-id="3c910-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="3c910-135">资产和资产类型的组合用作下面三个屏幕截图中显示的计算的基础，这将在详细程度增加。</span><span class="sxs-lookup"><span data-stu-id="3c910-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="3c910-136">**按日期分组**、**按资产分组**、**按功能位置分组**操作窗格组中的按钮和**故障**按钮（故障 ID）中通常包含期间或资产关联。</span><span class="sxs-lookup"><span data-stu-id="3c910-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="3c910-137">**特征**、**区域**、**类型**、**成因**和**补救措施**按钮是故障管理中用于分析资产故障登记和找出问题区域的分类。</span><span class="sxs-lookup"><span data-stu-id="3c910-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="3c910-138">**按特征、资产和资产类型分组**</span><span class="sxs-lookup"><span data-stu-id="3c910-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="3c910-139">在下面的屏幕截图中，添加了**资产**和**资产类型**，以便提供有关故障登记的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="3c910-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="3c910-140">故障特征现在已拆分为**资产** / **资产类型** / **特征**组合。</span><span class="sxs-lookup"><span data-stu-id="3c910-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="3c910-141">在**概率 %** 列，如果将**资产** / **资产类型** / **特征**的所有百分比分别相加，则相加之和分别为 100%。</span><span class="sxs-lookup"><span data-stu-id="3c910-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="3c910-142">在此故障分析中，概率基于**特征**登记。</span><span class="sxs-lookup"><span data-stu-id="3c910-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="3c910-143">如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障特征以找到方法来限制该故障特征的登记数量。</span><span class="sxs-lookup"><span data-stu-id="3c910-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![图 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="3c910-145">**按两个特征、资产和资产类型分组**</span><span class="sxs-lookup"><span data-stu-id="3c910-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="3c910-146">在下面的屏幕截图中，向**特征**、**资产**和**资产类型**添加了**区域**，以便提供有关故障登记的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="3c910-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="3c910-147">在**概率 %** 列，如果资产的**资产** / **资产类型** / **特征**的所有百分比分别相加，则相加之和分别为 100%。</span><span class="sxs-lookup"><span data-stu-id="3c910-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="3c910-148">在此故障分析中，概率基于**特征**和**区域**的组合。</span><span class="sxs-lookup"><span data-stu-id="3c910-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="3c910-149">如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障区域以找到方法来限制该故障区域的登记数量。</span><span class="sxs-lookup"><span data-stu-id="3c910-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![图 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="3c910-151">**按三个特征、资产和资产类型分组**</span><span class="sxs-lookup"><span data-stu-id="3c910-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="3c910-152">在下面的屏幕截图中，添加了**类型**，并显示了此示例中最详细的计算。</span><span class="sxs-lookup"><span data-stu-id="3c910-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="3c910-153">在**概率 %** 列，如果资产的**资产** / **资产类型** / **特征**的所有百分比分别相加，则相加之和分别为 100%。</span><span class="sxs-lookup"><span data-stu-id="3c910-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="3c910-154">在此故障分析中，概率基于**特征**、**区域**和**类型**的组合。</span><span class="sxs-lookup"><span data-stu-id="3c910-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="3c910-155">如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障类型以找到方法来限制该故障类型的登记数量。</span><span class="sxs-lookup"><span data-stu-id="3c910-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![图 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="3c910-157">有关为工人和维护请求创建的所有故障登记的概览，请单击**资产管理** > **查询** > **资产故障** > **资产故障**。</span><span class="sxs-lookup"><span data-stu-id="3c910-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="3c910-158">在**资产故障**页中，选择一个资产故障登记，然后展开**相关信息**窗格以查看与关联的工作订单或维护请求有关的信息。</span><span class="sxs-lookup"><span data-stu-id="3c910-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

