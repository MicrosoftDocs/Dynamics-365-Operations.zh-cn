---
title: 购买交易记录中的预缴税金
description: 对于有预缴税金的供应商，您可以在 **所有供应商** 页上分配默认的 **预缴税金组**。
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: faeaf0746532875d3517a208c9c338c112bf2c77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816875"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="4ebfb-103">购买交易记录中的预缴税金</span><span class="sxs-lookup"><span data-stu-id="4ebfb-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="4ebfb-104">对于有预缴税金的供应商，您可以在 **所有供应商** 页上分配默认的 **预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="4ebfb-105">转到 **导航窗格 > 模块 > 应付帐款 > 供应商 > 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="4ebfb-106">单击相应的供应商帐户，单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="4ebfb-107">在 **发票和交货** 选项卡中，将 **计算预缴税金** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="4ebfb-108">如果未在数据中为此供应商打开 **计算预缴税金**，将不会计算预缴税金。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="4ebfb-109">在 **预缴税金组** 中选择一个预缴税金组。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="4ebfb-110">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-110">Click **Save**.</span></span>

<span data-ttu-id="4ebfb-111">对于有预缴税金的产品/服务，您可以在 **已发布产品** 中分配默认的 **物料预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="4ebfb-112">转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="4ebfb-113">单击相应的物料编号，单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="4ebfb-114">在 **采购** 选项卡中，单击 **计算预缴税金**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="4ebfb-115">如果在 **已发布产品** 页上的 **采购** 选项卡中未将此产品的 **计算预缴税金** 设置为 **是**，将不计算预缴税金。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="4ebfb-116">在 **物料预缴税金组** 列表中选择一个物料预缴税金组。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="4ebfb-117">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-117">Click **Save**.</span></span>

<span data-ttu-id="4ebfb-118">预缴税金组和物料预缴税金组可以在页面中分配：</span><span class="sxs-lookup"><span data-stu-id="4ebfb-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="4ebfb-119">**采购订单**</span><span class="sxs-lookup"><span data-stu-id="4ebfb-119">**Purchase order**</span></span>
- <span data-ttu-id="4ebfb-120">**供应商账单**</span><span class="sxs-lookup"><span data-stu-id="4ebfb-120">**Vendor invoice**</span></span>
- <span data-ttu-id="4ebfb-121">**账单日记帐**</span><span class="sxs-lookup"><span data-stu-id="4ebfb-121">**Invoice journal**</span></span>

<span data-ttu-id="4ebfb-122">创建 **采购订单** 和/或 **待定供应商发票页** 时，默认的预缴税金组和物料预缴税金组将被带入行中。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="4ebfb-123">对于 **供应商发票日记帐**，您可以打开 **计算预缴税金**，然后在日记帐中的 **常规** 选项卡中选择 **物料预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="4ebfb-124">临时预缴税金金额可在 **采购订单** 页上 **总计** 选项卡的 **调整后预缴税金** 字段中找到。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![采购订单中包含预缴税金](media/withholding-tax-adjusted.png)

<span data-ttu-id="4ebfb-126">预缴税金根据 **供应商付款日记帐** 计算。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="4ebfb-127">您可以在 **结算交易** 页上的 **预缴税金** 选项卡中手动调整适用的预缴税金代码以及实际的预缴税金金额。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![可以在“结算交易”页上手动调整预缴](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="4ebfb-129">所得的预缴税金金额将从供应商付款中扣除，并过帐到相关凭证中的 **预缴税金科目**。</span><span class="sxs-lookup"><span data-stu-id="4ebfb-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![显示相关凭证的预缴税金科目](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]