---
title: 配置 Common Data Service 集成
description: 您可以打开或关闭 Common Data Service 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621296"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="b05a1-104">配置 Common Data Service 集成</span><span class="sxs-lookup"><span data-stu-id="b05a1-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="b05a1-105">您可以打开或关闭 Common Data Service 和 Dynamics 365 Human Resources 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="b05a1-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="b05a1-106">您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。</span><span class="sxs-lookup"><span data-stu-id="b05a1-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="b05a1-107">关闭集成后，用户可以在 Human Resources 或 Common Data Service 中进行更改，但是这些更改在两个环境之间不同步。</span><span class="sxs-lookup"><span data-stu-id="b05a1-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="b05a1-108">默认情况下，已关闭 Human Resources 和 Common Data Service 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="b05a1-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="b05a1-109">在以下情况下，您可能需要关闭集成：</span><span class="sxs-lookup"><span data-stu-id="b05a1-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="b05a1-110">您正在通过数据管理框架填写数据，并且必须多次导入数据才能使其进入正确状态。</span><span class="sxs-lookup"><span data-stu-id="b05a1-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="b05a1-111">Human Resources 或 Common Data Service 中的数据存在问题。</span><span class="sxs-lookup"><span data-stu-id="b05a1-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="b05a1-112">如果关闭集成，您可以在一个环境中删除一条记录，而在另一个环境中不删除。</span><span class="sxs-lookup"><span data-stu-id="b05a1-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="b05a1-113">重新打开集成后，未删除记录的环境中的记录将同步到已删除记录的环境。</span><span class="sxs-lookup"><span data-stu-id="b05a1-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="b05a1-114">同步将在下一次运行 **Common Data Service 集成错过的请求同步**批处理作业时开始。</span><span class="sxs-lookup"><span data-stu-id="b05a1-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="b05a1-115">关闭数据集成时，请确保不要在两个环境中编辑同一个记录。</span><span class="sxs-lookup"><span data-stu-id="b05a1-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="b05a1-116">当您重新打开集成时，上次编辑的记录将被同步。</span><span class="sxs-lookup"><span data-stu-id="b05a1-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="b05a1-117">因此，如果您在两个环境中均未对记录进行相同更改，可能会发生数据丢失。</span><span class="sxs-lookup"><span data-stu-id="b05a1-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="b05a1-118">访问 Common Data Service 集成页面</span><span class="sxs-lookup"><span data-stu-id="b05a1-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="b05a1-119">在要查看或配置与 Common Data Service 集成的设置的 Human Resources 实例中，选择**系统管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="b05a1-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="b05a1-120">[![系统管理磁贴](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="b05a1-121">选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="b05a1-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="b05a1-122">[![链接选项卡](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="b05a1-123">在**集成**下，选择 **Common Data Service 配置**。</span><span class="sxs-lookup"><span data-stu-id="b05a1-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="b05a1-124">[![Common Data Service 配置链接](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="b05a1-125">打开或关闭 Human Resources 和 Common Data Service 之间的数据集成</span><span class="sxs-lookup"><span data-stu-id="b05a1-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="b05a1-126">要打开集成，请将**启用对 Common Data Service 的集成**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b05a1-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b05a1-127">当您打开集成时，下次运行 **Common Data Service 集成错过的请求同步**批处理作业时，将同步数据。</span><span class="sxs-lookup"><span data-stu-id="b05a1-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="b05a1-128">批处理作业完成后，所有数据都应该可用。</span><span class="sxs-lookup"><span data-stu-id="b05a1-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="b05a1-129">要关闭集成，请将此选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="b05a1-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="b05a1-130">[![打开或关闭 Common Data Service 集成](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="b05a1-131">强烈建议在执行数据迁移任务时关闭 Common Data Service 集成。</span><span class="sxs-lookup"><span data-stu-id="b05a1-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="b05a1-132">上载大量数据会严重影响性能。</span><span class="sxs-lookup"><span data-stu-id="b05a1-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="b05a1-133">例如，启用集成后，上载 2000 个工作人员可能要花费几个小时，禁用后则不到一小时。</span><span class="sxs-lookup"><span data-stu-id="b05a1-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="b05a1-134">本示例中提供的数字仅用于演示目的。</span><span class="sxs-lookup"><span data-stu-id="b05a1-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="b05a1-135">导入记录所需的确切时间由于很多因素可能出现很大差异。</span><span class="sxs-lookup"><span data-stu-id="b05a1-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="b05a1-136">查看数据集成详细信息</span><span class="sxs-lookup"><span data-stu-id="b05a1-136">View data integration details</span></span>

<span data-ttu-id="b05a1-137">在 **Common Data Service 集成**页面的**管理**快速选项卡上，您可以看到记录在 Human Resources 和 Common Data Service 之间如何链接在一起。</span><span class="sxs-lookup"><span data-stu-id="b05a1-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="b05a1-138">要查看实体的记录，请在 **CDS 实体名称**字段中选择实体。</span><span class="sxs-lookup"><span data-stu-id="b05a1-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="b05a1-139">网格显示链接到所选实体的所有记录。</span><span class="sxs-lookup"><span data-stu-id="b05a1-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="b05a1-140">[![查看实体的记录](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b05a1-141">当前不会列出所有 Common Data Service 实体。</span><span class="sxs-lookup"><span data-stu-id="b05a1-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="b05a1-142">只有支持使用自定义字段的实体会显示在网格中。</span><span class="sxs-lookup"><span data-stu-id="b05a1-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="b05a1-143">新实体将在陆续发布的 Human Resources 中提供。</span><span class="sxs-lookup"><span data-stu-id="b05a1-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="b05a1-144">网格包括以下字段：</span><span class="sxs-lookup"><span data-stu-id="b05a1-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="b05a1-145">**CDS 实体名称** – Common Data Service 中实体的名称。</span><span class="sxs-lookup"><span data-stu-id="b05a1-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="b05a1-146">**CDS 实体引用** – Common Data Service 用于标识记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="b05a1-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="b05a1-147">此值等效于 Human Resources **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="b05a1-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="b05a1-148">在 Microsoft Excel 中打开 Common Data Service 实体时，您可以找到此标识符。</span><span class="sxs-lookup"><span data-stu-id="b05a1-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="b05a1-149">**Human Resources 实体名称** – 上次将数据同步到 Common Data Service 的实体。</span><span class="sxs-lookup"><span data-stu-id="b05a1-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="b05a1-150">此实体可以具有 Common Data Service 前缀或另一个前缀。</span><span class="sxs-lookup"><span data-stu-id="b05a1-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="b05a1-151">**Human Resources 引用** – 与 Human Resources 中的记录关联的 **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="b05a1-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="b05a1-152">**已从 CDS 中删除** – 指示记录是否已从 Common Data Service 中删除的值。</span><span class="sxs-lookup"><span data-stu-id="b05a1-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="b05a1-153">从 Common Data Service 中删除 Human Resources 中的记录的关联</span><span class="sxs-lookup"><span data-stu-id="b05a1-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="b05a1-154">如果您在 Human Resources 和 Common Data Service 之间进行数据同步期间遇到问题，可以通过清除跟踪并使跟踪表重新同步来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="b05a1-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="b05a1-155">如果您删除关联，然后更改或删除 Common Data Service 中的记录，更改将不会同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="b05a1-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="b05a1-156">如果您在 Human Resources 中进行更改，将创建新的跟踪记录，并在 Common Data Service 中更新该记录。</span><span class="sxs-lookup"><span data-stu-id="b05a1-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="b05a1-157">要删除 Human Resources 和 Common Data Service 之间的记录的关联，请在 **CDS 实体名称**字段中选择实体，然后选择**清除跟踪信息**。</span><span class="sxs-lookup"><span data-stu-id="b05a1-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="b05a1-158">[![清除跟踪信息](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="b05a1-159">要在清除跟踪后在实体上运行完全同步，请参见下一个过程。</span><span class="sxs-lookup"><span data-stu-id="b05a1-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="b05a1-160">在 Human Resources 和 Common Data Service 之间同步实体</span><span class="sxs-lookup"><span data-stu-id="b05a1-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="b05a1-161">在以下情况下使用此过程：</span><span class="sxs-lookup"><span data-stu-id="b05a1-161">Use this procedure when:</span></span>

- <span data-ttu-id="b05a1-162">从 Common Data Service 进行的更改需要很长时间才会在 Human Resources 中显示。</span><span class="sxs-lookup"><span data-stu-id="b05a1-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="b05a1-163">必须在清除跟踪后刷新跟踪表。</span><span class="sxs-lookup"><span data-stu-id="b05a1-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="b05a1-164">若要在 Human Resources 与 Common Data Service 之间对实体运行网站同步：</span><span class="sxs-lookup"><span data-stu-id="b05a1-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="b05a1-165">在 **CDS 实体名称**字段中选择实体。</span><span class="sxs-lookup"><span data-stu-id="b05a1-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="b05a1-166">选择**立即同步**。</span><span class="sxs-lookup"><span data-stu-id="b05a1-166">Select **Sync now**.</span></span>

<span data-ttu-id="b05a1-167">[![运行完全同步](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="b05a1-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


