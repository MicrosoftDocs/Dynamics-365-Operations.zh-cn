---
title: 电子开票常见问题解答
description: 本文提供有关电子开票的常见问题的信息。
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fbb43438a9da567460eb744afb64dae5274f04a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904345"
---
# <a name="electronic-invoicing-faq"></a>电子开票常见问题解答

[!include [banner](../includes/banner.md)]

本文提供有关电子开票服务的常见问题的解答。 电子开票扩展 Dynamics 365 Finance、Dynamics 365 Supply Chain Management 和 Dynamics 365 Project Operations 中存在的电子开票功能。 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>电子发票的重要意义是什么？为什么对我的组织重要？

随着组织在全球范围内的发展以及在各个地区的足迹不断扩大，运营的复杂性和风险继续加剧。 保持合规性并适应经常变化的法规是一项日益严峻的挑战，在开具发票时尤为重要。 由于公司依赖纸质单据和手工完成，因此开具发票在传统上成本昂贵且容易出错。  

组织已经开始放弃纸质发票，以降低成本并加快端到端流程。 各国政府越来越多地将电子开票作为税务数字化的关键组成部分。 通过要求组织以数字方式向税务主管机构提交实时税务信息，政府可以最大程度地减少逃税和操纵，并减少欺诈。 

世界正在转向无纸化单据处理，如果不实施电子开票，客户可能会面临合规性问题、不必要的成本以及落后于竞争对手的风险。 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>难道 Finance、Supply Chain Management 和 Project Operations 已包括电子开票功能？ 作为客户，这给我带来了什么价值？ 

电子开票扩展了 Finance、Supply Chain Management 和 Project Operations 中存在的电子开票功能。 该功能还简化了对最新电子开票标准的遵守，并为电子发票处理和交换中的不同地区提供一致的体验。 电子开票的功能解锁了一系列好处，包括： 

   - 更加快速轻松地采用国家/地区特定要求。
   - 电子开票解决方案实施的标准化。 
   - 增强的电子发票处理可追溯性。  
   - 更易于维护，以适应不断变化的法律要求和本地业务惯例。 
   - 简化的解决方案包装。
   - 大量已提交单据的扩展功能可加快周转。
   - 与其他公司共享您的解决方案的能力。

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>电子开票服务是否支持 Finance、Supply Chain Management 和 Project Operations 的本地安装？ 

当前平台不允许使用本地版本，并且将来没有提供这项支持的计划。

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>电子开票服务是否与供应商导入自动化功能交互？

否。 有实现此交互的计划，但没有计划的时间线。 计划后，将在[发布计划](/dynamics365/release-plans/)中公布日期。

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>电子开票服务如何将文件附件处理到电子发票中？ 将 PDF 文件嵌入到 XML 文件中时是否需要 SharePoint 服务器？

附加到电子发票的文件作为 XML 元素中的嵌入式二进制数据进行处理。 嵌入 PDF 文件时不需要 SharePoint 服务器，但附件必须存储在 Finance、Supply Chain Management 和 Project Operations 单据管理系统中。

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>是否可以根据我所在国家/地区的规定提供电子开票服务？

电子开票服务是一个微服务平台，将在全球范围内提供。

Microsoft 计划为 Microsoft 在功能上进行了本地化的国家/地区发布电子发票格式和集成。 有关详细信息，请参阅[电子开票功能的可用性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)。

如果未列出您所在国家/地区的电子开票格式，该平台将在未来计划支持此情况。 您仍然可以受益于电子开票具有的配置功能，并可以自己配置电子开票格式，也可以与合作伙伴/ISV 合作为您的组织配置该格式。

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Dynamics 365 for Regulatory Services 是否是链接到 Finance 或 Supply Chain Management 的新模块，例如 Human Resources 或 Project Operations？ 是否有额外的费用？

Dynamics 365 for Regulatory Services (RCS) 是用于配置全球化资源的云服务。 RCS 对所有 Finance、Supply Chain Management 和 Project Operations 许可证持有者免费。

若要进行 RCS 注册，请转到 <https://marketing.configure.global.dynamics.com/>。

有关详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)。

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>我是需要注册才能获取电子开票服务，还是只是在“功能管理”中将其打开即可？

如果您有 Finance、Supply Chain Management 和 Project Operations 的许可证，请参阅[开始使用电子开票附加产品服务管理](e-invoicing-get-started-service-administration.md)以注册电子开票。

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>电子开票服务是否适用于第 1 层虚拟机？ 最低要求的环境是什么？

与电子开票服务的集成需要至少第 2 层虚拟机来托管 Finance 或 Supply Chain Management。 有关环境计划的详细信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>电子开票服务是否具有用于测试发票提交的测试模式？

这可以通过配置来实现。 若要测试发票提交，您可以从用户接受度测试 (UAT) 环境连接到 Finance 或 Supply Chain Management，然后提交测试发票。 电子开票支持配置测试数字证书，如果电子发票需要数字审批，则可以设置由税务主管机构发布的测试 Web 服务中的 URL。

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>是否有任何关于开箱即用的国家/地区特定的电子开票功能的文档？

是。 有关电子开票功能的可用性及其支持的格式的信息，请参阅[电子开票功能的可用性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)。

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>电子开票服务是否允许为特定国家/地区配置的 Finance 或 Supply Chain Management 中的法人使用来自不同国家/地区的电子开票功能？

是。 如果满足以下条件，可以使用电子开票功能来独立于法人所在国家/地区处理业务文档提交：

   - 生成的业务文档使用适当的文档模型映射。
   - 在电子开票功能中配置的业务文档和适用性规则之间是匹配的。

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>电子开票服务是否使用 Finance 和 Supply Chain Management 中电子报告模块提供的相同配置和设计体验？ 

是。 Finance 和 Supply Chain Management 中电子报告 (ER) 模块中使用的相同设计器工具用于创建和配置数据模型映射和文件格式配置。 这些设计器工具还在 Regulatory Configuration Services (RCS) 中用于创建和配置在电子开票功能的配置中使用的数据模型映射和文件格式配置。

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>是否可以扩展和配置适用性规则，以使它们不与任何特定参数（如法人）关联？

是。 适用性规则是完全可配置的。 您可以添加或删除子句、构建逻辑操作以及将子句分组和取消分组。 有关详细信息，请参阅[适用性规则](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules)。

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>电子开票服务是否支持添加其他 ER 格式配置以生成其他类型的文档？ 它是否支持通过电子方式将文档发送给客户，如交货通知？

您可以使用其他 ER 格式配置来生成所需的输出文件。 但是，ER 格式配置必须从在 Finance 或 Supply Chain Management 中配置用于生成业务文档的相同 ER 发票模型映射派生。 电子开票原本不支持将输出文件作为 EDI 交易直接发送给客户。

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>电子开票服务是否支持与客户交换电子发票？ 它是否支持为同一个发票配置不同的发票格式？

路线图上有接收和导入供应商电子发票的功能，但是当前不支持自动将电子发票发送给客户。

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>电子开票服务是否会扩展来支持与其他公司交换 EDI 消息？

电子开票服务的重点是交换由法规合规性要求驱动的电子发票消息类型。 路线图上有接收和导入供应商电子发票，但是目前原本不支持将电子发票文件发送给客户，除了将电子发票发送给客户属于监管要求的情况。

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>电子开票服务是否支持导入或合并在旧版电子开票功能的 ER 格式配置中进行的自定义？

您可以在电子开票服务中重用 ER 格式配置。 但是，ER 格式配置必须从电子发票功能应使用的相同 ER 发票模型映射派生，此映射在 Finance 或 Supply Chain Management 中被配置为用于生成业务文档。

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>电子开票服务是否支持从自定义表开具电子发票？ 如果支持，您如何为这些新表和实体创建 ER 数据模型配置？

是。 但是，它需要自定义发票模型映射，并向自定义表添加必要的引用，或者根据复杂性来创建新的发票模型映射。

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>电子开票服务是否支持不同的 Web 服务终结点？

电子发票支持不同的 Web 服务终结点。 您可以将可配置集成与 REST Web 服务或一些参数化的特定于国家/地区的 Web 服务集成结合使用。 可以使用不同版本的配置为相同的 Web 服务和 API 配置不同的终结点。 有关详细信息，请参阅[按操作排列的参数列表](e-invoicing-setup.md#list-of-parameters-by-action)。

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>电子开票是否已与北欧国家/地区的不同发票经营者的 API 集成，还是应该分别处理？

Microsoft 将通过使用电子开票功能不断扩展功能范围，以提供现成的集成。 有关支持的格式和集成的详细信息，请参阅[电子开票功能的可用性](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features)。

> [!NOTE] 
> 如果找不到所需的答案，请通过 <D365EInvoicePreview@microsoft.com> 使用电子邮件将您的问题发送给产品开发团队。 我们将与您联系或改善此常见问题解答的范围。
