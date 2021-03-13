---
title: 设置原因代码
description: Dynamics 365 Human Resources 使用原因代码来解释为什么员工的福利正在更改。
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae82c8312d344f5380adec8413766304681a0a05
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111613"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="c11c7-103">设置原因代码</span><span class="sxs-lookup"><span data-stu-id="c11c7-103">Set up reason codes</span></span>

<span data-ttu-id="c11c7-104">Dynamics 365 Human Resources 使用原因代码来解释为什么员工的福利正在更改。</span><span class="sxs-lookup"><span data-stu-id="c11c7-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="c11c7-105">自 2021 年 1 月起，原因代码将迁移到 **人事管理** 工作区，而不是 **福利管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="c11c7-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="c11c7-106">有关详细信息，请参阅[将原因代码手动迁移到“人事管理”](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management)。</span><span class="sxs-lookup"><span data-stu-id="c11c7-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="c11c7-107">创建原因代码</span><span class="sxs-lookup"><span data-stu-id="c11c7-107">Create reason codes</span></span>

1. <span data-ttu-id="c11c7-108">在 **人事管理** 工作区（或 **福利管理** 工作区(如果您的原因代码尚未迁移)），选择 **链接**，然后选择 **原因代码**。</span><span class="sxs-lookup"><span data-stu-id="c11c7-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="c11c7-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c11c7-109">Select **New**.</span></span>

3. <span data-ttu-id="c11c7-110">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="c11c7-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c11c7-111">字段</span><span class="sxs-lookup"><span data-stu-id="c11c7-111">Field</span></span> | <span data-ttu-id="c11c7-112">说明</span><span class="sxs-lookup"><span data-stu-id="c11c7-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c11c7-113">**原因代码**</span><span class="sxs-lookup"><span data-stu-id="c11c7-113">**Reason code**</span></span> | <span data-ttu-id="c11c7-114">用于标识员工更改福利计划登记的原因的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="c11c7-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="c11c7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="c11c7-115">**Description**</span></span> | <span data-ttu-id="c11c7-116">原因代码的描述。</span><span class="sxs-lookup"><span data-stu-id="c11c7-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="c11c7-117">在 **适用场景** 下，将 **福利管理** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c11c7-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="c11c7-118">（如果原因代码尚未迁移到 **人事管理** 工作区则不适用。）</span><span class="sxs-lookup"><span data-stu-id="c11c7-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="c11c7-119">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c11c7-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="c11c7-120">将原因代码手动迁移到“人事管理”</span><span class="sxs-lookup"><span data-stu-id="c11c7-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="c11c7-121">2021 年 1 月，原因代码将迁移到 **人事管理** 工作区，而不是 **福利管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="c11c7-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="c11c7-122">大部分原因代码数据将在您的环境中自动迁移。</span><span class="sxs-lookup"><span data-stu-id="c11c7-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="c11c7-123">部分原因代码数据可能无法迁移。</span><span class="sxs-lookup"><span data-stu-id="c11c7-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="c11c7-124">例如，原因码现在最多包含 15 个字符，因此任何长度超过 15 个字符的原因码都不会自动迁移。</span><span class="sxs-lookup"><span data-stu-id="c11c7-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="c11c7-125">您会在 **福利管理** 工作区的 **链接** 页上看到一个横幅，通知您有关迁移以及是否有任何原因代码未迁移的信息。</span><span class="sxs-lookup"><span data-stu-id="c11c7-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="c11c7-126">选择 **原因代码** 了解有关迁移状态的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c11c7-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="c11c7-127">[![原因代码](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="c11c7-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="c11c7-128">选择迁移失败的原因代码。</span><span class="sxs-lookup"><span data-stu-id="c11c7-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="c11c7-129">[![原因代码迁移状态](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="c11c7-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="c11c7-130">选择 **迁移原因代码**。</span><span class="sxs-lookup"><span data-stu-id="c11c7-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="c11c7-131">[![迁移原因代码](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="c11c7-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="c11c7-132">在 **福利原因代码迁移** 窗格中，有两个用于映射到人事管理原因代码的选项：</span><span class="sxs-lookup"><span data-stu-id="c11c7-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="c11c7-133">要在“人事管理”中使用现有原因代码，从 **使用现有原因代码** 下拉列表中选择一个。</span><span class="sxs-lookup"><span data-stu-id="c11c7-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="c11c7-134">如果尚未将另一个福利管理原因代码迁移到“人事管理”，您只能在其中使用现有原因代码。</span><span class="sxs-lookup"><span data-stu-id="c11c7-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="c11c7-135">要在“人事管理”中创建新的原因代码，在 **新建原因代码** 中输入新的原因代码，然后在 **新增描述** 中输入描述。</span><span class="sxs-lookup"><span data-stu-id="c11c7-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="c11c7-136">[![映射到人事管理原因代码](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="c11c7-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="c11c7-137">原因代码迁移到“人事管理”后，在“福利管理”中使用它们的选项将自动设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c11c7-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="c11c7-138">[![在“福利管理”中使用原因代码](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="c11c7-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>