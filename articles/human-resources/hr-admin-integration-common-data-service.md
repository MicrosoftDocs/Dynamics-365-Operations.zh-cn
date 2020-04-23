---
title: 配置 Common Data Service 集成
description: 您可以打开或关闭 Common Data Service 和 Dynamics 365 Human Resources 之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04280aa0908ed6dab86ef87b6c1843e4b4348e08
ms.sourcegitcommit: c9657b44adb9c1a77c7c2f6ab63a58cc848974ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198414"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="5c419-104">配置 Common Data Service 集成</span><span class="sxs-lookup"><span data-stu-id="5c419-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="5c419-105">您可以打开或关闭 Common Data Service 和 Dynamics 365 Human Resources 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="5c419-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="5c419-106">您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。</span><span class="sxs-lookup"><span data-stu-id="5c419-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="5c419-107">关闭集成后，用户可以在 Human Resources 或 Common Data Service 中进行更改，但是这些更改在两个环境之间不同步。</span><span class="sxs-lookup"><span data-stu-id="5c419-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="5c419-108">默认情况下，已关闭 Human Resources 和 Common Data Service 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="5c419-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="5c419-109">在以下情况下，您可能需要关闭集成：</span><span class="sxs-lookup"><span data-stu-id="5c419-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="5c419-110">您正在通过数据管理框架填写数据，并且必须多次导入数据才能使其进入正确状态。</span><span class="sxs-lookup"><span data-stu-id="5c419-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="5c419-111">Human Resources 或 Common Data Service 中的数据存在问题。</span><span class="sxs-lookup"><span data-stu-id="5c419-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="5c419-112">如果关闭集成，您可以在一个环境中删除一条记录，而在另一个环境中不删除。</span><span class="sxs-lookup"><span data-stu-id="5c419-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="5c419-113">重新打开集成后，未删除记录的环境中的记录将同步到已删除记录的环境。</span><span class="sxs-lookup"><span data-stu-id="5c419-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="5c419-114">同步将在下一次运行 **Common Data Service 集成错过的请求同步**批处理作业时开始。</span><span class="sxs-lookup"><span data-stu-id="5c419-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="5c419-115">关闭数据集成时，请确保不要在两个环境中编辑同一个记录。</span><span class="sxs-lookup"><span data-stu-id="5c419-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="5c419-116">当您重新打开集成时，上次编辑的记录将被同步。</span><span class="sxs-lookup"><span data-stu-id="5c419-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="5c419-117">因此，如果您在两个环境中均未对记录进行相同更改，可能会发生数据丢失。</span><span class="sxs-lookup"><span data-stu-id="5c419-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="5c419-118">访问 Common Data Service 集成页面</span><span class="sxs-lookup"><span data-stu-id="5c419-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="5c419-119">在要查看或配置与 Common Data Service 集成的设置的 Human Resources 实例中，选择**系统管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="5c419-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="5c419-120">[![系统管理磁贴](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="5c419-121">选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="5c419-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="5c419-122">[![链接选项卡](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="5c419-123">在**集成**下，选择 **Common Data Service 配置**。</span><span class="sxs-lookup"><span data-stu-id="5c419-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="5c419-124">[![Common Data Service 配置链接](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="5c419-125">打开或关闭 Human Resources 和 Common Data Service 之间的数据集成</span><span class="sxs-lookup"><span data-stu-id="5c419-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="5c419-126">要打开集成，请将**启用对 Common Data Service 的集成**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="5c419-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c419-127">当您打开集成时，下次运行 **Common Data Service 集成错过的请求同步**批处理作业时，将同步数据。</span><span class="sxs-lookup"><span data-stu-id="5c419-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="5c419-128">批处理作业完成后，所有数据都应该可用。</span><span class="sxs-lookup"><span data-stu-id="5c419-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="5c419-129">要关闭集成，请将此选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="5c419-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="5c419-130">[![打开或关闭 Common Data Service 集成](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="5c419-131">查看数据集成详细信息</span><span class="sxs-lookup"><span data-stu-id="5c419-131">View data integration details</span></span>

<span data-ttu-id="5c419-132">在 **Common Data Service 集成**页面的**管理**快速选项卡上，您可以看到记录在 Human Resources 和 Common Data Service 之间如何链接在一起。</span><span class="sxs-lookup"><span data-stu-id="5c419-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="5c419-133">要查看实体的记录，请在 **CDS 实体名称**字段中选择实体。</span><span class="sxs-lookup"><span data-stu-id="5c419-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="5c419-134">网格显示链接到所选实体的所有记录。</span><span class="sxs-lookup"><span data-stu-id="5c419-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="5c419-135">[![查看实体的记录](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5c419-136">当前不会列出所有 Common Data Service 实体。</span><span class="sxs-lookup"><span data-stu-id="5c419-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="5c419-137">只有支持使用自定义字段的实体会显示在网格中。</span><span class="sxs-lookup"><span data-stu-id="5c419-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="5c419-138">新实体将在陆续发布的 Human Resources 中提供。</span><span class="sxs-lookup"><span data-stu-id="5c419-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="5c419-139">网格包括以下字段：</span><span class="sxs-lookup"><span data-stu-id="5c419-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="5c419-140">**CDS 实体名称** – Common Data Service 中实体的名称。</span><span class="sxs-lookup"><span data-stu-id="5c419-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="5c419-141">**CDS 实体引用** – Common Data Service 用于标识记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="5c419-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="5c419-142">此值等效于 Human Resources **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="5c419-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="5c419-143">在 Microsoft Excel 中打开 Common Data Service 实体时，您可以找到此标识符。</span><span class="sxs-lookup"><span data-stu-id="5c419-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="5c419-144">**Human Resources 实体名称** – 上次将数据同步到 Common Data Service 的实体。</span><span class="sxs-lookup"><span data-stu-id="5c419-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="5c419-145">此实体可以具有 Common Data Service 前缀或另一个前缀。</span><span class="sxs-lookup"><span data-stu-id="5c419-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="5c419-146">**Human Resources 引用** – 与 Human Resources 中的记录关联的 **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="5c419-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="5c419-147">**已从 CDS 中删除** – 指示记录是否已从 Common Data Service 中删除的值。</span><span class="sxs-lookup"><span data-stu-id="5c419-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="5c419-148">从 Common Data Service 中删除 Human Resources 中的记录的关联</span><span class="sxs-lookup"><span data-stu-id="5c419-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="5c419-149">如果您在 Human Resources 和 Common Data Service 之间进行数据同步期间遇到问题，可以通过清除跟踪并使跟踪表重新同步来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="5c419-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="5c419-150">如果您删除关联，然后更改或删除 Common Data Service 中的记录，更改将不会同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="5c419-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="5c419-151">如果您在 Human Resources 中进行更改，将创建新的跟踪记录，并在 Common Data Service 中更新该记录。</span><span class="sxs-lookup"><span data-stu-id="5c419-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="5c419-152">要删除 Human Resources 和 Common Data Service 之间的记录的关联，请在 **CDS 实体名称**字段中选择实体，然后选择**清除跟踪信息**。</span><span class="sxs-lookup"><span data-stu-id="5c419-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="5c419-153">[![清除跟踪信息](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="5c419-154">要在清除跟踪后在实体上运行完全同步，请参见下一个过程。</span><span class="sxs-lookup"><span data-stu-id="5c419-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="5c419-155">在 Human Resources 和 Common Data Service 之间同步实体</span><span class="sxs-lookup"><span data-stu-id="5c419-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="5c419-156">在以下情况下使用此过程：</span><span class="sxs-lookup"><span data-stu-id="5c419-156">Use this procedure when:</span></span>

- <span data-ttu-id="5c419-157">从 Common Data Service 进行的更改需要很长时间才会在 Human Resources 中显示。</span><span class="sxs-lookup"><span data-stu-id="5c419-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="5c419-158">必须在清除跟踪后刷新跟踪表。</span><span class="sxs-lookup"><span data-stu-id="5c419-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="5c419-159">若要在 Human Resources 与 Common Data Service 之间对实体运行网站同步：</span><span class="sxs-lookup"><span data-stu-id="5c419-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="5c419-160">在 **CDS 实体名称**字段中选择实体。</span><span class="sxs-lookup"><span data-stu-id="5c419-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="5c419-161">选择**立即同步**。</span><span class="sxs-lookup"><span data-stu-id="5c419-161">Select **Sync now**.</span></span>

<span data-ttu-id="5c419-162">[![运行完全同步](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="5c419-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


