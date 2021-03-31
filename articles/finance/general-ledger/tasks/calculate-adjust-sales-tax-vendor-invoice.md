---
title: 计算和调整供应商发票上的销售税
description: 本主题介绍如何在 Dynamics 365 Finance 中调整供应商发票上的销售税。
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204729"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="64cb6-103">计算和调整供应商发票上的销售税</span><span class="sxs-lookup"><span data-stu-id="64cb6-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64cb6-104">本主题介绍如何调整供应商发票上的销售税。</span><span class="sxs-lookup"><span data-stu-id="64cb6-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="64cb6-105">如果原始单据显示计算的不同税额，您可在过帐前调整这些税额。</span><span class="sxs-lookup"><span data-stu-id="64cb6-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="64cb6-106">本任务使用 DEMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="64cb6-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="64cb6-107">在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票日记帐**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="64cb6-108">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-108">Select **New**.</span></span>
3. <span data-ttu-id="64cb6-109">在新行的 **名称** 字段中，选择下拉菜单中的一个选项。</span><span class="sxs-lookup"><span data-stu-id="64cb6-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="64cb6-110">在操作窗格中，选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="64cb6-111">在 **帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="64cb6-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="64cb6-112">在 **发票** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="64cb6-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="64cb6-113">在 **信用** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="64cb6-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="64cb6-114">在 **抵销帐户** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="64cb6-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="64cb6-115">选择 **销售税**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="64cb6-116">在 **实际销售税总额** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="64cb6-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="64cb6-117">在 **调整** 选项卡中，可调整每个销售税代码的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="64cb6-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="64cb6-118">选择 **通过计算得出的金额重置实际金额**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="64cb6-119">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-119">Select **OK**.</span></span>
14. <span data-ttu-id="64cb6-120">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="64cb6-120">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]