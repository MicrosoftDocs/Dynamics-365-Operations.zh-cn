---
title: 检查货物质量
description: 本主题说明如何处理质检订单。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956126"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="e89ee-103">检查货物质量</span><span class="sxs-lookup"><span data-stu-id="e89ee-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e89ee-104">本主题说明如何处理质检订单。</span><span class="sxs-lookup"><span data-stu-id="e89ee-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="e89ee-105">质量检查通常由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="e89ee-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="e89ee-106">如果安装了标准演示数据，您可以使用它来完成本主题中的过程。</span><span class="sxs-lookup"><span data-stu-id="e89ee-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="e89ee-107">要使用演示数据，在开始前选择 *USMF* 法人。</span><span class="sxs-lookup"><span data-stu-id="e89ee-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="e89ee-108">然后，必须确认采购订单 *000016* 并过帐产品收据。</span><span class="sxs-lookup"><span data-stu-id="e89ee-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="e89ee-109">质检订单将自动生成。</span><span class="sxs-lookup"><span data-stu-id="e89ee-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="e89ee-110">步骤 1：选择质检订单</span><span class="sxs-lookup"><span data-stu-id="e89ee-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="e89ee-111">要选择质检订单，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e89ee-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="e89ee-112">转到 **库存管理 \> 定期任务 \> 质量管理 \> 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="e89ee-113">在开始此过程前，选择生成的质检订单。</span><span class="sxs-lookup"><span data-stu-id="e89ee-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="e89ee-114">步骤 2：记录测试结果</span><span class="sxs-lookup"><span data-stu-id="e89ee-114">Step 2: Record test results</span></span>

<span data-ttu-id="e89ee-115">要记录测试结果，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e89ee-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="e89ee-116">选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-116">Select **Results**.</span></span>
1. <span data-ttu-id="e89ee-117">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-117">Select **Edit**.</span></span>
1. <span data-ttu-id="e89ee-118">在 **结果数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e89ee-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="e89ee-119">在 **结果** 字段中，选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e89ee-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="e89ee-120">在此示例中，结果将基于预定义的结果。</span><span class="sxs-lookup"><span data-stu-id="e89ee-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="e89ee-121">通常，您将记录更具体的测试结果，如尺寸或其他维度。</span><span class="sxs-lookup"><span data-stu-id="e89ee-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="e89ee-122">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-122">Select **Save**.</span></span>
1. <span data-ttu-id="e89ee-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e89ee-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="e89ee-124">步骤 3：验证质检订单</span><span class="sxs-lookup"><span data-stu-id="e89ee-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="e89ee-125">要验证质检订单，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e89ee-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="e89ee-126">选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-126">Select **Validate**.</span></span>
1. <span data-ttu-id="e89ee-127">在 **验证者** 字段中，选择执行检查的用户。</span><span class="sxs-lookup"><span data-stu-id="e89ee-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="e89ee-128">选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-128">Select **Select**.</span></span>
1. <span data-ttu-id="e89ee-129">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e89ee-129">Select **OK**.</span></span>
1. <span data-ttu-id="e89ee-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e89ee-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
