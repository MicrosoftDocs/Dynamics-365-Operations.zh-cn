---
title: "财务维度"
description: "本主题介绍财务维度的不同类型以及如何设置。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="a028d-103">财务维度</span><span class="sxs-lookup"><span data-stu-id="a028d-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a028d-104">本主题说明财务维度的不同类型以及如何设置。</span><span class="sxs-lookup"><span data-stu-id="a028d-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="a028d-105">使用**财务维度**页可创建可用作会计科目表的科目段的财务维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="a028d-106">有两类财务维度：自定义维度和实体支持的维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="a028d-107">自定义维度在法人之间共享，并且值由用户输入和维护。</span><span class="sxs-lookup"><span data-stu-id="a028d-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="a028d-108">对于实体支持的维度，其值在系统的其他地方进行定义，如客户或商店实体。</span><span class="sxs-lookup"><span data-stu-id="a028d-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="a028d-109">有些实体支持的维度在法人间共享，而有些实体支持的维度则特定于公司。</span><span class="sxs-lookup"><span data-stu-id="a028d-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="a028d-110">在您创建了财务维度之后，使用**财务维度值**页给每个财务维度分配附加属性。</span><span class="sxs-lookup"><span data-stu-id="a028d-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="a028d-111">您可以使用财务维度代表法人。</span><span class="sxs-lookup"><span data-stu-id="a028d-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="a028d-112">您不必在 Microsoft Dynamics 365 for Finance and Operations 中创建实体。</span><span class="sxs-lookup"><span data-stu-id="a028d-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a028d-113">但是，财务维度不用来解决法人的运营或业务需求。</span><span class="sxs-lookup"><span data-stu-id="a028d-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="a028d-114">将 Finance and Operations 中的单位间核算功能设计成仅满足由每个交易记录所创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="a028d-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="a028d-115">在将财务维度设置为法人之前，评估您的业务流程中的以下区域以确定此设置是否适用于您的组织：</span><span class="sxs-lookup"><span data-stu-id="a028d-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="a028d-116">库存</span><span class="sxs-lookup"><span data-stu-id="a028d-116">Inventory</span></span>
- <span data-ttu-id="a028d-117">财务维度和法人之间的销售和采购</span><span class="sxs-lookup"><span data-stu-id="a028d-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="a028d-118">计算和申报销售税</span><span class="sxs-lookup"><span data-stu-id="a028d-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="a028d-119">操作报告</span><span class="sxs-lookup"><span data-stu-id="a028d-119">Operational reporting</span></span>

<span data-ttu-id="a028d-120">这是一些限制：</span><span class="sxs-lookup"><span data-stu-id="a028d-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="a028d-121">您只可以以法人身份使用销售纳税仅功能，但是不可以凭财务维度使用此功能。</span><span class="sxs-lookup"><span data-stu-id="a028d-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="a028d-122">有些报表不包括财务维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="a028d-123">因此，要按财务维度进行报告，您可能必须修改报表。</span><span class="sxs-lookup"><span data-stu-id="a028d-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="a028d-124">自定义维度</span><span class="sxs-lookup"><span data-stu-id="a028d-124">Custom dimensions</span></span>

<span data-ttu-id="a028d-125">若要创建用户定义的财务维度，在**使用以下来源中的值**字段中，选择**&lt;自定义维度&gt;**。</span><span class="sxs-lookup"><span data-stu-id="a028d-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="a028d-126">您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。</span><span class="sxs-lookup"><span data-stu-id="a028d-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="a028d-127">您可以输入保持不变的每个维度值的信息，例如字母或连字符 (-)。</span><span class="sxs-lookup"><span data-stu-id="a028d-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="a028d-128">还可以输入数字标志 (\#) 和和符号 (&) 作为每次要更改的字母和数字的占位符创建维度值。</span><span class="sxs-lookup"><span data-stu-id="a028d-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="a028d-129">使用一个数字标志 (\#) 作为编号占位符和符号 (&) 作为信函的占位符。</span><span class="sxs-lookup"><span data-stu-id="a028d-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="a028d-130">只有在**&lt;使用以下来源中的值&gt;**字段中选择**自定义维度**后，用于格式掩码的字段才可用。</span><span class="sxs-lookup"><span data-stu-id="a028d-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="a028d-131">**示例**</span><span class="sxs-lookup"><span data-stu-id="a028d-131">**Example**</span></span>

<span data-ttu-id="a028d-132">若要限制维度值到“CC”和三个数字，输入 **CC-\#\#\#** 作为格式掩码。</span><span class="sxs-lookup"><span data-stu-id="a028d-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="a028d-133">实体支持的维度</span><span class="sxs-lookup"><span data-stu-id="a028d-133">Entity-backed dimensions</span></span>

<span data-ttu-id="a028d-134">若要创建实体支持的财务维度，在**使用以下来源中的值**字段中，选择财务维度所基于的系统定义的实体。</span><span class="sxs-lookup"><span data-stu-id="a028d-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="a028d-135">随后将从此实体创建财务维度值。</span><span class="sxs-lookup"><span data-stu-id="a028d-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="a028d-136">例如，要为项目创建维度值，请选择**项目**。</span><span class="sxs-lookup"><span data-stu-id="a028d-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="a028d-137">将为每个项目名称将创建维度值。</span><span class="sxs-lookup"><span data-stu-id="a028d-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="a028d-138">**财务维度值**页显示实体的值。</span><span class="sxs-lookup"><span data-stu-id="a028d-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="a028d-139">如果这些值是公司特定的，则页面上还显示公司。</span><span class="sxs-lookup"><span data-stu-id="a028d-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="a028d-140">激活维度</span><span class="sxs-lookup"><span data-stu-id="a028d-140">Activating dimensions</span></span>

<span data-ttu-id="a028d-141">在您启用财务维度时，表进行更新，使其包含财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="a028d-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="a028d-142">删除被移除的维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="a028d-143">启用财务维度前，您可以输入维度值。</span><span class="sxs-lookup"><span data-stu-id="a028d-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="a028d-144">不过，在启用财务维度前，无法在任何地方使用财务维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="a028d-145">例如，到启用财务维度以前，您不能将财务维度添加到科目结构。</span><span class="sxs-lookup"><span data-stu-id="a028d-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="a028d-146">在您单击**启用**后，所有维度更新并显示状态更改。</span><span class="sxs-lookup"><span data-stu-id="a028d-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="a028d-147">翻译</span><span class="sxs-lookup"><span data-stu-id="a028d-147">Translations</span></span>

<span data-ttu-id="a028d-148">在**文本翻译**页，可为所选财务维度输入不同语言的文本。</span><span class="sxs-lookup"><span data-stu-id="a028d-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="a028d-149">在**主科目翻译**页，可为主科目输入不同语言的文本。</span><span class="sxs-lookup"><span data-stu-id="a028d-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="a028d-150">法人覆盖</span><span class="sxs-lookup"><span data-stu-id="a028d-150">Legal entity overrides</span></span>

<span data-ttu-id="a028d-151">并非所有的维度都对所有法人有效。</span><span class="sxs-lookup"><span data-stu-id="a028d-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="a028d-152">此外，某些维度可能仅针对特定的期间有关。</span><span class="sxs-lookup"><span data-stu-id="a028d-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="a028d-153">在这些情况下，您可以使用**法人覆盖**部分指定将为其暂停维度的公司、所有者以及维度有效的期间。</span><span class="sxs-lookup"><span data-stu-id="a028d-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="a028d-154">删除财务维度</span><span class="sxs-lookup"><span data-stu-id="a028d-154">Deleting financial dimensions</span></span>

<span data-ttu-id="a028d-155">为了帮助维护数据的引用完整性，很少删除财务维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="a028d-156">如果要删除财务维度，则评估以下条件：</span><span class="sxs-lookup"><span data-stu-id="a028d-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="a028d-157">财务维度是否在已过帐或未过帐的交易记录或任何类型的维度值组合上使用？</span><span class="sxs-lookup"><span data-stu-id="a028d-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="a028d-158">财务维度是否在任何活动的科目结构、高级规则结构或财务维度集中使用？</span><span class="sxs-lookup"><span data-stu-id="a028d-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="a028d-159">财务维度是否是默认维度集成格式的一部分？</span><span class="sxs-lookup"><span data-stu-id="a028d-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="a028d-160">财务维度是否已设置为默认维度？</span><span class="sxs-lookup"><span data-stu-id="a028d-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="a028d-161">如果满足任何条件，则不能删除财务维度。</span><span class="sxs-lookup"><span data-stu-id="a028d-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="a028d-162">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="a028d-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="a028d-163">定义财务维度</span><span class="sxs-lookup"><span data-stu-id="a028d-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="a028d-164">维护财务维度默认模板</span><span class="sxs-lookup"><span data-stu-id="a028d-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

