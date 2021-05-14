---
title: 创建销售价选择条件
description: 此过程显示如何为基于属性的销售价模型创建销售价选择条件。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920523"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="e852a-103">创建销售价选择条件</span><span class="sxs-lookup"><span data-stu-id="e852a-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e852a-104">此过程显示如何为基于属性的销售价模型创建销售价选择条件。</span><span class="sxs-lookup"><span data-stu-id="e852a-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="e852a-105">此过程要求至少有一个销售价模型可用。</span><span class="sxs-lookup"><span data-stu-id="e852a-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="e852a-106">此示例使用 USMF 演示数据公司中的扬声器解决方案销售价模型的价格模型。</span><span class="sxs-lookup"><span data-stu-id="e852a-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="e852a-107">通常，产品经理使用此过程。</span><span class="sxs-lookup"><span data-stu-id="e852a-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="e852a-108">为现有销售价模型添加新条件</span><span class="sxs-lookup"><span data-stu-id="e852a-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="e852a-109">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="e852a-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="e852a-110">在此列表中，选择扬声器解决方案产品模型的行，但是不选择模型名称的链接。</span><span class="sxs-lookup"><span data-stu-id="e852a-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="e852a-111">在操作窗格上，选择 **模型**。</span><span class="sxs-lookup"><span data-stu-id="e852a-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="e852a-112">选择 **价格模型条件**。</span><span class="sxs-lookup"><span data-stu-id="e852a-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="e852a-113">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e852a-113">Select **New**.</span></span>
1. <span data-ttu-id="e852a-114">在 **名称** 字段中，键入“客户组 10”。</span><span class="sxs-lookup"><span data-stu-id="e852a-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="e852a-115">价格模型条件的名称用于帮助识别基础选择条件。</span><span class="sxs-lookup"><span data-stu-id="e852a-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="e852a-116">在 **价格模型** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e852a-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="e852a-117">在 **订单类型** 字段中选择 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="e852a-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="e852a-118">订单类型确定将可用于选择查询的数据库字段。</span><span class="sxs-lookup"><span data-stu-id="e852a-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="e852a-119">在 **生效日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="e852a-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="e852a-120">在 **到期日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="e852a-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="e852a-121">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e852a-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="e852a-122">为选择条件创建查询</span><span class="sxs-lookup"><span data-stu-id="e852a-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="e852a-123">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="e852a-123">Select **Edit**.</span></span>
2. <span data-ttu-id="e852a-124">在 **表** 字段中，选择 *客户*。</span><span class="sxs-lookup"><span data-stu-id="e852a-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="e852a-125">在 **字段** 字段中，选择 *客户组*。</span><span class="sxs-lookup"><span data-stu-id="e852a-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="e852a-126">在此示例中，我们为选择条件使用特定客户组。</span><span class="sxs-lookup"><span data-stu-id="e852a-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="e852a-127">在 **条件** 字段中，选择 *客户组 10*。</span><span class="sxs-lookup"><span data-stu-id="e852a-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="e852a-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e852a-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]