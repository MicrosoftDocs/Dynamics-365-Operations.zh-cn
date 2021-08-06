---
title: Dynamics 365 Supply Chain Management 版本 10.0.19（2021 年 6 月）中的新增功能或更改的功能
description: 此主题介绍了 Dynamics 365 Supply Chain Management 10.0.19 中的新增功能或更改的功能。
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 98f9fffcbf93871de302a0d8b4b9675889ef5e40
ms.sourcegitcommit: 908a85987b604a7782407da70fb70ef75c07989f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/19/2021
ms.locfileid: "6641120"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Dynamics 365 Supply Chain Management 版本 10.0.19（2021 年 6 月）中的新增功能或更改的功能

[!include [banner](../includes/banner.md)]

此主题列出了 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.19 中的新增或更改的功能。 此版本的构建版本号为 10.0.837，并以下面的形式提供：

- **版本预览：** 2021 年 4 月
- **版本正式发布（自行更新）：** 2021 年 6 月
- **版本正式发布（自动更新）：** 2021 年 6 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 *功能* 列提供了指向[发布计划](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features)的链接，您可以在那里查看每项功能的官方发布日期。 *更多信息* 列提供了更多详细信息和/或相关文档的链接。

这些功能中的大多数必须先使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用，然后才能使用。

| 特征区域 | 功能 | 更多信息 |
|---|---|---|
| 库存和物流 | [联系人数据实体导出优化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | 此功能启用后，对引用数据的更改将不会导致相关联系人被包含在下一个增量导出中。 此功能禁用后，对引用数据的更改会让相关联系人被包含在下一个增量导出中。 |
| 库存和物流 | [带有缩放单元的仓库执行功能的增量增强](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[消息处理程序消息](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[仓库库存调整](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[云和边缘缩放单元的仓库管理工作负载](../cloud-edge/cloud-edge-workload-warehousing.md) |
| 库存和物流 | [销售报价单页上的文档介绍和文档结论字段的查找功能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | 此功能为 **销售报价单** 页上的 **文档介绍** 和 **文档结论** 字段添加了查找功能。<br><br>默认情况下启用了此功能。 |
| 库存和物流 | [在自定义硬件上使用边缘缩放单元的仓库执行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [使用 LBD 在自定义硬件上部署边缘缩放单元](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| 制造 | [在自定义硬件上使用边缘缩放单元的制造执行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [使用 LBD 在自定义硬件上部署边缘缩放单元](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| 计划 | [计划优化的无限容量计划](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | 此功能为计划优化启用具有无限容量的容量计划。 如果未启用此功能，计划的生产订单将从已发布产品库存提前期获取其提前期，不论计划时限如何。 |
| 计划 | 基于查询的计划订单确认 | [确定计划订单](../master-planning/planning-optimization/planned-order-firming.md) |
| 产品信息管理 | [变型建议页改进](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [创建预定义的产品变型](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 每一项增强都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。 如果要使用这些功能中的任何一个，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中明确启用。

| 特征区域 | 功能管理中的功能名称&nbsp;&nbsp;&nbsp; | 更多信息 |
|---|---|---|
| 销售和市场营销 | 销售历史记录清理性能改进 | 如果销售历史记录清理不是经常在具有大量销售更新的环境中运行，可能会花费很长时间。 为了减少持续时间并提高可靠性，此功能将清理分为可在有限持续时间内运行的批处理。 在可能的情况下，将利用数据库功能来最大程度地减少锁定，和避免在清理过程中加入交易表。 |
| 销售和市场营销 | 使用内部公司订单的确认日期更新请求接收日期 | 使用此功能，您可以控制在使用内部公司直接交货时销售和购买日期字段值发生什么行为。 您可以选择系统是更新请求的日期还是跳过更新日期。 如果您跳过更新，请求的日期将代表客户的请求。 如果启用更新，请求的日期（使用交货日期控制时）仅在最初代表客户的请求。 当与 *无* 不同时，交货日期控制将覆盖最初的请求。 您可以使用内部公司供应商或客户设置上的新 **使用确认日期更新请求接收日期** 设置来设置此选项。<br><br>如果禁用此功能，系统将根据交货日期控制规则覆盖原始销售订单上的请求收货日期，但请求的装运日期将保持不变。 |
| 仓库管理 | 在发放到仓库时将数量向下舍入到最近的销售单位 | 此功能添加了一个选项，该选项可以限制下达到仓库的订单数量。 启用后，订单数量将向下舍入到最接近的整数销售单位，包含少于一个销售单位的数量的订单将被拒绝下达。 |
| 仓库管理 | 组织范围的“计划工作创建”波次方法 | 启用此功能后，*计划工作创建* 波次方法将被配置为跨所有法人并行运行。 其他一些设置也将受到影响。 完整详细信息请参阅[在波次期间计划工作创建](../warehousing/configure-wave-schedule-work-creation.md)。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助主题。 它们不一定与上一节中列出的为此版本添加的新功能相关，但是它们可以帮助您从现有功能中获得更多益处。

| 特征区域 | 新增或更新主题 |
|---|---|
| 工程更改管理 | [工程更改管理常见问题](../engineering-change-management/change-management-faq.md) |
| 采购 | [供应商的类别请求](../procurement/category-requests-from-vendors.md) |
| 产品信息管理 | [管理度量单位](../pim/tasks/manage-unit-measure.md)<br><br>[产品配置模型计算](../pim/config-model-calculations.md) |
| 生产控制 | [统一作业 ID 编号规则](../production-control/unified-job-ids.md) |
| 运输管理 | [LTL 类](../transportation/ltl-class.md)<br><br>[NMFC 代码](../transportation/nmfc-codes.md) |
| 仓库管理 | [仓库批处理和序列预留层次结构疑难解答](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| 仓库管理、波次创建和处理 | [波次创建和处理](../warehousing/wave-processing.md)<br><br>[用于波次处理的仓库参数](../warehousing/wave-warehouse-parameters.md)<br><br>[波次模板](../warehousing/wave-templates.md)<br><br>[波次分配](../warehousing/wave-allocation-method.md)<br><br>[波次期间安排工作创建](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[集装化](../warehousing/wave-containerization.md)<br><br>[波次执行通知](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.19 中包含平台更新。 若要了解详细信息，请参阅 [Finance and Operations 应用版本 10.0.19（2021 年 6 月）的平台更新](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.19 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415)。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365：2021 发布波次 1 计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365：2021 发布波次 1 计划](/dynamics365-release-plan/2021wave1/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
