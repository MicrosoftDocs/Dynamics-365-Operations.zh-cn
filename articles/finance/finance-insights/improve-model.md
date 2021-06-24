---
title: 改进预测模型（预览）
description: 本主题介绍可用于改善预测模型性能的功能。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186634"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="a4e65-103">改进预测模型（预览）</span><span class="sxs-lookup"><span data-stu-id="a4e65-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a4e65-104">本主题介绍可用于改善预测模型性能的功能。</span><span class="sxs-lookup"><span data-stu-id="a4e65-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="a4e65-105">您开始在 Microsoft Dynamics 365 Finance 中的 **客户付款预测** 工作区中开始改进模型。</span><span class="sxs-lookup"><span data-stu-id="a4e65-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="a4e65-106">然后在 AI Builder 中完成改进步骤。</span><span class="sxs-lookup"><span data-stu-id="a4e65-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="a4e65-107">选择历史结果</span><span class="sxs-lookup"><span data-stu-id="a4e65-107">Select historical outcomes</span></span>

<span data-ttu-id="a4e65-108">您首先选择三种可能的发票结果中的一个或多个：**按时**、**逾期** 和 **严重逾期**。</span><span class="sxs-lookup"><span data-stu-id="a4e65-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="a4e65-109">应选择所有三个结果。</span><span class="sxs-lookup"><span data-stu-id="a4e65-109">All three outcomes should be selected.</span></span> <span data-ttu-id="a4e65-110">如果您清除任何结果的选择，发票将被从训练过程中筛选掉，并且预测的准确性将降低。</span><span class="sxs-lookup"><span data-stu-id="a4e65-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="a4e65-111">[![确认结果](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="a4e65-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="a4e65-112">如果您的组织仅需要两个结果，则将 **逾期** 和 **严重逾期** 阈值设置为 0（零）天。</span><span class="sxs-lookup"><span data-stu-id="a4e65-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="a4e65-113">这样，您可以有效地将预测折叠为二进制状态 **按时** 或 **逾期**。</span><span class="sxs-lookup"><span data-stu-id="a4e65-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="a4e65-114">选择字段</span><span class="sxs-lookup"><span data-stu-id="a4e65-114">Select fields</span></span>

<span data-ttu-id="a4e65-115">当您选择要包含在模型中的字段时，请注意列表包含了映射到 Azure 数据湖中的数据的 Microsoft Dataverse 表中的所有可用字段。</span><span class="sxs-lookup"><span data-stu-id="a4e65-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="a4e65-116">**不** 应选择其中一些字段。</span><span class="sxs-lookup"><span data-stu-id="a4e65-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="a4e65-117">不应选择的字段属于以下三类之一：</span><span class="sxs-lookup"><span data-stu-id="a4e65-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="a4e65-118">该字段是 Dataverse 表的必填字段，但在数据湖中没有其支持数据。</span><span class="sxs-lookup"><span data-stu-id="a4e65-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="a4e65-119">该字段是一个 ID，因此对于机器学习功能没有意义。</span><span class="sxs-lookup"><span data-stu-id="a4e65-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="a4e65-120">该字段表示在预测期间将不可用的信息。</span><span class="sxs-lookup"><span data-stu-id="a4e65-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="a4e65-121">以下各节显示了可用于发票和客户实体的字段，并列出了 **不** 应选中进行训练的字段。</span><span class="sxs-lookup"><span data-stu-id="a4e65-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="a4e65-122">为每个字段指定的类别是指前面列表中的类别。</span><span class="sxs-lookup"><span data-stu-id="a4e65-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="a4e65-123">发票 Dataverse 表</span><span class="sxs-lookup"><span data-stu-id="a4e65-123">Invoice Dataverse table</span></span>

<span data-ttu-id="a4e65-124">下图显示可用于发票表的字段。</span><span class="sxs-lookup"><span data-stu-id="a4e65-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="a4e65-125">[![发票表的可用字段](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="a4e65-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="a4e65-126">不应选择以下字段进行训练：</span><span class="sxs-lookup"><span data-stu-id="a4e65-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="a4e65-127">**发票科目**（类别 2）</span><span class="sxs-lookup"><span data-stu-id="a4e65-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="a4e65-128">**已结**（类别 3）– 此字段用于筛选要训练的发票（已结）和预测（未结）。</span><span class="sxs-lookup"><span data-stu-id="a4e65-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="a4e65-129">**名称**（类别 1）</span><span class="sxs-lookup"><span data-stu-id="a4e65-129">**Name** (category 1)</span></span>
- <span data-ttu-id="a4e65-130">**源 Id**（类别 2）</span><span class="sxs-lookup"><span data-stu-id="a4e65-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="a4e65-131">**源记录**（类别 2）</span><span class="sxs-lookup"><span data-stu-id="a4e65-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="a4e65-132">**源表**（类别 2）</span><span class="sxs-lookup"><span data-stu-id="a4e65-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="a4e65-133">客户 Dataverse 表</span><span class="sxs-lookup"><span data-stu-id="a4e65-133">Customer Dataverse table</span></span>

<span data-ttu-id="a4e65-134">下图显示可用于客户表的字段。</span><span class="sxs-lookup"><span data-stu-id="a4e65-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="a4e65-135">[![客户表的可用字段](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="a4e65-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="a4e65-136">不应选择以下字段进行训练：</span><span class="sxs-lookup"><span data-stu-id="a4e65-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="a4e65-137">**行唯一键**（类别 2）</span><span class="sxs-lookup"><span data-stu-id="a4e65-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="a4e65-138">筛选器</span><span class="sxs-lookup"><span data-stu-id="a4e65-138">Filters</span></span>

<span data-ttu-id="a4e65-139">筛选器当前不支持“客户付款预测器”方案。</span><span class="sxs-lookup"><span data-stu-id="a4e65-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="a4e65-140">因此，请选择 **跳过此步骤**，然后转到摘要页面。</span><span class="sxs-lookup"><span data-stu-id="a4e65-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="a4e65-141">[![带筛选器的焦点模型](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="a4e65-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
