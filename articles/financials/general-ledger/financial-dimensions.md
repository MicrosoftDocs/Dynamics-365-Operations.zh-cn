---
title: "财务维度"
description: "本主题介绍财务维度的不同类型以及如何设置。"
author: aprilolson
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: 9973d03de031ad2fa5647bb167c12b9231633a22
ms.contentlocale: zh-cn
ms.lasthandoff: 10/01/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="c23e1-103">财务维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-103">Financial dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c23e1-104">本主题说明财务维度的不同类型以及如何设置。</span><span class="sxs-lookup"><span data-stu-id="c23e1-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="c23e1-105">使用**财务维度**页可创建可用作会计科目表的科目段的财务维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="c23e1-106">有两类财务维度：自定义维度和实体支持的维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="c23e1-107">自定义维度在法人之间共享，并且值由用户输入和维护。</span><span class="sxs-lookup"><span data-stu-id="c23e1-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="c23e1-108">对于实体支持的维度，其值在系统的其他地方进行定义，如客户或商店实体中。</span><span class="sxs-lookup"><span data-stu-id="c23e1-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as in Customers or Stores entities.</span></span> <span data-ttu-id="c23e1-109">有些实体支持的维度在法人间共享，而有些实体支持的维度则特定于公司。</span><span class="sxs-lookup"><span data-stu-id="c23e1-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span>

<span data-ttu-id="c23e1-110">在您创建了财务维度之后，使用**财务维度值**页给每个财务维度分配附加属性。</span><span class="sxs-lookup"><span data-stu-id="c23e1-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span>

<span data-ttu-id="c23e1-111">您可以使用财务维度代表法人。</span><span class="sxs-lookup"><span data-stu-id="c23e1-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="c23e1-112">您不必在 Microsoft Dynamics 365 for Finance and Operations 中创建实体。</span><span class="sxs-lookup"><span data-stu-id="c23e1-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c23e1-113">但是，财务维度不用来解决法人的运营或业务需求。</span><span class="sxs-lookup"><span data-stu-id="c23e1-113">However, financial dimensions aren't designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="c23e1-114">将 Finance and Operations 中的单位间核算功能设计成仅满足由每个交易记录所创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="c23e1-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span>

<span data-ttu-id="c23e1-115">在将财务维度设置为法人之前，评估您的业务流程中的以下区域以确定此设置是否适用于您的组织：</span><span class="sxs-lookup"><span data-stu-id="c23e1-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="c23e1-116">库存</span><span class="sxs-lookup"><span data-stu-id="c23e1-116">Inventory</span></span>
- <span data-ttu-id="c23e1-117">财务维度和法人之间的销售和采购</span><span class="sxs-lookup"><span data-stu-id="c23e1-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="c23e1-118">计算和申报销售税</span><span class="sxs-lookup"><span data-stu-id="c23e1-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="c23e1-119">操作报告</span><span class="sxs-lookup"><span data-stu-id="c23e1-119">Operational reporting</span></span>

<span data-ttu-id="c23e1-120">这是一些限制：</span><span class="sxs-lookup"><span data-stu-id="c23e1-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="c23e1-121">您只可以以法人身份使用销售纳税仅功能，但是不可以凭财务维度使用此功能。</span><span class="sxs-lookup"><span data-stu-id="c23e1-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="c23e1-122">有些报表不包括财务维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="c23e1-123">因此，要按财务维度进行报告，您可能必须修改报表。</span><span class="sxs-lookup"><span data-stu-id="c23e1-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="c23e1-124">自定义维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-124">Custom dimensions</span></span>

<span data-ttu-id="c23e1-125">若要创建用户定义的财务维度，在**使用以下来源中的值**字段中，选择 **&lt;&nbsp;自定义维度&nbsp;&gt;**。</span><span class="sxs-lookup"><span data-stu-id="c23e1-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt;&nbsp;Custom dimension&nbsp;&gt;**.</span></span>

<span data-ttu-id="c23e1-126">您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。</span><span class="sxs-lookup"><span data-stu-id="c23e1-126">You can also specify an account mask to limit the amount and type of information that can be entered for dimension values.</span></span> <span data-ttu-id="c23e1-127">您可以输入保持不变的每个维度值的信息，例如字母或连字符 (-)。</span><span class="sxs-lookup"><span data-stu-id="c23e1-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="c23e1-128">还可以输入数字标志 (\#) 和和符号 (&) 作为每次要更改的字符的占位符创建维度值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-128">You can also enter number signs (\#) and ampersands (&) as placeholders for characters that will change every time that a dimension value is created.</span></span> <span data-ttu-id="c23e1-129">使用一个数字标志 (\#) 作为编号占位符和符号 (&) 作为信函的占位符。</span><span class="sxs-lookup"><span data-stu-id="c23e1-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="c23e1-130">只有在**使用以下来源中的值**字段中选择 **&lt;&nbsp;自定义维度**&nbsp;&gt; 后，用于格式掩码的字段才可用。</span><span class="sxs-lookup"><span data-stu-id="c23e1-130">The field for the format mask is available only when you select **&lt;&nbsp;Custom dimension&nbsp;&gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="c23e1-131">**示例**</span><span class="sxs-lookup"><span data-stu-id="c23e1-131">**Example**</span></span>

<span data-ttu-id="c23e1-132">若要限制维度值到“CC”和三个数字，输入 **CC-\#\#\#** 作为格式掩码。</span><span class="sxs-lookup"><span data-stu-id="c23e1-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="c23e1-133">实体支持的维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-133">Entity-backed dimensions</span></span>

<span data-ttu-id="c23e1-134">若要创建实体支持的财务维度，在**使用以下来源中的值**字段中，选择财务维度所基于的系统定义的实体。</span><span class="sxs-lookup"><span data-stu-id="c23e1-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="c23e1-135">随后将从此实体创建财务维度值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="c23e1-136">例如，要为项目创建维度值，请选择**项目**。</span><span class="sxs-lookup"><span data-stu-id="c23e1-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="c23e1-137">将为每个项目名称将创建维度值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="c23e1-138">**财务维度值**页显示实体的值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="c23e1-139">如果这些值是公司特定的，则页面上还显示公司。</span><span class="sxs-lookup"><span data-stu-id="c23e1-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="c23e1-140">激活维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-140">Activating dimensions</span></span>

<span data-ttu-id="c23e1-141">在您启用财务维度时，表进行更新，使其包含财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="c23e1-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="c23e1-142">删除被移除的维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="c23e1-143">启用财务维度前，您可以输入维度值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="c23e1-144">不过，在启用财务维度前，无法在任何地方使用财务维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="c23e1-145">例如，到启用财务维度以前，您不能将财务维度添加到科目结构。</span><span class="sxs-lookup"><span data-stu-id="c23e1-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="c23e1-146">在您选择**启用**后，所有维度更新并显示状态更改。</span><span class="sxs-lookup"><span data-stu-id="c23e1-146">When you select **Activate**, all dimensions are updated and show status changes.</span></span>

## <a name="translations"></a><span data-ttu-id="c23e1-147">翻译</span><span class="sxs-lookup"><span data-stu-id="c23e1-147">Translations</span></span>

<span data-ttu-id="c23e1-148">在**文本翻译**页，可为所选财务维度输入不同语言的文本。</span><span class="sxs-lookup"><span data-stu-id="c23e1-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="c23e1-149">在**主科目翻译**页，可为主科目输入不同语言的文本。</span><span class="sxs-lookup"><span data-stu-id="c23e1-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="c23e1-150">法人覆盖</span><span class="sxs-lookup"><span data-stu-id="c23e1-150">Legal entity overrides</span></span>

<span data-ttu-id="c23e1-151">并非所有的维度都对所有法人有效。</span><span class="sxs-lookup"><span data-stu-id="c23e1-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="c23e1-152">此外，某些维度可能仅针对特定的期间有关。</span><span class="sxs-lookup"><span data-stu-id="c23e1-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="c23e1-153">在这些情况下，您可以使用**法人覆盖**部分指定将为其暂停维度的公司、所有者以及维度有效的期间。</span><span class="sxs-lookup"><span data-stu-id="c23e1-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="c23e1-154">删除财务维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-154">Deleting financial dimensions</span></span>

<span data-ttu-id="c23e1-155">为了帮助维护数据的引用完整性，很少删除财务维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="c23e1-156">如果要删除财务维度，则评估以下条件：</span><span class="sxs-lookup"><span data-stu-id="c23e1-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="c23e1-157">财务维度是否在已过帐或未过帐的交易记录上或任何类型的维度值组合中使用？</span><span class="sxs-lookup"><span data-stu-id="c23e1-157">Has the financial dimension been used on any posted or unposted transactions, or in any type of dimension value combination?</span></span>
- <span data-ttu-id="c23e1-158">财务维度是否在任何活动的科目结构、高级规则结构或财务维度集中使用？</span><span class="sxs-lookup"><span data-stu-id="c23e1-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="c23e1-159">财务维度是否是默认维度集成格式的一部分？</span><span class="sxs-lookup"><span data-stu-id="c23e1-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="c23e1-160">财务维度是否已设置为默认维度？</span><span class="sxs-lookup"><span data-stu-id="c23e1-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="c23e1-161">如果满足任何条件，则不能删除财务维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>

## <a name="default-dimension-values"></a><span data-ttu-id="c23e1-162">默认维度值</span><span class="sxs-lookup"><span data-stu-id="c23e1-162">Default dimension values</span></span>

<span data-ttu-id="c23e1-163">可将主记录（如客户和供应商）中的值用作新维度中的缺省值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-163">You can use values from master records, such as customer and vendor, as default values in new dimensions.</span></span> <span data-ttu-id="c23e1-164">创建新维度时，将在这些主记录的维度值中输入主记录 ID。</span><span class="sxs-lookup"><span data-stu-id="c23e1-164">When the new dimensions are created, the master record ID is entered in the dimension values for those master records.</span></span> <span data-ttu-id="c23e1-165">例如，创建新客户时，将在客户维度中输入客户 ID。</span><span class="sxs-lookup"><span data-stu-id="c23e1-165">For example, when you create a new customer, the customer ID is entered in the customer dimension.</span></span> <span data-ttu-id="c23e1-166">创建销售订单、发票或其他需要客户 ID 的单据时，将使用现有缺省规则，并将客户 ID 添加到单据中。</span><span class="sxs-lookup"><span data-stu-id="c23e1-166">When you create sales orders, invoices, or other documents that require a customer ID, the existing defaulting rules are used, and the customer ID is added to the document.</span></span>

<span data-ttu-id="c23e1-167">此功能由维度中的设置控制。</span><span class="sxs-lookup"><span data-stu-id="c23e1-167">This feature is controlled by a setting in the dimension.</span></span> <span data-ttu-id="c23e1-168">此设置的名称为**在创建的每个新 DimensionName 上将值复制到此维度**，其中 **DimensionName** 是维度的名称。</span><span class="sxs-lookup"><span data-stu-id="c23e1-168">This setting is named **Copy values to this dimension on each new DimensionName created**, where **DimensionName** is the name of the dimension.</span></span> <span data-ttu-id="c23e1-169">默认情况下，已关闭此功能。</span><span class="sxs-lookup"><span data-stu-id="c23e1-169">By default, the feature is turned off.</span></span> <span data-ttu-id="c23e1-170">但是，随时可以打开。</span><span class="sxs-lookup"><span data-stu-id="c23e1-170">However, it can be turned on at any time.</span></span>

<span data-ttu-id="c23e1-171">如果维度已经有记录，打开此功能时，将更新主记录。</span><span class="sxs-lookup"><span data-stu-id="c23e1-171">If records already exist for the dimension, the master records are updated when you turn the feature on.</span></span> <span data-ttu-id="c23e1-172">但是，不更新现有单据和交易记录。</span><span class="sxs-lookup"><span data-stu-id="c23e1-172">However, existing documents and transactions aren't updated.</span></span>

## <a name="derived-dimensions"></a><span data-ttu-id="c23e1-173">派生的维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-173">Derived dimensions</span></span>

<span data-ttu-id="c23e1-174">可配置维度，以便在单据中输入该维度时自动输入其他维度的信息。</span><span class="sxs-lookup"><span data-stu-id="c23e1-174">You can configure a dimension so that information for other dimensions is automatically entered when you enter that dimension in a document.</span></span> <span data-ttu-id="c23e1-175">例如，如果输入成本中心 10，可能在部门维度中自动输入值 **20**。</span><span class="sxs-lookup"><span data-stu-id="c23e1-175">For example, if you enter cost center 10, a value of **20** can be automatically entered in the department dimension.</span></span>

<span data-ttu-id="c23e1-176">可以在维度页中设置派生值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-176">You can set up derived values on the dimensions page.</span></span>

1. <span data-ttu-id="c23e1-177">选择维度，然后选择**派生维度**。</span><span class="sxs-lookup"><span data-stu-id="c23e1-177">Select a dimension and then select **Derived dimensions**.</span></span>

    <span data-ttu-id="c23e1-178">**派生维度**页中有一个网格。</span><span class="sxs-lookup"><span data-stu-id="c23e1-178">The **Derived dimensions** page includes a grid.</span></span> <span data-ttu-id="c23e1-179">所选维度部分是该网格中的第一个列。</span><span class="sxs-lookup"><span data-stu-id="c23e1-179">The selected dimension segment is the first column in this grid.</span></span>

2. <span data-ttu-id="c23e1-180">添加应派生的段。</span><span class="sxs-lookup"><span data-stu-id="c23e1-180">Add the segments that should be derived.</span></span> <span data-ttu-id="c23e1-181">每段显示为一列。</span><span class="sxs-lookup"><span data-stu-id="c23e1-181">Each segment appears as a column.</span></span>

<span data-ttu-id="c23e1-182">在第一列中输入应从维度派生的维度组合。</span><span class="sxs-lookup"><span data-stu-id="c23e1-182">Enter the dimension combinations that should be derived from the dimension in the first column.</span></span> <span data-ttu-id="c23e1-183">例如，要将成本中心用作部门和库位的派生来源，请输入成本中心 10，部门 20 和库位 30。</span><span class="sxs-lookup"><span data-stu-id="c23e1-183">For example, to use the cost center as the dimension that the department and location are derived from, enter cost center 10, department 20, and location 30.</span></span> <span data-ttu-id="c23e1-184">然后，在主记录中或交易记录页上输入成本中心 10 时，将缺省输入部门 20 和库位 30。</span><span class="sxs-lookup"><span data-stu-id="c23e1-184">Then, when you enter cost center 10 in a master record or on a transaction page, department 20 and location 30 are entered by default.</span></span>

<span data-ttu-id="c23e1-185">派生维度过程不会覆盖派生维度的现有值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-185">The derived dimension process doesn't override existing values for derived dimensions.</span></span> <span data-ttu-id="c23e1-186">例如，如果输入成本中心 10，但不输入其他任何维度，将缺省输入部门 20 和库位 30。</span><span class="sxs-lookup"><span data-stu-id="c23e1-186">For example, if you enter cost center 10, and no other dimension is entered, department 20 and location 30 are entered by default.</span></span> <span data-ttu-id="c23e1-187">但是，如果更改成本中心，将不更改已建立的值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-187">However, if you change the cost center, the values that have already been established aren't changed.</span></span> <span data-ttu-id="c23e1-188">因此，可基于主记录建立缺省维度，而派生维度不会更改这些维度。</span><span class="sxs-lookup"><span data-stu-id="c23e1-188">Therefore, you can establish default dimensions on master records, and those dimensions won't be changed by derived dimensions.</span></span>

### <a name="derived-dimensions-and-entities"></a><span data-ttu-id="c23e1-189">派生维度和实体</span><span class="sxs-lookup"><span data-stu-id="c23e1-189">Derived dimensions and entities</span></span>

<span data-ttu-id="c23e1-190">可通过使用实体设置派生维度段和值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-190">You can set up the derived dimensions segments and values by using entities.</span></span>

- <span data-ttu-id="c23e1-191">派生维度实体设置驱动维度和用于这些维度的段。</span><span class="sxs-lookup"><span data-stu-id="c23e1-191">The Derived dimensions entity sets up the driving dimensions and the segments that are used for those dimensions.</span></span>
- <span data-ttu-id="c23e1-192">可通过 DerivedDimensionValue 实体导入应该为每个驱动维度派生的值。</span><span class="sxs-lookup"><span data-stu-id="c23e1-192">The DerivedDimensionValue entity lets you import the values that should be derived for each driving dimension.</span></span>

<span data-ttu-id="c23e1-193">使用实体导入数据时，如果该实体导入维度，则除非实体特意覆盖这些维度，否则导入期间将应用派生维度规则。</span><span class="sxs-lookup"><span data-stu-id="c23e1-193">When you use an entity to import data, if that entity imports dimensions, the derived dimension rules are applied during the import unless the entity specifically overrides those dimensions.</span></span>

<span data-ttu-id="c23e1-194">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c23e1-194">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c23e1-195">定义财务维度</span><span class="sxs-lookup"><span data-stu-id="c23e1-195">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="c23e1-196">维护财务维度默认模板</span><span class="sxs-lookup"><span data-stu-id="c23e1-196">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

