---
title: 不符合项的诊断类型
description: 本主题介绍如何使用和创建可用于不符合项的诊断类型。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022268"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="bcb55-103">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="bcb55-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcb55-104">本主题介绍如何使用和创建可用于不符合项的诊断类型。</span><span class="sxs-lookup"><span data-stu-id="bcb55-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="bcb55-105">您将使用 **诊断类型** 页定义诊断操作的分类。</span><span class="sxs-lookup"><span data-stu-id="bcb55-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="bcb55-106">然后，当您为不符合项创建更正时，将选择诊断。</span><span class="sxs-lookup"><span data-stu-id="bcb55-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="bcb55-107">更正指定应对已审核的未达标采取的诊断操作类型以及应该执行操作的用户。</span><span class="sxs-lookup"><span data-stu-id="bcb55-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="bcb55-108">它还指定请求的完成日期和计划的完成日期。</span><span class="sxs-lookup"><span data-stu-id="bcb55-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="bcb55-109">诊断类型的示例</span><span class="sxs-lookup"><span data-stu-id="bcb55-109">Examples of diagnostic types</span></span>

<span data-ttu-id="bcb55-110">您在一家制造公司工作，有几个物料未通过质量测试。</span><span class="sxs-lookup"><span data-stu-id="bcb55-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="bcb55-111">这些物料被移至隔离区域并标记为未达标产品。</span><span class="sxs-lookup"><span data-stu-id="bcb55-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="bcb55-112">一个不符合项记录在 Microsoft Dynamics 365 Supply Chain Management 中创建，用于跟踪问题解决过程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="bcb55-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="bcb55-113">在这种情况下，出现了质量问题，因为包装物料的机器的轴承损坏，出现过热现象。</span><span class="sxs-lookup"><span data-stu-id="bcb55-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="bcb55-114">更正此问题的方法是更换机器中的零件。</span><span class="sxs-lookup"><span data-stu-id="bcb55-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="bcb55-115">配置诊断类型时，您可以创建多个记录，每个记录代表机器可能存在的一个不同问题类型。</span><span class="sxs-lookup"><span data-stu-id="bcb55-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="bcb55-116">或者，您可以创建一个代表机器维修的通用诊断类型。</span><span class="sxs-lookup"><span data-stu-id="bcb55-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="bcb55-117">创建诊断类型</span><span class="sxs-lookup"><span data-stu-id="bcb55-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="bcb55-118">转到 **库存管理 \> 设置 \> 质量管理 \> 诊断类型**。</span><span class="sxs-lookup"><span data-stu-id="bcb55-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="bcb55-119">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="bcb55-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bcb55-120">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="bcb55-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bcb55-121">**诊断** – 输入诊断类型的唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="bcb55-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="bcb55-122">**描述** – 输入诊断类型的详细描述。</span><span class="sxs-lookup"><span data-stu-id="bcb55-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="bcb55-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bcb55-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bcb55-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="bcb55-124">Additional resources</span></span>

- [<span data-ttu-id="bcb55-125">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="bcb55-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="bcb55-126">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="bcb55-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="bcb55-127">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="bcb55-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="bcb55-128">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="bcb55-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="bcb55-129">不符合项的问题类型</span><span class="sxs-lookup"><span data-stu-id="bcb55-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="bcb55-130">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="bcb55-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="bcb55-131">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="bcb55-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="bcb55-132">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="bcb55-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
