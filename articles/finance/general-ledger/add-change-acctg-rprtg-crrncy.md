---
title: 更改记帐或申报币种
description: 本主题介绍了如何更改记帐或申报币种，或者如何将申报币种添加到分类帐设置中。
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0435deb009173684c7faaf5340e8095c019ec71c
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085466"
---
# <a name="change-the-accounting-or-reporting-currency"></a><span data-ttu-id="b7570-103">更改记帐或申报币种</span><span class="sxs-lookup"><span data-stu-id="b7570-103">Change the accounting or reporting currency</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7570-104">本主题介绍了如何更改记帐或申报币种，或者如何将申报币种添加到分类帐设置中。</span><span class="sxs-lookup"><span data-stu-id="b7570-104">This topic explains how to change the accounting or reporting currency, or add a reporting currency to the setup of a ledger.</span></span>

## <a name="symptom"></a><span data-ttu-id="b7570-105">问题</span><span class="sxs-lookup"><span data-stu-id="b7570-105">Symptom</span></span>

<span data-ttu-id="b7570-106">您想要更改记帐或申报币种，或者将申报币种添加到分类帐设置中。</span><span class="sxs-lookup"><span data-stu-id="b7570-106">You want to change the accounting or reporting currency, or add a reporting currency to the ledger setup.</span></span> <span data-ttu-id="b7570-107">发生此情况通常是由于以下原因：</span><span class="sxs-lookup"><span data-stu-id="b7570-107">This typically occurs in the following scenarios:</span></span>

- <span data-ttu-id="b7570-108">设置法人时指定了错误的记帐或申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-108">The wrong accounting or reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="b7570-109">您现在想要更改该币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-109">You now want to change that currency.</span></span>
- <span data-ttu-id="b7570-110">设置法人时指定了申报币种，但是组织现在想要删除该申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-110">A reporting currency was specified when a legal entity was set up, but the organization now wants to remove the reporting currency.</span></span>
- <span data-ttu-id="b7570-111">组织正在升级或迁移到 Microsoft Dynamics 365 Finance，想要更改记帐或申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-111">The organization is upgrading or migrating to Microsoft Dynamics 365 Finance, and wants to change the accounting or reporting currency.</span></span>

<span data-ttu-id="b7570-112">先前未使用双货币功能的组织现在想要开始使用该功能。</span><span class="sxs-lookup"><span data-stu-id="b7570-112">An organization that didn't previously use the Dual currency capability wants to start to use it.</span></span> <span data-ttu-id="b7570-113">发生此问题通常是由于以下原因。</span><span class="sxs-lookup"><span data-stu-id="b7570-113">This issue typically occurs in the following scenarios.</span></span>

- <span data-ttu-id="b7570-114">设置法人时未指定申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-114">No reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="b7570-115">（申报币种为可选项。）您现在想要添加申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-115">(A reporting currency is optional.) You now want to add a reporting currency.</span></span>

## <a name="resolution"></a><span data-ttu-id="b7570-116">解决方法</span><span class="sxs-lookup"><span data-stu-id="b7570-116">Resolution</span></span>

<span data-ttu-id="b7570-117">最重要的注意事项是：是否已在分类帐设置的法人中过帐任何交易记录（实际或预算）。</span><span class="sxs-lookup"><span data-stu-id="b7570-117">The most important consideration is whether any transactions (actual or budget) have been posted in the legal entity for the ledger setup.</span></span> <span data-ttu-id="b7570-118">**如果已在法人中过帐任何交易记录（实际或预算），则无法更改记帐或申报币种，也不能添加申报币种。**</span><span class="sxs-lookup"><span data-stu-id="b7570-118">**You can't change the accounting or reporting currency, or add a reporting currency, if any transactions (actual or budget) have been posted in the legal entity.**</span></span> <span data-ttu-id="b7570-119">根据是否已过帐交易记录，按照以下部分之一中的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="b7570-119">Follow the steps in one of the following sections, depending on whether transactions have been posted.</span></span>

### <a name="no-transactions-have-been-posted"></a><span data-ttu-id="b7570-120">未过帐任何交易记录</span><span class="sxs-lookup"><span data-stu-id="b7570-120">No transactions have been posted</span></span>

1. <span data-ttu-id="b7570-121">在您要为其更新币种的法人中，转到 **总帐 \> 分类帐设置 \> 分类帐**。</span><span class="sxs-lookup"><span data-stu-id="b7570-121">In the legal entity that you're updating currencies for, go to **General ledger \> Ledger setup \> Ledger**.</span></span>
2. <span data-ttu-id="b7570-122">在 **分类帐** 页面上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b7570-122">On the **Ledger** page, select **Edit**.</span></span>
3. <span data-ttu-id="b7570-123">在 **币种** 快速选项卡上，选择要用于法人的记帐币种和申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-123">On the **Currency** FastTab, select the accounting currency and reporting currency to use for the legal entity.</span></span>
4. <span data-ttu-id="b7570-124">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b7570-124">Select **Save**.</span></span>

<span data-ttu-id="b7570-125">如果 **分类帐** 页面上的记帐币种和申报币种字段不可用，则说明已在法人中过帐一个或多个交易记录（实际或预算）。</span><span class="sxs-lookup"><span data-stu-id="b7570-125">If the fields for the accounting currency and the reporting currency aren't available on the **Ledger** page, one or more transactions (actual or budget) have been posted in the legal entity.</span></span> <span data-ttu-id="b7570-126">因此，无法更改币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-126">Therefore, the currencies can't be changed.</span></span> <span data-ttu-id="b7570-127">在这种情况下，请按照下一部分中的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="b7570-127">In this case, follow the steps in the next section.</span></span>

### <a name="transactions-have-been-posted"></a><span data-ttu-id="b7570-128">已过帐交易记录</span><span class="sxs-lookup"><span data-stu-id="b7570-128">Transactions have been posted</span></span>

<span data-ttu-id="b7570-129">**如果已在法人中过帐了交易记录，则更改或添加记帐和申报币种的唯一方法是创建一个具有正确币种的新法人。**</span><span class="sxs-lookup"><span data-stu-id="b7570-129">**If transactions have been posted in the legal entity, the only way to change or add accounting and reporting currencies is to create a new legal entity that has the correct currencies.**</span></span> <span data-ttu-id="b7570-130">为了帮助简化此过程，可使用系统中的数据管理功能将当前法人中的设置记录和主记录复制到新法人。</span><span class="sxs-lookup"><span data-stu-id="b7570-130">To help make this process easier, Data management in the system lets you copy setup records and master records from the current legal entity to a new legal entity.</span></span>

<span data-ttu-id="b7570-131">对记帐和申报币种所做的更改会产生扩散性影响。</span><span class="sxs-lookup"><span data-stu-id="b7570-131">Changes to the accounting and reporting currencies are pervasive.</span></span> <span data-ttu-id="b7570-132">这些更改不仅会影响总帐，还会影响每个子分类帐（应收帐款、应付帐款、库存、项目等）、每个独立软件供应商 (ISV) 解决方案以及您为存储金额而进行的任何扩展。</span><span class="sxs-lookup"><span data-stu-id="b7570-132">They affect not only General ledger but also every subledger (Accounts receivable, Accounts payable, Inventory, Project, and so on), every independent software vendor (ISV) solutions, and any extension that you've made that stores amounts.</span></span>

<span data-ttu-id="b7570-133">查找每笔金额并将其转换为其他币种的流程可能会出错。</span><span class="sxs-lookup"><span data-stu-id="b7570-133">The process of finding and translating each amount to a different currency is subject to error.</span></span> <span data-ttu-id="b7570-134">因此，工程团队不会批准用于更改或添加记帐和申报币种的脚本。</span><span class="sxs-lookup"><span data-stu-id="b7570-134">Therefore, the engineering team won't approve a script that changes or adds accounting and reporting currencies.</span></span> <span data-ttu-id="b7570-135">此外，尽管可以通过过去用于 Microsoft Dynamics AX 2012 的工具来更改或添加记帐和申报币种，但 AX 2012 R3 和 Finance 中均已弃用该工具。</span><span class="sxs-lookup"><span data-stu-id="b7570-135">Additionally, although a tool that used to be available for Microsoft Dynamics AX 2012 let you change or add accounting and reporting currencies, that tool was deprecated for both AX 2012 R3 and Finance.</span></span>

<span data-ttu-id="b7570-136">请按照以下步骤将当前法人中的设置和主数据复制到新法人。</span><span class="sxs-lookup"><span data-stu-id="b7570-136">Follow these steps to copy the setup and master data from the current legal entity to a new legal entity.</span></span>

1. <span data-ttu-id="b7570-137">转到 **工作区 \> 数据管理**。</span><span class="sxs-lookup"><span data-stu-id="b7570-137">Go to **Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="b7570-138">选择 **导入/导出** 组下的 **模板**。</span><span class="sxs-lookup"><span data-stu-id="b7570-138">Select **Templates** under the **Import/Export** group.</span></span>
3. <span data-ttu-id="b7570-139">确保模板可用。</span><span class="sxs-lookup"><span data-stu-id="b7570-139">Make sure that templates are available.</span></span> <span data-ttu-id="b7570-140">如果没有任何可用的模板，请选择 **加载默认模板**，然后等待生成模板。</span><span class="sxs-lookup"><span data-stu-id="b7570-140">If no templates are available, select **Load default templates**, and wait for the templates to be generated.</span></span>
4. <span data-ttu-id="b7570-141">返回到 **数据管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="b7570-141">Return to the **Data management** workspace.</span></span>
5. <span data-ttu-id="b7570-142">选择 **复制到法人**。</span><span class="sxs-lookup"><span data-stu-id="b7570-142">Select **Copy into legal entity**.</span></span>
6. <span data-ttu-id="b7570-143">输入组名称和描述。</span><span class="sxs-lookup"><span data-stu-id="b7570-143">Enter a group name and description.</span></span>
7. <span data-ttu-id="b7570-144">在 **源法人** 字段中，选择要从中复制数据的法人。</span><span class="sxs-lookup"><span data-stu-id="b7570-144">In the **Source legal entity** field, select the legal entity to copy data from.</span></span>
8. <span data-ttu-id="b7570-145">在 **目标法人** 快速选项卡中，选择 **创建法人** 以创建一个新法人，可将源法人数据复制到该新法人中。</span><span class="sxs-lookup"><span data-stu-id="b7570-145">In the **Destination legal entities** FastTab, select **Create legal entities** to create a new legal entity that you can copy the source legal entity data to.</span></span> <span data-ttu-id="b7570-146">选择 **选择现有** 以将数据复制到现有的法人。</span><span class="sxs-lookup"><span data-stu-id="b7570-146">Select **Select existing** to copy data to an existing legal entity.</span></span>
9. <span data-ttu-id="b7570-147">可选：将 **复制编号规则** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b7570-147">Optional: Set the **Copy number sequences** field to **Yes**.</span></span> <span data-ttu-id="b7570-148">（建议您在复制数据时执行此步骤。）</span><span class="sxs-lookup"><span data-stu-id="b7570-148">(This step is recommended when you copy data.)</span></span>
10. <span data-ttu-id="b7570-149">在 **选定的法人** 区域中，选择 **添加模板**。</span><span class="sxs-lookup"><span data-stu-id="b7570-149">In the **Selected entities** area, select **Add template**.</span></span>
11. <span data-ttu-id="b7570-150">选择要使用的模板。</span><span class="sxs-lookup"><span data-stu-id="b7570-150">Select the templates to use.</span></span> <span data-ttu-id="b7570-151">建议用于新法人的模板包括 **025 - 总帐** 和 **财务**。</span><span class="sxs-lookup"><span data-stu-id="b7570-151">Suggested templates for a new legal entity include **025 - General Ledger** and **Financials**.</span></span> <span data-ttu-id="b7570-152">我们建议您查看所有其他可用的模板，以确定它们中是否有任何模板适合于您的要求。</span><span class="sxs-lookup"><span data-stu-id="b7570-152">We recommend that you review all the other available templates to determine whether any of them apply to your requirements.</span></span>
12. <span data-ttu-id="b7570-153">选择 **复制到法人** 以启动批处理流程，此流程将创建选定的实体，并将其复制到目标法人。</span><span class="sxs-lookup"><span data-stu-id="b7570-153">Select **Copy into legal entity** to start a batch process that will create the selected entities and copy them into the destination legal entity.</span></span>
13. <span data-ttu-id="b7570-154">在该流程完成之后，但在过帐任何交易记录之前，请转到分类帐，并按照本主题前面所述更新记帐和申报币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-154">After the process is completed, but before any transaction are posted, go to the ledger, and update the accounting and reporting currencies as described earlier in this topic.</span></span>

<span data-ttu-id="b7570-155">如果您创建了一个新法人，以便可以更改记帐或申报币种，请核实是否已将期初余额从旧法人的币种转换为新币种。</span><span class="sxs-lookup"><span data-stu-id="b7570-155">If you created a new legal entity so that you can change the accounting or reporting currency, verify that the beginning balances are translated from the currencies of the old legal entity to the new currencies.</span></span>

<span data-ttu-id="b7570-156">有关介绍上述步骤的视频，请参阅[复制到法人](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017)。</span><span class="sxs-lookup"><span data-stu-id="b7570-156">For a video that shows the preceding steps, see [Copy Into Legal Entity](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span></span>
