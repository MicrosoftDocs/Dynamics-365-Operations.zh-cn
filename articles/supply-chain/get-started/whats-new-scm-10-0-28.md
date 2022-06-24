---
title: Dynamics 365 Supply Chain Management 10.0.28 的预览（2022 年 8 月）
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.28 中的新增功能或更改的功能。
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 2b129481399897337e960ec2d708d69a563b5435
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902044"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Dynamics 365 Supply Chain Management 10.0.28 的预览（2022 年 8 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 预览版本 10.0.28 中的新增功能或更改的功能。 此版本的构建版本号为 10.0.1264，并按以下时间表提供：

- **版本预览：** 2022 年 5 月
- **版本正式发布（自行更新）：** 2022 年 7 月
- **版本正式发布（自动更新）：** 2022 年 7 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 库存和物流 | [第三方货运转运商的到岸成本集成实体](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [到岸成本实体概览](../landed-cost/landed-cost-entities-overview.md) | 默认启用 |
| 计划 | [需求驱动材料要求计划 (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | 即将推出 | 功能管理：<br>*(预览版)用于计划优化的 DDMRP* |
| 计划 | [可承诺量 (CTP) 的计划优化支持](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | 即将推出 | 功能管理：<br>*(预览版)用于计划优化的 CTP* |
| 计划 | [保质期计划优化支持](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | 即将推出 | 默认启用 |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 库存和仓库管理 | 启用内部公司现有量以仅显示非零现有数量 | 利用此功能，您可以选择是否应在内部公司现有量清单中包含现有数量为零的物料。 您可以使用 **不在内部公司现有量列表中显示具有零现有数量的物料** 设置来控制此选项，此功能会将此设置添加到 **库存和仓库管理参数** 页面。 |
| 库存和仓库管理 | (印度)对于转移价格规则，“源仓库代码”设置为“所有”时将会忽略库位 | <p>此功能仅适用于印度本地化。 它使设置存货转移中物料的转移价格的流程更加直观。</p><p>您可以通过为每个物料配置转移定价规则来设置转移价格。 执行此配置的一种方法是包括规则行，其中 **源仓库代码** 字段设置为 *全部*。 此设置指示无论从哪个仓库中领取物料，都应该应用由行定义的转移价格。 启用此功能后，**源仓库代码** 字段设置为 *全部* 的价格规则将忽略 **位置** 设置。 因此，无论在转移单上指定的位置如何，该规则都将适用。 此行为可能是预期行为，因为位置位于存储维度层次结构中的仓库下面。</p><p>如果没有此功能，则仅在转移单上的位置与为规则设置的位置完全匹配时，系统才将应用此类规则。 （如果为规则设置了空白位置，则系统仅将该规则应用于该位置也具有空白值的转移单。）</p> |
| 库存和仓库管理 | 库存现有量报表数据清除 | 此功能提供了一种清除用于创建 *库存现有量报表存储* 报表的数据的方法。 |
| 生产控制 | 为服务协议和服务订单行分配项目活动 | 此功能将名为 **项目活动** 的字段添加到服务协议和服务订单行，以便您可以为它们设置项目活动。 当您过帐要求设置项目活动的服务管理项目日记帐时，此功能将有助于防止锁定错误。  |
| 仓库管理 | 针对管理员或类似的受信任用户的转移行手动领料服务 | 利用此功能，管理员可以手动选取与转移行相关的库存交易。 这些行包括已发放到仓库的行。 管理员应仅在特殊情况下执行此选取，例如系统处于损坏状态时。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助文章。 按照前几节的列举，这些文章未必与此发行版中增加的新功能有关。 但是，它们可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新文章 |
|---|---|
| 成本管理 | [固定收货价](../cost-management/fixed-receipt-price.md) |
| 成本管理 | [库存成本计算常见问题](../cost-management/inventory-costing-faq.md) |
| 成本管理 | [过帐到费用帐户的会计原则](../cost-management/post-to-charge-account-accounting-principle.md) |
| 库存管理 | [库存交易详细信息](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.28 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.28 的平台更新（2022 年 6 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.28 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 和行业云：2022 版本第 1 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2022 版本第 1 波计划](/dynamics365-release-plan/2022wave1/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management 中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
