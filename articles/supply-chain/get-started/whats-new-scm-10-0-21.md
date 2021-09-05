---
title: Dynamics 365 Supply Chain Management 10.0.21 预览（2021 年 10 月）
description: 此主题介绍了 Dynamics 365 Supply Chain Management 10.0.21 中的新增功能或更改的功能。
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42d296cb0402b5e96f23d628f08a28fb35683d5f
ms.sourcegitcommit: 5a44eb4f555bf5ee0b1293f0ecdc37ee8b53aa24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/17/2021
ms.locfileid: "7391200"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Dynamics 365 Supply Chain Management 10.0.21 预览（2021 年 10 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题列出了 Microsoft Dynamics 365 Supply Chain Management 预览版 10.0.21 中的新增功能或更改的功能。 此版本的构建版本号为 10.0.960，并以下面的形式提供：

- **版本预览：** 2021 年 8 月
- **版本的正式发布时间（自行更新）：** 2021 年 9 月
- **版本的正式发布时间（自动更新）：** 2021 年 10 月

## <a name="known-deployment-issue"></a>已知部署问题

在 IaaS 上部署版本 10.0.21 时，您可能会收到以下部署警告：

**警告代码：** 95017

**警告消息**：对 VM 执行脚本 \[SetupDiagnostics\] 失败

尽管出现警告，但部署将正常工作。 但是，Lifecycle Services (LCS) 中可能会出现以下已知问题：

- 在 **环境监控** 页面上，**查看详细版本信息** 链接将不会显示，因此您将无法查看环境中安装的模块的特定版本。 如果没有此数据，后续修补程序可能会失败，因为应用修补程序的流程使用此数据验证是否满足模块版本先决条件。 由于无法在生产中使用 PEAP/预览版本或应用修补程序，因此影响应最小。
- SQL 见解下 **环境监视** 页面上的 **性能指标** 和 **索引分析** 选项卡将不会显示任何数据。 所有其他 **环境监视** 功能将正常工作。
- **完整系统诊断** 页面将无法访问。 有关夜间收集器运行的状态及其规则检测到的问题的关联数据也将不会显示。

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 *功能* 列提供了指向[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)的链接，您可以在那里查看每项功能的官方发布日期。 *更多信息* 列提供了更多详细信息和/或相关文档的链接。

这些功能中的大多数必须先使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用，然后才能使用。 某些列出的功能仍处于预览状态，而其他功能可能已正式发布。

| 特征区域 | 功能 | 更多信息 |
|---|---|---|
| 库存和物流&nbsp;&nbsp; | [Dynamics 365 Supply Chain Management 全球库存核算加载项](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [“全球库存核算”主页](../global-inventory-accounting/global-inventory-accounting-home.md) |
| 库存和物流&nbsp;&nbsp; | [使用连接到抵销帐户的代码过帐现有库存量调整](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [库存盘点原因代码](../warehousing/reason-codes-for-counting-journals.md) |
| 库存和物流&nbsp;&nbsp; | [销售报价引用数据导出策略](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | 选择对报价单所引用的数据的更改是否会导致这些报价单（或行）包含在下一次增量导出中。 如果您选择不包含此类报价单或行，则您的增量导出将更快地运行。<br><br>此功能会将一个名为 **在更改跟踪期间跳过销售报价参考数据** 的设置添加到 **应收帐款参数** 页面。 |
| 库存和物流&nbsp;&nbsp; | [使用 GS1 格式标准扫描仓库中的条码](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 条码和 QR 码](../warehousing/gs1-barcodes.md) |
| 库存和物流&nbsp;&nbsp; | [库存可见性加载项中的软预留](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [库存可见性预留](../inventory/inventory-visibility-reservations.md) |
| 库存和物流&nbsp;&nbsp; | [返点管理的扣缴和实际称重增强功能](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [使用扣缴工作台管理扣缴](../rebate-management/deduction-workbench.md )<br><br>[处理、审核和发布返点](../rebate-management/process-review-post.md)<br><br>[返点管理交易](../rebate-management/rebate-management-deals.md) |
| 库存和物流&nbsp;&nbsp; | [仓库应用步骤说明](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [为 Warehouse Management 移动应用自定义步骤标题和说明](../warehousing/mobile-app-titles-instructions.md) |
| 库存和物流&nbsp;&nbsp; | [到岸成本的工作中断和跟踪更新](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [要储存的更新追踪信息](../landed-cost/update-tracking-putaway.md )<br><br>[在途货物处理](../landed-cost/in-transit-processing.md) |
| 主计划 | [计划优化的负天数](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [延迟容差（负天数）](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 每一项增强都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。 如果要使用这些功能中的任何一个，您必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中明确启用。

| 特征区域 | 功能管理中的功能名称&nbsp;&nbsp;&nbsp; | 更多信息 |
|---|---|---|
| 成本管理 | 库存结算进度详细信息 | 此预览功能启用库存结算进度的详细视图。 |
| 采购 | 防止工作流中包含多个采购申请时过度消耗常规预算预留 | 此预览功能可改进用户提交和审核超出常规预算预留行余额的采购申请时的错误检查。 这有助于防止在工作流中存在多个采购申请时过度消耗常规预算预留。 |
| 生产控制 | 在生产车间执行界面中显示完整序列、批处理和牌照编号 | 此功能为查看生产车间执行界面中的序列号、批处理和牌照号列表提供了改进的体验。 显示内容从字符数有限的卡视图更改为提供足够空间来显示完整值的列表视图。 该列表还提供搜索特定数字的功能。 |
| 销售和市场营销 | 限制可选择进行过帐的销售订单数 | 利用此功能，您可以定义在从销售订单列表页面中过帐确认单、领料单、装箱单和发票时可以选择的最大销售订单数。 它已自动启用。 该功能向 **应收帐款参数** 页面添加了一个名为 **要过帐的最大销售订单数** 的设置。 新设置默认为值 *100*。 此功能有助于在选择大量销售订单时改进销售订单列表页的性能。 它对可由定期任务处理的销售订单的数量没有影响。 |
| 仓库管理 | 将储存工作与 ASN 分离 | 当您在缩放单元上运行仓库管理工作负荷（作为分布式混合拓扑的一部分）时，需要使用此功能发送和接收预装运通知 (ASN)。 它添加了专门存储有关储存工作的信息的新数据库表。 以前，此信息存储在也用于 ASN 的表中。 |
| 仓库管理 | 放入混合单位 | 允许系统将物料插入包括混合单位（例如盒子和箱子）的库位。 对于每个时隙模板行，此功能允许您选择该行是应将物料插入到混合单元库位还是单个单元库位。 |
| 仓库管理 | 对装箱工作站上关闭/重新打开的集装箱使用更快的 API | 启用此预览功能后，将使用新的轻量流程创建与集装箱相关的库存交易记录，该流程可提高在手动包装站处理期间关闭或重新打开集装箱的性能。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助主题。 它们不一定与上一节中列出的为此版本添加的新功能相关，但是它们可以帮助您从现有功能中获得更多益处。

| 特征区域 | 新增或更新主题 |
|---|---|
| 主计划 | [库存预测](../master-planning/inventory-forecast.md) |
| 主计划 | [计划优化未使用的参数](../master-planning/planning-optimization/not-used-parameters.md) |
| 主计划 | [补货方法和数量修改](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| 主计划 | [具有无限容量的计划](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| 主计划 | [查看计划历史记录和计划日志](../master-planning/planning-optimization/plan-history-logs.md) |
| 仓库管理 | [集装箱包装策略](../warehousing/container-packing-strategy-overview.md) |
| 仓库管理 | [周期盘点示例方案](../warehousing/cycle-counting-scenarios.md) |
| 仓库管理 | [通过 V2 数据实体导入传入 ASN](../warehousing/import-asn-v2-data-entity.md) |
| 仓库管理 | [销售订单和转移单过量领料](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| 仓库管理 | [波次期间安排波次标签打印](../warehousing/configure-task-based-wave-label-printing.md) |
| 仓库管理 | [Warehouse Management 移动应用中的新增功能或更改的功能](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.21 中包含平台更新。 若要了解详细信息，请参阅 [Finance and Operations 应用版本 10.0.21 的平台更新（2021 年 10 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.21 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de)。

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
