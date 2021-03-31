---
title: 设置要合并的子公司法人
description: 本主题说明如何使用合并公司的会计科目表。
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
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 44bd184514b24a816cc83f6b0070a5e08163921b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204801"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a><span data-ttu-id="7f411-103">设置要合并的子公司法人</span><span class="sxs-lookup"><span data-stu-id="7f411-103">Set up a subsidiary legal entity for consolidation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f411-104">您准备用于合并的子公司帐户的方法取决于，一部分，在何种程度上结构在子公司中法人在合并法人中反映的会计科目表。</span><span class="sxs-lookup"><span data-stu-id="7f411-104">The method that you use to prepare subsidiary accounts for consolidation depends in part on the extent to which the structure of the chart of accounts in the subsidiary legal entity reflects the chart of accounts in the consolidated legal entity.</span></span>

<span data-ttu-id="7f411-105">在开始合并作为关闭期间结束之前，完成该期间结束关闭执行准备性活动，但在合并完成前不关闭子公司帐户。</span><span class="sxs-lookup"><span data-stu-id="7f411-105">Before you start a consolidation as part of period-end closing, complete the preparatory activities for the period-end closing, but don't close the subsidiary accounts until the consolidation is completed.</span></span> <span data-ttu-id="7f411-106">有关期间结束关闭的详细信息，请参阅[在期间结束时关闭总帐](close-general-ledger-at-period-end.md)和[关帐会计年度](tasks/close-fiscal-year.md)。</span><span class="sxs-lookup"><span data-stu-id="7f411-106">For more information about period-end closing, see [Close the general ledger at period end](close-general-ledger-at-period-end.md) and [Close the fiscal year](tasks/close-fiscal-year.md).</span></span>

> [!NOTE]
>  <span data-ttu-id="7f411-107">我们建议您使用 Microsoft Dynamics 365 Finance 的 Management Reporter 以合并格式合并多个法人的财务结果。</span><span class="sxs-lookup"><span data-stu-id="7f411-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="7f411-108">通过 Management Reporter，您可以跨法人创建合并的财务报表，使用 Excel 从其他来源导入合并数据，并将金额转换为任意数量的报告货币，而无需在 Dynamics 365 Finance 中运行合并流程。</span><span class="sxs-lookup"><span data-stu-id="7f411-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a><span data-ttu-id="7f411-109">将子公司主科目映射到合并主科目</span><span class="sxs-lookup"><span data-stu-id="7f411-109">Map subsidiary main accounts to consolidated main accounts</span></span>

<span data-ttu-id="7f411-110">如果会计科目表在子公司中的法人不遵循在合并的法人会计科目表，则映射在子公司中的主帐户到在合并法人的主科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-110">If the chart of accounts in the subsidiary legal entity doesn't follow the chart of accounts in the consolidated legal entity, you can map the main accounts in the subsidiary to the main accounts in the consolidated legal entity.</span></span>

1. <span data-ttu-id="7f411-111">在 *子公司法人* 中，转到 **总帐 \> 设置** \> **会计科目表 \> 会计科目表**。</span><span class="sxs-lookup"><span data-stu-id="7f411-111">In the *subsidiary legal entity*, go to **General ledger \> Setup** \> **Chart of accounts \> Chart of accounts**.</span></span>
2. <span data-ttu-id="7f411-112">选择某一会计科目表。</span><span class="sxs-lookup"><span data-stu-id="7f411-112">Select a chart of accounts.</span></span> <span data-ttu-id="7f411-113">在 **主科目** 快速选项卡上，选择一个主科目，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="7f411-113">On the **Main accounts** FastTab, select a main account, and then select **Edit**.</span></span>
3. <span data-ttu-id="7f411-114">选择必须映射到合并的主科目的每个子公司主科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-114">Select each subsidiary main account that must be mapped to a consolidated main account.</span></span> <span data-ttu-id="7f411-115">在 **常规** 快速选项卡上，在 **合并科目** 字段中，输入所选子公司主科目必须将余额或交易记录转移到的合并法人中的科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-115">On the **General** FastTab, in the **Consolidation account** field, enter the account in the consolidated legal entity that the balance or transactions of the selected subsidiary main account must be transferred to.</span></span> <span data-ttu-id="7f411-116">您可以输入若干子公司科目的相同的合并主科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-116">You can enter the same consolidated main account for several subsidiary accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f411-117">如果映射的子公司科目的主科目类型与合并法人中的科目的主科目类型不同，则具有 **总计** 主科目类型的科目值将在合并期间被覆盖。</span><span class="sxs-lookup"><span data-stu-id="7f411-117">If the main account types of the subsidiary accounts that are mapped differ from the main account types of the accounts in the consolidated legal entity, the values of accounts that have a main account type of **Total** are overwritten during consolidation.</span></span>

4. <span data-ttu-id="7f411-118">为合并法人准备基于财务维度的报表和财务报表。</span><span class="sxs-lookup"><span data-stu-id="7f411-118">Prepare reports and financial statements for the consolidated legal entity that are based on financial dimensions.</span></span> <span data-ttu-id="7f411-119">请按照以下步骤将子公司科目中使用的财务维度映射到合并法人中的财务维度：</span><span class="sxs-lookup"><span data-stu-id="7f411-119">Follow these steps to map the financial dimensions that are used in the subsidiary accounts to the financial dimensions in the consolidated legal entity:</span></span>

    1. <span data-ttu-id="7f411-120">在 *子公司法人* 中，转到 **总帐 \> 设置 \> 财务维度 \> 财务维度**，选择一个财务维度，然后选择 **财务维度值**。</span><span class="sxs-lookup"><span data-stu-id="7f411-120">In the *subsidiary legal entity*, go to **General ledger \> Setup \> Financial dimensions \> Financial dimensions**, select a financial dimension, and then select **Financial dimension values**.</span></span>
    2. <span data-ttu-id="7f411-121">选择财务维度值以映射到合并法人中不同的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="7f411-121">Select the financial dimension value to map to a different financial dimension value in the consolidated legal entity.</span></span>
    3. <span data-ttu-id="7f411-122">在 **常规** 快速选项卡上，在 **组维度** 字段中，在合并的法人中输入财务维度。</span><span class="sxs-lookup"><span data-stu-id="7f411-122">On the **General** FastTab, in the **Group dimension** field, enter the financial dimension in the consolidated legal entity.</span></span> <span data-ttu-id="7f411-123">在合并期间，此财务维度将分配给在子公司法人中使用所选财务维度的交易记录和余额。</span><span class="sxs-lookup"><span data-stu-id="7f411-123">During consolidation, this financial dimension will be assigned to transactions and balances that use the selected financial dimension in the subsidiary legal entity.</span></span> <span data-ttu-id="7f411-124">在此处输入的财务维度必须在合并的法人中使用。</span><span class="sxs-lookup"><span data-stu-id="7f411-124">The financial dimensions that you enter here must be used in the consolidated legal entity.</span></span> <span data-ttu-id="7f411-125">您可以分配将用作为若干子公司财务维度的财务维度组的财务维度。</span><span class="sxs-lookup"><span data-stu-id="7f411-125">You can assign the financial dimension that is used as the group financial dimension to several subsidiary financial dimensions.</span></span>

5. <span data-ttu-id="7f411-126">如果您要进行在线合并，请按照以下步骤确保转移按预期进行：</span><span class="sxs-lookup"><span data-stu-id="7f411-126">If you're doing an online consolidation, follow these steps to ensure that the transfers occur as you intend:</span></span>

    1. <span data-ttu-id="7f411-127">在 *合并的法人* 中，转到 **总帐 \> 定期 \> 合并 \> 合并\[导出目标\]** 打开 **合并\[在线\]** 页。</span><span class="sxs-lookup"><span data-stu-id="7f411-127">In the *consolidated legal entity*, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Export to\]** to open the **Consolidate \[Online\]** page.</span></span>
    2. <span data-ttu-id="7f411-128">在 **条件** 选项卡上，选中 **使用合并科目** 复选框。</span><span class="sxs-lookup"><span data-stu-id="7f411-128">On the **Criteria** tab, select the **Use consolidation account** check box.</span></span>
    3. <span data-ttu-id="7f411-129">在 **财务维度** 选项卡上，选择适当的财务维度。</span><span class="sxs-lookup"><span data-stu-id="7f411-129">On the **Financial dimensions** tab, select the appropriate financial dimensions.</span></span>
    4. <span data-ttu-id="7f411-130">对于所选的每个财务维度，请在 **段顺序** 字段中输入数字指示维度显示应该遵循的顺序。</span><span class="sxs-lookup"><span data-stu-id="7f411-130">For each financial dimension that you select, enter a number in the **Segment order** field to indicate the order that the dimensions should appear in.</span></span>

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a><span data-ttu-id="7f411-131">在子公司和合并的法人中维护相同的会计科目表</span><span class="sxs-lookup"><span data-stu-id="7f411-131">Maintain the same chart of accounts in the subsidiary and consolidated legal entities</span></span>

<span data-ttu-id="7f411-132">主科目在合并的法人中时，主科目在子公司中法人可能会具有相同帐号和相同的会计科目表的结构。</span><span class="sxs-lookup"><span data-stu-id="7f411-132">The main accounts in the subsidiary legal entity might have the same account numbers and the same structure for the chart of accounts as the main accounts in the consolidated legal entity.</span></span> <span data-ttu-id="7f411-133">在此情况下，您不必手动映射子公司中的主科目到合并的法人主科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-133">In this case, you don't have to manually map the main accounts in the subsidiary to the main accounts in the consolidated legal entity.</span></span>

<span data-ttu-id="7f411-134">在开始合并之前，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7f411-134">Before you start the consolidation, follow these steps.</span></span>

1. <span data-ttu-id="7f411-135">在 *合并的法人* 中，转到 **总帐 \> 定期 \> 合并 \> 合并\[导出目标\]** 打开 **合并\[在线\]** 页。</span><span class="sxs-lookup"><span data-stu-id="7f411-135">In the *consolidated legal entity*, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Export to\]** to open the **Consolidate \[Online\]** page.</span></span>
2. <span data-ttu-id="7f411-136">选中 **使用合并科目** 复选框。</span><span class="sxs-lookup"><span data-stu-id="7f411-136">Select the **Use consolidation account** check box.</span></span> <span data-ttu-id="7f411-137">在合并期间，交易记录和余额将自动转移到正确的科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-137">During consolidation, transactions and balances will automatically be transferred to the correct account.</span></span>

> [!NOTE]
> <span data-ttu-id="7f411-138">如果科目不符，则合并将停止，并且系统将显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="7f411-138">If the accounts don't correspond, the consolidation stops, and you receive a message.</span></span>

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a><span data-ttu-id="7f411-139">基于现有会计科目表创建合并的法人的会计科目表</span><span class="sxs-lookup"><span data-stu-id="7f411-139">Create a chart of accounts for the consolidated legal entity, based on an existing chart of accounts</span></span>

<span data-ttu-id="7f411-140">即使尚未在合并的法人中创建会计科目表，您也可以执行合并。</span><span class="sxs-lookup"><span data-stu-id="7f411-140">You can do a consolidation even if a chart of accounts hasn't already been created in the consolidated legal entity.</span></span>

- <span data-ttu-id="7f411-141">如果您计划希望在合并的法人中使用的科目结构，您可以将子公司科目映射到此结构。</span><span class="sxs-lookup"><span data-stu-id="7f411-141">If you've planned the account structure that you want to use in the consolidated legal entity, you can map the subsidiary accounts to this structure.</span></span>
- <span data-ttu-id="7f411-142">如果您没有任何子公司科目映射，则在子公司数据转移到合并时法人，科目将在合并的法人中自动创建。</span><span class="sxs-lookup"><span data-stu-id="7f411-142">If you don't map any subsidiary accounts, the accounts in the consolidated legal entity are automatically created when subsidiary data is transferred to the consolidated legal entity.</span></span> <span data-ttu-id="7f411-143">这些科目基于主科目。</span><span class="sxs-lookup"><span data-stu-id="7f411-143">These accounts are based on the main account.</span></span> <span data-ttu-id="7f411-144">随后的数据合并的法人中累计和子公司科目具有相同的科目编号。</span><span class="sxs-lookup"><span data-stu-id="7f411-144">Subsequent data is accumulated in accounts in the consolidated legal entity that have the same account number as the subsidiary accounts.</span></span>

<span data-ttu-id="7f411-145">不论您是否映射了这些科目，在运行此类合并前，请在合并法人中的 **合并** 页上清除 **使用合并科目** 复选框。</span><span class="sxs-lookup"><span data-stu-id="7f411-145">Regardless of whether you've mapped accounts, clear the **Use consolidation account** check box on the **Consolidate** page in the consolidated legal entity before you run this type of consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="7f411-146">您可以使用从子公司法人的会计科目表之一的方法，在合并法人中创建会计科目表。</span><span class="sxs-lookup"><span data-stu-id="7f411-146">You can use this method to create a chart of accounts in the consolidated legal entity from the chart of accounts in one of the subsidiary legal entities.</span></span> <span data-ttu-id="7f411-147">（有关详细信息，请参阅[合并科目组和其他合并科目](../budgeting/consolidation-account-groups-consolidation-accounts.md)。）然后将相应的合并转换原则分配给各合并主科目，并且为所有子公司法人运行合并。</span><span class="sxs-lookup"><span data-stu-id="7f411-147">(For more information, see [Consolidation account groups and additional consolidation accounts](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Then assign an appropriate consolidation conversion principle to each consolidated main account, and run the consolidation for all the subsidiary legal entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]