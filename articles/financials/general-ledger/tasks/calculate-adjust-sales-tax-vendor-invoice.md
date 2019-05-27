---
title: 计算和调整供应商发票上的销售税
description: 如果原始单据显示计算的不同税额，您可在过帐前调整这些税额。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545163"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="fa75d-103">计算和调整供应商发票上的销售税</span><span class="sxs-lookup"><span data-stu-id="fa75d-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa75d-104">如果原始单据显示计算的不同税额，您可在过帐前调整这些税额。</span><span class="sxs-lookup"><span data-stu-id="fa75d-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="fa75d-105">本任务使用 DEMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="fa75d-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="fa75d-106">转到应付账目>发票>发票记账。</span><span class="sxs-lookup"><span data-stu-id="fa75d-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="fa75d-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-107">Click New.</span></span>
3. <span data-ttu-id="fa75d-108">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="fa75d-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fa75d-109">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="fa75d-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fa75d-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="fa75d-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="fa75d-111">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-111">Click Lines.</span></span>
7. <span data-ttu-id="fa75d-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="fa75d-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fa75d-113">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="fa75d-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="fa75d-114">在“发票”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="fa75d-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="fa75d-115">在“信用”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fa75d-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="fa75d-116">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="fa75d-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="fa75d-117">单击“销售税”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-117">Click Sales tax.</span></span>
13. <span data-ttu-id="fa75d-118">在“实际销售税总额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fa75d-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="fa75d-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-119">Click OK.</span></span>
15. <span data-ttu-id="fa75d-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-120">Click Save.</span></span>
16. <span data-ttu-id="fa75d-121">单击“销售税”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-121">Click Sales tax.</span></span>
17. <span data-ttu-id="fa75d-122">在“调整”选项卡中，可调整每个销售税代码的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="fa75d-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="fa75d-123">单击“通过计算得出的金额重置实际金额”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="fa75d-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-124">Click OK.</span></span>
20. <span data-ttu-id="fa75d-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fa75d-125">Click Save.</span></span>

