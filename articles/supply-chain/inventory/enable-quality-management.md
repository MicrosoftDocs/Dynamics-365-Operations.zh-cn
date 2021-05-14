---
title: 启用质量和不符合项管理
description: 本主题概述了在 Microsoft Dynamics 365 Supply Chain Management 中设置和配置质量和不符合项管理功能的流程。
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956246"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="07636-103">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="07636-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07636-104">本主题概述了在 Microsoft Dynamics 365 Supply Chain Management 中设置和配置质量和不符合项管理功能的流程。</span><span class="sxs-lookup"><span data-stu-id="07636-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="07636-105">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="07636-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="07636-106">请按照以下步骤在系统上启用质量管理。</span><span class="sxs-lookup"><span data-stu-id="07636-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="07636-107">转到 **库存管理 \> 设置 \> 库存和仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="07636-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="07636-108">在 **质量管理** 选项卡上，将 **使用质量管理** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="07636-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="07636-109">在 **小时工资率** 字段中用本币输入人工小时工资率。</span><span class="sxs-lookup"><span data-stu-id="07636-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="07636-110">小时工资率用于计算与未达标相关的工序的成本。</span><span class="sxs-lookup"><span data-stu-id="07636-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="07636-111">小时工资率和计算的成本为未达标提供了参考信息。</span><span class="sxs-lookup"><span data-stu-id="07636-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="07636-112">它们不与其他功能交互。</span><span class="sxs-lookup"><span data-stu-id="07636-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="07636-113">选择 **报表设置**。</span><span class="sxs-lookup"><span data-stu-id="07636-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="07636-114">为各个报表类型添加新行，然后选择要用于每个报表的文档类型。</span><span class="sxs-lookup"><span data-stu-id="07636-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="07636-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="07636-115">Close the page.</span></span>
1. <span data-ttu-id="07636-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="07636-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="07636-117">质量管理配置流程</span><span class="sxs-lookup"><span data-stu-id="07636-117">Quality management configuration process</span></span>

<span data-ttu-id="07636-118">您必须先配置系统和先决条件，然后才能够开始使用质量管理功能和生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="07636-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="07636-119">这里是配置质量管理所需的步骤列表。</span><span class="sxs-lookup"><span data-stu-id="07636-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="07636-120">[启用质量和不符合项管理](#enable-qm)。</span><span class="sxs-lookup"><span data-stu-id="07636-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="07636-121">可选：[配置测试仪器](quality-test-instruments.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="07636-122">[配置测试](quality-tests.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="07636-123">[配置测试变量和结果](quality-test-variables.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="07636-124">[配置测试组](quality-test-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="07636-125">可选：[配置质量组，并链接到产品](quality-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="07636-126">可选：[配置质量关联](quality-associations.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="07636-127">配置完成后，您可以开始创建和处理质检订单。</span><span class="sxs-lookup"><span data-stu-id="07636-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="07636-128">有关如何创建和处理质检订单的详细信息，请参阅[质检订单](quality-orders.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="07636-129">不符合项管理配置流程</span><span class="sxs-lookup"><span data-stu-id="07636-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="07636-130">您必须先配置系统和先决条件，然后才能够开始使用不符合项管理功能和生成不符合项。</span><span class="sxs-lookup"><span data-stu-id="07636-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="07636-131">这里是配置不符合项管理所需的步骤列表。</span><span class="sxs-lookup"><span data-stu-id="07636-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="07636-132">[启用质量和不符合项管理](#enable-qm)。</span><span class="sxs-lookup"><span data-stu-id="07636-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="07636-133">[配置负责审核不符合项的工作人员](quality-responsible-workers.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="07636-134">[配置问题类型](quality-problem-types.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="07636-135">[配置隔离区域](quality-quarantine-zones.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="07636-136">[配置诊断类型](quality-diagnostic-types.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="07636-137">[配置操作](quality-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="07636-138">可选：[配置质量费用](quality-charges.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="07636-139">配置完成后，您可以开始创建和处理不符合项。</span><span class="sxs-lookup"><span data-stu-id="07636-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="07636-140">有关如何创建和处理不符合项的详细信息，请参阅[创建和处理不符合项](tasks/create-process-non-conformance.md)。</span><span class="sxs-lookup"><span data-stu-id="07636-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07636-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="07636-141">Additional resources</span></span>

- [<span data-ttu-id="07636-142">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="07636-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="07636-143">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="07636-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="07636-144">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="07636-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
