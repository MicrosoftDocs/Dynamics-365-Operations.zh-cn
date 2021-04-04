---
title: 检查货物质量
description: 本主题说明如何处理质检订单。
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e37ac8c9320d427b9f9a3ca32b0e4667c7023339
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244415"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="26f19-103">检查货物质量</span><span class="sxs-lookup"><span data-stu-id="26f19-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26f19-104">本主题说明如何处理质检订单。</span><span class="sxs-lookup"><span data-stu-id="26f19-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="26f19-105">您可以使用 USMF 公司演示数据运行此指南。</span><span class="sxs-lookup"><span data-stu-id="26f19-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="26f19-106">在开始此示例过程前，需要确认采购订单为“000016”，并且将产品收据过帐。</span><span class="sxs-lookup"><span data-stu-id="26f19-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="26f19-107">这将自动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="26f19-107">This will automatically create a quality order.</span></span> <span data-ttu-id="26f19-108">质量检查通常由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="26f19-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="26f19-109">选择质检订单。</span><span class="sxs-lookup"><span data-stu-id="26f19-109">Select a quality order</span></span>
1. <span data-ttu-id="26f19-110">在导航窗格中，转到 **模块 > 库存管理 > 定期任务 > 质量管理 > 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="26f19-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="26f19-111">在开始此过程前，选择已创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="26f19-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="26f19-112">记录测试结果</span><span class="sxs-lookup"><span data-stu-id="26f19-112">Record test results</span></span>
1. <span data-ttu-id="26f19-113">选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="26f19-113">Select **Results**.</span></span>
2. <span data-ttu-id="26f19-114">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="26f19-114">Select **Edit**.</span></span>
3. <span data-ttu-id="26f19-115">在 **结果数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="26f19-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="26f19-116">在 **结果** 字段中，在下拉菜单中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="26f19-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="26f19-117">在此示例中，结果将基于预定义的结果。</span><span class="sxs-lookup"><span data-stu-id="26f19-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="26f19-118">通常您可以记录更具体的测试结果，例如大小或其他维度。</span><span class="sxs-lookup"><span data-stu-id="26f19-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="26f19-119">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="26f19-119">Select **Save**.</span></span>
6. <span data-ttu-id="26f19-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26f19-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="26f19-121">验证质检订单</span><span class="sxs-lookup"><span data-stu-id="26f19-121">Validate the quality order</span></span>
1. <span data-ttu-id="26f19-122">选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="26f19-122">Select **Validate**.</span></span>
2. <span data-ttu-id="26f19-123">在 **验证者** 字段中，从下拉菜单选择执行检查的用户。</span><span class="sxs-lookup"><span data-stu-id="26f19-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="26f19-124">单击 **选择**。</span><span class="sxs-lookup"><span data-stu-id="26f19-124">Click **Select**.</span></span>
4. <span data-ttu-id="26f19-125">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="26f19-125">Select **OK**.</span></span>
5. <span data-ttu-id="26f19-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26f19-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]