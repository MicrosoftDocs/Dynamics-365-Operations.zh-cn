---
title: 电子开票常见问题解答
description: 本主题提供有关电子开票的常见问题的信息。
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 41cddcdad5043ec314a94dda67f4f2e9de406cac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840164"
---
# <a name="electronic-invoicing-faq"></a>电子开票常见问题解答

[!include [banner](../includes/banner.md)]

本主题提供有关电子开票的常见问题的解答。 电子开票扩展 Dynamics 365 Finance、Dynamics 365 Supply Chain Management 和 Dynamics 365 Project Operations 中存在的电子开票功能。 

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

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>电子开票是否支持 Finance、Supply Chain Management 和 Project Operations 的本地安装？ 

当前平台不允许使用本地版本，并且将来没有提供这项支持的计划。

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>电子开票是否与供应商导入自动化功能交互？

否。 有实现此交互的计划，但没有计划的时间线。 计划后，将在[发布计划](https://docs.microsoft.com/dynamics365/release-plans/)中公布日期。

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>电子开票如何将文件附件处理到电子发票中？ 将 PDF 文件嵌入到 XML 文件中时是否需要 SharePoint 服务器？

附加到电子发票的文件作为 XML 元素中的嵌入式二进制数据进行处理。 嵌入 PDF 文件时不需要 SharePoint 服务器，但附件必须存储在 Finance、Supply Chain Management 和 Project Operations 单据管理系统中。

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>是否可以根据我所在国家/地区的规定提供电子开票？

电子开票是一个微服务平台，将在全球范围内提供。

Microsoft 计划为 Microsoft 在功能上进行了本地化的国家/地区发布电子发票格式和集成。 有关详细信息，请参阅[电子开票功能的可用性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)。

如果未列出您所在国家/地区的电子开票格式，该平台将在未来计划支持此情况。 您仍然可以受益于电子开票具有的配置功能，并可以自己配置电子开票格式，也可以与合作伙伴/ISV 合作为您的组织配置该格式。

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Dynamics 365 for Regulatory Services 是否是链接到 Finance 或 Supply Chain Management 的新模块，例如 Human Resources 或 Project Operations？ 是否有额外的费用？

Dynamics 365 for Regulatory Services (RCS) 是用于配置全球化资源的云服务。 RCS 对所有 Finance、Supply Chain Management 和 Project Operations 许可证持有者免费。

若要进行 RCS 注册，请转到 <https://marketing.configure.global.dynamics.com/>。

有关详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)。

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>我是需要注册才能获得电子开票，还是仅在功能管理中就能打开它？

如果您有 Finance、Supply Chain Management 和 Project Operations 的许可证，请参阅[开始使用电子开票附加产品服务管理](e-invoicing-get-started-service-administration.md)以注册电子开票。

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>电子开票是否适用于第 1 层虚拟机？ 最低要求的环境是什么？

与电子开票的集成需要至少第 2 层虚拟机来托管 Finance 或 Supply Chain Management。 有关环境计划的详细信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>电子开票是否具有用于测试发票提交的测试模式？

这可以通过配置来实现。 若要测试发票提交，您可以从用户接受度测试 (UAT) 环境连接到 Finance 或 Supply Chain Management，然后提交测试发票。 电子开票支持配置测试数字证书，如果电子发票需要数字审批，则可以设置由税务主管机构发布的测试 Web 服务中的 URL。

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>是否有任何关于开箱即用的国家/地区特定的电子开票功能的文档？

是。 有关电子开票功能的可用性及其支持的格式的信息，请参阅[电子开票功能的可用性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)。

> [!NOTE] 
> 如果找不到所需的答案，请通过 <D365EInvoicePreview@microsoft.com> 使用电子邮件将您的问题发送给产品开发团队。 我们将与您联系或改善此常见问题解答的范围。
