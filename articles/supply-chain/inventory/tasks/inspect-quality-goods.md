---
title: 检查货物质量
description: 本主题说明如何处理质检订单。
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75fbfbb7b993b528e96d247dafa2bdfe20837987
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145609"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="1f78f-103">检查货物质量</span><span class="sxs-lookup"><span data-stu-id="1f78f-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f78f-104">本主题说明如何处理质检订单。</span><span class="sxs-lookup"><span data-stu-id="1f78f-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="1f78f-105">您可以使用 USMF 公司演示数据运行此指南。</span><span class="sxs-lookup"><span data-stu-id="1f78f-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="1f78f-106">在开始此示例过程前，需要确认采购订单为“000016”，并且将产品收据过帐。</span><span class="sxs-lookup"><span data-stu-id="1f78f-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="1f78f-107">这将自动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="1f78f-107">This will automatically create a quality order.</span></span> <span data-ttu-id="1f78f-108">质量检查通常由质检员执行。</span><span class="sxs-lookup"><span data-stu-id="1f78f-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="1f78f-109">选择质检订单。</span><span class="sxs-lookup"><span data-stu-id="1f78f-109">Select a quality order</span></span>
1. <span data-ttu-id="1f78f-110">在导航窗格中，转到**模块 > 库存管理 > 定期任务 > 质量管理 > 质检订单**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="1f78f-111">在开始此过程前，选择已创建的质检订单。</span><span class="sxs-lookup"><span data-stu-id="1f78f-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="1f78f-112">记录测试结果</span><span class="sxs-lookup"><span data-stu-id="1f78f-112">Record test results</span></span>
1. <span data-ttu-id="1f78f-113">选择**结果**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-113">Select **Results**.</span></span>
2. <span data-ttu-id="1f78f-114">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-114">Select **Edit**.</span></span>
3. <span data-ttu-id="1f78f-115">在**结果数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="1f78f-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="1f78f-116">在**结果**字段中，在下拉菜单中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="1f78f-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="1f78f-117">在此示例中，结果将基于预定义的结果。</span><span class="sxs-lookup"><span data-stu-id="1f78f-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="1f78f-118">通常您可以记录更具体的测试结果，例如大小或其他维度。</span><span class="sxs-lookup"><span data-stu-id="1f78f-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="1f78f-119">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-119">Select **Save**.</span></span>
6. <span data-ttu-id="1f78f-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1f78f-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="1f78f-121">验证质检订单</span><span class="sxs-lookup"><span data-stu-id="1f78f-121">Validate the quality order</span></span>
1. <span data-ttu-id="1f78f-122">选择**验证**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-122">Select **Validate**.</span></span>
2. <span data-ttu-id="1f78f-123">在**验证者**字段中，从下拉菜单选择执行检查的用户。</span><span class="sxs-lookup"><span data-stu-id="1f78f-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="1f78f-124">单击**选择**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-124">Click **Select**.</span></span>
4. <span data-ttu-id="1f78f-125">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1f78f-125">Select **OK**.</span></span>
5. <span data-ttu-id="1f78f-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1f78f-126">Close the page.</span></span>

