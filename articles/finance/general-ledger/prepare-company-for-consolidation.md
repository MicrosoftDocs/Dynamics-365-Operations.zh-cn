---
title: 为合并流程准备法人
description: 在合并过程中，您将来自若干法人帐户组的交易记录汇集到单组法人帐户中。 本主题说明如何为合并准备法人。
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990288"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="14068-104">为合并流程准备法人</span><span class="sxs-lookup"><span data-stu-id="14068-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14068-105">在合并过程中，您将来自若干法人帐户组的交易记录汇集到单组法人帐户中。</span><span class="sxs-lookup"><span data-stu-id="14068-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="14068-106">本主题说明如何为合并准备法人。</span><span class="sxs-lookup"><span data-stu-id="14068-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="14068-107">我们建议您使用 Microsoft Dynamics 365 Finance 的 Management Reporter 以合并格式合并多个法人的财务结果。</span><span class="sxs-lookup"><span data-stu-id="14068-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="14068-108">通过 Management Reporter，您可以跨法人创建合并的财务报表，使用 Excel 从其他来源导入合并数据，并将金额转换为任意数量的报告货币，而无需在 Dynamics 365 Finance 中运行合并流程。</span><span class="sxs-lookup"><span data-stu-id="14068-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="14068-109">您可以从合并的法人打印报表，例如财务报表。</span><span class="sxs-lookup"><span data-stu-id="14068-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="14068-110">但是，您不能为每日交易记录使用合并的法人。</span><span class="sxs-lookup"><span data-stu-id="14068-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="14068-111">您可以合并使用与合并的法人不同数据库的法人的数据。</span><span class="sxs-lookup"><span data-stu-id="14068-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="14068-112">此合并过程称作 *导入合并*。</span><span class="sxs-lookup"><span data-stu-id="14068-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="14068-113">或者，法人实体可以将相同数据卡用作合并的法人。</span><span class="sxs-lookup"><span data-stu-id="14068-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="14068-114">此合并过程称作 *在线合并*。</span><span class="sxs-lookup"><span data-stu-id="14068-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="14068-115">合并的法人收集子公司的结果和余额。</span><span class="sxs-lookup"><span data-stu-id="14068-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="14068-116">若要为一个合并准备合并的法人，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="14068-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="14068-117">转到 **总帐 \> 设置 \> 组织 \> 法人**。</span><span class="sxs-lookup"><span data-stu-id="14068-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="14068-118">选择 **新建** 创建将成为合并的法人的法人。</span><span class="sxs-lookup"><span data-stu-id="14068-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="14068-119">选中 **用于财务合并流程** 复选框，然后输入有关合并的法人的信息。</span><span class="sxs-lookup"><span data-stu-id="14068-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="14068-120">请确保输入与您希望出现在合并的法人的财务报表中的相同的信息。</span><span class="sxs-lookup"><span data-stu-id="14068-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="14068-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14068-121">Close the page.</span></span>
5. <span data-ttu-id="14068-122">在页面右上角的字段中选择合并的法人，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="14068-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="14068-123">转到 **总帐 \> 设置 \> 分类帐**。</span><span class="sxs-lookup"><span data-stu-id="14068-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="14068-124">为合并的法人选择会计科目表、会计日历、记帐币种、一个可选申报币种和默认汇率类型。</span><span class="sxs-lookup"><span data-stu-id="14068-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="14068-125">转到 **总帐 \> 设置 \> 货币 \> 货币汇率**。</span><span class="sxs-lookup"><span data-stu-id="14068-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="14068-126">为子公司法人的货币设置相关期间中的货币汇率。</span><span class="sxs-lookup"><span data-stu-id="14068-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="14068-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14068-127">Close the page.</span></span>
11. <span data-ttu-id="14068-128">如果合并的法人有使用外币的子公司，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="14068-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="14068-129">转到 **总帐 \> 设置 \> 过帐 \> 自动交易记录帐户**。</span><span class="sxs-lookup"><span data-stu-id="14068-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="14068-130">在 **过帐类型** 字段中，选择适当的科目：</span><span class="sxs-lookup"><span data-stu-id="14068-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="14068-131">如果法人有在财务或运营上与母法人相互依赖的外国子公司，则为 **合并差异的损益科目** 过帐类型选择适当的科目。</span><span class="sxs-lookup"><span data-stu-id="14068-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="14068-132">如果您合并财务和运营上从母法人独立的子公司，或包含财务和运营上从母法人独立的若干子公司的结果的法人，且如果您使用转换方法合并数据，则为 **合并差异的资产负债科目** 过帐类型选择适当的科目。</span><span class="sxs-lookup"><span data-stu-id="14068-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="14068-133">在 **主科目** 字段中，选择应用于外币重估调整的主科目。</span><span class="sxs-lookup"><span data-stu-id="14068-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="14068-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="14068-134">Close the page.</span></span>

    <span data-ttu-id="14068-135">如果您在该期间的早期创建合并的法人，则您可以在合并期间汇率发生变化时，重估外币金额。</span><span class="sxs-lookup"><span data-stu-id="14068-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="14068-136">合并的法人现在为 **合并** 定期作业进行设置。</span><span class="sxs-lookup"><span data-stu-id="14068-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="14068-137">您可以执行导入合并或在线合并。</span><span class="sxs-lookup"><span data-stu-id="14068-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="14068-138">要进行导入合并，转到 **总帐 \> 定期 \> 合并 \> 合并\[导入来源\]**。</span><span class="sxs-lookup"><span data-stu-id="14068-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="14068-139">要进行在线合并，转到 **总帐 \> 定期 \> 合并 \> 合并\[在线\]**。</span><span class="sxs-lookup"><span data-stu-id="14068-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="14068-140">在您可以处理合并前，必须准备用于合并的子公司法人。</span><span class="sxs-lookup"><span data-stu-id="14068-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="14068-141">有关详细信息，请参阅[设置要合并的子公司法人](set-up-subsidiary-company-for-consolidation.md)。</span><span class="sxs-lookup"><span data-stu-id="14068-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>
