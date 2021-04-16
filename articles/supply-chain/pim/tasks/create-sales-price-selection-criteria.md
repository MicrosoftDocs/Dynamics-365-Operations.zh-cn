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
ms.openlocfilehash: 5a616dcfdd755efc9bf0473e9239acb9127f11f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818149"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="38245-103">创建销售价选择条件</span><span class="sxs-lookup"><span data-stu-id="38245-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38245-104">此过程显示如何为基于属性的销售价模型创建销售价选择条件。</span><span class="sxs-lookup"><span data-stu-id="38245-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="38245-105">此过程要求至少有一个销售价模型可用。</span><span class="sxs-lookup"><span data-stu-id="38245-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="38245-106">此示例使用 USMF 演示数据公司中的扬声器解决方案销售价模型的价格模型。</span><span class="sxs-lookup"><span data-stu-id="38245-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="38245-107">通常，产品经理使用此过程。</span><span class="sxs-lookup"><span data-stu-id="38245-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="38245-108">为现有销售价模型添加新条件</span><span class="sxs-lookup"><span data-stu-id="38245-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="38245-109">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="38245-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="38245-110">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="38245-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="38245-111">在此列表中，选择扬声器解决方案产品模型的行，但是不单击模型名称的链接。</span><span class="sxs-lookup"><span data-stu-id="38245-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="38245-112">在“操作窗格”上单击“模型”。</span><span class="sxs-lookup"><span data-stu-id="38245-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="38245-113">单击“价格模型条件”。</span><span class="sxs-lookup"><span data-stu-id="38245-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="38245-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="38245-114">Click New.</span></span>
7. <span data-ttu-id="38245-115">在“名称”字段中，键入“客户组 10”。</span><span class="sxs-lookup"><span data-stu-id="38245-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="38245-116">价格模型条件的名称用于帮助识别基础选择条件。</span><span class="sxs-lookup"><span data-stu-id="38245-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="38245-117">在“价格模型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="38245-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="38245-118">在“订单类型”字段中选择“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="38245-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="38245-119">订单类型确定将可用于选择查询的数据库字段。</span><span class="sxs-lookup"><span data-stu-id="38245-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="38245-120">在“生效日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="38245-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="38245-121">在“到期日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="38245-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="38245-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="38245-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="38245-123">为选择条件创建查询</span><span class="sxs-lookup"><span data-stu-id="38245-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="38245-124">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="38245-124">Click Edit.</span></span>
2. <span data-ttu-id="38245-125">在“表”字段中，选择“客户”。</span><span class="sxs-lookup"><span data-stu-id="38245-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="38245-126">在“字段”字段中，选择“客户组”。</span><span class="sxs-lookup"><span data-stu-id="38245-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="38245-127">在此示例中，我们为选择条件使用特定客户组。</span><span class="sxs-lookup"><span data-stu-id="38245-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="38245-128">在“条件”字段中，选择“客户组 10”。</span><span class="sxs-lookup"><span data-stu-id="38245-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="38245-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="38245-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]