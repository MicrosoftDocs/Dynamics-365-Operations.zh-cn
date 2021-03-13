---
title: 按时间顺序对文件和凭证编号
description: 本主题说明如何为适用的单据和相关凭证设置和使用时间顺序编号。
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104352"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="f1906-103">按时间顺序对文件和凭证编号</span><span class="sxs-lookup"><span data-stu-id="f1906-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f1906-104">在某些国家/地区，法律要求按时间顺序对文件和相关凭证编号。</span><span class="sxs-lookup"><span data-stu-id="f1906-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="f1906-105">时间顺序必须受期间支持。</span><span class="sxs-lookup"><span data-stu-id="f1906-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="f1906-106">属于较早期间的所有编号必须小于属于较晚期间的编号。</span><span class="sxs-lookup"><span data-stu-id="f1906-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="f1906-107">为了满足此要求，实现了按时间顺序编号的功能。</span><span class="sxs-lookup"><span data-stu-id="f1906-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="f1906-108">本主题说明如何为适用的单据和相关凭证配置和使用时间顺序编号。</span><span class="sxs-lookup"><span data-stu-id="f1906-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f1906-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="f1906-109">Prerequisites</span></span>

<span data-ttu-id="f1906-110">在“功能管理”工作区中，开启 **按时间顺序编号** 功能：</span><span class="sxs-lookup"><span data-stu-id="f1906-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="f1906-111">有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f1906-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="f1906-112">配置按时间顺序编号</span><span class="sxs-lookup"><span data-stu-id="f1906-112">Configure chronological numbering</span></span>

<span data-ttu-id="f1906-113">按时间顺序编号会影响以下单据。</span><span class="sxs-lookup"><span data-stu-id="f1906-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="f1906-114">**应收账款**</span><span class="sxs-lookup"><span data-stu-id="f1906-114">**Accounts receivable**</span></span>
- <span data-ttu-id="f1906-115">客户账单</span><span class="sxs-lookup"><span data-stu-id="f1906-115">Customer invoice</span></span>
- <span data-ttu-id="f1906-116">客户账单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-116">Customer invoice voucher</span></span>
- <span data-ttu-id="f1906-117">销售贷方通知单</span><span class="sxs-lookup"><span data-stu-id="f1906-117">Sales credit note</span></span>
- <span data-ttu-id="f1906-118">销售贷方通知单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-118">Sales credit note voucher</span></span>
- <span data-ttu-id="f1906-119">普通账单</span><span class="sxs-lookup"><span data-stu-id="f1906-119">Free text invoice</span></span>
- <span data-ttu-id="f1906-120">普通账单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-120">Free text invoice voucher</span></span>
- <span data-ttu-id="f1906-121">普通贷方通知单</span><span class="sxs-lookup"><span data-stu-id="f1906-121">Free text credit note</span></span>
- <span data-ttu-id="f1906-122">普通贷方通知单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-122">Free text credit note voucher</span></span>
- <span data-ttu-id="f1906-123">装箱单</span><span class="sxs-lookup"><span data-stu-id="f1906-123">Packing slip</span></span>
- <span data-ttu-id="f1906-124">装箱单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-124">Packing slip voucher</span></span>
- <span data-ttu-id="f1906-125">装箱单更正凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="f1906-126">利息单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-126">Interest note voucher</span></span>
- <span data-ttu-id="f1906-127">催款单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-127">Collection letter voucher</span></span>

<span data-ttu-id="f1906-128">**应付帐款**</span><span class="sxs-lookup"><span data-stu-id="f1906-128">**Accounts payable**</span></span>
- <span data-ttu-id="f1906-129">账单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-129">Invoice voucher</span></span>
- <span data-ttu-id="f1906-130">贷方通知单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-130">Credit note voucher</span></span>
- <span data-ttu-id="f1906-131">物料收货凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-131">Product receipt voucher</span></span>

<span data-ttu-id="f1906-132">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="f1906-132">**Project management**</span></span>
- <span data-ttu-id="f1906-133">账单</span><span class="sxs-lookup"><span data-stu-id="f1906-133">Invoice</span></span>
- <span data-ttu-id="f1906-134">账单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-134">Invoice voucher</span></span>
- <span data-ttu-id="f1906-135">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="f1906-135">Credit note</span></span>
- <span data-ttu-id="f1906-136">贷方通知单凭证</span><span class="sxs-lookup"><span data-stu-id="f1906-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="f1906-137">定义编号规则</span><span class="sxs-lookup"><span data-stu-id="f1906-137">Define number sequences</span></span>

<span data-ttu-id="f1906-138">要定义编号规则，转到 **组织管理** > **编号规则** > **编号规则**。</span><span class="sxs-lookup"><span data-stu-id="f1906-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="f1906-139">您可以根据需要定义任意数量的编号规则，以覆盖所需单据的受影响期间。</span><span class="sxs-lookup"><span data-stu-id="f1906-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="f1906-140">为每个编号规则指定一个公司。</span><span class="sxs-lookup"><span data-stu-id="f1906-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="f1906-141">必须定义编号规则的细分，让它们为期间提供时间顺序。</span><span class="sxs-lookup"><span data-stu-id="f1906-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="f1906-142">例如，细分名称可以包含标识特定期间的特殊前缀。</span><span class="sxs-lookup"><span data-stu-id="f1906-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![编号规则设置](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="f1906-144">配置编号规则组</span><span class="sxs-lookup"><span data-stu-id="f1906-144">Configure number sequence groups</span></span>

<span data-ttu-id="f1906-145">要配置编号规则组，转到 **应收帐款** > **设置** > **应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="f1906-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="f1906-146">在 **编号规则** 选项卡上，根据需要定义任意数量的编号规则组以覆盖受影响的期间。</span><span class="sxs-lookup"><span data-stu-id="f1906-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="f1906-147">对于每个组，在 **引用** 部分，选择其中一个受支持的单据引用，在 **编号规则代码** 字段中，引用先前为相关期间创建的编号规则。</span><span class="sxs-lookup"><span data-stu-id="f1906-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![编号规则组设置](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="f1906-149">同样，在 **应付帐款** 和 **项目管理和会计** 模块中配置编号规则组。</span><span class="sxs-lookup"><span data-stu-id="f1906-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="f1906-150">配置编号规则组的时间顺序</span><span class="sxs-lookup"><span data-stu-id="f1906-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="f1906-151">要配置编号规则组的时间顺序，转到 **组织管理** > **编号规则** > **时间顺序编号规则组**。</span><span class="sxs-lookup"><span data-stu-id="f1906-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="f1906-152">定义编号规则组的适用条件。</span><span class="sxs-lookup"><span data-stu-id="f1906-152">Define the applicability conditions for number sequence groups.</span></span>

![时间顺序编号设置](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="f1906-154">字段</span><span class="sxs-lookup"><span data-stu-id="f1906-154">Field</span></span>            | <span data-ttu-id="f1906-155">说明</span><span class="sxs-lookup"><span data-stu-id="f1906-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1906-156">生效日期</span><span class="sxs-lookup"><span data-stu-id="f1906-156">Effective</span></span>  | <span data-ttu-id="f1906-157">编号规则组适用性的开始日期。</span><span class="sxs-lookup"><span data-stu-id="f1906-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="f1906-158">到期日期</span><span class="sxs-lookup"><span data-stu-id="f1906-158">Expiration</span></span>      | <span data-ttu-id="f1906-159">编号规则组适用性的结束日期。</span><span class="sxs-lookup"><span data-stu-id="f1906-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="f1906-160">如果不应用结束日期，选择 **从不**。</span><span class="sxs-lookup"><span data-stu-id="f1906-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="f1906-161">编号规则组</span><span class="sxs-lookup"><span data-stu-id="f1906-161">Number sequence group</span></span> | <span data-ttu-id="f1906-162">将用于在期间内生成单据编号的编号规则组。</span><span class="sxs-lookup"><span data-stu-id="f1906-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="f1906-163">原始编号规则组</span><span class="sxs-lookup"><span data-stu-id="f1906-163">Original number sequence group</span></span> | <span data-ttu-id="f1906-164">此编号规则组代码用于在单据已分配了特定的 *永久* 编号规则组的情况下进行其他筛选。</span><span class="sxs-lookup"><span data-stu-id="f1906-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="f1906-165">空值被视为特定值。</span><span class="sxs-lookup"><span data-stu-id="f1906-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="f1906-166">如果您需要忽略初步分配的组，请为此设置使用 **默认** 选项。</span><span class="sxs-lookup"><span data-stu-id="f1906-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="f1906-167">默认值</span><span class="sxs-lookup"><span data-stu-id="f1906-167">Default</span></span> | <span data-ttu-id="f1906-168">如果打开，系统将忽略初步分配的单据编号规则组，仅使用期间开始和结束日期进行适用性分析。</span><span class="sxs-lookup"><span data-stu-id="f1906-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="f1906-169">如果关闭，系统将使用完整组合 **生效日期** + **到期日期** + **原始编号规则组** 进行选择。</span><span class="sxs-lookup"><span data-stu-id="f1906-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="f1906-170">单据过帐</span><span class="sxs-lookup"><span data-stu-id="f1906-170">Document posting</span></span>
<span data-ttu-id="f1906-171">当您过帐单据时，会根据单据的过帐日期将适当的编号规则组分配给该单据，然后根据检测到的编号规则将该编号规则组用于生成单据编号。</span><span class="sxs-lookup"><span data-stu-id="f1906-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="f1906-172">系统将提供有关编号规则组分配的消息。</span><span class="sxs-lookup"><span data-stu-id="f1906-172">The system provides a message regarding the number sequence group assignment.</span></span>

![文档编号](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="f1906-174">对于有些国家/地区，已经为单据编号实现了特定逻辑。</span><span class="sxs-lookup"><span data-stu-id="f1906-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="f1906-175">在这种情况下，国家/地区特定的逻辑将替代 **按时间顺序编号** 功能。</span><span class="sxs-lookup"><span data-stu-id="f1906-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>
