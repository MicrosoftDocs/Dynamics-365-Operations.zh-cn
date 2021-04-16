---
title: 波次处理的仓库参数
description: 本主题介绍如何为波次处理设置仓库参数。 您可以使用波次处理将多个工作订单的领料工作分组到单个波次中。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 77513185a3323a2e78f641d25b86b2896f9f7881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838002"
---
# <a name="warehouse-parameters-for-wave-processing"></a><span data-ttu-id="c1ec0-104">波次处理的仓库参数</span><span class="sxs-lookup"><span data-stu-id="c1ec0-104">Warehouse parameters for wave processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1ec0-105">本主题介绍如何为波次处理设置仓库参数。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-105">This topic describes how to set up warehouse parameters for wave processing.</span></span> <span data-ttu-id="c1ec0-106">您可以使用波次处理将多个工作订单的领料工作分组到单个波次中。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-106">You can use wave processing to group picking work for multiple work orders into a single wave.</span></span>

<span data-ttu-id="c1ec0-107">若要使用波次处理，请在 **仓库管理参数** 页面上指定以下内容：</span><span class="sxs-lookup"><span data-stu-id="c1ec0-107">To use wave processing, specify the following on the **Warehouse management parameters** page:</span></span>

- <span data-ttu-id="c1ec0-108">是否可使用批处理作业处理波次。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-108">If you can process waves by using a batch job.</span></span>
- <span data-ttu-id="c1ec0-109">是否在处理波次时收集日志文件中的信息。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-109">If you collect information in a log file when waves are processed.</span></span>

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a><span data-ttu-id="c1ec0-110">为波次处理设置仓库管理参数</span><span class="sxs-lookup"><span data-stu-id="c1ec0-110">Set up warehouse management parameters for wave processing</span></span>

<span data-ttu-id="c1ec0-111">若要为波次处理设置仓库参数，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c1ec0-111">To set up warehouse parameters for wave processing, follow these steps:</span></span>

1. <span data-ttu-id="c1ec0-112">转到 **仓库管理** \> **设置** \> **仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-112">Go to **Warehouse management** \> **Setup** \> **Warehouse management parameters**.</span></span>

1. <span data-ttu-id="c1ec0-113">在 **波次处理** 快速选项卡上，进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="c1ec0-113">On the **Wave processing** FastTab, make the following settings:</span></span>

    - <span data-ttu-id="c1ec0-114">**波次处理批处理组** - 选择当使用批处理作业处理波次时使用的批处理组。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-114">**Wave processing batch group** - Select the batch group to use when you process waves by using batch jobs.</span></span> <span data-ttu-id="c1ec0-115">批处理组指定将运行批处理作业的服务器。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-115">The batch group specifies the server that batch jobs will run on.</span></span>
    - <span data-ttu-id="c1ec0-116">**批量处理波次** - 选择是否使波次由批处理作业自动处理。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-116">**Process waves in batch** - Choose whether to enable waves to be automatically processed by a batch job.</span></span> <span data-ttu-id="c1ec0-117">必须将此设置为 *是* 以使用并行处理。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-117">You must set this to *Yes* to use parallel processing.</span></span> <span data-ttu-id="c1ec0-118">在 **处理波次** 页面上设置批处理作业。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-118">You set up the batch job on the **Process waves** page.</span></span> <span data-ttu-id="c1ec0-119">（另请参阅此列表末尾的注释。）</span><span class="sxs-lookup"><span data-stu-id="c1ec0-119">(See also the note at the end of this list.)</span></span>
    - <span data-ttu-id="c1ec0-120">**创建波次进度日志** - 选择系统是否应在每次开始和结束分配物料及其维度时生成日志记录。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-120">**Create wave progress log** - Choose whether the system should generate a log record every time allocation for an item and its dimensions begins and ends.</span></span> <span data-ttu-id="c1ec0-121">仅应在需要时（例如，在初始测试或故障排除期间）启用此日志。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-121">You should only enable this log when you need it, for example, during initial testing or for troubleshooting.</span></span> <span data-ttu-id="c1ec0-122">有关详细信息，请参阅[波次分配](wave-allocation-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-122">For more information, see [Wave allocation](wave-allocation-method.md).</span></span>
    - <span data-ttu-id="c1ec0-123">**创建波次处理历史记录日志** - 选择是否在处理波次后（包括在并行处理待处理分配期间）在日志文件中自动保存有关波次的信息。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-123">**Create wave processing history log** - Choose whether to automatically save information about a wave in a log file after the wave is processed, including during the parallel processing of pending allocations.</span></span> <span data-ttu-id="c1ec0-124">通常，您仅应在故障排除期间启用此功能，因为它会增加额外的开销。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-124">Typically you should only enable this during troubleshooting because it adds extra overhead.</span></span> <span data-ttu-id="c1ec0-125">若要查看日志，请转到 **仓库管理 \> 出库波次 \> 波次处理历史记录日志**。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-125">To view the log, go to **Warehouse management \> Outbound waves \> Wave processing history log**.</span></span> <span data-ttu-id="c1ec0-126">有关详细信息，请参阅[波次创建和处理](wave-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-126">For more information, see [Wave creation and processing](wave-processing.md).</span></span>
    - <span data-ttu-id="c1ec0-127">**创建集装化历史记录日志** - 选择是否在处理波次后在日志文件中自动保存有关波次的集装化的信息。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-127">**Create containerization history log** - Choose whether to automatically save information about containerization for a wave in a log file after the wave is processed.</span></span> <span data-ttu-id="c1ec0-128">若要查看日志，请转到 **仓库管理 \> 包装和集装化 \> 集装化历史记录**。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-128">To view the log, go to **Warehouse management \> Packing and containerization \> Containerization history**.</span></span>
    - <span data-ttu-id="c1ec0-129">**等待锁定(毫秒)** - 以毫秒为单位输入分配步骤等待由另一分配步骤锁定的系统资源的时间。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-129">**Wait for lock (ms)** - Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="c1ec0-130">当超过该时间，将不处理波次，并且显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-130">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span>

1. <span data-ttu-id="c1ec0-131">在 **发放到仓库** 快速选项卡上，进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="c1ec0-131">On the **Release to warehouse** FastTab, make the following setting:</span></span>

    - <span data-ttu-id="c1ec0-132">**批处理失败时的错误** - 选择是否在发放到仓库批处理作业失败时生成错误。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-132">**Error on batch failure** - Choose whether to generate an error when a release to warehouse batch job fails.</span></span> <span data-ttu-id="c1ec0-133">如果启用此功能，失败的作业将以 *错误* 状态结束。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-133">If this is enabled, failed jobs will end with a status of *Error*.</span></span> <span data-ttu-id="c1ec0-134">如果禁用此功能，失败的作业将以 *已结束* 状态结束。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-134">If this is disabled, failed jobs will end with a status of *Ended*.</span></span>

> [!NOTE]
> <span data-ttu-id="c1ec0-135">在用于处理波次的波次模板上，可以指定设置自动波次处理。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-135">On the wave template that is used to process the wave, you can specify the settings that automate wave processing.</span></span> <span data-ttu-id="c1ec0-136">如果为批处理作业设置计划，则应将时间与设置协调以进行波次模板中的自动化。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-136">If you set up a schedule for the batch job, you should coordinate the timing with the settings for automation in the wave template.</span></span> <span data-ttu-id="c1ec0-137">有关详细信息，请参阅[创建波次模板](wave-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-137">For more information, see [Create a wave template](wave-templates.md).</span></span>
>
> <span data-ttu-id="c1ec0-138">如果使用 *运输管理* 和 *高级仓库管理*，您可以指定是否在处理波次时合并装载。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-138">If you are using *Transportation management* and *Advanced warehouse management*, you can specify whether to consolidate loads when you process a wave.</span></span> <span data-ttu-id="c1ec0-139">例如，当若干小的装载同时装运时，这很有用。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-139">For example, this is useful when several small loads can be shipped at the same time.</span></span> <span data-ttu-id="c1ec0-140">若要在处理波次时合并装载，请在 **装载** 选项卡上，选中 **在波次处理期间合并装载** 复选框。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-140">To consolidate loads when you process a wave, on the **Loads** tab, select the **Consolidate loads during wave processing** check box.</span></span></P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a><span data-ttu-id="c1ec0-141">设置生产波次的完整或部分预留</span><span class="sxs-lookup"><span data-stu-id="c1ec0-141">Set up full or partial reservation for production waves</span></span>

<span data-ttu-id="c1ec0-142">对于销售订单和看板订单，在订单发放到仓库前，必须预留库存。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-142">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="c1ec0-143">否则，无法以波次处理物料或分配行。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-143">Otherwise, the items or allocation lines cannot be processed in a wave.</span></span> <span data-ttu-id="c1ec0-144">但是，生产订单稍微更加灵活。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-144">However, production orders are slightly more flexible.</span></span> <span data-ttu-id="c1ec0-145">对于生产订单，您可以指定以下内容：</span><span class="sxs-lookup"><span data-stu-id="c1ec0-145">For production orders, you can specify the following:</span></span>

- <span data-ttu-id="c1ec0-146">尽管无法预留所有材料，仍允许将生产订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-146">Allow production orders to be released to the warehouse although all materials cannot be reserved.</span></span> <span data-ttu-id="c1ec0-147">如果选择此选项，则当附加材料变为可用时必须手动重复对仓库流程的发放。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-147">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span> <span data-ttu-id="c1ec0-148">例如，如果您有开始生产所需的物料，并且可以等待附加物料变为可用，这很有用。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-148">For example, this is useful if you have the materials that you need to start a production, and can wait until the additional materials become available.</span></span>
- <span data-ttu-id="c1ec0-149">需要预留所有物料，然后才能将订单发放到仓库。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-149">Require that all materials are reserved before an order can be released to the warehouse.</span></span>

<span data-ttu-id="c1ec0-150">若要全部预留或允许部分预留，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c1ec0-150">To require full reservation or allow partial reservation, follow these steps:</span></span>

1. <span data-ttu-id="c1ec0-151">转到 **生产控制** \> **设置** \> **生产控制参数**。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-151">Go to **Production control** \> **Setup** \> **Production control parameters**.</span></span>
1. <span data-ttu-id="c1ec0-152">在 **常规** 选项卡上，在 **发放到仓库** 字段中，选择默认设置。</span><span class="sxs-lookup"><span data-stu-id="c1ec0-152">On the **General** tab, in the **Release to warehouse** field, select the default setting.</span></span>
