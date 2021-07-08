---
title: 在波次期间计划波次标签打印
description: 本主题介绍了如何设置和使用基于任务的波次标签打印功能。
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 32842c32599b3ca5d84cc9f715a1453d55e176dc
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301878"
---
# <a name="schedule-wave-label-printing-during-wave"></a><span data-ttu-id="ea3c1-103">在波次期间计划波次标签打印</span><span class="sxs-lookup"><span data-stu-id="ea3c1-103">Schedule wave label printing during wave</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea3c1-104">使用 *基于任务的波次标签打印* 功能作为波次流程的一部分，以帮助提高效率，并使系统创建波次标签并在单独的任务中工作。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-104">Use the *Task based wave label printing* feature as part of your waving process to help improve efficiency, and to have the system create wave labels and work in separate tasks.</span></span>

<span data-ttu-id="ea3c1-105">配置波次标签打印的流程很复杂，并且依赖于准确的配置和主数据。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-105">The process of configuring wave label printing is complex and relies on accurate configuration and master data.</span></span> <span data-ttu-id="ea3c1-106">生成波次标签记录失败的情况并不少见，当失败时，整个波次处理都会回滚。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-106">It isn't uncommon for the generation of wave label records to fail, and when it does, the whole wave processing is rolled back.</span></span> <span data-ttu-id="ea3c1-107">*基于任务的波次标签打印* 功能帮助您避免在每次错误打印波次标签时都必须重新创建工作和工作行。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-107">The *Task based wave label printing* feature helps you avoid having to re-create work and work lines every time that a wave label is incorrectly printed.</span></span>

<span data-ttu-id="ea3c1-108">使用 *基于任务的波次标签打印* 功能时，系统首先创建工作和工作行。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-108">When you use the *Task based wave label printing* feature, the system first creates work and work lines.</span></span> <span data-ttu-id="ea3c1-109">然后，创建并打印波次标签。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-109">It then creates and prints wave labels.</span></span> <span data-ttu-id="ea3c1-110">最后，如果正确创建了波次标签，将发放工作和波次以供领料。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-110">Finally, if the wave labels are correctly created, it releases the work and wave for picking.</span></span>

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a><span data-ttu-id="ea3c1-111">在功能管理中打开“基于任务的波次标签打印”功能</span><span class="sxs-lookup"><span data-stu-id="ea3c1-111">Turn on the Task based wave label printing feature in feature management</span></span>

<span data-ttu-id="ea3c1-112">若要使用本主题中描述的功能，必须为您的系统打开这些功能。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-112">To use the features that are described in this topic, they must be turned on for your system.</span></span> <span data-ttu-id="ea3c1-113">使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区按以下顺序打开功能：</span><span class="sxs-lookup"><span data-stu-id="ea3c1-113">Use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to turn on the features in the following order:</span></span>

1. <span data-ttu-id="ea3c1-114">*波次标签打印* – 为波次标签打印启用波次流程方法时需要此功能。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-114">*Wave label printing* – This feature is required to enable the wave process method for wave label printing.</span></span>
1. <span data-ttu-id="ea3c1-115">*组织范围内的工作锁定* - 手动和自动配置计划的工作创建时需要此功能。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-115">*Organization-wide work blocking* – This feature is required for both manual and automatic configuration of scheduled work creation.</span></span>
1. <span data-ttu-id="ea3c1-116">*基于任务的波次标签打印* – 将波次标签打印拆分为单独的交易范围时需要此功能。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-116">*Task based wave label printing* – This feature is required to split off wave label printing to a separate transaction scope.</span></span>

## <a name="manually-enable-the-new-wave-step-method"></a><span data-ttu-id="ea3c1-117">手动启用新的波次步骤方法</span><span class="sxs-lookup"><span data-stu-id="ea3c1-117">Manually enable the new wave step method</span></span>

<span data-ttu-id="ea3c1-118">必须首先创建新的波次步骤方法并启用它来进行并行异步任务处理。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-118">You must first create the new wave step method and enable it for parallel, asynchronous task processing.</span></span>

1. <span data-ttu-id="ea3c1-119">转到 **仓库管理 \> 设置 \> 波次 \> 波次流程方法**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-119">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="ea3c1-120">在操作窗格上，选择 **重新生成方法**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-120">On the Action Pane, select **Regenerate method**.</span></span> <span data-ttu-id="ea3c1-121">请注意，*waveLabelPrinting* 将添加到可在装运波次模板中使用的波次流程方法列表中。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-121">Notice that *waveLabelPrinting* is added to the list of wave process methods that you can use in your shipping wave templates.</span></span>
1. <span data-ttu-id="ea3c1-122">选择 **方法名称** 字段设置为 *waveLabelPrinting* 的记录，然后在操作窗格上，选择 **任务配置**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-122">Select the record where the **Method name** field is set to *waveLabelPrinting*, and then, on the Action Pane, select **Task configuration**.</span></span>
1. <span data-ttu-id="ea3c1-123">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-123">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ea3c1-124">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="ea3c1-124">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ea3c1-125">**仓库** – 选择用于计划工作创建处理的仓库。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-125">**Warehouse** – Select the warehouse that you will use to schedule work creation processing.</span></span> <span data-ttu-id="ea3c1-126">（如果您使用演示数据进行测试，可以选择仓库 *24*。）</span><span class="sxs-lookup"><span data-stu-id="ea3c1-126">(If you're using demo data for testing purposes, you can select warehouse *24*.)</span></span>
    - <span data-ttu-id="ea3c1-127">**最大批处理任务数** – 指定最大批处理任务数。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-127">**Maximum number of batch tasks** – Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="ea3c1-128">在大多数情况下，该值应介于 *8* 至 *16* 之间。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-128">In most cases, the value should be from *8* through *16*.</span></span> <span data-ttu-id="ea3c1-129">但是，我们建议您尝试为您的场景找到最佳设置。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-129">However, we recommend that you experiment to find the optimal setting for your scenarios.</span></span>
    - <span data-ttu-id="ea3c1-130">**波次处理批处理组** – 选择专用的波次处理批处理组以优化批处理队列处理。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-130">**Wave processing batch group** – Select a dedicated wave processing batch group to optimize batch queue processing.</span></span>

<span data-ttu-id="ea3c1-131">您现在可以更新现有的波次模板，以便它使用 *波次标签打印* 波次处理方法。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-131">You can now update an existing wave template so that it uses the *Wave label printing* wave processing method.</span></span> <span data-ttu-id="ea3c1-132">或者，您可以创建一个使用它的新波次模板。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-132">Alternatively, you can create a new wave template that uses it.</span></span>

1. <span data-ttu-id="ea3c1-133">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-133">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="ea3c1-134">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ea3c1-135">在列表窗格中，选择要更新的波次模板。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-135">In the list pane, select the wave template to update.</span></span> <span data-ttu-id="ea3c1-136">（如果您使用演示数据进行测试，可以选择仓库 *24 装运默认*。）</span><span class="sxs-lookup"><span data-stu-id="ea3c1-136">(If you're using demo data for testing purposes, you can select *24 Shipping default*.)</span></span>
1. <span data-ttu-id="ea3c1-137">在 **方法** 快速选项卡上的 **其余方法** 列中，选择 **名称** 字段设置为 *waveLabelPrinting* 的行。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-137">On the **Methods** FastTab, in the **Remaining methods** column, select the row where the **Name** field is set to *waveLabelPrinting*.</span></span>
1. <span data-ttu-id="ea3c1-138">选择 **添加**（向右箭头按钮）以将选定行添加到 **选定方法** 列。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-138">Select **add** (right arrow button) to move the selected row to the **Selected methods** column.</span></span>
1. <span data-ttu-id="ea3c1-139">在 **波次步骤代码** 字段中，输入将用于使波次模板与波次标签模板连接的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-139">In the **Wave step code** field, enter a wave step code that will be used to connect the wave template with a wave label template.</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="ea3c1-140">设置波次任务处理阈值数据</span><span class="sxs-lookup"><span data-stu-id="ea3c1-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="ea3c1-141">首次使用任何基于任务的处理运行波次流程时，系统将创建默认的波次任务处理阈值数据。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-141">The first time that a wave process runs by using any task-based processing, the system creates default wave task processing threshold data.</span></span> <span data-ttu-id="ea3c1-142">此数据用于控制波次处理是异步运行还是基于任务，以便它可以并行处理和创建波次标签。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-142">This data is used to control whether wave processing will run asynchronously and be task-based, so that it can process and create wave labels in parallel.</span></span>

<span data-ttu-id="ea3c1-143">默认数据最初会为最小工作 ID 数 (`MinimumWorkThresholdForLabelPrinting`) 使用阈值 *1*。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-143">The default data initially uses a threshold value of *1* for the minimum number of work IDs (`MinimumWorkThresholdForLabelPrinting`).</span></span> <span data-ttu-id="ea3c1-144">因此，当系统处理具有多个工作 ID 的波次时，它将在单独的交易中使用基于任务的波次标签处理。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-144">Therefore, when the system processes a wave that has more than one work ID, it will use task-based processing of wave labels in a separate transaction.</span></span> <span data-ttu-id="ea3c1-145">您可以在测试环境中手动插入或更新 `WHSWaveTaskProcessingThresholdParameters` 表中的此数据。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-145">You can manually insert or update this data in the `WHSWaveTaskProcessingThresholdParameters` table in your test environments.</span></span> <span data-ttu-id="ea3c1-146">若要在生产环境中更改此设置，必须联系 Microsoft 支持部门以请求更新。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-146">To change the setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a><span data-ttu-id="ea3c1-147">使用基于任务的波次标签打印时波次处理逻辑的变化</span><span class="sxs-lookup"><span data-stu-id="ea3c1-147">Changes to the wave processing logic when task-based wave label printing is used</span></span>

<span data-ttu-id="ea3c1-148">如果波次标签处理超过波次任务处理阈值，将启动基于任务的处理。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-148">If the wave label processing exceeds the wave task processing threshold, task-based processing is initiated.</span></span> <span data-ttu-id="ea3c1-149">在下一个适合波次模板的波次处理中，波次标签打印将在工作创建后立即在单独的 *ttsbegin*/*ttscommit* 交易中运行。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-149">In the next wave processing that fits the wave template, wave label printing will run in a standalone *ttsbegin*/*ttscommit* transaction immediately after work creation.</span></span> <span data-ttu-id="ea3c1-150">如果工作发放（解锁）在波次模板上配置为自动运行，将仅在波次标签打印流程成功完成后进行。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-150">If work release (unblocking) is configured on the wave template to run automatically, it occurs only after the wave label printing process is successfully completed.</span></span>

<span data-ttu-id="ea3c1-151">如果波次标签生成失败（例如，如果将工作数量转换为波次标签数量失败并引发错误），仅相应的交易失败。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-151">If wave label generation fails (for example, if conversion of the work quantity to the wave label quantity fails and throws an error), only the appropriate transaction fails.</span></span> <span data-ttu-id="ea3c1-152">先前创建的工作保持冻结状态。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-152">The work that was previously created remains frozen.</span></span> <span data-ttu-id="ea3c1-153">若要更正错误并打印波次标签，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-153">To correct errors and print the wave labels, follow these steps.</span></span>

1. <span data-ttu-id="ea3c1-154">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-154">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="ea3c1-155">在网格中选择相关波次。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-155">Select the relevant wave in the grid.</span></span>
1. <span data-ttu-id="ea3c1-156">在“操作窗格”的 **波次** 选项卡上，在 **打印** 组中，选择 **波次标签**。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-156">On the Action Pane, on the **Wave** tab, in the **Print** group, select **Wave labels**.</span></span>
1. <span data-ttu-id="ea3c1-157">按照屏幕上的说明发送标签进行打印。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-157">Follow the on-screen instructions to send the labels for printing.</span></span>
1. <span data-ttu-id="ea3c1-158">在操作窗格上的 **波次** 选项卡上，在 **波次** 组中，选择 **发放** 以手动发放选定波次的工作。</span><span class="sxs-lookup"><span data-stu-id="ea3c1-158">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Release** to manually release the work for the selected wave.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea3c1-159">其他资源</span><span class="sxs-lookup"><span data-stu-id="ea3c1-159">Additional resources</span></span>

- [<span data-ttu-id="ea3c1-160">波次标签打印</span><span class="sxs-lookup"><span data-stu-id="ea3c1-160">Wave label printing</span></span>](configure-wave-label-printing.md)
- [<span data-ttu-id="ea3c1-161">波次期间安排工作创建</span><span class="sxs-lookup"><span data-stu-id="ea3c1-161">Schedule work creation during wave</span></span>](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
