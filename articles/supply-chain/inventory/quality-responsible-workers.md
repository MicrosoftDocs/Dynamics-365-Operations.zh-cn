---
title: 负责审核不符合项的工作人员
description: 本主题介绍如何配置负责审核不符合项的工作人员。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956567"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="e3bec-103">负责审核不符合项的工作人员</span><span class="sxs-lookup"><span data-stu-id="e3bec-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3bec-104">本主题介绍如何配置负责审核不符合项的工作人员。</span><span class="sxs-lookup"><span data-stu-id="e3bec-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="e3bec-105">必须先审核不符合项，然后用户才能够开始输入更正或操作等详细信息。</span><span class="sxs-lookup"><span data-stu-id="e3bec-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="e3bec-106">必须先将用户的用户 ID（用户记录）链接到工作人员记录，然后用户才能够批准或拒绝不符合项。</span><span class="sxs-lookup"><span data-stu-id="e3bec-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="e3bec-107">您可以选择配置负责质量的工作人员，然后允许一个工作人员代表另一个工作人员审核工作。</span><span class="sxs-lookup"><span data-stu-id="e3bec-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="e3bec-108">支持用户进行不符合项处理</span><span class="sxs-lookup"><span data-stu-id="e3bec-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="e3bec-109">您必须先将用户的用户记录链接到工作人员记录，然后用户才能够批准或拒绝不符合项。</span><span class="sxs-lookup"><span data-stu-id="e3bec-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="e3bec-110">然后审核字段可以自动设置，并可以为工时单自动填充当前用户。</span><span class="sxs-lookup"><span data-stu-id="e3bec-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="e3bec-111">您必须先在用户的用户选项中启用文档处理，然后用户才能够使用文档注释。</span><span class="sxs-lookup"><span data-stu-id="e3bec-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="e3bec-112">转到 **系统管理 \> 用户 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="e3bec-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="e3bec-113">查找并打开应该可以批准或拒绝不符合项的用户。</span><span class="sxs-lookup"><span data-stu-id="e3bec-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="e3bec-114">将 **人员** 字段设置为与当前用户记录相关的工作人员的姓名。</span><span class="sxs-lookup"><span data-stu-id="e3bec-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="e3bec-115">在操作窗格上，选择 **用户选项**。</span><span class="sxs-lookup"><span data-stu-id="e3bec-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="e3bec-116">在当前用户记录的 **选项** 页面上的 **首选项** 选项卡上，将 **启用文档处理** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="e3bec-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="e3bec-117">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="e3bec-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="e3bec-118">定义负责质量的工作人员</span><span class="sxs-lookup"><span data-stu-id="e3bec-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="e3bec-119">转到 **库存管理 \> 设置 \> 质量控制 \> 负责质量的工作人员**。</span><span class="sxs-lookup"><span data-stu-id="e3bec-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="e3bec-120">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e3bec-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="e3bec-121">在 **工作人员** 字段中，选择输入质量数据的工作人员。</span><span class="sxs-lookup"><span data-stu-id="e3bec-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="e3bec-122">在 **负责工作人员** 字段中，选择所选工作人员代表其参与工作的工作人员。</span><span class="sxs-lookup"><span data-stu-id="e3bec-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="e3bec-123">不符合项创建和更新时，此工作人员默认将被输入到 **工作人员** 字段中。</span><span class="sxs-lookup"><span data-stu-id="e3bec-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3bec-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="e3bec-124">Additional resources</span></span>

- [<span data-ttu-id="e3bec-125">质量管理概览</span><span class="sxs-lookup"><span data-stu-id="e3bec-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="e3bec-126">启用质量和不符合项管理</span><span class="sxs-lookup"><span data-stu-id="e3bec-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="e3bec-127">质量费用</span><span class="sxs-lookup"><span data-stu-id="e3bec-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="e3bec-128">不符合项的隔离区域</span><span class="sxs-lookup"><span data-stu-id="e3bec-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="e3bec-129">不符合项的诊断类型</span><span class="sxs-lookup"><span data-stu-id="e3bec-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="e3bec-130">不符合项的质量费用</span><span class="sxs-lookup"><span data-stu-id="e3bec-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="e3bec-131">不符合项的操作</span><span class="sxs-lookup"><span data-stu-id="e3bec-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="e3bec-132">仓库流程质量管理</span><span class="sxs-lookup"><span data-stu-id="e3bec-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
