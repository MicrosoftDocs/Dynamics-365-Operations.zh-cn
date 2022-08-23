---
title: Dynamics 365 Commerce 10.0.29 预览版（2022 年 10 月）
description: 本文介绍 Microsoft Dynamics 365 Commerce 10.0.29 中的新增功能或更改的功能。
author: josaw1
ms.date: 08/02/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c1f85fcd8f79106a3af93489d3bef608b9840bf3
ms.sourcegitcommit: 91f58a9863f4e8f30ac787c2a9771c1ff6a05f72
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/03/2022
ms.locfileid: "9224230"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Dynamics 365 Commerce 10.0.29 预览版（2022 年 10 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文列出了 Microsoft Dynamics 365 Commerce 预览版 10.0.29 中的新增或更改的功能。 此版本的构建版本号为 10.0.1326，并按以下时间表提供：

- **版本预览：** 2022 年 8 月
- **版本的正式发布时间（自行更新）：** 2022 年 9 月
- **版本的正式发布时间（自动更新）：** 2022 年 10 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---------|------------------|----------------|--------------| 
| B2B | [启用对跨渠道的销售协议的支持](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | 此功能使企业到企业 (B2B) 销售人员组织能够使用 Commerce headquarters 中的销售协议为买方定义基于合同的定价。 当 B2B 买家在电子商务网站上购物时，为 B2B 买家组织配置的基于合同的定价会自动应用于整个产品发现、购买和结账体验。 | 功能管理<p>*支持跨商业渠道的销售协议* |
| Customer Service | [使用 Dynamics 365 Customer Service 全渠道启用 Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | 一流的客户支持体验是为消费者提供愉快的个性化商务体验的关键。 目前存在多个商业接触点，例如实体店、在线渠道和社交渠道。 消费者希望在所有这些接触点中拥有个性化的支持体验。 此功能通过与 Dynamics 365 Customer Service 全渠道集成，帮助您提高购物车转化为销售的转化率，增加与消费者的个性化互动，并增强客户服务。 | 由管理员/制作者启用 |
| 电子商务 | 支持在电子商务中比较产品 | 允许购物者比较各种类别的产品，以便他们能为自己做出正确的购买决定。 此功能适用于企业对消费者 (B2C) 和 B2B 站点。 | 站点生成器 | 
| 礼品卡 | 支持零售礼品卡表以实现跨公司数据共享 | Dynamics headquarters 支持为 Dynamics 架构中的特定表启用跨公司数据共享的功能。 在此功能中，Dynamics 365 Commerce 增加了对零售礼品卡表跨公司数据共享的支持。 因此，一家公司的礼品卡现在可以将其数据复制到环境中的另一家公司。 对原始公司礼品卡表所做的更改将共享到复制的公司礼品卡表。 | 开发人员 |
| 性能 | 删除“编辑客户”场景的 RTS 依赖项 | 高可用性和高性能是对销售点 (POS) 和电子商务渠道的默认期望。 为了帮助达到这些期望，在编辑客户信息时，Dynamics 365 Commerce 渠道不再需要依赖与 Commerce headquarters 的实时通信。 为异步和非异步客户异步编辑客户信息的功能有助于减少对 Commerce headquarters 的实时调用。 | 由管理员/制作者启用 |

## <a name="feature-state-changes-in-this-release"></a>此版本中的功能状态更改

下表列出了版本 10.0.29 中强制或默认启用的功能。 更新到版本 10.0.29 后，系统即会自动启用所有这些功能。 强制功能无法关闭，但仍可使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)关闭默认开启的功能。

此表还列出了以前处于公开预览版状态，但在版本 10.0.29 中已变为正式发布的功能。 此更改指示现在建议在生产环境中使用这些功能。 除非另外指明，否则这些功能默认情况下处于关闭状态。 因此，如果您要使用它们，那么您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用它们。

| 功能 | 标题 | 新功能状态 |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(巴西)特定于巴西的 Commerce 功能 | 默认打开 |
| RetailAdvancedGTETaxAdjustmentFeature | (印度)将 Retail POS 中为零售交易记录计算的 GST 应用于零售对帐单 | 默认打开 |
| RetailChronologicalInvoicePostingFeature_IT | (意大利)启用未按时间顺序过帐的零售发票 | 默认打开 |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (墨西哥)零售全球 CFDI 中的折扣调整 | 默认打开 |
| RetailFiscalIntegrationConfigurationEnhancementFeature | 会计集成技术配置文件覆盖 | 默认打开 |
| RetailFiscalIntegrationConnectorLocationFeature | 来自 POS 收银机的直接会计集成 | 默认打开 |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | 会计整合本地存储备份 | 默认打开 |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | 已推迟单据登记 | 默认打开 |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | POS 收银机的会计登记状态 | 默认打开 |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (印度)根据发票地址为电子商务订单计算 GST | 默认打开 |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (波兰)零售账单的默认销售单据状态 | 默认打开 |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (墨西哥)在“Retail CFDI 全局”中对税金基准金额进行舍入重新计算。 | 默认打开 |
| RetailSupplementaryInvoiceFeature | 为零售商店中完成的现金和结转交易记录启用补充账单 | 默认打开 |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  启用缓冲库存和库存水平    |  默认打开|
|RetailInboundOutboundInventoryValidationFeature|   在 POS 入站和出站库存操作中启用验证   |   默认打开   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  增强的电子商务渠道端库存计算逻辑 |   默认打开   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    销售点中的库存调整   |  默认打开  |
| RetailMultiplePickupDeliveryModeFeature |  支持多种提货交货模式     |   强制    |
|  RetailProductAvailabilityOptimizationFeature |   优化的产品可用性计算  |  强制 |
|   RetailPricingDataManagerV2Feature   |   提高 Commerce 定价引擎的性能 |   强制 |
|  RetailPricingPreventUnintendedRecalculationFeature   | 防止商务订单出现意外的价格错误    |  强制  |
| RetailTeamsIntegration    |   启用 Microsoft Teams 集成| 强制   |  
| ConsumerEFDSyncProcessFeature_BR | （巴西）NFC-e 同步处理 | 默认打开 |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | 支持会计整合框架中的内部和外部连接器 | 强制 |
| RetailTaxRegistrationIdEnableFeature_BR | (巴西)在 Retail POS 中按税务登记编号搜索客户 | 强制 |
| RetailTaxRegistrationIdEnableFeature_IN | (印度)在 Retail POS 中按税务登记编号搜索客户 | 强制 |
| RetailTaxRegistrationIdEnableFeature_IT | (意大利) Retail POS 中的客户信息管理 | 强制 |
| RetailTaxRegistrationIdEnableFeature_PL | (波兰) Retail POS 中的客户信息管理 | 强制 |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (印度零售 GST)参考原始发票更新贷方通知单 | 强制 |
| RetailUserDefinedCertificateProfileFeature | 用于零售商店的用户定义的证书配置文件 | 强制 |
  

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Commerce 10.0.29 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.29 的平台更新（2022 年 10 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md)。 

### <a name="bug-fixes"></a>缺陷修复

有关版本 10.0.29 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c)。 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 和行业云：2022 版本第 2 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2022 版本第 2 波计划](/dynamics365-release-plan/2022wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-features"></a>已删除和弃用的功能

[Dynamics 365 Commerce 中已删除或弃用的功能](removed-deprecated-features-commerce.md)一文介绍了针对 Commerce 删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Commerce 中已删除或弃用的功能](removed-deprecated-features-commerce.md)一文中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
