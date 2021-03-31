---
title: 按分录的销售税明细报表
description: 此主题说明如何使用按分录的销售税明细报表查看和打印有关为其计算销售税的分录的信息。
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b90ae491605bf59b93137936a2804c4b84c6e1b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204874"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="a3a2a-103">按分录的销售税明细报表</span><span class="sxs-lookup"><span data-stu-id="a3a2a-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3a2a-104">此主题说明如何使用 **按分录的销售税明细** 报表查看和打印有关为其计算销售税的分录的信息。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="a3a2a-105">纳税科目与非纳税科目</span><span class="sxs-lookup"><span data-stu-id="a3a2a-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="a3a2a-106">**按分录的销售税明细** 报表显示纳税科目和非纳税科目的税收交易记录。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="a3a2a-107">这些科目按以下方法分类：</span><span class="sxs-lookup"><span data-stu-id="a3a2a-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="a3a2a-108">**纳税科目** – 在过帐税务交易记录时，科目被视为纳税科目，并且 **销售税** 日记帐行中的主科目也是纳税科目，如应付销售税科目或应收销售税科目。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="a3a2a-109">**非纳税科目** – 在过帐税务交易记录时，科目被视为非纳税科目，并且原始交易记录中的主科目也是非纳税科目，如收入科目或费用科目。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="a3a2a-110">对于纳税科目，报表中的 **来源**、**应收销售税** 和 **应付销售税** 列显示 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="a3a2a-111">对于非纳税科目，这些列显示金额。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="a3a2a-112">筛选报表中的数据</span><span class="sxs-lookup"><span data-stu-id="a3a2a-112">Filtering the data on the report</span></span>

<span data-ttu-id="a3a2a-113">生成此报表时，以下默认字段可用。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="a3a2a-114">可使用这些字段筛选此报表中显示的数据。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="a3a2a-115">字段</span><span class="sxs-lookup"><span data-stu-id="a3a2a-115">Field</span></span>                      | <span data-ttu-id="a3a2a-116">说明</span><span class="sxs-lookup"><span data-stu-id="a3a2a-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="a3a2a-117">日期</span><span class="sxs-lookup"><span data-stu-id="a3a2a-117">Date</span></span>                       | <span data-ttu-id="a3a2a-118">使用 **开始** 和 **结束** 部分中的字段为税务交易记录定义日期范围。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="a3a2a-119">主科目</span><span class="sxs-lookup"><span data-stu-id="a3a2a-119">Main account</span></span>               | <span data-ttu-id="a3a2a-120">使用 **开始** 和 **结束** 部分中的字段为主科目定义范围。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="a3a2a-121">增值税代码</span><span class="sxs-lookup"><span data-stu-id="a3a2a-121">Sales tax code</span></span>             | <span data-ttu-id="a3a2a-122">使用 **开始** 和 **结束** 部分中的字段为销售税代码定义范围。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="a3a2a-123">分组</span><span class="sxs-lookup"><span data-stu-id="a3a2a-123">Grouping</span></span>                   | <span data-ttu-id="a3a2a-124">选择应该按会计科目还是销售税代码为报表分组。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="a3a2a-125">小计(按销售税代码)</span><span class="sxs-lookup"><span data-stu-id="a3a2a-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="a3a2a-126">如果将此选项设置为 **是**，则按销售税代码显示小计。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="a3a2a-127">仅合计</span><span class="sxs-lookup"><span data-stu-id="a3a2a-127">Totals only</span></span>                | <span data-ttu-id="a3a2a-128">如果将此选项设置为 **是**，则仅显示合计。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="a3a2a-129">仅主科目</span><span class="sxs-lookup"><span data-stu-id="a3a2a-129">Main accounts only</span></span>         | <span data-ttu-id="a3a2a-130">如果将此选项设置为 **是**，则报表中仅包含主科目。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="a3a2a-131">报表中仅显示非纳税科目</span><span class="sxs-lookup"><span data-stu-id="a3a2a-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="a3a2a-132">若要在报表中仅显示非纳税科目，请设置筛选条件，如星号 (\*)，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="a3a2a-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![报表显示非纳税科目](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]