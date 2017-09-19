--- 
title: "使用可变权重将变型产品添加到采购订单"
description: "此程序会逐步演示如何使用变型权重，自动填充每个产品变型的采购订单行。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3db13646c82ea6dc6949aaa714a5769f9c5ad2a9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="cbc00-103">使用可变权重将变型产品添加到采购订单</span><span class="sxs-lookup"><span data-stu-id="cbc00-103">Add variant products to purchase orders using variant weights</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbc00-104">此程序会逐步演示如何使用变型权重，自动填充每个产品变型的采购订单行。</span><span class="sxs-lookup"><span data-stu-id="cbc00-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="cbc00-105">在您选择您想要购买的产品数量时，基于产品变型的配置权重为所有产品变型创建采购订单行，且随附数量建议。</span><span class="sxs-lookup"><span data-stu-id="cbc00-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="cbc00-106">此程序不包括配置产品维度和产品变型的权重值的步骤。</span><span class="sxs-lookup"><span data-stu-id="cbc00-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="cbc00-107">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="cbc00-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="cbc00-108">转到“应付帐款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="cbc00-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-109">Click New.</span></span>
3. <span data-ttu-id="cbc00-110">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cbc00-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cbc00-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cbc00-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cbc00-112">切换“概况”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="cbc00-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="cbc00-113">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="cbc00-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cbc00-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cbc00-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cbc00-115">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cbc00-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="cbc00-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cbc00-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cbc00-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cbc00-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="cbc00-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-118">Click OK.</span></span>
12. <span data-ttu-id="cbc00-119">切换“行详细信息”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="cbc00-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="cbc00-120">单击“变型”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cbc00-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="cbc00-121">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-121">Click Add line.</span></span>
15. <span data-ttu-id="cbc00-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="cbc00-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="cbc00-123">在“物料编号”字段中，输入“0140”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="cbc00-124">将“数量”设置为“1000”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="cbc00-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cbc00-125">Click Save.</span></span>

