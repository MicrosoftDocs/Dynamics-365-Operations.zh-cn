---
title: 不符合项的问题类型
description: 本主题介绍如何创建和使用不符合项的问题类型。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022148"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="da06c-103">不符合项的问题类型</span><span class="sxs-lookup"><span data-stu-id="da06c-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da06c-104">本主题介绍如何创建和使用不符合项的问题类型。</span><span class="sxs-lookup"><span data-stu-id="da06c-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="da06c-105">您将使用 **问题类型** 页定义各个不符合项类型可能遇到的质量问题的分类。</span><span class="sxs-lookup"><span data-stu-id="da06c-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="da06c-106">对于创建的每个问题类型，您必须指定可以使用该问题类型的不符合项类型。</span><span class="sxs-lookup"><span data-stu-id="da06c-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="da06c-107">您可以设置以下不符合项类型：</span><span class="sxs-lookup"><span data-stu-id="da06c-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="da06c-108">**内部** – 此类型的不符合项与现有库存量相关（例如，质检订单或隔离订单）。</span><span class="sxs-lookup"><span data-stu-id="da06c-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="da06c-109">**客户** – 此类型的不符合项与销售订单相关。</span><span class="sxs-lookup"><span data-stu-id="da06c-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="da06c-110">**供应商** – 此类型的不符合项与采购订单相关。</span><span class="sxs-lookup"><span data-stu-id="da06c-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="da06c-111">**服务请求** – 此类型的不符合项与服务订单相关。</span><span class="sxs-lookup"><span data-stu-id="da06c-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="da06c-112">**生产** – 此类型的不符合项与批次订单或生产订单相关。</span><span class="sxs-lookup"><span data-stu-id="da06c-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="da06c-113">**联产品生产** – 此类型的不符合项与联产品的批次订单相关。</span><span class="sxs-lookup"><span data-stu-id="da06c-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="da06c-114">当您创建新的问题类型时，在操作窗格上选择 **不符合项类型** 可以创建一个或多个为该问题类型授权的不符合项类型的列表。</span><span class="sxs-lookup"><span data-stu-id="da06c-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="da06c-115">例如，与某一缺陷代码相关的问题类型可以应用于所有不符合项类型。</span><span class="sxs-lookup"><span data-stu-id="da06c-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="da06c-116">但是，与客户投诉相关的问题类型只能应用于 **客户** 和 **服务请求** 不符合项类型。</span><span class="sxs-lookup"><span data-stu-id="da06c-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="da06c-117">问题类型的示例</span><span class="sxs-lookup"><span data-stu-id="da06c-117">Examples of problem types</span></span>

<span data-ttu-id="da06c-118">以下是可用于不同不符合项类型的问题类型的一些场景示例：</span><span class="sxs-lookup"><span data-stu-id="da06c-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="da06c-119">**客户：** 客户提出投诉、客户发起退货或未达到质量规范。</span><span class="sxs-lookup"><span data-stu-id="da06c-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="da06c-120">**供应商：** 产品损坏、未达到质量规范或接收了错误产品。</span><span class="sxs-lookup"><span data-stu-id="da06c-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="da06c-121">**服务请求：** 未达到质量规范、客户提出投诉或需要维修机器。</span><span class="sxs-lookup"><span data-stu-id="da06c-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="da06c-122">**生产：** 未达到质量规范、需要维修机器或产品损坏。</span><span class="sxs-lookup"><span data-stu-id="da06c-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="da06c-123">**联产品生产：** 未达到质量规范、需要维修机器或产品损坏。</span><span class="sxs-lookup"><span data-stu-id="da06c-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="da06c-124">创建问题类型并将其分配给不符合项类型</span><span class="sxs-lookup"><span data-stu-id="da06c-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="da06c-125">转到 **库存管理 \> 设置 \> 质量管理 \> 问题类型**。</span><span class="sxs-lookup"><span data-stu-id="da06c-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="da06c-126">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="da06c-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da06c-127">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="da06c-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="da06c-128">**问题类型** – 输入问题类型的唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="da06c-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="da06c-129">**描述** – 输入问题类型的详细描述。</span><span class="sxs-lookup"><span data-stu-id="da06c-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="da06c-130">在仍选择新行的同时，在操作窗格上选择 **不符合项类型**。</span><span class="sxs-lookup"><span data-stu-id="da06c-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="da06c-131">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="da06c-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="da06c-132">然后，对于新行，将 **不符合项类型** 字段设置为您要允许问题类型使用的不符合项类型。</span><span class="sxs-lookup"><span data-stu-id="da06c-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="da06c-133">对要为问题类型授权的每个其他不符合项类型重复上述步骤。</span><span class="sxs-lookup"><span data-stu-id="da06c-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="da06c-134">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="da06c-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da06c-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="da06c-135">Additional resources</span></span>

- [<span data-ttu-id="da06c-136">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="da06c-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="da06c-137">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="da06c-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="da06c-138">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="da06c-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="da06c-139">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="da06c-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="da06c-140">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="da06c-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="da06c-141">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="da06c-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="da06c-142">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="da06c-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="da06c-143">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="da06c-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
