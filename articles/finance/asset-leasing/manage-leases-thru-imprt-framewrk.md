---
title: 通过租赁导入框架管理租赁
description: 本主题说明如何使用租赁导入框架同时调整多个租赁。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 26fb195ff18dc0c86d3546b782265043c2c78bf4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819786"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="19382-103">通过租赁导入框架管理租赁</span><span class="sxs-lookup"><span data-stu-id="19382-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19382-104">本主题说明如何使用租赁导入框架一个步骤调整多个租赁。</span><span class="sxs-lookup"><span data-stu-id="19382-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="19382-105">通过使用此功能，您可以节省时间，还可以通过减少人为错误的几率来确保进行更准确的调整。</span><span class="sxs-lookup"><span data-stu-id="19382-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="19382-106">此外，此功能还可以连接 Microsoft Dynamics 365 Finance 与外部数据实体来高效上传数据。</span><span class="sxs-lookup"><span data-stu-id="19382-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="19382-107">以下数据实体可用于将资产租赁与外部系统集成：</span><span class="sxs-lookup"><span data-stu-id="19382-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="19382-108">租赁暂存</span><span class="sxs-lookup"><span data-stu-id="19382-108">Lease staging</span></span>
- <span data-ttu-id="19382-109">付款合同暂存</span><span class="sxs-lookup"><span data-stu-id="19382-109">Payment contract staging</span></span>
- <span data-ttu-id="19382-110">执行合同暂存</span><span class="sxs-lookup"><span data-stu-id="19382-110">Executory contract staging</span></span>

<span data-ttu-id="19382-111">您可以使用导入过程调整租赁，更新非金融信息或添加新租赁。</span><span class="sxs-lookup"><span data-stu-id="19382-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="19382-112">导入之前，您可以查看和编辑租赁数据。</span><span class="sxs-lookup"><span data-stu-id="19382-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="19382-113">系统可以通过租赁导入套件运行以下三个过程。</span><span class="sxs-lookup"><span data-stu-id="19382-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="19382-114">流程类型</span><span class="sxs-lookup"><span data-stu-id="19382-114">Process type</span></span>  | <span data-ttu-id="19382-115">说明</span><span class="sxs-lookup"><span data-stu-id="19382-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="19382-116">添加记录</span><span class="sxs-lookup"><span data-stu-id="19382-116">Add record</span></span>    | <span data-ttu-id="19382-117">采用此流程类型的迁移租赁会在系统中创建租赁。</span><span class="sxs-lookup"><span data-stu-id="19382-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="19382-118">必须手动确认付款计划，并且在迁移后必须手动过帐初始确认日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="19382-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="19382-119">更新记录</span><span class="sxs-lookup"><span data-stu-id="19382-119">Update record</span></span> | <span data-ttu-id="19382-120">采用此流程类型的迁移租赁将更新系统中已存在的租赁的字段值。</span><span class="sxs-lookup"><span data-stu-id="19382-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="19382-121">将仅更新 **更新字段选择** 页面中已选择的字段。</span><span class="sxs-lookup"><span data-stu-id="19382-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="19382-122">我们建议您在 **更新字段选择** 页面中选择非金融字段，因为此流程类型不会调整租赁。</span><span class="sxs-lookup"><span data-stu-id="19382-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="19382-123">调整记录</span><span class="sxs-lookup"><span data-stu-id="19382-123">Adjust record</span></span> | <span data-ttu-id="19382-124">采用此流程类型的迁移租赁会调整租赁。</span><span class="sxs-lookup"><span data-stu-id="19382-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="19382-125">此调整将导致对租赁进行金融租赁修改。</span><span class="sxs-lookup"><span data-stu-id="19382-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="19382-126">处理租赁后，系统会使用租赁导入套件中的新数据创建新的付款计划。</span><span class="sxs-lookup"><span data-stu-id="19382-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="19382-127">系统不会确认付款计划或过帐调整日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="19382-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="19382-128">在通过 **数据管理** 工作区上传信息之后，请打开 **导入标题** 页面（**资产租赁 \> 租赁导入框架 \> 导入标题**）。</span><span class="sxs-lookup"><span data-stu-id="19382-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="19382-129">此页面列出了前面列出的三个数据实体的所有导入。</span><span class="sxs-lookup"><span data-stu-id="19382-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="19382-130">要在运行处理之前查看租赁暂存数据，请选择 **暂存数据**。</span><span class="sxs-lookup"><span data-stu-id="19382-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="19382-131">比较功能用于将要导入的记录与系统中已经存在的相应记录进行比较。</span><span class="sxs-lookup"><span data-stu-id="19382-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="19382-132">要比较单个租赁记录，请选择一个租赁，然后选择 **比较**。</span><span class="sxs-lookup"><span data-stu-id="19382-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="19382-133">迁移租赁记录之前，您应该完成此步骤以生成一个 **差异** 报告。</span><span class="sxs-lookup"><span data-stu-id="19382-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="19382-134">比较功能将暂存数据中的值与系统中当前租赁的值进行比较。</span><span class="sxs-lookup"><span data-stu-id="19382-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="19382-135">比较功能不适用于采用 **添加记录** 流程类型的租赁，因为没有什么可与这种租赁进行比较。</span><span class="sxs-lookup"><span data-stu-id="19382-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="19382-136">要同时比较多个租赁，请转到 **资产租赁 \> 租赁导入框架 \> 定期 \> 比较**，然后选择 **比较**。</span><span class="sxs-lookup"><span data-stu-id="19382-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="19382-137">对于每个实体，您可以查看系统中当前内容与暂存表中内容之间的差异。</span><span class="sxs-lookup"><span data-stu-id="19382-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="19382-138">对于暂存表中的每个实体，选择 **查看差异**。</span><span class="sxs-lookup"><span data-stu-id="19382-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="19382-139">出现的对话框显示当前值和建议的暂存值。</span><span class="sxs-lookup"><span data-stu-id="19382-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="19382-140">您也可以通过在 **新值** 列中更新再选择 **更新暂存** 来更新暂存值。</span><span class="sxs-lookup"><span data-stu-id="19382-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="19382-141">您可以验证租赁，以确保可以将记录导入系统中，而不会产生错误。</span><span class="sxs-lookup"><span data-stu-id="19382-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="19382-142">在迁移租赁记录之前，系统将运行几次验证以确保成功导入记录。</span><span class="sxs-lookup"><span data-stu-id="19382-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="19382-143">要验证单个租赁，请选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="19382-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="19382-144">要同时验证多个租赁，请转到 **资产租赁 \> 租赁导入框架 \> 定期 \> 验证**，然后选择 **比较**。</span><span class="sxs-lookup"><span data-stu-id="19382-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="19382-145">要处理单个租赁，请在 **导入标题** 页中选择 **迁移租赁记录**。</span><span class="sxs-lookup"><span data-stu-id="19382-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="19382-146">迁移租赁时，系统将执行 **流程类型** 字段中指定的操作。</span><span class="sxs-lookup"><span data-stu-id="19382-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="19382-147">要同时验证多个租赁，请转到 **资产租赁 \> 租赁导入框架 \> 定期 \> 验证**，然后选择 **比较**。</span><span class="sxs-lookup"><span data-stu-id="19382-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="19382-148">比较租赁后，您可以运行报告以查看导入 ID 中包含的每个租赁的差异。</span><span class="sxs-lookup"><span data-stu-id="19382-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="19382-149">要为一份租赁运行报告，请在暂存数据中选择该租赁，然后选择 **比较并查看报告 \> 差异报告**。</span><span class="sxs-lookup"><span data-stu-id="19382-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="19382-150">要同时验证多个租赁，请转到 **资产租赁 \> 查询和报告 \> 差异报告**  验证，然后选择 **比较**。</span><span class="sxs-lookup"><span data-stu-id="19382-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="19382-151">设置更新字段</span><span class="sxs-lookup"><span data-stu-id="19382-151">Set up update fields</span></span>

<span data-ttu-id="19382-152">如果您使用租赁导入框架更新租赁，并且流程类型为 **更新记录**，您可以选择要更新的特定字段。</span><span class="sxs-lookup"><span data-stu-id="19382-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="19382-153">转到 **资产租赁 \> 租赁导入框架 \> 设置 \> 更新字段选择**。</span><span class="sxs-lookup"><span data-stu-id="19382-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="19382-154">在出现的页面上，选择要更新的字段，然后选择绿色箭头将其移至 **选定字段** 列表。</span><span class="sxs-lookup"><span data-stu-id="19382-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="19382-155">只能使用租赁导入套件更新 **选定字段** 列表中的字段。</span><span class="sxs-lookup"><span data-stu-id="19382-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]