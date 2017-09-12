---
title: "向 CFO 工作区添加财务维度"
description: "本主题说明如何向 CFO 工作区添加财务维度，以便可将其用于分类帐和预算报表。"
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: zh-cn
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="e982b-103">向 CFO 工作区添加财务维度</span><span class="sxs-lookup"><span data-stu-id="e982b-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e982b-104">本主题说明如何向首席财务官 (CFO) 工作区添加财务维度，以便可将其用于分类帐和预算报表。</span><span class="sxs-lookup"><span data-stu-id="e982b-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="e982b-105">CFO 工作区具有**概述**选项卡和**财务**选项卡。</span><span class="sxs-lookup"><span data-stu-id="e982b-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="e982b-106">这两个选项卡上的报表受以下两个度量支持：LedgerActivityMeasure 和 BudgetActivityMeasure。</span><span class="sxs-lookup"><span data-stu-id="e982b-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="e982b-107">在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月更新中，这两个度量与 DimensionCombinationEntity 实体之间存在关系。</span><span class="sxs-lookup"><span data-stu-id="e982b-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="e982b-108">因此，您可以选择维度。</span><span class="sxs-lookup"><span data-stu-id="e982b-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="e982b-109">在 Finance and Operations 中的**实体商店**页中，更新 **LedgerActivityMeasure** 和 **BudgetActivityMeasure** 度量。</span><span class="sxs-lookup"><span data-stu-id="e982b-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="e982b-110">在 Microsoft Visual Studio 中，打开“应用程序资源管理器”，然后搜索 **LedgerCFO**。</span><span class="sxs-lookup"><span data-stu-id="e982b-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="e982b-111">在**资源**下，打开 **LedgerCFOWorkspacePBIX**。</span><span class="sxs-lookup"><span data-stu-id="e982b-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="e982b-112">资源在 Microsoft Power BI 桌面中打开时，依次选择**获取数据**、**SQL Server 数据库**和**连接**。</span><span class="sxs-lookup"><span data-stu-id="e982b-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="e982b-113">输入服务器名称，然后输入 **AxDW** 作为数据库。</span><span class="sxs-lookup"><span data-stu-id="e982b-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="e982b-114">选择 **DirectQuery**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e982b-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="e982b-115">搜索并选择 **LedgerActivityMeasure\_DimensionCombination**，然后选择**加载**。</span><span class="sxs-lookup"><span data-stu-id="e982b-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="e982b-116">在**字段**列表中，重命名表**财务维度**，以便轻松识别。</span><span class="sxs-lookup"><span data-stu-id="e982b-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="e982b-117">选择**管理关系**，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="e982b-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="e982b-118">在第一个字段中，选择**总帐活动**，然后选择 **LedgerDimension**。</span><span class="sxs-lookup"><span data-stu-id="e982b-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="e982b-119">在第二个字段中，选择 **LedgerActivityMeasure\_DimensionCombination**（如果已重命名表，则选择**财务维度**）。</span><span class="sxs-lookup"><span data-stu-id="e982b-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="e982b-120">选择 **DimensionCombinationRECID** 标题。</span><span class="sxs-lookup"><span data-stu-id="e982b-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="e982b-121">在**基数**字段中，选择**多对单**。</span><span class="sxs-lookup"><span data-stu-id="e982b-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="e982b-122">将**跨筛选器方向**值更改为 **单一**。</span><span class="sxs-lookup"><span data-stu-id="e982b-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="e982b-123">同时选择**使此关系可用**和**假设引用完整性**，选择**确定**，然后选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="e982b-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="e982b-124">[![创建关系](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="e982b-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="e982b-125">在**字段** 列表中，应该可以看到表和可用财务维度。</span><span class="sxs-lookup"><span data-stu-id="e982b-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="e982b-126">将所需财务维度拖到报表级筛选器。</span><span class="sxs-lookup"><span data-stu-id="e982b-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="e982b-127">保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="e982b-127">Save your changes.</span></span>
15. <span data-ttu-id="e982b-128">在应用程序对象树 (AOT) 中，右键单击项目，然后选择 **同步**。</span><span class="sxs-lookup"><span data-stu-id="e982b-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="e982b-129">构建项目，然后打开应用程序查看结果。</span><span class="sxs-lookup"><span data-stu-id="e982b-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="e982b-130">[![已完成的工作区](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="e982b-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

