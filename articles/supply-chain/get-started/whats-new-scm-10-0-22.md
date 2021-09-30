---
title: Dynamics 365 Supply Chain Management 10.0.22 预览版（2021 年 11 月）
description: 此主题介绍了 Microsoft Dynamics 365 Supply Chain Management 10.0.22 中的新增功能或更改的功能。
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4aac62b36cd271e1c5fc3bcbbfdd785963fc368
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2021
ms.locfileid: "7484064"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Dynamics 365 Supply Chain Management 10.0.22 预览版（2021 年 11 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题列出了 Microsoft Dynamics 365 Supply Chain Management 预览版 10.0.22 中的新增功能或更改的功能。 此版本的构建版本号为 10.0.995，并以下面的形式提供：

- **预览版本：** 2021 年 9 月
- **版本的正式发布时间（自我更新）：** 2021 年 10 月
- **版本的正式发布时间（自动更新）：** 2021 年 11 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 *功能* 列提供了指向[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)的链接，您可以在那里查看每项功能的官方发布日期。 *更多信息* 列提供了更多详细信息和/或相关文档的链接。 若要确定如何开启功能，请参阅 *启用方式* 列。 有关如何使用功能管理的详细信息，请参阅[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的功能。

| 特征区域 | 功能 | 更多信息 | 启用者: ，时间:  |
|---|---|---|---|
| 计划 | [计划优化对基于产能的资源分配的支持](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [基于功能选择资源的计划](../master-planning/planning-optimization/capability-based-scheduling.md) | 功能管理（*计划优化的无限容量计划*） |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。 如果要使用这些功能中的任何一个，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中明确启用。

| 特征区域 | 功能管理中的功能名称 | 更多信息 |
|---|---|---|
| 成本管理 | 为标准成本舍入评估创建相关凭证 | <p>在创建库存财务过帐（如销售订单发票或库存交易记录）时，此功能会导致系统为任何相关标准成本舍入重估创建单独的凭证，然后将其作为相关凭证附加到该财务过帐凭证。</p><p>如果没有此功能，系统将记录将标准成本舍入重估记录到同一个凭证过帐中。 该行为有时可能导致日期信息冲突，因为重估使用会话日期或系统日期，而财务过帐则使用过帐日期。</p> |
| 分布式混合拓扑 | *（无需功能管理。）* | <p>此版本扩展云和边缘缩放单元的仓库管理工作负荷出站负荷计划功能。</p><p>有关详细信息，请参阅 [Cloud Scale Unit 和 Edge Scale Unit 的仓库管理工作负荷](../cloud-edge/cloud-edge-workload-warehousing.md)。</p> |
| 工程更改管理 | 生成工程产品的变型 | <p>利用此功能，您可以根据工程产品的颜色、尺寸、样式或配置维度为工程产品生成多个变型。</p><p>有关详细信息，请参阅[生成工程产品的变型](../engineering-change-management/engineering-variants.md)。</p> |
| 库存和仓库管理 | 库存可见性与预留抵销的集成 | <p>仅在启用 *库存可见性集成* 功能后才能 启用此功能。 其还可用于抵销对库存可见性进行的预留。</p><p>有关详细信息，请参阅[库存可见性预留](../inventory/inventory-visibility-reservations.md)。</p> |
| 销售和市场营销 | 限制可选择进行过帐的销售订单数 | <p>此功能自动启用。 其向 **应收帐款参数** 页面添加了一个 **要过帐的最大销售订单数** 字段。 利用此此，您可以定义在从销售订单列表页面中过帐确认单、领料单、装箱单和发票时可以选择的最大销售订单数。 默认值为 *100*。</p><p>此功能有助于在选择大量销售订单时改进销售订单列表页的性能。 它对可由定期任务处理的销售订单的数量没有影响。</p> |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助主题。 按照上一部分的列举，这些主题未必与此发行版中增加的新功能有关。 但是，可能可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新主题 |
|---|---|
| 工程更改管理 | [工程更改管理概述](../engineering-change-management/product-engineering-overview.md)现在列出了功能管理中可用的所有相关可选功能 |
| 主计划 | [需求预测设置](../master-planning/demand-forecasting-setup.md) |
| 主计划 | [净需求和计划优化限定标准信息](../master-planning/planning-optimization/net-requirements.md) |
| 仓库管理 | [发放到仓库](../warehousing/release-to-warehouse-process.md)提供整个发放到仓库流程的详细概览 |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.22 中包含平台更新。 若要了解详细信息，请参阅 [Finance and Operations 应用版本 10.0.22 的平台更新（2021 年 11 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md)。 <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.22 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299)。

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 和行业云：2021 版本第 2 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2021 版本第 2 波计划](/dynamics365-release-plan/2021wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
