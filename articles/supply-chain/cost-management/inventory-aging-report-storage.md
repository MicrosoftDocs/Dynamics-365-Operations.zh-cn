---
title: 库龄报表
description: 本主题介绍使您可以运行库龄报表并使输出以表单和图表形式提供的功能。
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810243"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="cd818-103">库龄报表</span><span class="sxs-lookup"><span data-stu-id="cd818-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cd818-104">在 Microsoft Dynamics 365 Supply Chain Management 中，您可以运行**库龄**报表，并使输出以表单和图表形式提供。</span><span class="sxs-lookup"><span data-stu-id="cd818-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="cd818-105">在表单中，根据配置的布局动态调整列和聚合余额。</span><span class="sxs-lookup"><span data-stu-id="cd818-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="cd818-106">图表提供支持筛选的可视概览，并允许您向下钻取到详细信息。</span><span class="sxs-lookup"><span data-stu-id="cd818-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="cd818-107">此外，名为**库龄报表**的数据实体使您可以将**库龄**报表运行的结果导出为 Microsoft Excel 文件或 PDF 文件等格式。</span><span class="sxs-lookup"><span data-stu-id="cd818-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="cd818-108">在输出包含很多行的情况下，这种运行**库龄**报表的方法很有用。</span><span class="sxs-lookup"><span data-stu-id="cd818-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="cd818-109">例如，如果您有 50,000 个商品和 300 个作为仓库创建的商店，并且您按商品、站点和仓库请求库龄，输出将包含许多行。</span><span class="sxs-lookup"><span data-stu-id="cd818-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="cd818-110">运行库龄报表</span><span class="sxs-lookup"><span data-stu-id="cd818-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="cd818-111">转到**成本管理 \> 查询和报表 \> 库龄报表存储**。</span><span class="sxs-lookup"><span data-stu-id="cd818-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="cd818-112">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="cd818-112">Select **New**.</span></span>
1. <span data-ttu-id="cd818-113">在**流程标识符 – 名称**字段中，输入报表的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="cd818-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="cd818-114">选择**标识 – ID** 报表，并根据需要对其进行筛选。</span><span class="sxs-lookup"><span data-stu-id="cd818-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="cd818-115">报表执行始终在批处理作业中完成。</span><span class="sxs-lookup"><span data-stu-id="cd818-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="cd818-116">批处理作业完成后，输出将显示在**库龄报表存储**页面上。</span><span class="sxs-lookup"><span data-stu-id="cd818-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="cd818-117">要作为具有传统网格布局的表单查看输出，请选择**查看详细信息**。</span><span class="sxs-lookup"><span data-stu-id="cd818-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="cd818-118">要以汇总图表形式查看输出，请选择**查看图表**。</span><span class="sxs-lookup"><span data-stu-id="cd818-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cd818-119">表单将不包括报表布局中定义的小计。</span><span class="sxs-lookup"><span data-stu-id="cd818-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="cd818-120">**库龄报表**数据实体使您可以通过将**流程标识符 – 名称**字段的筛选器应用到数据管理支持的任何格式来导出**库龄**报表的输出。</span><span class="sxs-lookup"><span data-stu-id="cd818-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
