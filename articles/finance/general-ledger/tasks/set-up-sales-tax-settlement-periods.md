---
title: 设置销售税结算期间
description: 本主题说明如何在 Dynamics 365 Finance 中设置销售税结算期。
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944769"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="e43d8-103">设置销售税结算期间</span><span class="sxs-lookup"><span data-stu-id="e43d8-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e43d8-104">本主题说明如何设置销售税结算期。</span><span class="sxs-lookup"><span data-stu-id="e43d8-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="e43d8-105">销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。</span><span class="sxs-lookup"><span data-stu-id="e43d8-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="e43d8-106">结算流程可在结算期间或特定日期间隔内运行。</span><span class="sxs-lookup"><span data-stu-id="e43d8-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="e43d8-107">所有与结算期间相关的税务代码将进行结算。</span><span class="sxs-lookup"><span data-stu-id="e43d8-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="e43d8-108">根据相关销售税主管机构的设置，应交税金过帐到供应商或总帐科目。</span><span class="sxs-lookup"><span data-stu-id="e43d8-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="e43d8-109">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="e43d8-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e43d8-110">在导航窗格中，转到 **模块 > 纳税 > 间接税 > 销售税 > 销售税结算期**。</span><span class="sxs-lookup"><span data-stu-id="e43d8-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="e43d8-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e43d8-111">Select **New**.</span></span>
3. <span data-ttu-id="e43d8-112">在 **结算期间** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="e43d8-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="e43d8-113">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e43d8-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e43d8-114">在 **主管机构** 字段中，选择接收为结算期间创建的报表和付款的销售税主管机构。</span><span class="sxs-lookup"><span data-stu-id="e43d8-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="e43d8-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e43d8-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e43d8-116">在 **付款期限** 字段中，在下拉菜单中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e43d8-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="e43d8-117">相关销售税主管机构可以设置为供应商，销售税结算将创建开放式供应商发票。</span><span class="sxs-lookup"><span data-stu-id="e43d8-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="e43d8-118">付款期限定义开放式供应商发票的到期日期。</span><span class="sxs-lookup"><span data-stu-id="e43d8-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="e43d8-119">为结算期间间隔选择类型。</span><span class="sxs-lookup"><span data-stu-id="e43d8-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="e43d8-120">输入每一期间的期间间隔单位数。</span><span class="sxs-lookup"><span data-stu-id="e43d8-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="e43d8-121">例如，1 个季度有 3 个月。</span><span class="sxs-lookup"><span data-stu-id="e43d8-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="e43d8-122">选择或清除 **使用批处理进行销售税结算** 复选框。</span><span class="sxs-lookup"><span data-stu-id="e43d8-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="e43d8-123">结算期的结算流程可在后台将交易记录作为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="e43d8-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="e43d8-124">这是对在期间间隔内的大量涉税交易记录的建议。</span><span class="sxs-lookup"><span data-stu-id="e43d8-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="e43d8-125">选择或清除 **防止生成抵消税交易记录** 复选框。</span><span class="sxs-lookup"><span data-stu-id="e43d8-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="e43d8-126">默认情况下，系统在结算过程中生成抵消税交易记录，如果在某期间间隔内存在大量税交易记录，这可能造成性能问题。</span><span class="sxs-lookup"><span data-stu-id="e43d8-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="e43d8-127">选择此复选框以防止生成抵消税交易记录。</span><span class="sxs-lookup"><span data-stu-id="e43d8-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="e43d8-128">展开 **期间间隔** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e43d8-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="e43d8-129">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="e43d8-129">Select **Add**.</span></span>
14. <span data-ttu-id="e43d8-130">在新行中的 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="e43d8-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="e43d8-131">在 **结束日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="e43d8-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="e43d8-132">选择 **新建期间间隔**。</span><span class="sxs-lookup"><span data-stu-id="e43d8-132">Select **New period interval**.</span></span> <span data-ttu-id="e43d8-133">一旦输入第一个期间间隔，可自动创建新期间。</span><span class="sxs-lookup"><span data-stu-id="e43d8-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="e43d8-134">您可以返回和根据需要添加新期间间隔。</span><span class="sxs-lookup"><span data-stu-id="e43d8-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="e43d8-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e43d8-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
