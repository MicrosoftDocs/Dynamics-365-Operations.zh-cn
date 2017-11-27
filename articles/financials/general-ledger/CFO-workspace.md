---
title: "向 CFO 工作区添加财务维度"
description: "本主题说明如何向 CFO 工作区添加财务维度，以便可将其用于分类帐和预算报表。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5faefe5da8c3a64987a38ebef92eb87049ebe874
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="6f937-103">向 CFO 工作区添加财务维度</span><span class="sxs-lookup"><span data-stu-id="6f937-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6f937-104">本主题说明如何向首席财务官 (CFO) 工作区添加财务维度，以便可将其用于分类帐和预算报表。</span><span class="sxs-lookup"><span data-stu-id="6f937-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="6f937-105">CFO 工作区具有**概述**选项卡和**财务**选项卡。这两个选项卡上的报表受以下两个度量支持：LedgerActivityMeasure 和 BudgetActivityMeasure。</span><span class="sxs-lookup"><span data-stu-id="6f937-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="6f937-106">在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）中，这两个度量与 DimensionCombinationEntity 实体之间存在关系。</span><span class="sxs-lookup"><span data-stu-id="6f937-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="6f937-107">因此，您可以选择维度。</span><span class="sxs-lookup"><span data-stu-id="6f937-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="6f937-108">在 Finance and Operations 中的**实体商店**页中，更新 **LedgerActivityMeasure** 和 **BudgetActivityMeasure** 度量。</span><span class="sxs-lookup"><span data-stu-id="6f937-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="6f937-109">在 Microsoft Visual Studio 中，打开“应用程序资源管理器”，然后搜索 **LedgerCFO**。</span><span class="sxs-lookup"><span data-stu-id="6f937-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="6f937-110">在**资源**下，打开 **LedgerCFOWorkspacePBIX**。</span><span class="sxs-lookup"><span data-stu-id="6f937-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="6f937-111">资源在 Microsoft Power BI 桌面中打开时，依次选择**获取数据**、**SQL Server 数据库**和**连接**。</span><span class="sxs-lookup"><span data-stu-id="6f937-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="6f937-112">输入服务器名称，然后输入 **AxDW** 作为数据库。</span><span class="sxs-lookup"><span data-stu-id="6f937-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="6f937-113">选择 **DirectQuery**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="6f937-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="6f937-114">搜索并选择 **LedgerActivityMeasure\_DimensionCombination**，然后选择**加载**。</span><span class="sxs-lookup"><span data-stu-id="6f937-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="6f937-115">在**字段**列表中，重命名表**财务维度**，以便轻松识别。</span><span class="sxs-lookup"><span data-stu-id="6f937-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="6f937-116">选择**管理关系**，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="6f937-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="6f937-117">在第一个字段中，选择**总帐活动**，然后选择 **LedgerDimension**。</span><span class="sxs-lookup"><span data-stu-id="6f937-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="6f937-118">在第二个字段中，选择 **LedgerActivityMeasure\_DimensionCombination**（如果已重命名表，则选择**财务维度**）。</span><span class="sxs-lookup"><span data-stu-id="6f937-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="6f937-119">选择 **DimensionCombinationRECID** 标题。</span><span class="sxs-lookup"><span data-stu-id="6f937-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="6f937-120">在**基数**字段中，选择**多对单**。</span><span class="sxs-lookup"><span data-stu-id="6f937-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="6f937-121">将**跨筛选器方向**值更改为 **单一**。</span><span class="sxs-lookup"><span data-stu-id="6f937-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="6f937-122">同时选择**使此关系可用**和**假设引用完整性**，选择**确定**，然后选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="6f937-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="6f937-123">[![创建关系](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="6f937-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="6f937-124">在**字段** 列表中，应该可以看到表和可用财务维度。</span><span class="sxs-lookup"><span data-stu-id="6f937-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="6f937-125">将所需财务维度拖到报表级筛选器。</span><span class="sxs-lookup"><span data-stu-id="6f937-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="6f937-126">保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="6f937-126">Save your changes.</span></span>
15. <span data-ttu-id="6f937-127">在应用程序对象树 (AOT) 中，右键单击项目，然后选择 **同步**。</span><span class="sxs-lookup"><span data-stu-id="6f937-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="6f937-128">构建项目，然后打开应用程序查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f937-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="6f937-129">[![已完成的工作区](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="6f937-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

