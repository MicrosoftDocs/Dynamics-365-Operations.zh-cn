---
title: 从应付帐款创建和购置资产
description: '本指到任务帮助了解如何遵照采购流程来创建和购置固定资产。 '
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b27ccc3b4c4f5470d3a5b8ed7347e269c6793b87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976033"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="aef65-103">从应付帐款创建和购置资产</span><span class="sxs-lookup"><span data-stu-id="aef65-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aef65-104">本指到任务帮助了解如何遵照采购流程来创建和购置固定资产。 </span><span class="sxs-lookup"><span data-stu-id="aef65-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="aef65-105">本任务需要用到普通及应付帐目会计和演示公司USMF的数据。</span><span class="sxs-lookup"><span data-stu-id="aef65-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="aef65-106">设置固定资产参数</span><span class="sxs-lookup"><span data-stu-id="aef65-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="aef65-107">在 **导航窗格** 中，转到 **模块 > 固定资产 > 设置 > 固定资产参数**。</span><span class="sxs-lookup"><span data-stu-id="aef65-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="aef65-108">展开 **采购订单** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="aef65-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="aef65-109">选中 **允许从采购中购置资产** 复选框。</span><span class="sxs-lookup"><span data-stu-id="aef65-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="aef65-110">选中 **在产品收据或发票过帐期间创建资产** 复选框。</span><span class="sxs-lookup"><span data-stu-id="aef65-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="aef65-111">创建新的供应商发票</span><span class="sxs-lookup"><span data-stu-id="aef65-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="aef65-112">在 **导航窗格** 中，转到 **模块 > 应付帐款 > 工作区 > 供应商发票条目**。</span><span class="sxs-lookup"><span data-stu-id="aef65-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="aef65-113">单击 **新建供应商发票**。</span><span class="sxs-lookup"><span data-stu-id="aef65-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="aef65-114">在 **发票帐户** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="aef65-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aef65-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="aef65-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="aef65-116">在 **编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="aef65-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="aef65-117">在 **过帐日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="aef65-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="aef65-118">单击 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="aef65-118">Click **Add line**.</span></span>
8. <span data-ttu-id="aef65-119">在 **物料编号** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="aef65-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="aef65-120">输入固定资产购置时可使用的非贮存物料或采购类别。</span><span class="sxs-lookup"><span data-stu-id="aef65-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="aef65-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="aef65-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="aef65-122">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="aef65-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="aef65-123">一个发票行只创建一哥固定资产，不考虑数量。</span><span class="sxs-lookup"><span data-stu-id="aef65-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="aef65-124">发票数量字段的值会被传送到固定资产数量参数</span><span class="sxs-lookup"><span data-stu-id="aef65-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="aef65-125">在 **单价** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="aef65-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="aef65-126">展开 **行详细信息** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="aef65-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="aef65-127">单击 **固定资产** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="aef65-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="aef65-128">选中 **创建新的固定资产** 复选框。</span><span class="sxs-lookup"><span data-stu-id="aef65-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="aef65-129">在 **固定资产组** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="aef65-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="aef65-130">在列表中，选择创建新固定资产时要使用的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="aef65-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="aef65-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="aef65-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="aef65-132">单击 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="aef65-132">Click **Post**.</span></span> <span data-ttu-id="aef65-133">在过帐发票时，将会创建和购置固定资产。</span><span class="sxs-lookup"><span data-stu-id="aef65-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

