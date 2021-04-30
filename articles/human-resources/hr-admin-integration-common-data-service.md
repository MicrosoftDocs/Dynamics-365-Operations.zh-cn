---
title: 配置 Dataverse 集成
description: 您可以打开或关闭 Microsoft Dataverse 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步表，以帮助解决两个环境之间的数据问题。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890020"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="92893-104">配置 Dataverse 集成</span><span class="sxs-lookup"><span data-stu-id="92893-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="92893-105">您可以打开或关闭 Microsoft Dataverse 和 Dynamics 365 Human Resources 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="92893-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="92893-106">您还可以查看同步详细信息、清除跟踪数据以及重新同步表，以帮助解决两个环境之间的数据问题。</span><span class="sxs-lookup"><span data-stu-id="92893-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="92893-107">有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="92893-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="92893-108">关闭集成后，用户可以在 Human Resources 或 Dataverse 中进行更改，但是这些更改在两个环境之间不同步。</span><span class="sxs-lookup"><span data-stu-id="92893-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="92893-109">默认情况下，已关闭 Human Resources 和 Dataverse 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="92893-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="92893-110">在以下情况下，您可能需要关闭集成：</span><span class="sxs-lookup"><span data-stu-id="92893-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="92893-111">您正在通过数据管理框架填写数据，并且必须多次导入数据才能使其进入正确状态。</span><span class="sxs-lookup"><span data-stu-id="92893-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="92893-112">Human Resources 或 Dataverse 中的数据存在问题。</span><span class="sxs-lookup"><span data-stu-id="92893-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="92893-113">如果关闭集成，您可以在一个环境中删除一条记录，而在另一个环境中不删除。</span><span class="sxs-lookup"><span data-stu-id="92893-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="92893-114">重新打开集成后，未删除记录的环境中的记录将同步到已删除记录的环境。</span><span class="sxs-lookup"><span data-stu-id="92893-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="92893-115">同步将在下一次运行 **Dataverse 集成错过的请求同步** 批处理作业时开始。</span><span class="sxs-lookup"><span data-stu-id="92893-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="92893-116">关闭数据集成时，请确保不要在两个环境中编辑同一个记录。</span><span class="sxs-lookup"><span data-stu-id="92893-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="92893-117">当您重新打开集成时，上次编辑的记录将被同步。</span><span class="sxs-lookup"><span data-stu-id="92893-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="92893-118">因此，如果您在两个环境中均未对记录进行相同更改，可能会发生数据丢失。</span><span class="sxs-lookup"><span data-stu-id="92893-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="92893-119">访问 Dataverse 集成页面</span><span class="sxs-lookup"><span data-stu-id="92893-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="92893-120">在要查看或配置与 Dataverse 集成的设置的 Human Resources 实例中，选择 **系统管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="92893-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="92893-121">[![系统管理磁贴](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="92893-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="92893-122">选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="92893-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="92893-123">[![链接选项卡](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="92893-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="92893-124">在 **集成** 下，选择 **Dataverse 配置**。</span><span class="sxs-lookup"><span data-stu-id="92893-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="92893-125">[![Dataverse 配置链接](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="92893-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="92893-126">打开或关闭 Human Resources 和 Dataverse 之间的数据集成</span><span class="sxs-lookup"><span data-stu-id="92893-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="92893-127">要打开集成，在 **Microsoft Dataverse 集成** 页上将 **启用 Dataverse 集成** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="92893-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92893-128">当您打开集成时，下次运行 **Dataverse 集成错过的请求同步** 批处理作业时，将同步数据。</span><span class="sxs-lookup"><span data-stu-id="92893-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="92893-129">批处理作业完成后，所有数据都应该可用。</span><span class="sxs-lookup"><span data-stu-id="92893-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="92893-130">要关闭集成，请将此选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="92893-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="92893-131">[![打开或关闭 Dataverse 集成](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="92893-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="92893-132">强烈建议在执行数据迁移任务时关闭 Dataverse 集成。</span><span class="sxs-lookup"><span data-stu-id="92893-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="92893-133">上载大量数据会严重影响性能。</span><span class="sxs-lookup"><span data-stu-id="92893-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="92893-134">例如，启用集成后，上载 2000 个工作人员可能要花费几个小时，禁用后则不到一小时。</span><span class="sxs-lookup"><span data-stu-id="92893-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="92893-135">本示例中提供的数字仅用于演示目的。</span><span class="sxs-lookup"><span data-stu-id="92893-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="92893-136">导入记录所需的确切时间由于很多因素可能出现很大差异。</span><span class="sxs-lookup"><span data-stu-id="92893-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="92893-137">查看数据集成详细信息</span><span class="sxs-lookup"><span data-stu-id="92893-137">View data integration details</span></span>

<span data-ttu-id="92893-138">在 **Microsoft Dataverse 集成** 页面的 **管理** 快速选项卡上，您可以看到行在 Human Resources 和 Dataverse 之间如何链接在一起。</span><span class="sxs-lookup"><span data-stu-id="92893-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="92893-139">要查看表的行，在 **Dataverse 表** 字段中选择该表。</span><span class="sxs-lookup"><span data-stu-id="92893-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="92893-140">网格将显示链接到所选表的所有行。</span><span class="sxs-lookup"><span data-stu-id="92893-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="92893-141">当前不会列出所有 Dataverse 表。</span><span class="sxs-lookup"><span data-stu-id="92893-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="92893-142">只有支持使用自定义字段的表会显示在网格中。</span><span class="sxs-lookup"><span data-stu-id="92893-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="92893-143">新表将在陆续发布的 Human Resources 中提供。</span><span class="sxs-lookup"><span data-stu-id="92893-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="92893-144">网格包括以下字段：</span><span class="sxs-lookup"><span data-stu-id="92893-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="92893-145">**Dataverse 表** – Dataverse 中的表的名称。</span><span class="sxs-lookup"><span data-stu-id="92893-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="92893-146">**Dataverse 表引用** – Dataverse 用于标识记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="92893-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="92893-147">此值等效于 Human Resources **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="92893-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="92893-148">在 Microsoft Excel 中打开 Dataverse 表时，您可以找到此标识符。</span><span class="sxs-lookup"><span data-stu-id="92893-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="92893-149">**Human Resources 实体名称** – 上次将数据同步到 Dataverse 的 Human Resources 实体。</span><span class="sxs-lookup"><span data-stu-id="92893-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="92893-150">此实体可以具有 Dataverse 前缀或另一个前缀。</span><span class="sxs-lookup"><span data-stu-id="92893-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="92893-151">**Human Resources 引用** – 与 Human Resources 中的记录关联的 **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="92893-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="92893-152">**已从 Dataverse 中删除** – 指示行是否已从 Dataverse 中删除的值。</span><span class="sxs-lookup"><span data-stu-id="92893-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="92893-153">Human Resources 中的记录与 Dataverse 中的行对应。</span><span class="sxs-lookup"><span data-stu-id="92893-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="92893-154">从 Dataverse 行中删除 Human Resources 记录的关联</span><span class="sxs-lookup"><span data-stu-id="92893-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="92893-155">如果您在 Human Resources 和 Dataverse 之间进行数据同步期间遇到问题，可以通过清除跟踪并使跟踪表重新同步来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="92893-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="92893-156">如果您删除关联，然后更改或删除 Dataverse 中的行，更改将不会同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="92893-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="92893-157">如果您在 Human Resources 中进行更改，将创建新的跟踪记录，并在 Dataverse 中更新该行。</span><span class="sxs-lookup"><span data-stu-id="92893-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="92893-158">要删除 Human Resources 记录和 Dataverse 行之间的记录的关联，请在 **Dataverse 表** 字段中选择表，然后选择 **清除跟踪信息**。</span><span class="sxs-lookup"><span data-stu-id="92893-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="92893-159">[![清除跟踪信息](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="92893-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="92893-160">要在清除跟踪后在表上运行完全同步，请参见下一个过程。</span><span class="sxs-lookup"><span data-stu-id="92893-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="92893-161">在 Human Resources 和 Dataverse 之间同步表</span><span class="sxs-lookup"><span data-stu-id="92893-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="92893-162">在以下情况下使用此过程：</span><span class="sxs-lookup"><span data-stu-id="92893-162">Use this procedure when:</span></span>

- <span data-ttu-id="92893-163">从 Dataverse 进行的更改需要很长时间才会在 Human Resources 中显示。</span><span class="sxs-lookup"><span data-stu-id="92893-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="92893-164">必须在清除跟踪后刷新跟踪表。</span><span class="sxs-lookup"><span data-stu-id="92893-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="92893-165">若要在 Human Resources 与 Dataverse 之间对表运行完全同步：</span><span class="sxs-lookup"><span data-stu-id="92893-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="92893-166">在 **Dataverse 表** 字段中选择表。</span><span class="sxs-lookup"><span data-stu-id="92893-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="92893-167">选择 **立即同步**。</span><span class="sxs-lookup"><span data-stu-id="92893-167">Select **Sync now**.</span></span>

<span data-ttu-id="92893-168">[![运行完全同步](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="92893-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="92893-169">请参阅</span><span class="sxs-lookup"><span data-stu-id="92893-169">See also</span></span>

[<span data-ttu-id="92893-170">Dataverse 表</span><span class="sxs-lookup"><span data-stu-id="92893-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="92893-171">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="92893-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="92893-172">Human Resources 虚拟表常见问题解答</span><span class="sxs-lookup"><span data-stu-id="92893-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="92893-173">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="92893-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="92893-174">术语更新</span><span class="sxs-lookup"><span data-stu-id="92893-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]