---
title: 配置 Common Data Service 集成
description: 您可以打开或关闭 Common Data Service 和 Microsoft Dynamics 365 Human Resources 实例之间的集成。 您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008196"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="fcd27-104">配置 Common Data Service 集成</span><span class="sxs-lookup"><span data-stu-id="fcd27-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="fcd27-105">您可以打开或关闭 Common Data Service 和 Microsoft Dynamics 365 Human Resources 实例之间的集成。</span><span class="sxs-lookup"><span data-stu-id="fcd27-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="fcd27-106">您还可以查看同步详细信息、清除跟踪数据以及重新同步实体，以帮助解决两个环境之间的数据问题。</span><span class="sxs-lookup"><span data-stu-id="fcd27-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="fcd27-107">关闭集成后，用户可以在 Human Resources 或 Common Data Service 中进行更改，但是这些更改在两个环境之间不同步。</span><span class="sxs-lookup"><span data-stu-id="fcd27-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="fcd27-108">默认情况下，Human Resources 和 Common Data Service 之间的集成是打开还是关闭，具体取决于环境中是否存在演示数据：</span><span class="sxs-lookup"><span data-stu-id="fcd27-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="fcd27-109">不包含演示数据的新环境为**关**</span><span class="sxs-lookup"><span data-stu-id="fcd27-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="fcd27-110">包含演示数据的新环境为**开**</span><span class="sxs-lookup"><span data-stu-id="fcd27-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="fcd27-111">包含演示数据的新环境将在预配后开始同步数据。</span><span class="sxs-lookup"><span data-stu-id="fcd27-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="fcd27-112">在以下情况下，您可能需要关闭集成：</span><span class="sxs-lookup"><span data-stu-id="fcd27-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="fcd27-113">您正在通过数据管理框架填写数据，并且必须多次导入数据才能使其进入正确状态。</span><span class="sxs-lookup"><span data-stu-id="fcd27-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="fcd27-114">Human Resources 或 Common Data Service 中的数据存在问题。</span><span class="sxs-lookup"><span data-stu-id="fcd27-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="fcd27-115">如果关闭集成，您可以在一个环境中删除一条记录，而在另一个环境中不删除。</span><span class="sxs-lookup"><span data-stu-id="fcd27-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="fcd27-116">重新打开集成后，未删除记录的环境中的记录将同步回已删除记录的环境。</span><span class="sxs-lookup"><span data-stu-id="fcd27-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="fcd27-117">同步将在下一次运行 **Common Data Service 集成错过的请求同步**批处理作业时开始。</span><span class="sxs-lookup"><span data-stu-id="fcd27-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="fcd27-118">关闭数据集成时，请确保不要在两个环境中编辑同一个记录。</span><span class="sxs-lookup"><span data-stu-id="fcd27-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="fcd27-119">当您重新打开集成时，上次编辑的记录将被同步。</span><span class="sxs-lookup"><span data-stu-id="fcd27-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="fcd27-120">因此，如果您在两个环境中均未对记录进行相同更改，可能会发生数据丢失。</span><span class="sxs-lookup"><span data-stu-id="fcd27-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="fcd27-121">访问 Common Data Service 集成页面</span><span class="sxs-lookup"><span data-stu-id="fcd27-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="fcd27-122">在要查看或配置与 Common Data Service 集成的设置的 Human Resources 实例中，选择**系统管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="fcd27-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="fcd27-123">[![系统管理磁贴](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="fcd27-124">选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="fcd27-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="fcd27-125">[![链接选项卡](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="fcd27-126">在**集成**下，选择 **Common Data Service 配置**。</span><span class="sxs-lookup"><span data-stu-id="fcd27-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="fcd27-127">[![Common Data Service 配置链接](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="fcd27-128">打开或关闭 Human Resources 和 Common Data Service 之间的数据集成</span><span class="sxs-lookup"><span data-stu-id="fcd27-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="fcd27-129">要打开集成，请将**启用对 Common Data Service 的集成**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="fcd27-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fcd27-130">当您打开集成时，下次运行 **Common Data Service 集成错过的请求同步**批处理作业时，将同步数据。</span><span class="sxs-lookup"><span data-stu-id="fcd27-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="fcd27-131">批处理作业完成后，所有数据都应该可用。</span><span class="sxs-lookup"><span data-stu-id="fcd27-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="fcd27-132">要关闭集成，请将此选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="fcd27-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="fcd27-133">[![打开或关闭 Common Data Service 集成](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="fcd27-134">查看数据集成详细信息</span><span class="sxs-lookup"><span data-stu-id="fcd27-134">View data integration details</span></span>

<span data-ttu-id="fcd27-135">在 **Common Data Service 集成**页面的**管理**快速选项卡上，您可以看到记录在 Human Resources 和 Common Data Service 之间如何链接在一起。</span><span class="sxs-lookup"><span data-stu-id="fcd27-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="fcd27-136">要查看实体的记录，请在 **CDS 实体名称**字段中选择实体。</span><span class="sxs-lookup"><span data-stu-id="fcd27-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="fcd27-137">网格显示链接到所选实体的所有记录。</span><span class="sxs-lookup"><span data-stu-id="fcd27-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="fcd27-138">[![查看实体的记录](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="fcd27-139">当前不会列出所有 Common Data Service 实体。</span><span class="sxs-lookup"><span data-stu-id="fcd27-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="fcd27-140">只有支持使用自定义字段的实体会显示在网格中。</span><span class="sxs-lookup"><span data-stu-id="fcd27-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="fcd27-141">新实体将在陆续发布的 Human Resources 中提供。</span><span class="sxs-lookup"><span data-stu-id="fcd27-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="fcd27-142">网格包括以下字段：</span><span class="sxs-lookup"><span data-stu-id="fcd27-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="fcd27-143">**CDS 实体名称** – Common Data Service 中实体的名称。</span><span class="sxs-lookup"><span data-stu-id="fcd27-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="fcd27-144">**CDS 实体引用** – Common Data Service 用于标识记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="fcd27-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="fcd27-145">此值等效于 Human Resources **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="fcd27-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="fcd27-146">在 Microsoft Excel 中打开 Common Data Service 实体时，您可以找到此标识符。</span><span class="sxs-lookup"><span data-stu-id="fcd27-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="fcd27-147">**Human Resources 实体名称** – 上次将数据同步到 Common Data Service 的实体。</span><span class="sxs-lookup"><span data-stu-id="fcd27-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="fcd27-148">此实体可以具有 Common Data Service 前缀或另一个前缀。</span><span class="sxs-lookup"><span data-stu-id="fcd27-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="fcd27-149">**Human Resources 引用** – 与 Human Resources 中的记录关联的 **RecId** 值。</span><span class="sxs-lookup"><span data-stu-id="fcd27-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="fcd27-150">**已从 CDS 中删除** – 指示记录是否已从 Common Data Service 中删除的值。</span><span class="sxs-lookup"><span data-stu-id="fcd27-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="fcd27-151">从 Common Data Service 中删除 Human Resources 中的记录的关联</span><span class="sxs-lookup"><span data-stu-id="fcd27-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="fcd27-152">如果您在 Human Resources 和 Common Data Service 之间进行数据同步期间遇到问题，可以通过清除跟踪并使跟踪表重新同步来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="fcd27-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="fcd27-153">如果您删除关联，然后更改或删除 Common Data Service 中的记录，更改将不会同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="fcd27-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="fcd27-154">如果您在 Human Resources 中进行更改，将创建新的跟踪记录，并在 Common Data Service 中更新该记录。</span><span class="sxs-lookup"><span data-stu-id="fcd27-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="fcd27-155">要删除 Human Resources 和 Common Data Service 之间的记录的关联，请在 **CDS 实体名称**字段中选择实体，然后选择**清除跟踪信息**。</span><span class="sxs-lookup"><span data-stu-id="fcd27-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="fcd27-156">[![清除跟踪信息](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="fcd27-157">要在清除跟踪后在实体上运行完全同步，请参见下一个过程。</span><span class="sxs-lookup"><span data-stu-id="fcd27-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="fcd27-158">在 Human Resources 和 Common Data Service 之间同步实体</span><span class="sxs-lookup"><span data-stu-id="fcd27-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="fcd27-159">如果来自 Common Data Service 的更改花费的时间太长而无法显示在 Human Resources 中，或者在清除跟踪之后必须刷新跟踪表，请使用此过程。</span><span class="sxs-lookup"><span data-stu-id="fcd27-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="fcd27-160">要在 Human Resources 和 Common Data Service 之间的实体上运行完全同步，请在 **CDS 实体名称**字段中选择该实体，然后选择**立即同步**。</span><span class="sxs-lookup"><span data-stu-id="fcd27-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="fcd27-161">[![运行完全同步](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="fcd27-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


