---
title: 确认来自批处理作业的出站装运
description: 本主题介绍如何设置自动确认准备装运负荷的出站转移单装运的批处理作业。
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4c4fd5e8cdea9a7fc05ec9cbc7866c44c6f78b2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243959"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="ed728-103">确认来自批处理作业的出站装运</span><span class="sxs-lookup"><span data-stu-id="ed728-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed728-104">本主题介绍如何设置自动确认准备装运负荷的出站转移单装运的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="ed728-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="ed728-105">这里介绍的批处理作业仅适用于转移单装运，不适用于销售订单。</span><span class="sxs-lookup"><span data-stu-id="ed728-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="ed728-106">启用“从批处理作业确认出站装运”功能</span><span class="sxs-lookup"><span data-stu-id="ed728-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="ed728-107">此功能只有在系统中启用了之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="ed728-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="ed728-108">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页面检查功能状态，并在需要时启用。</span><span class="sxs-lookup"><span data-stu-id="ed728-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="ed728-109">此功能的清单如下：</span><span class="sxs-lookup"><span data-stu-id="ed728-109">The feature is listed as:</span></span>

- <span data-ttu-id="ed728-110">**模块** - *仓库管理*</span><span class="sxs-lookup"><span data-stu-id="ed728-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="ed728-111">**功能名称** - *从批处理作业确认出站装运*</span><span class="sxs-lookup"><span data-stu-id="ed728-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="ed728-112">处理出站装运</span><span class="sxs-lookup"><span data-stu-id="ed728-112">Process outbound shipments</span></span>

<span data-ttu-id="ed728-113">设置计划的批处理作业来为准备装运的负荷运行出站装运确认：</span><span class="sxs-lookup"><span data-stu-id="ed728-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="ed728-114">转到 **仓库管理 \> 定期任务 \> 处理出站装运**。</span><span class="sxs-lookup"><span data-stu-id="ed728-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="ed728-115">**确认装运** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="ed728-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="ed728-116">在 **要包括的记录** 快速选项卡中，选择 **筛选**。</span><span class="sxs-lookup"><span data-stu-id="ed728-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ed728-117">查询编辑器对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="ed728-117">The query editor dialog box opens.</span></span> <span data-ttu-id="ed728-118">在 **范围** 选项卡上，添加具有以下值的行：</span><span class="sxs-lookup"><span data-stu-id="ed728-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="ed728-119">**表** - *负荷*</span><span class="sxs-lookup"><span data-stu-id="ed728-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="ed728-120">**派生表** - *负荷*</span><span class="sxs-lookup"><span data-stu-id="ed728-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="ed728-121">**字段** - *负荷状态*</span><span class="sxs-lookup"><span data-stu-id="ed728-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="ed728-122">**条件** - *已装载*</span><span class="sxs-lookup"><span data-stu-id="ed728-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="ed728-123">选择 **确定** 返回到 **确认装运** 对话框。</span><span class="sxs-lookup"><span data-stu-id="ed728-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="ed728-124">在 **在后台运行** 快速选项卡上，将 **批处理** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="ed728-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="ed728-125">在 **在后台运行** 快速选项卡上，选择 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="ed728-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="ed728-126">**定义重复执行** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="ed728-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="ed728-127">根据业务需要设置运行计划。</span><span class="sxs-lookup"><span data-stu-id="ed728-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="ed728-128">选择 **确定** 返回到 **确认装运** 对话框。</span><span class="sxs-lookup"><span data-stu-id="ed728-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="ed728-129">在 **确认装运** 对话框中选择 **确定**，将批处理作业添加到批处理队列中。</span><span class="sxs-lookup"><span data-stu-id="ed728-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="ed728-130">有关详细信息，请参阅[批处理概览](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ed728-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]