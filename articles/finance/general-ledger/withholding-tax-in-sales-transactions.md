---
title: 销售交易记录中的预缴税金
description: 本主题列出了避免为选定客户计算预缴税金的步骤。 对于在向您的付款中指定预缴税金的客户，您可以分配默认的预缴税金组。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: c839df1b54cdb60beefa6dc6c3fc6e945a6eac85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256635"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="b6936-104">销售交易记录中的预缴税金</span><span class="sxs-lookup"><span data-stu-id="b6936-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="b6936-105">本主题列出了避免为选定客户计算预缴税金的步骤。</span><span class="sxs-lookup"><span data-stu-id="b6936-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="b6936-106">对于在向您的付款中指定预缴税金的客户，您可以在 **客户** 页分配默认的 **预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="b6936-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="b6936-107">转到 **导航窗格 > 模块 > 应收帐款 > 客户 > 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="b6936-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="b6936-108">单击相应的客户帐户，单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b6936-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="b6936-109">在 **发票和交货** 选项卡中，将 **计算预缴税金** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b6936-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="b6936-110">如果未在主数据中为此客户打开 **计算预缴税金**，将不会计算预缴税金。</span><span class="sxs-lookup"><span data-stu-id="b6936-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="b6936-111">在 **预缴税金组** 中选择一个预缴税金组。</span><span class="sxs-lookup"><span data-stu-id="b6936-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="b6936-112">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b6936-112">Click **Save**.</span></span>

<span data-ttu-id="b6936-113">对于有预缴税金的产品/服务，您可以在 **已发布产品** 中分配默认的 **物料预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="b6936-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="b6936-114">转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。</span><span class="sxs-lookup"><span data-stu-id="b6936-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="b6936-115">单击相应的物料编号，单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b6936-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="b6936-116">在 **销售** 选项卡中，单击 **计算预缴税金**。</span><span class="sxs-lookup"><span data-stu-id="b6936-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="b6936-117">如果在 **已发布产品** 页上的 **销售** 选项卡中未将此产品的 **计算预缴税金** 设置为 **是**，将不计算预缴税金。</span><span class="sxs-lookup"><span data-stu-id="b6936-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="b6936-118">在 **物料预缴税金组** 列表中选择一个物料预缴税金组。</span><span class="sxs-lookup"><span data-stu-id="b6936-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="b6936-119">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b6936-119">Click **Save**.</span></span>

<span data-ttu-id="b6936-120">预缴税金组和物料预缴税金组可以使用 **销售订单** 页分配。</span><span class="sxs-lookup"><span data-stu-id="b6936-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="b6936-121">创建新的销售订单时，默认预缴税金组和物料预缴税金组将用作销售订单行上的默认条目。</span><span class="sxs-lookup"><span data-stu-id="b6936-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="b6936-122">预缴税金使用 **客户付款日记帐** 计算和过帐。</span><span class="sxs-lookup"><span data-stu-id="b6936-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="b6936-123">您可以在 **结算交易** 页上的 **预缴税金** 选项卡中手动调整适用的预缴税金代码以及实际的预缴税金金额。</span><span class="sxs-lookup"><span data-stu-id="b6936-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="b6936-124">计算出的预缴税金金额将从客户付款中扣除，并过帐到相关凭证中的 **预缴税金冲销** 科目。</span><span class="sxs-lookup"><span data-stu-id="b6936-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]