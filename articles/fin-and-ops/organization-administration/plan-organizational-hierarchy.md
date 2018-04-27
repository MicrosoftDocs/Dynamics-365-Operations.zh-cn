---
title: "规划组织层次结构"
description: "设置组织和组织层次结构之前，请确保了解如何以最好的方式为业务建模。"
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d669defa13e8f32cd29463324e580a6d738c3e2a
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-organizational-hierarchy"></a>规划组织层次结构

[!INCLUDE [banner](../includes/banner.md)]

在 Microsoft Dynamics 365 for Finance and Operations 中设置组织和组织层次结构之前，请确保您已计划好您的业务将如何建模。 组织模型对 Finance and Operations 实施和业务流程有重大影响。 

组织层次结构表示构成业务的组织之间的关系。 因此，在您建模组织时最重要的注意事项是您的业务结构。 我们建议您基于高管和各功能区域（如财务和会计、人力资源、运营、采购、销售和市场）的高级经理的反馈来定义组织结构。 

在您计划层次结构时，考虑组织层次结构和财务维度之间的关系也十分重要。 您可以设置多个组织层次结构来表示您业务的不同视图。 通过使用财务维度，您可以基于这些视图创建报表。 与您的 Microsoft Dynamics 365 for Finance and Operations 合作伙伴一起创建满足组织和法定申报需求的层次结构。 

> [!Note]
> 尽管在 Finance and Operations 中您可以不创建法人而是使用财务维度代表法人，但财务维度并不能用于满足法人的运营或业务需要。 将 Finance and Operations 中的单位间核算功能设计成仅满足由每个交易记录所创建的会计条目。 

> [!Caution]
> 您不应仅基于本文中的信息来确定如何建模组织。 本文档仅作为一个参考指南。 您可以与您的 Finance and Operations 合作伙伴共同制定附加指南。 您的 Finance and Operations 合作伙伴获得了在不同行业和跨客户群的经验。

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>确定是否以法人或运营单位建模内部组织

您必须具有至少一个法人在 Finance and Operations 中代表您的业务。 法人可以输入法律合同，并需要准备报告其业绩的财务报表。 

在 Finance and Operations 中，法人可用于交易业务或合并。 这意味着在 Finance and Operations 中的法人不必代表您业务中的实际实体。 例如，参与交易的公司可以拥有子公司法人。 在这种情况下，交易需要法人，并且需要虚拟法人以合并子公司法人的结果和余额。 

您的业务中的内部组织，例如区域办公室，可以表示为附加的法人或者为主要法人的运营单位。 运营单位不需要是法律上定义的组织。 运营单位用于控制业务中的经济资源和运营流程。 例如，部门和成本中心是运营单位。 

在 Finance and Operations 中的一些功能根据该组织是否为法人或运营单位而进行不同的工作。 在您做出决定时，请仔细考虑下述功能。 


### <a name="master-data"></a>主数据
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织      
必须为每个法人设置一些主数据，如客户、付款期限、税务主管机构和特定站点的库存预留。 在所有法人中共享一些主数据，如用户、产品和大多数人力资源数据。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
在运营单位中共享主数据。 

### <a name="module-parameters"></a>模块参数
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织    
必须按照法人设置模块的参数，如应收账款参数、应付账款参数和现金和银行管理参数。 由于法人的模块设置为单独的，每个子公司可以符合当地法律要求和商业惯例。 例如，专业服务法人和制造法人可以具有不同的模块参数，即使它们向同一个母公司报告。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
在运营单位中共享模块参数。 

### <a name="data-security"></a>数据安全
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织    
大多数数据通过公司 ID 自动保护。 公司 ID 对于与法人关联的数据是唯一的标识符。 公司只可与一个法人关联，法人也只可与一个公司关联。 用户仅可以访问他们有权访问的公司数据。 您无需自定义 Finance and Operations 来通过公司 ID 保护数据。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
可以通过创建自定义的数据安全策略按运营单位保护数据。 数据安全策略用于限制对数据的访问。 例如，假定只允许用户在特定运营单位创建采购订单。 可以创建数据安全策略来防止用户从其他运营单位访问采购订单的数据。 交易量和安全策略的数量会影响业绩。 在您设计安全策略时，请考虑业绩。 

### <a name="ledgers"></a>分类帐
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织    
每个法人需要分类帐来提供会计科目表、记帐币种、申报币种和会计日历。 资产负债表可以仅为法人创建。 主科目、维度、科目结构、会计科目表和会计准则可以由多个法人使用。

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
运营单位不能拥有自己的分类帐信息。 如果您的内部组织不需要唯一的分类帐，您可以以运营单位建模它们。 将针对层次结构中的母法人设置分类帐信息。 可以针对法人中的运营单位或针对母法人创建损益表。 

### <a name="fiscal-calendars"></a>会计日历 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织    
每个法人拥有自己的会计日历。 如果您的内部组织使用不同的会计年度和会计日历，您必须以法人建模组织。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
运营单位必须共享会计日历。 如果您的内部组织可以使用相同的会计年度和会计日历，您可以以运营单位建模组织。 

### <a name="consolidation"></a>合并
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织    
您必须将区域办公室的财务结果合并入单个合并的公司中以便准备财务报表。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
不要求合并，因为在运营单位中已共享数据。 

### <a name="centralized-payments"></a>集中付款
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织 
必须设置集中付款，以便所有子法人的发票可以支付给单个母法人或自单个母法人支付。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
不要求集中付款，因为所有发票在单个法人中记录。

### <a name="intercompany-transactions"></a>内部公司事务
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织 
内部公司销售订单、采购订单、付款或收货可以应用于彼此。 您无需使用日记帐凭证。 您可以在子级别分类帐（应收账款、应付账款）中查看内部公司交易记录。 以下示例说明了如何处理内部公司交易记录。 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>示例 1：总部对区域办公室提供服务且必须将那些服务的成本记于区域办公室的帐目上
如果您以法人建模区域办公室，您具有以下选项： 
- 总部创建日记帐条目以交叉记录区域办公室的费用。 不能计算交易记录的帐龄。
- 总部将服务的采购订单发送到区域办公室。 与内部公司的子分类帐交易记录一起，在区域办公室的法人中自动创建销售订单。 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>示例 2：总部采购和支付交付至区域办公室的服务
如果您以法人建模区域办公室，您具有以下选项： 
- 发票和付款遵循总部的管理要求。 总部可以创建日记帐条目以交叉记录区域办公室的费用。 不能计算交易记录的帐龄。 
- 发票和付款遵循总部的管理要求。 总部可以创建内部公司的子分类帐交易记录。

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
在运营单位中的内部公司交易记录仅通过日记帐凭证支持。 运营单位不能从同一法人中的另一个运营单位签发或接收采购订单、销售订单或发票。 您不能在子级别分类帐（应收账款、应付账款）中查看内部公司交易记录。 以下示例说明了如何处理内部公司交易记录。 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>示例 1：总部对区域办公室提供服务且必须将那些服务的成本记于区域办公室的帐目上
如果您以运营单位建模区域办公室，则总部输入费用交易记录并将它编码至区域办公室。 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>示例 2: 总部采购和支付交付至区域办公室的服务。
如果您以运营单位建模区域办公室，则发票和付款遵循总部的管理要求。 可以将发票编码至区域办公室。 在损益表中，请使用平衡的财务维度以报告区域办公室的成本。

### <a name="local-tax-requirements"></a>本地纳税要求
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
法人将遵循该法人所登记国家/地区的税务主管机构的税法。 例如，在丹麦登记的法人需要遵循丹麦的税务法律和法规。 在 Finance and Operations 中，法人仅可以属于一个国家/地区。 您为法人的主要地址选择的国家/地区将控制该法人可用的特定于国家/地区的功能。 例如，如果法人的主要地址位于丹麦，则与丹麦税务法律和法规相关的功能变得可用。 因此，如果您的组织位于不同的国家/地区且要求不同的本地税务选项，则必须以单独的法人设置该组织。

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
运营单位使用母法人的国家/地区环境。 在同一法人中的运营单位不能具有不同的特定于国家/地区的要求。 如果您的组织在同一个国家/地区且使用相同的税务选项，您可以以运营单位进行设置。


### <a name="statutory-reporting-for-a-countryregion"></a>国家/地区的法定报表 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
对于由 Finance and Operations 支持的国家/地区，可以创建大多数法定报表。 有关每个国家/地区可用报表的信息，请参阅 Finance and Operations 的 [Microsoft Dynamics 本地化门户](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC)。 （需要一个客户源登陆。） 

> [!Note]
> 在 Finance and Operations 中，总帐中的过帐层允许您对母公司进行条目调整，这里与子公司相比使用了不同的会计标准。 例如，对于使用英国通用会计制度 (UK GAAP) 的公司，您可以在过帐层中进行条目调整。 这些条目可以合并入使用美国通用会计制度 (GAAP) 的母公司。 调整条目不影响英国 GAAP 报表。

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
必须通过使用另一个申请创建法定报表。 您必须确保在 Finance and Operations 中获得数据，以支持每个运营单位的需求，此处它们与总部的需求不同。 

### <a name="currency"></a>货币
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
如果您的组织必须使用不同功能币种，则必须以法人建模组织。 针对每个法人设置功能币种。 不过，您可以以多个币种输入交易记录。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
如果您的组织可以使用单个功能币种，您可以以运营单位建模组织。 运营单位必须共享一种功能币种。 但是，您可以输入交易记录并以多个币种创建报表。 


### <a name="year-end-closing"></a>年终结算
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
如果法律和会计准则在您的组织所在国家/地区中存在不同，那么对于每个组织您可能需要采用不同的年终结算过程。 这意味着您必须以法人建模组织。 每个法人具有自己的年终结算过程。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
如果法律和会计准则在您的组织所在的国家/地区中相同，您可能使用单个集的年终结算过程。 这意味着您可以以运营单位建模组织。 所有运营单位必须使用相同的年终结算过程。 

### <a name="number-sequences"></a>编号规则
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
可以按法人设置一些参考的编号规则。 可以共享一些编号规则。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
可以按运营单位设置一些参考的编号规则。 可以共享一些编号规则。

### <a name="products"></a>产品 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
共享产品定义，且必须将其发布至各个法人只后它们才可以包含在交易记录中。 每个交易记录具有自己的已发布产品集，它们可包含于交易记录文档中。 如果您的组织必须使用不同产品集，则必须以法人建模组织。 

> [!Note]
> 即使共享产品定义，在已发布产品的每个法人中，您可以为每个库存站点的物料指定不同的销售、采购和库存参数。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
所有运营单位共享同一个产品集。 如果您的内部组织可以共享同一个产品集，您可以以运营单位建模组织。 

### <a name="inquiry-and-reporting"></a>查询和报表  
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>如果以法人建模组织
您必须手动更改公司来输入交易记录及在多个法人中执行查询。 因为数据安全边界，合并的查询和报表将会使用大量资源并且非常耗时。 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>如果以运营单位建模组织 
您不需要更改公司以从多个运营单位访问数据。 合并的查询与报表和单独的区域查询更容易和快捷。

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>建模组织和层次结构的最佳实践
在您执行个组织层次结构时，请考虑以下最佳实践:
-   创建一个分部建模法人和业务单位之间的交叉点。 然后可以支持数据从部门到法定报表中法人，以及从部门到内部报表中的业务单位。 部门可以充当收益中心。 如果您使用部门，则不必使用法人和业务单位作为科目结构中的维度。 您可以只使用部门作为维度。 但是，如果成本中心只用作成本累加器，并且部门用于收入确认，您必须使用成本中心以及部门作为科目结构中的维度。
-   如果您具有报告损益的复杂的需求，请建模工序单位的多个层次结构。
-   在单个法人中，请不要因为是相同的层次结构而建模多个层次结构。
-   不要创建每个目标的层次结构。 通常，您可为多个目的使用层次结构。 例如，工序单位的一个层次结构可以分配给所有策略关联用途。
-   创建平衡的层次结构。 在层次结构中，与根节点有相同距离的任何节点定义为一个级别。 在一个平衡层次结构中，只有运营单位的一种类型可能发生在每个级别，并且从根节点到各个级别的距离是一致的。 如果在部门和法人或业务单位之间有中间级别，可能需要占位符组织创建一个平衡层次结构。
-   如果法人的结构也是您运行的结构，不建模运营单位的单独的层次结构。 法人和运营单位的杂项的层次结构可以为两个目的。
-   在建模主要更改结构方案之前，请使用层次结构的生效日期执行后果分析和验证测试。
-   使用更改层次结构的草图样式，然后才可以在生产环境发布新版本。
-   限制有权限从在生产环境中的层次结构添加或删除组织的员工的编号。 较小的编号减少可能出现最高错误的机会，并且必须进行更正。

