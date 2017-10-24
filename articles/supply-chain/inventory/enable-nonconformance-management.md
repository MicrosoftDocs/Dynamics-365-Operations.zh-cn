---
title: "不符合项管理"
description: "本文介绍使用未达标所需的基本设置。 如果要使用质检订单还需要其他设置。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: ce9dbbb79d4281c004e4c052774eb4776218f1ef
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2017

---

# <a name="nonconformance-management"></a><span data-ttu-id="3b439-104">不符合项管理</span><span class="sxs-lookup"><span data-stu-id="3b439-104">Nonconformance management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3b439-105">本文介绍使用未达标所需的基本设置。</span><span class="sxs-lookup"><span data-stu-id="3b439-105">This article describes the basic setup that is required in order to use nonconformances.</span></span> <span data-ttu-id="3b439-106">如果要使用质检订单还需要其他设置。</span><span class="sxs-lookup"><span data-stu-id="3b439-106">Additional setup is required if you want to use quality orders.</span></span>

<span data-ttu-id="3b439-107">要启用未达标管理，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="3b439-107">To enable nonconformance management, follow these steps:</span></span>

1.  <span data-ttu-id="3b439-108">定义与未达标有关的库存和仓库管理参数：</span><span class="sxs-lookup"><span data-stu-id="3b439-108">Define the Inventory and warehouse management parameters that are related to nonconformances:</span></span>
    -   <span data-ttu-id="3b439-109">将**使用质量管理**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="3b439-109">Set the **Use quality management** option to **Yes**.</span></span>
    -   <span data-ttu-id="3b439-110">在**小时工资率**字段中用本币输入人工小时工资率。</span><span class="sxs-lookup"><span data-stu-id="3b439-110">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="3b439-111">小时工资率用于计算与未达标相关的工序的成本。</span><span class="sxs-lookup"><span data-stu-id="3b439-111">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="3b439-112">小时工资率和计算的成本为未达标提供了参考信息。</span><span class="sxs-lookup"><span data-stu-id="3b439-112">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="3b439-113">它们不与其他功能交互。</span><span class="sxs-lookup"><span data-stu-id="3b439-113">They don't interact with other functionality.</span></span>
    -   <span data-ttu-id="3b439-114">使用**报表设置**页上的**质量管理**选项卡定义要打印的单据类型。</span><span class="sxs-lookup"><span data-stu-id="3b439-114">Use the **Quality management** tab on the **Report setup** page to define the type of document to print.</span></span> <span data-ttu-id="3b439-115">您可以打印未达标报表，未达标标记或更正报表。</span><span class="sxs-lookup"><span data-stu-id="3b439-115">You can print a nonconformance report, a nonconformance tag, or a correction report.</span></span> <span data-ttu-id="3b439-116">您可以定义多个记录在报表上打印不同的文档类型，或打印内部和外部注释。</span><span class="sxs-lookup"><span data-stu-id="3b439-116">You can define more than one record to print different document types on a report, or to print internal and external notes.</span></span> <span data-ttu-id="3b439-117">您可能发现使用**单据类型**页为未达标并且更正的唯一单据类型来定义唯一的文档类型很有帮助。</span><span class="sxs-lookup"><span data-stu-id="3b439-117">You might find it helpful to use the **Document type** page to define a unique document type for nonconformances and a unique document type for corrections.</span></span> <span data-ttu-id="3b439-118">例如，要通过未达标的唯一单据类型，输入与未达标有关的注释。</span><span class="sxs-lookup"><span data-stu-id="3b439-118">For example, want to enter notes about a nonconformance by using the unique document type for nonconformances.</span></span> <span data-ttu-id="3b439-119">在这种情况下，请在报表选项中确定唯一单据类型。</span><span class="sxs-lookup"><span data-stu-id="3b439-119">In this case, identify the unique document type in the report options.</span></span>
    -   <span data-ttu-id="3b439-120">启用未达标和更正参考的编号规则。</span><span class="sxs-lookup"><span data-stu-id="3b439-120">Enable number sequences for nonconformance and correction references.</span></span>

2.  <span data-ttu-id="3b439-121">支持用户审核未达标。</span><span class="sxs-lookup"><span data-stu-id="3b439-121">Enable user approval of nonconformances.</span></span> <span data-ttu-id="3b439-122">使用**用户**页的**姓名**字段向必须审核未达标的每个用户分配员工。</span><span class="sxs-lookup"><span data-stu-id="3b439-122">Use the **Name** field on the **Users** page to assign an employee to each user who must approve a nonconformance.</span></span> <span data-ttu-id="3b439-123">系统将使用更改未达标的状态以跟踪未达标历史记录的员工。</span><span class="sxs-lookup"><span data-stu-id="3b439-123">The system uses the employees who change the status of a noncomformance to track the nonconformance history.</span></span> <span data-ttu-id="3b439-124">除非用户被分配员工标识符，否则他们无法审核未达标。</span><span class="sxs-lookup"><span data-stu-id="3b439-124">Users can't approve a nonconformance unless they have been assigned an employee identifier.</span></span>
3.  <span data-ttu-id="3b439-125">定义将分配给未达标的问题类型。</span><span class="sxs-lookup"><span data-stu-id="3b439-125">Define the problem types that will be assigned to nonconformances.</span></span> <span data-ttu-id="3b439-126">使用**问题类型**页定义各类未达标类型遇到的质量问题分类。</span><span class="sxs-lookup"><span data-stu-id="3b439-126">Use the **Problem types** page to define a classification of quality problems that are encountered for the various nonconformance types.</span></span> <span data-ttu-id="3b439-127">您可以设置以下未达标类型：**内部**、**客户**、**供应商**、**服务请求**、**生产**和**联产品生产**。</span><span class="sxs-lookup"><span data-stu-id="3b439-127">You can set up the following nonconformance types: **Internal**, **Customer**, **Vendor**, **Service request**, **Production**, and **Co-product production**.</span></span> <span data-ttu-id="3b439-128">使用**未达标类型**页来授权用于一个或多个未达标类型的问题类型。</span><span class="sxs-lookup"><span data-stu-id="3b439-128">Use the **Non conformance types** page to authorize a problem type to be used in one or more nonconformance types.</span></span> <span data-ttu-id="3b439-129">例如，关于缺陷代码的问题类型可能适用于所有未达标类型，而有关客户投诉的问题类型可能只适用于**客户**和**服务请求**未达标类型。</span><span class="sxs-lookup"><span data-stu-id="3b439-129">For example, a problem type that is related to a defect code might apply to all nonconformance types, whereas a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>
4.  <span data-ttu-id="3b439-130">定义检验区域，提供有关应处理的有缺陷物料的准则。</span><span class="sxs-lookup"><span data-stu-id="3b439-130">Define quarantine zones to provide guidance about defective material should be handled.</span></span> <span data-ttu-id="3b439-131">使用**检验区域**页定义可以分配给未达标的区域。</span><span class="sxs-lookup"><span data-stu-id="3b439-131">Use the **Quarantine zones** page to define zones that can be assigned to a nonconformance.</span></span> <span data-ttu-id="3b439-132">打印的未达标标记将显示分配的检验区域和有关使用的信息，以提供有关如何处理有缺陷物料的指导。</span><span class="sxs-lookup"><span data-stu-id="3b439-132">The printed nonconformance tag will show the assigned quarantine zone and information about usage, to provide guidance about how to handle defective material.</span></span> <span data-ttu-id="3b439-133">这些区域可以与库存库位或运营资源对应。</span><span class="sxs-lookup"><span data-stu-id="3b439-133">The zones might correspond to inventory locations or operations resources.</span></span>
5.  <span data-ttu-id="3b439-134">定义将分配给更正的诊断类型。</span><span class="sxs-lookup"><span data-stu-id="3b439-134">Define the diagnostic types that will be assigned to corrections.</span></span> <span data-ttu-id="3b439-135">使用**诊断类型**页定义诊断操作的分类。</span><span class="sxs-lookup"><span data-stu-id="3b439-135">Use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="3b439-136">更正指定应对已审核的未达标采取的诊断操作类型以及应该执行操作的用户。</span><span class="sxs-lookup"><span data-stu-id="3b439-136">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="3b439-137">它还指定请求的完成日期和计划的完成日期。</span><span class="sxs-lookup"><span data-stu-id="3b439-137">It also specifies the requested completion date and the planned completion date.</span></span>
6.  <span data-ttu-id="3b439-138">定义将分配给未达标的相关工序。</span><span class="sxs-lookup"><span data-stu-id="3b439-138">Define the related operations that will be assigned to nonconformances.</span></span> <span data-ttu-id="3b439-139">使用**工序**页定义可以对已审核的未达标执行的工作的分类。</span><span class="sxs-lookup"><span data-stu-id="3b439-139">Use the **Operations** page to define a classification of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="3b439-140">向未达标分配相关工序时，可以提供详细信息，如有关执行该工序所需的关联物料、工时和杂项费用的信息。</span><span class="sxs-lookup"><span data-stu-id="3b439-140">When you assign a related operation to a nonconformance, you can provide detailed information, such as information about the associated material, labor hours, and miscellaneous charges that are required in order to perform the operation.</span></span> <span data-ttu-id="3b439-141">此信息用于计算工序的估计成本。</span><span class="sxs-lookup"><span data-stu-id="3b439-141">This information is used to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="3b439-142">这些详细信息和预估成本用于参考。</span><span class="sxs-lookup"><span data-stu-id="3b439-142">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="3b439-143">针对质量的相关工序不同于可以为生产工艺路线定义的工序。</span><span class="sxs-lookup"><span data-stu-id="3b439-143">The related operations for quality differ from the operations that can be defined for a production route.</span></span>


<a name="see-also"></a><span data-ttu-id="3b439-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b439-144">See also</span></span>
--------

[<span data-ttu-id="3b439-145">创建和处理未达标（任务指南）</span><span class="sxs-lookup"><span data-stu-id="3b439-145">Create and process a non conformance (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-process-non-conformance)

[<span data-ttu-id="3b439-146">质量管理流程</span><span class="sxs-lookup"><span data-stu-id="3b439-146">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="3b439-147">设置不符合项管理的先决条件（任务指南）</span><span class="sxs-lookup"><span data-stu-id="3b439-147">Set up prerequisites for non-conformance management (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/inventory/tasks/set-up-prerequisites-nonconformance-management)
