---
title: 规划组织层次结构
description: 设置组织和组织层次结构之前，请确保了解如何以最好的方式为业务建模。
author: sericks007
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec071844f09caca1c83ff35a75b26922c6185c5b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747577"
---
# <a name="plan-your-organizational-hierarchy"></a><span data-ttu-id="ce556-103">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="ce556-103">Plan your organizational hierarchy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce556-104">在设置组织和组织层次结构之前，请确保您已计划好您的业务将如何建模。</span><span class="sxs-lookup"><span data-stu-id="ce556-104">Before you set up organizations and organization hierarchies, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="ce556-105">组织模型对实施和业务流程有重大影响。</span><span class="sxs-lookup"><span data-stu-id="ce556-105">The organization model has a significant effect on the implementation and business processes.</span></span>

<span data-ttu-id="ce556-106">组织层次结构表示构成业务的组织之间的关系。</span><span class="sxs-lookup"><span data-stu-id="ce556-106">Organizational hierarchies represent the relationships between the organizations that make up a business.</span></span> <span data-ttu-id="ce556-107">因此，在您建模组织时最重要的注意事项是您的业务结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-107">Therefore, the most important consideration when you model organizations is the structure of your business.</span></span> <span data-ttu-id="ce556-108">我们建议您基于高管和各功能区域（如财务和会计、人力资源、运营、采购、销售和市场）的高级经理的反馈来定义组织结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-108">We recommend that you define organization structures based on feedback from executives and senior managers from functional areas, such as finance and accounting, human resources, operations, purchasing, and sales and marketing.</span></span>

<span data-ttu-id="ce556-109">在您计划层次结构时，考虑组织层次结构和财务维度之间的关系也十分重要。</span><span class="sxs-lookup"><span data-stu-id="ce556-109">When you are planning hierarchies, it is also important to consider the relationship between the organizational hierarchy and financial dimensions.</span></span> <span data-ttu-id="ce556-110">您可以设置多个组织层次结构来表示您业务的不同视图。</span><span class="sxs-lookup"><span data-stu-id="ce556-110">You can set up multiple organizational hierarchies to represent different views of your business.</span></span> <span data-ttu-id="ce556-111">通过使用财务维度，您可以基于这些视图创建报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-111">By using financial dimensions, you can create reports based on these views.</span></span> <span data-ttu-id="ce556-112">与您的合作伙伴创建满足组织和法定申报需求的层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-112">Work with your partner to create hierarchies that address both organizational and statutory reporting needs.</span></span>

> [!NOTE]
> <span data-ttu-id="ce556-113">尽管您可以使用财务维度代表法人，而不创建法人，但财务维度并非设计用于满足法人的运营或业务需要。</span><span class="sxs-lookup"><span data-stu-id="ce556-113">Although you can use financial dimensions to represent legal entities without creating the legal entities, financial dimensions aren't designed to address the operational or business needs of legal entities.</span></span> <span data-ttu-id="ce556-114">将单位间核算功能设计成仅满足由每个交易记录创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="ce556-114">The interunit accounting functionality is designed to address only the accounting entries that are created by each transaction.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce556-115">您不应仅基于本文中的信息来确定如何建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-115">You shouldn't decide how to model organizations based only on the information in this article.</span></span> <span data-ttu-id="ce556-116">本文档仅作为一个参考指南。</span><span class="sxs-lookup"><span data-stu-id="ce556-116">This documentation is a guide.</span></span> <span data-ttu-id="ce556-117">您可以与您的合作伙伴共同制定附加指南。</span><span class="sxs-lookup"><span data-stu-id="ce556-117">You can work with your Partner for additional guidance.</span></span> <span data-ttu-id="ce556-118">您的合作伙伴具有在不同行业和客户中购置经验。</span><span class="sxs-lookup"><span data-stu-id="ce556-118">Your Partner has gained experience in various industries and across the customer base.</span></span>

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a><span data-ttu-id="ce556-119">确定是否以法人或运营单位建模内部组织</span><span class="sxs-lookup"><span data-stu-id="ce556-119">Decide whether to model internal organizations as legal entities or operating units</span></span>

<span data-ttu-id="ce556-120">您必须具有至少一个法人，以表示您的业务。</span><span class="sxs-lookup"><span data-stu-id="ce556-120">You must have at least one legal entity to represent your business.</span></span> <span data-ttu-id="ce556-121">法人可以输入法律合同，并需要准备报告其业绩的财务报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-121">A legal entity can enter legal contracts and is required to prepare financial statements that report on its performance.</span></span>

<span data-ttu-id="ce556-122">法人可用于交易业务或合并。</span><span class="sxs-lookup"><span data-stu-id="ce556-122">Legal entities can be used for transactional business or for consolidation.</span></span> <span data-ttu-id="ce556-123">这意味着在 Finance and Operations 中的法人不必代表您业务中的实际实体。</span><span class="sxs-lookup"><span data-stu-id="ce556-123">This means that a legal entity in Finance and Operations does not necessarily represent a real entity in your business.</span></span> <span data-ttu-id="ce556-124">例如，参与交易的公司可以拥有子公司法人。</span><span class="sxs-lookup"><span data-stu-id="ce556-124">For example, a company that participates in transactions can own subsidiary legal entities.</span></span> <span data-ttu-id="ce556-125">在这种情况下，交易需要法人，并且需要虚拟法人以合并子公司法人的结果和余额。</span><span class="sxs-lookup"><span data-stu-id="ce556-125">In this scenario, a legal entity is required for transactions, and a virtual legal entity is required to consolidate the results and balances of the subsidiary legal entities.</span></span>

<span data-ttu-id="ce556-126">您的业务中的内部组织，例如区域办公室，可以表示为附加的法人或者为主要法人的运营单位。</span><span class="sxs-lookup"><span data-stu-id="ce556-126">Internal organizations in your business, such as regional offices, can be represented as additional legal entities, or as operating units of the main legal entity.</span></span> <span data-ttu-id="ce556-127">运营单位不需要是法律上定义的组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-127">An operating unit is not required to be a legally defined organization.</span></span> <span data-ttu-id="ce556-128">运营单位用于控制业务中的经济资源和运营流程。</span><span class="sxs-lookup"><span data-stu-id="ce556-128">Operating units are used to control economic resources and operational processes in the business.</span></span> <span data-ttu-id="ce556-129">例如，部门和成本中心是运营单位。</span><span class="sxs-lookup"><span data-stu-id="ce556-129">For example, departments and cost centers are operating units.</span></span>

<span data-ttu-id="ce556-130">一些功能根据该组织是否为法人或运营单位而进行不同的工作。</span><span class="sxs-lookup"><span data-stu-id="ce556-130">Some functionality works differently depending on whether the organization is a legal entity or an operating unit.</span></span> <span data-ttu-id="ce556-131">在您做出决定时，请仔细考虑下述功能。</span><span class="sxs-lookup"><span data-stu-id="ce556-131">Carefully consider the functionality described below as you make your decision.</span></span>

### <a name="master-data"></a><span data-ttu-id="ce556-132">主数据</span><span class="sxs-lookup"><span data-stu-id="ce556-132">Master data</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-133">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-133">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-134">必须为每个法人设置一些主数据，如客户、付款期限、税务主管机构和特定站点的库存预留。</span><span class="sxs-lookup"><span data-stu-id="ce556-134">Some master data, such as customers, payment terms, tax authorities, and site-specific stock ordering, must be set up for each legal entity.</span></span> <span data-ttu-id="ce556-135">在所有法人中共享一些主数据，如用户、产品和大多数人力资源数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-135">Some master data, such as users, products, and most human resources data, is shared among all legal entities.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-136">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-136">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-137">在运营单位中共享主数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-137">Master data is shared among operating units.</span></span>

### <a name="module-parameters"></a><span data-ttu-id="ce556-138">模块参数</span><span class="sxs-lookup"><span data-stu-id="ce556-138">Module parameters</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-139">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-139">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-140">必须按照法人设置模块的参数，如应收帐款参数、应付帐款参数和现金和银行管理参数。</span><span class="sxs-lookup"><span data-stu-id="ce556-140">Parameters for modules, such as Accounts receivable parameters, Accounts payable parameters, and Cash and bank management parameters, must be set per legal entity.</span></span> <span data-ttu-id="ce556-141">由于法人的模块设置为单独的，每个子公司可以符合当地法律要求和商业惯例。</span><span class="sxs-lookup"><span data-stu-id="ce556-141">Because the module setup for legal entities is separate, each subsidiary can comply with local statutory requirements and business practices.</span></span> <span data-ttu-id="ce556-142">例如，专业服务法人和制造法人可以具有不同的模块参数，即使它们向同一个母公司报告。</span><span class="sxs-lookup"><span data-stu-id="ce556-142">For example, a professional services legal entity and a manufacturing legal entity can have different module parameters even though they report to the same parent company.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-143">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-143">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-144">在运营单位中共享模块参数。</span><span class="sxs-lookup"><span data-stu-id="ce556-144">Module parameters are shared among operating units.</span></span>

### <a name="data-security"></a><span data-ttu-id="ce556-145">数据安全</span><span class="sxs-lookup"><span data-stu-id="ce556-145">Data security</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-146">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-146">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-147">大多数数据通过公司 ID 自动保护。</span><span class="sxs-lookup"><span data-stu-id="ce556-147">Most data is automatically secured by company ID.</span></span> <span data-ttu-id="ce556-148">公司 ID 对于与法人关联的数据是唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="ce556-148">A company ID is a unique identifier for the data that is associated with a legal entity.</span></span> <span data-ttu-id="ce556-149">公司只可与一个法人关联，法人也只可与一个公司关联。</span><span class="sxs-lookup"><span data-stu-id="ce556-149">A company can be associated with only one legal entity, and a legal entity can be associated with only one company.</span></span> <span data-ttu-id="ce556-150">用户仅可以访问他们有权访问的公司数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-150">Users can access data only for the companies that they have access to.</span></span> <span data-ttu-id="ce556-151">您无需自定义来通过公司 ID 保护数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-151">You do not need to customize to secure data by company ID.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-152">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-152">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-153">可以通过创建自定义的数据安全策略按运营单位保护数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-153">Data can be secured per operating unit by creating customized data security policies.</span></span> <span data-ttu-id="ce556-154">数据安全策略用于限制对数据的访问。</span><span class="sxs-lookup"><span data-stu-id="ce556-154">Data security policies are used to limit access to data.</span></span> <span data-ttu-id="ce556-155">例如，假定只允许用户在特定运营单位创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="ce556-155">For example, assume that a user is allowed to create purchase orders only in a particular operating unit.</span></span> <span data-ttu-id="ce556-156">可以创建数据安全策略来防止用户从其他运营单位访问采购订单的数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-156">Data security policies can be created to prevent the user from accessing purchase order data from any other operating unit.</span></span> <span data-ttu-id="ce556-157">交易量和安全策略的数量会影响业绩。</span><span class="sxs-lookup"><span data-stu-id="ce556-157">The volume of transactions and the number of security policies can affect performance.</span></span> <span data-ttu-id="ce556-158">在您设计安全策略时，请考虑业绩。</span><span class="sxs-lookup"><span data-stu-id="ce556-158">When you design security policies, keep performance in mind.</span></span>

### <a name="ledgers"></a><span data-ttu-id="ce556-159">分类帐</span><span class="sxs-lookup"><span data-stu-id="ce556-159">Ledgers</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-160">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-160">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-161">每个法人需要分类帐来提供会计科目表、记帐币种、申报币种和会计日历。</span><span class="sxs-lookup"><span data-stu-id="ce556-161">Each legal entity requires a ledger that provides a chart of accounts, accounting currency, reporting currency, and fiscal calendar.</span></span> <span data-ttu-id="ce556-162">资产负债表可以仅为法人创建。</span><span class="sxs-lookup"><span data-stu-id="ce556-162">A balance sheet can be created only for a legal entity.</span></span> <span data-ttu-id="ce556-163">主科目、维度、科目结构、会计科目表和会计准则可以由多个法人使用。</span><span class="sxs-lookup"><span data-stu-id="ce556-163">Main accounts, dimensions, account structures, charts of accounts, and account rules can be used by more than one legal entity.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-164">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-164">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-165">运营单位不能拥有自己的分类帐信息。</span><span class="sxs-lookup"><span data-stu-id="ce556-165">An operating unit can't have its own ledger information.</span></span> <span data-ttu-id="ce556-166">如果您的内部组织不需要唯一的分类帐，您可以以运营单位建模它们。</span><span class="sxs-lookup"><span data-stu-id="ce556-166">If your internal organizations do not require unique ledgers, you can model them as operating units.</span></span> <span data-ttu-id="ce556-167">将针对层次结构中的母法人设置分类帐信息。</span><span class="sxs-lookup"><span data-stu-id="ce556-167">Ledger information will be set up for the parent legal entity in the hierarchy.</span></span> <span data-ttu-id="ce556-168">可以针对法人中的运营单位或针对母法人创建损益表。</span><span class="sxs-lookup"><span data-stu-id="ce556-168">Income statements can be created for operating units within a legal entity or for the parent legal entity.</span></span>

### <a name="fiscal-calendars"></a><span data-ttu-id="ce556-169">会计日历</span><span class="sxs-lookup"><span data-stu-id="ce556-169">Fiscal calendars</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-170">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-170">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-171">每个法人拥有自己的会计日历。</span><span class="sxs-lookup"><span data-stu-id="ce556-171">Each legal entity has its own fiscal calendar.</span></span> <span data-ttu-id="ce556-172">如果您的内部组织使用不同的会计年度和会计日历，您必须以法人建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-172">If your internal organizations use different fiscal years and fiscal calendars, you must model the organizations as legal entities.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-173">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-173">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-174">运营单位必须共享会计日历。</span><span class="sxs-lookup"><span data-stu-id="ce556-174">Operating units must share a fiscal calendar.</span></span> <span data-ttu-id="ce556-175">如果您的内部组织可以使用相同的会计年度和会计日历，您可以以运营单位建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-175">If your internal organizations can use the same fiscal years and fiscal calendars, you can model the organizations as operating units.</span></span>

### <a name="consolidation"></a><span data-ttu-id="ce556-176">合并</span><span class="sxs-lookup"><span data-stu-id="ce556-176">Consolidation</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-177">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-177">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-178">您必须将区域办公室的财务结果合并入单个合并的公司中以便准备财务报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-178">You must consolidate the financial results for regional offices into a single, consolidated company in order to prepare financial statements.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-179">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-179">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-180">不要求合并，因为在运营单位中已共享数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-180">Consolidation is not required, because data is already shared among operating units.</span></span>

### <a name="centralized-payments"></a><span data-ttu-id="ce556-181">集中付款</span><span class="sxs-lookup"><span data-stu-id="ce556-181">Centralized payments</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-182">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-182">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-183">必须设置集中付款，以便所有子法人的发票可以支付给单个母法人或自单个母法人支付。</span><span class="sxs-lookup"><span data-stu-id="ce556-183">Centralized payments must be set up so that invoices for all child legal entities can be paid to or from a single parent legal entity.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-184">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-184">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-185">不要求集中付款，因为所有发票在单个法人中记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-185">Centralized payments are not required because all invoices are recorded in a single legal entity.</span></span>

### <a name="intercompany-transactions"></a><span data-ttu-id="ce556-186">内部公司事务</span><span class="sxs-lookup"><span data-stu-id="ce556-186">Intercompany transactions</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-187">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-187">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-188">内部公司销售订单、采购订单、付款或收货可以应用于彼此。</span><span class="sxs-lookup"><span data-stu-id="ce556-188">Intercompany sales orders, purchase orders, payments, or receipts can be applied to one another.</span></span> <span data-ttu-id="ce556-189">您无需使用日记帐凭证。</span><span class="sxs-lookup"><span data-stu-id="ce556-189">You are not required to use journal vouchers.</span></span> <span data-ttu-id="ce556-190">您可以在子级别分类帐（应收帐款、应付帐款）中查看内部公司交易记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-190">You can view intercompany transactions at the sub-ledger level (Accounts receivable, Accounts payable).</span></span> <span data-ttu-id="ce556-191">以下示例说明了如何处理内部公司交易记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-191">The following examples illustrate how intercompany transactions are handled.</span></span>

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a><span data-ttu-id="ce556-192">示例 1：总部对区域办公室提供服务且必须将那些服务的成本记于区域办公室的帐目上</span><span class="sxs-lookup"><span data-stu-id="ce556-192">Example 1: Headquarters provides services to regional offices and must charge the costs of those services to the regional offices</span></span>

<span data-ttu-id="ce556-193">如果您以法人建模区域办公室，您具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="ce556-193">If you model the regional office as a legal entity, you have the following options:</span></span>

- <span data-ttu-id="ce556-194">总部创建日记帐条目以交叉记录区域办公室的费用。</span><span class="sxs-lookup"><span data-stu-id="ce556-194">Headquarters creates a journal entry to cross-charge the regional office for the expense.</span></span> <span data-ttu-id="ce556-195">不能计算交易记录的帐龄。</span><span class="sxs-lookup"><span data-stu-id="ce556-195">The transactions cannot be aged.</span></span>
- <span data-ttu-id="ce556-196">总部将服务的采购订单发送到区域办公室。</span><span class="sxs-lookup"><span data-stu-id="ce556-196">Headquarters sends a purchase order for the services to the regional office.</span></span> <span data-ttu-id="ce556-197">与内部公司的子分类帐交易记录一起，在区域办公室的法人中自动创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="ce556-197">A sales order is automatically created in the legal entity for the regional office, with intercompany sub-ledger transactions.</span></span>

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a><span data-ttu-id="ce556-198">示例 2：总部采购和支付交付至区域办公室的服务</span><span class="sxs-lookup"><span data-stu-id="ce556-198">Example 2: Headquarters procures and pays for service that is delivered to a regional office</span></span>

<span data-ttu-id="ce556-199">如果您以法人建模区域办公室，您具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="ce556-199">If you model the regional office as a legal entity, you have the following options:</span></span>

- <span data-ttu-id="ce556-200">发票和付款遵循总部的管理要求。</span><span class="sxs-lookup"><span data-stu-id="ce556-200">The invoice and payment follow the regulatory requirements of headquarters.</span></span> <span data-ttu-id="ce556-201">总部可以创建日记帐条目以交叉记录区域办公室的费用。</span><span class="sxs-lookup"><span data-stu-id="ce556-201">Headquarters can create a journal entry to cross-charge the regional office for the expense.</span></span> <span data-ttu-id="ce556-202">不能计算交易记录的帐龄。</span><span class="sxs-lookup"><span data-stu-id="ce556-202">The transactions cannot be aged.</span></span>
- <span data-ttu-id="ce556-203">发票和付款遵循总部的管理要求。</span><span class="sxs-lookup"><span data-stu-id="ce556-203">The invoice and payment follow the regulatory requirements of headquarters.</span></span> <span data-ttu-id="ce556-204">总部可以创建内部公司的子分类帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-204">Headquarters can create an intercompany sub-ledger transaction.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-205">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-205">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-206">在运营单位中的内部公司交易记录仅通过日记帐凭证支持。</span><span class="sxs-lookup"><span data-stu-id="ce556-206">Intercompany transactions among operating units are supported only through journal vouchers.</span></span> <span data-ttu-id="ce556-207">运营单位不能从同一法人中的另一个运营单位签发或接收采购订单、销售订单或发票。</span><span class="sxs-lookup"><span data-stu-id="ce556-207">An operating unit cannot issue or receive a purchase order, sales order, or invoice from another operating unit in the same legal entity.</span></span> <span data-ttu-id="ce556-208">您不能在子级别分类帐（应收帐款、应付帐款）中查看内部公司交易记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-208">You cannot view intercompany transactions at the sub-ledger level (Accounts receivable, Accounts payable).</span></span> <span data-ttu-id="ce556-209">以下示例说明了如何处理内部公司交易记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-209">The following examples illustrate how intercompany transactions are handled.</span></span>

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a><span data-ttu-id="ce556-210">示例 1：总部对区域办公室提供服务且必须将那些服务的成本记于区域办公室的帐目上</span><span class="sxs-lookup"><span data-stu-id="ce556-210">Example 1: Headquarters provides services to regional offices and must charge the costs of those services to the regional offices</span></span>

<span data-ttu-id="ce556-211">如果您以运营单位建模区域办公室，则总部输入费用交易记录并将它编码至区域办公室。</span><span class="sxs-lookup"><span data-stu-id="ce556-211">If you model the regional office as an operating unit, headquarters enters an expense transaction and codes it to the regional office.</span></span>

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a><span data-ttu-id="ce556-212">示例 2：总部采购和支付交付至区域办公室的服务</span><span class="sxs-lookup"><span data-stu-id="ce556-212">Example 2: Headquarters procures and pays for service that is delivered to a regional office</span></span>

<span data-ttu-id="ce556-213">如果您以运营单位建模区域办公室，则发票和付款遵循总部的管理要求。</span><span class="sxs-lookup"><span data-stu-id="ce556-213">If you model the regional office as an operating unit, the invoice and payment follow the regulatory requirements of headquarters.</span></span> <span data-ttu-id="ce556-214">可以将发票编码至区域办公室。</span><span class="sxs-lookup"><span data-stu-id="ce556-214">The invoice can be coded to the regional office.</span></span> <span data-ttu-id="ce556-215">在损益表中，请使用平衡的财务维度以报告区域办公室的成本。</span><span class="sxs-lookup"><span data-stu-id="ce556-215">On the income statement, use a balancing financial dimension to report costs for the regional office.</span></span>

### <a name="local-tax-requirements"></a><span data-ttu-id="ce556-216">本地纳税要求</span><span class="sxs-lookup"><span data-stu-id="ce556-216">Local tax requirements</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-217">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-217">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-218">法人将遵循该法人所登记国家/地区的税务主管机构的税法。</span><span class="sxs-lookup"><span data-stu-id="ce556-218">A legal entity is subject to the tax laws of the tax authority in the country/region where the legal entity is registered.</span></span> <span data-ttu-id="ce556-219">例如，在丹麦登记的法人需要遵循丹麦的税务法律和法规。</span><span class="sxs-lookup"><span data-stu-id="ce556-219">For example, a legal entity that is registered in Denmark is subject to Danish tax laws and regulations.</span></span> <span data-ttu-id="ce556-220">法人仅可以属于一个国家/地区。</span><span class="sxs-lookup"><span data-stu-id="ce556-220">A legal entity can belong to only one country/region.</span></span> <span data-ttu-id="ce556-221">您为法人的主要地址选择的国家/地区将控制该法人可用的特定于国家/地区的功能。</span><span class="sxs-lookup"><span data-stu-id="ce556-221">The country/region that you select for the primary address of the legal entity controls the country/region-specific features that are available to that legal entity.</span></span> <span data-ttu-id="ce556-222">例如，如果法人的主要地址位于丹麦，则与丹麦税务法律和法规相关的功能变得可用。</span><span class="sxs-lookup"><span data-stu-id="ce556-222">For example, if the primary address of the legal entity is in Denmark, features that are related to Danish tax laws and regulations become available.</span></span> <span data-ttu-id="ce556-223">因此，如果您的组织位于不同的国家/地区且要求不同的本地税务选项，则必须以单独的法人设置该组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-223">Therefore, if your organizations are in different countries/regions and require different local tax options, you must set up the organizations as separate legal entities.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-224">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-224">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-225">运营单位使用母法人的国家/地区环境。</span><span class="sxs-lookup"><span data-stu-id="ce556-225">Operating units use the country context of the parent legal entity.</span></span> <span data-ttu-id="ce556-226">在同一法人中的运营单位不能具有不同的特定于国家/地区的要求。</span><span class="sxs-lookup"><span data-stu-id="ce556-226">Operating units in the same legal entity cannot have different country/region-specific requirements.</span></span> <span data-ttu-id="ce556-227">如果您的组织在同一个国家/地区且使用相同的税务选项，您可以以运营单位进行设置。</span><span class="sxs-lookup"><span data-stu-id="ce556-227">If your organizations are in the same country/region and use the same tax options, you can set them up as operating units.</span></span>

### <a name="statutory-reporting-for-a-countryregion"></a><span data-ttu-id="ce556-228">国家/地区的法定报表</span><span class="sxs-lookup"><span data-stu-id="ce556-228">Statutory reporting for a country/region</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-229">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-229">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-230">对于支持的国家/地区，可以创建大多数法定报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-230">For countries/regions that are supported, most statutory reports can be created.</span></span> 

> [!NOTE]
> <span data-ttu-id="ce556-231">总帐中的过帐层允许您对母公司进行条目调整，这里与子公司相比使用了不同的会计标准。</span><span class="sxs-lookup"><span data-stu-id="ce556-231">A posting layer in the general ledger allows you to make adjusting entries to a parent company that uses a different accounting standard than the child company.</span></span> <span data-ttu-id="ce556-232">例如，对于使用英国通用会计制度 (UK GAAP) 的公司，您可以在过帐层中进行条目调整。</span><span class="sxs-lookup"><span data-stu-id="ce556-232">For example, for a company that uses generally accepted accounting practices in the United Kingdom (UK GAAP), you can make adjusting entries in the posting layer.</span></span> <span data-ttu-id="ce556-233">这些条目可以合并入使用美国通用会计制度 (GAAP) 的母公司。</span><span class="sxs-lookup"><span data-stu-id="ce556-233">These entries can be consolidated into a parent company that uses generally accepted accounting principles (GAAP) in the United States.</span></span> <span data-ttu-id="ce556-234">调整条目不影响英国 GAAP 报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-234">The adjusting entries do not affect UK GAAP reporting.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-235">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-235">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-236">必须通过使用另一个申请创建法定报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-236">Statutory reports must be created by using another application.</span></span> <span data-ttu-id="ce556-237">您必须确保在 Finance and Operations 应用中获得数据，以支持每个运营单位的需求，此处它们与总部的需求不同。</span><span class="sxs-lookup"><span data-stu-id="ce556-237">You must ensure that data is captured in Finance and Operations apps to support the requirements of each operating unit, where they differ from the requirements of headquarters.</span></span>

### <a name="currency"></a><span data-ttu-id="ce556-238">货币</span><span class="sxs-lookup"><span data-stu-id="ce556-238">Currency</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-239">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-239">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-240">如果您的组织必须使用不同功能币种，则必须以法人建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-240">If your organizations must use different functional currencies, you must model the organizations as legal entities.</span></span> <span data-ttu-id="ce556-241">针对每个法人设置功能币种。</span><span class="sxs-lookup"><span data-stu-id="ce556-241">Functional currencies are set up per legal entity.</span></span> <span data-ttu-id="ce556-242">不过，您可以以多个币种输入交易记录。</span><span class="sxs-lookup"><span data-stu-id="ce556-242">However, you can enter transactions in multiple currencies.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-243">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-243">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-244">如果您的组织可以使用单个功能币种，您可以以运营单位建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-244">If your organizations can use a single functional currency, you can model the organizations as operating units.</span></span> <span data-ttu-id="ce556-245">运营单位必须共享一种功能币种。</span><span class="sxs-lookup"><span data-stu-id="ce556-245">Operating units must share a functional currency.</span></span> <span data-ttu-id="ce556-246">但是，您可以输入交易记录并以多个币种创建报表。</span><span class="sxs-lookup"><span data-stu-id="ce556-246">However, you can enter transactions and create reports in multiple currencies.</span></span>

### <a name="year-end-closing"></a><span data-ttu-id="ce556-247">年终结算</span><span class="sxs-lookup"><span data-stu-id="ce556-247">Year-end closing</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-248">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-248">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-249">如果法律和会计准则在您的组织所在国家/地区中存在不同，那么对于每个组织您可能需要采用不同的年终结算过程。</span><span class="sxs-lookup"><span data-stu-id="ce556-249">If laws and accounting practices differ among the countries/regions where your organizations are located, you may require different year-end procedures per organization.</span></span> <span data-ttu-id="ce556-250">这意味着您必须以法人建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-250">This means that you must model the organizations as legal entities.</span></span> <span data-ttu-id="ce556-251">每个法人具有自己的年终结算过程。</span><span class="sxs-lookup"><span data-stu-id="ce556-251">Each legal entity has its own year-end procedures.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-252">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-252">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-253">如果法律和会计准则在您的组织所在的国家/地区中相同，您可能使用单个集的年终结算过程。</span><span class="sxs-lookup"><span data-stu-id="ce556-253">If laws and accounting practices are the same among the countries/regions where your organizations are located, you may use a single set of year-end procedures.</span></span> <span data-ttu-id="ce556-254">这意味着您可以以运营单位建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-254">This means that you can model the organizations as operating units.</span></span> <span data-ttu-id="ce556-255">所有运营单位必须使用相同的年终结算过程。</span><span class="sxs-lookup"><span data-stu-id="ce556-255">All operating units must use the same year-end closing procedure.</span></span>

### <a name="number-sequences"></a><span data-ttu-id="ce556-256">编号规则</span><span class="sxs-lookup"><span data-stu-id="ce556-256">Number sequences</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-257">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-257">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-258">可以按法人设置一些参考的编号规则。</span><span class="sxs-lookup"><span data-stu-id="ce556-258">Number sequences for some references can be set up per legal entity.</span></span> <span data-ttu-id="ce556-259">可以共享一些编号规则。</span><span class="sxs-lookup"><span data-stu-id="ce556-259">Some number sequences can be shared.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-260">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-260">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-261">可以按运营单位设置一些参考的编号规则。</span><span class="sxs-lookup"><span data-stu-id="ce556-261">Number sequences for some references can be set up per operating unit.</span></span> <span data-ttu-id="ce556-262">可以共享一些编号规则。</span><span class="sxs-lookup"><span data-stu-id="ce556-262">Some number sequences can be shared.</span></span>

### <a name="products"></a><span data-ttu-id="ce556-263">产品</span><span class="sxs-lookup"><span data-stu-id="ce556-263">Products</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-264">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-264">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-265">共享产品定义，且必须将其发布至各个法人只后它们才可以包含在交易记录中。</span><span class="sxs-lookup"><span data-stu-id="ce556-265">Product definitions are shared, and they must be released to individual legal entities before they can be included in transactions.</span></span> <span data-ttu-id="ce556-266">每个交易记录具有自己的已发布产品集，它们可包含于交易记录文档中。</span><span class="sxs-lookup"><span data-stu-id="ce556-266">Each legal entity has its own set of released products that can be included in transaction documents.</span></span> <span data-ttu-id="ce556-267">如果您的组织必须使用不同产品集，则必须以法人建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-267">If your internal organizations must use different sets of products, you must model the organizations as legal entities.</span></span>

> [!NOTE]
> <span data-ttu-id="ce556-268">即使共享产品定义，在已发布产品的每个法人中，您可以为每个库存站点的物料指定不同的销售、采购和库存参数。</span><span class="sxs-lookup"><span data-stu-id="ce556-268">Even though product definitions are shared, in each legal entity where a product has been released, you can specify different sales, purchase, and stocking parameters for the item at each inventory site.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-269">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-269">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-270">所有运营单位共享同一个产品集。</span><span class="sxs-lookup"><span data-stu-id="ce556-270">All operating units share the same set of products.</span></span> <span data-ttu-id="ce556-271">如果您的内部组织可以共享同一个产品集，您可以以运营单位建模组织。</span><span class="sxs-lookup"><span data-stu-id="ce556-271">If your internal organizations can share the same set of products, you can model the organizations as operating units.</span></span>

### <a name="inquiry-and-reporting"></a><span data-ttu-id="ce556-272">查询和报表</span><span class="sxs-lookup"><span data-stu-id="ce556-272">Inquiry and reporting</span></span>

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a><span data-ttu-id="ce556-273">如果以法人建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-273">If the organization is modeled as a legal entity</span></span>

<span data-ttu-id="ce556-274">您必须手动更改公司来输入交易记录及在多个法人中执行查询。</span><span class="sxs-lookup"><span data-stu-id="ce556-274">You must manually change companies to enter transactions and perform inquiries in multiple legal entities.</span></span> <span data-ttu-id="ce556-275">因为数据安全边界，合并的查询和报表将会使用大量资源并且非常耗时。</span><span class="sxs-lookup"><span data-stu-id="ce556-275">Because of data security boundaries, consolidated inquiry and reporting can be resource intensive and time-consuming.</span></span>

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a><span data-ttu-id="ce556-276">如果以运营单位建模组织</span><span class="sxs-lookup"><span data-stu-id="ce556-276">If the organization is modeled as an operating unit</span></span>

<span data-ttu-id="ce556-277">您不需要更改公司以从多个运营单位访问数据。</span><span class="sxs-lookup"><span data-stu-id="ce556-277">You do not need to change companies to access data from multiple operating units.</span></span> <span data-ttu-id="ce556-278">合并的查询与报表和单独的区域查询更容易和快捷。</span><span class="sxs-lookup"><span data-stu-id="ce556-278">Consolidated inquiry and reporting and individual regional inquiry is easier and faster.</span></span>

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a><span data-ttu-id="ce556-279">建模组织和层次结构的最佳实践</span><span class="sxs-lookup"><span data-stu-id="ce556-279">Best practices for modeling organizations and hierarchies</span></span>

<span data-ttu-id="ce556-280">在您执行个组织层次结构时，请考虑以下最佳实践:</span><span class="sxs-lookup"><span data-stu-id="ce556-280">Consider the following best practices when you implement an organization hierarchy:</span></span>

- <span data-ttu-id="ce556-281">创建一个分部建模法人和业务单位之间的交叉点。</span><span class="sxs-lookup"><span data-stu-id="ce556-281">Create a department to model the intersection between a legal entity and a business unit.</span></span> <span data-ttu-id="ce556-282">然后可以支持数据从部门到法定报表中法人，以及从部门到内部报表中的业务单位。</span><span class="sxs-lookup"><span data-stu-id="ce556-282">You can then roll up data from a department to a legal entity for statutory reporting, and from a department to a business unit for internal reporting.</span></span> <span data-ttu-id="ce556-283">部门可以充当收益中心。</span><span class="sxs-lookup"><span data-stu-id="ce556-283">Departments can serve as profit centers.</span></span> <span data-ttu-id="ce556-284">如果您使用部门，则不必使用法人和业务单位作为科目结构中的维度。</span><span class="sxs-lookup"><span data-stu-id="ce556-284">If you use departments, you do not have to use legal entities and business units as dimensions in the account structure.</span></span> <span data-ttu-id="ce556-285">您可以只使用部门作为维度。</span><span class="sxs-lookup"><span data-stu-id="ce556-285">You can use just departments as a dimension.</span></span> <span data-ttu-id="ce556-286">但是，如果成本中心只用作成本累加器，并且部门用于收入确认，您必须使用成本中心以及部门作为科目结构中的维度。</span><span class="sxs-lookup"><span data-stu-id="ce556-286">However, you must use both cost centers and departments as dimensions in the account structure if cost centers are used only as cost accumulators, and departments are used for revenue recognition.</span></span>
- <span data-ttu-id="ce556-287">如果您具有报告损益的复杂的需求，请建模工序单位的多个层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-287">Model multiple hierarchies for operating units if you have complex requirements for reporting profit and loss.</span></span>
- <span data-ttu-id="ce556-288">在单个法人中，请不要因为是相同的层次结构而建模多个层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-288">In a single legal entity, do not model multiple hierarchies for the same hierarchy purpose.</span></span>
- <span data-ttu-id="ce556-289">不要创建每个目标的层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-289">Do not create a hierarchy for every purpose.</span></span> <span data-ttu-id="ce556-290">通常，您可为多个目的使用层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-290">Usually, you can use one hierarchy for multiple purposes.</span></span> <span data-ttu-id="ce556-291">例如，工序单位的一个层次结构可以分配给所有策略关联用途。</span><span class="sxs-lookup"><span data-stu-id="ce556-291">For example, one hierarchy of operating units can be assigned to all policy-related purposes.</span></span>
- <span data-ttu-id="ce556-292">创建平衡的层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-292">Create balanced hierarchies.</span></span> <span data-ttu-id="ce556-293">在层次结构中，与根节点有相同距离的任何节点定义为一个级别。</span><span class="sxs-lookup"><span data-stu-id="ce556-293">In a hierarchy, all nodes that are the same distance from the root node are defined as a level.</span></span> <span data-ttu-id="ce556-294">在一个平衡层次结构中，只有运营单位的一种类型可能发生在每个级别，并且从根节点到各个级别的距离是一致的。</span><span class="sxs-lookup"><span data-stu-id="ce556-294">In a balanced hierarchy, only one type of operating unit can occur at each level, and the distance from the root node to each level is consistent.</span></span> <span data-ttu-id="ce556-295">如果在部门和法人或业务单位之间有中间级别，可能需要占位符组织创建一个平衡层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-295">If there are intermediate levels between a department and a legal entity or a business unit, placeholder organizations may be required to create a balanced hierarchy.</span></span>
- <span data-ttu-id="ce556-296">如果法人的结构也是您运行的结构，不建模运营单位的单独的层次结构。</span><span class="sxs-lookup"><span data-stu-id="ce556-296">Do not model a separate hierarchy of operating units if the structure for legal entities is also your operating structure.</span></span> <span data-ttu-id="ce556-297">法人和运营单位的杂项的层次结构可以为两个目的。</span><span class="sxs-lookup"><span data-stu-id="ce556-297">A mixed hierarchy of legal entities and operating units may serve both purposes.</span></span>
- <span data-ttu-id="ce556-298">在建模主要更改结构方案之前，请使用层次结构的生效日期执行后果分析和验证测试。</span><span class="sxs-lookup"><span data-stu-id="ce556-298">Before you model major restructuring scenarios, use the hierarchy's effective dates to perform an impact analysis and a validation test.</span></span>
- <span data-ttu-id="ce556-299">使用更改层次结构的草图样式，然后才可以在生产环境发布新版本。</span><span class="sxs-lookup"><span data-stu-id="ce556-299">Use draft mode to change a hierarchy before you publish a new version in a production environment.</span></span>
- <span data-ttu-id="ce556-300">限制有权限从在生产环境中的层次结构添加或删除组织的员工的编号。</span><span class="sxs-lookup"><span data-stu-id="ce556-300">Limit the number of people who have permissions to add or remove organizations from a hierarchy in a production environment.</span></span> <span data-ttu-id="ce556-301">较小的编号减少可能出现最高错误的机会，并且必须进行更正。</span><span class="sxs-lookup"><span data-stu-id="ce556-301">A smaller number reduces the chance that costly mistakes can occur and corrections must be made.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
