---
title: Dynamics 365 Supply Chain Management 10.0.29 预览版（2022 年 10 月）
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.29 中的新增功能或更改的功能。
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 316650de19d3275f2c60c79c10d6ac8a8c79e1aa
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427866"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10029-october-2022"></a>Dynamics 365 Supply Chain Management 10.0.29 预览版（2022 年 10 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 预览版本 10.0.29 中的新增功能或更改的功能。 此版本的构建版本号为 10.0.1326，并按以下时间表提供：

- **版本预览：** 2022 年 8 月
- **版本的正式发布时间（自行更新）：** 2022 年 9 月
- **版本的正式发布时间（自动更新）：** 2022 年 10 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 库存和物流 | [在库存可见性中分配和预留 WMS 物料](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | 即将推出 | 默认启用 |
| 库存和物流 | [预加载简化的现有库存列表](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | 即将推出 | 默认启用 |
| 按订单生产供应自动化 | [按订单生产供应自动化](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [按订单生产供应自动化](../master-planning/make-to-order-supply-automation.md) | 功能管理：<br>*按订单生产供应自动化* |
| 计划 | [查看并应用 DDMRP 的详细见解](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [需求驱动材料要求计划概述](../master-planning/planning-optimization/ddmrp-overview.md) | 功能管理：<br>*(预览版)用于计划优化的 DDMRP* |
| 生产控制 | [在过帐到日记帐前将成品设置为实际可用](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [在过帐到日记帐前将成品设置为实际可用](../production-control/deferred-posting.md) | 功能管理：<br>*(预览版)在过帐到日记帐前将成品设置为实际可用* |
| 仓库管理 | [在 Warehouse Mobile App 中查找相关数据](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [使用 Warehouse Management 移动应用绕过查询数据](../warehousing/warehouse-app-data-inquiry.md) | 功能管理：<br>*Warehouse Management 应用数据查询流* |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 成本管理 | 联产品未决价格计算优化 | 此功能修复了使用多个线程计算联产品价格时有时会发生的冲突。 它使系统确保只计算一次每个联产品价格。 然后将该计算的结果用作所有其他计算的输入。 如果已存在待定价格，则使用该价格。 |
| 主计划 | 对计划优化中的交易记录进行分组 | 此功能可以帮助减少在使用计划优化时为提供单个销售订单行而生成的计划订单数。 启用此功能后，计划优化会将订单行的所有库存交易记录组合为一个针对完整数量的单一要求。 （此行为与内置计划引擎行为相匹配。）供应和需求将单独分组。 因此，在拆分交易记录以及使用不属于覆盖范围维度的维度（如批处理号或序列号）时，此功能有助于减少交易记录量。 |
| 采购 | 针对采购订单将供应商置于暂停状态 | 利用此功能，可针对采购订单将供应商置于暂停状态。 它添加了新的 *采购订单* 暂停类型，该类型针对采购订单将供应商标记为暂停。 您将无法为针对采购订单暂停的供应商创建新的采购订单，但您仍然可以为这些供应商处理任何未结发票或付款。 |
| 销售和市场营销 | 导入时计算行净额 | 利用此功能，您可以控制当您使用 OData 或双重写入通过 *销售订单行*、*销售报价行* 或 *退货单行* 实体导入数据时，系统是否应重新计算行合计。 只有当您还采用贸易协议评估政策来限制对销售订单行、销售报价行和/或退货单行的 **净额** 字段进行更改时，它才有效。 它将名为 **计算行净额** 的设置添加到 **应收帐款 > 设置 > 应收帐款参数** 页。 当此设置设为 *是* 时，系统将始终在需要时重新计算行金额（因此会忽略行净额的任何贸易协议评估政策）。 当此设置设为 *否* 时，系统绝不会自动计算行净额，即使传入行价格、数量和/或折扣更改意味着应重新计算行净额也不例外。 此功能默认情况下已启用，并且最初会将 **计算行净额** 设置为 *是*。 *无* 设置与版本 10.0.23 之前的系统行为匹配，并且主要用于支持旧版集成方案。<br><br>有关详细信息，请参阅[导入销售订单、报价和退货时重新计算行净额](../sales-marketing/calc-line-net-amounts-import.md)。 |
| 销售和市场营销 | 使用多个线程计算销售额总计 | 此功能使系统能够在批量计算销售总额时使用并行处理，从而帮助提高性能。 此功能将新的 **线程数** 字段添加到 **计算销售总计** 对话框中。 如果您选择在批处理中运行计算，则可以使用此字段设置最大线程数。 如果将值设置为 *0*（零）或 *1*，则将使用单个线程。 1 以上的值会启用多线程。 |
| 销售和市场营销 | 为内部公司更新手动输入的价格和折扣 | 此功能对内部公司订单的手动更改政策添加了支持。 它支持在内部公司销售和采购订单之间转移手动更改政策。 以前，仅非内部公司订单支持手动更改政策。 启用此功能后，系统将为您提供在将更改保存到内部公司订单后更新价格和折扣的选项。 此选项允许您选择是要将新价格和折扣详细信息应用于内部公司订单，还是使订单保持不变。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助文章。 按照前几节的列举，这些文章未必与此发行版中增加的新功能有关。 但是，它们可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新文章 |
|---|---|
| 主计划，CTP | [使用 CTP 计算销售订单交货日期](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| 主计划，DDMRP | [需求驱动材料要求计划概述](../master-planning/planning-optimization/ddmrp-overview.md)<br>[为您的系统启用 DDMRP 功能](../master-planning/planning-optimization/ddmrp-enable.md)<br>[库存过帐](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[缓冲区配置文件和级别](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[需求驱动型计划](../master-planning/planning-optimization/ddmrp-planning.md)<br>[可视化和协作执行](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| 仓库管理 | [装入集装箱以进行装运](../warehousing/packing-containers.md)<br>[出站集装箱装箱和装运处理的包装工作](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>此版本中的功能状态更改

下表列出了版本 10.0.29 中强制或默认启用的功能。 更新到版本 10.0.29 后，系统即会自动启用所有这些功能。 强制功能无法关闭，但仍可使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)关闭默认开启的功能。

此表还列出了以前处于公开预览版状态，但在版本 10.0.29 中已变为正式发布的功能。 此更改指示现在建议在生产环境中使用这些功能。 除非另外指明，否则这些功能默认情况下处于关闭状态。 因此，如果您要使用它们，那么您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用它们。

| 模块 | 功能名称 | 新功能状态 |
| --- | --- | --- |
| 资产管理 | [生产车间执行界面的资产管理功能](../production-control/production-floor-execution-configure.md) | 强制 |
| 成本管理 | [将“结帐与调整”中的“取消”标签更改为“冲销”](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | 强制 |
| 成本管理 | 清除物料清单计算详细信息交叉成本计算版本 | 强制 |
| 成本管理 | [比较物料价格存储](../cost-management/compare-item-price.md) | 强制 |
| 成本管理 | [成本计算级别](../cost-management/cost-calculation-level.md) | 默认打开 |
| 成本管理 | 为库存结转冲销启用用户定义的批处理号设置 | 默认打开 |
| 成本管理 | [库存结算进度详细信息](whats-new-scm-10-0-21.md) | 默认打开 |
| 成本管理 | [库存值报表存储](../cost-management/inventory-value-report-storage.md) | 强制 |
| 成本管理 | 库存值报表数据清除 | 强制 |
| 成本管理 | 移动平均，回退成本序列 | 强制 |
| 成本管理 | 在网格中显示库存结算日志 | 强制 |
| 成本管理 | 以汇总格式显示包含未完全结算的交易记录的物料 | 强制 |
| 库存和仓库管理 | 允许空的批属性值 | 强制 |
| 库存和仓库管理 | 自动递增库存转移单行的行号 | 强制 |
| 库存和仓库管理 | 从销售行创建转移单 | 强制 |
| 库存和仓库管理 | 在工作流中禁用库存日记帐行字段 | 强制 |
| 库存和仓库管理 | 启用库存质量管理参数警告功能 | 强制 |
| 库存和仓库管理 | (中国)从每月平均成本中排除实际收货和发货成本 | 默认打开 |
| 库存和仓库管理 | [库存日记账审核工作流](../inventory/inventory-journal-workflow.md) | 强制 |
| 库存和仓库管理 | [现有库存报表存储](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | 强制 |
| 库存和仓库管理 | [库存管理的已保存视图](saved-views-scm.md) | 强制 |
| 库存和仓库管理 | 转移单取消 | 强制 |
| 库存和仓库管理 | 在库存日记帐中使用度量单位和单位数量 | 强制 |
| 库存和仓库管理 | 将库存日记帐解锁 | 强制 |
| 制造 | [自动领取支持仓库的物料以便自动过帐领料单](whats-new-scm-10-0-23.md) | 正式发布 |
| 制造 | 允许在生产工艺路线工序的物料清单中显示库存维度 | 强制 |
| 制造 | [允许在从作业卡设备报告为完工入库时输入批号和序列号](../production-control/report-finished-job-device.md) | 默认打开 |
| 制造 | 改进的生产实际称重数量领料 | 默认打开 |
| 制造 | [生产车间执行界面的作业搜索](../production-control/production-floor-execution-configure.md) | 强制 |
| 制造 | [制造执行系统集成](../production-control/mes-integration.md) | 默认打开 |
| 制造 | [生产车间执行界面的“我的一天”视图](../production-control/production-floor-execution-configure.md) | 默认打开 |
| 制造 | [针对生产订单的按需物料可用性检查](whats-new-scm-10-0-24.md) | 默认打开 |
| 制造 | [覆盖默认生产预留](../production-control/override-default-reservation-principle.md) | 强制 |
| 制造 | [在生产车间执行界面（非 WMS）上登记物料消耗量](../production-control/production-floor-execution-configure.md) | 正式发布 |
| 制造 | [报告生产车间执行界面中的实际称重物料](../production-control/production-floor-execution-configure.md) | 正式发布 |
| 制造 | [报告来自生产车间执行界面的联产品和副产品](../production-control/production-floor-execution-configure.md) | 默认打开 |
| 制造 | [在生产车间执行界面中报告计划物料](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | 默认打开 |
| 制造 | [生产控制的已保存视图](saved-views-scm.md) | 强制 |
| 制造 | [在生产车间执行界面中显示完整序列、批处理和牌照编号](../production-control/production-floor-execution-configure.md) | 强制 |
| 制造 | [根据计划消耗日期验证原材料的到期日期](whats-new-scm-10-0-23.md) | 默认打开 |
| 主计划 | [自动确认计划优化](../master-planning/planning-optimization/planned-order-firming.md) | 强制 |
| 主计划 | [计划散装批次订单和包装批次订单的可批处理确认和合并](whats-new-scm-10-0-20.md) | 默认打开 |
| 主计划 | [启用预处理筛选器时包括现有物料](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | 默认打开 |
| 主计划 | [计划优化的无限容量计划](../master-planning/planning-optimization/infinite-capacity-planning.md) | 默认打开 |
| 主计划 | [计划优化的利润](../master-planning/planning-optimization/safety-margins.md) | 强制 |
| 主计划 | [计划优化的负天数](../master-planning/planning-optimization/delay-tolerance.md) | 强制 |
| 主计划 | [针对调整后需求预测的并行授权](whats-new-scm-10-0-20.md) | 强制 |
| 主计划 | [通过筛选确认计划订单](../master-planning/planning-optimization/planned-order-firming.md) | 强制 |
| 主计划 | [用于计划优化的计划生产订单](../master-planning/planning-optimization/production-planning.md) | 强制 |
| 主计划 | [用于计划优化的采购贸易协议](../master-planning/planning-optimization/purchase-trade-agreement.md) | 强制 |
| 主计划 | [计划订单的已保存视图](saved-views-scm.md) | 强制 |
| 采购 | 采购订单上起始金额和终止金额 | 强制 |
| 采购 | 禁用采购申请分配重置按钮 | 默认打开 |
| 采购 | [启用重置与采购相关的工作流](whats-new-scm-10-0-20.md) | 默认打开 |
| 采购 | [限制每个批处理任务的采购订单行数](whats-new-scm-10-0-27.md) | 默认打开 |
| 采购 | [将供应商的财务维度与采购订单上的有效维度链接财务维度合并](whats-new-scm-10-0-25.md) | 强制 |
| 采购 | [过帐收据和供应商发票的贮存产品的登记数量和非贮存产品的剩余数量](whats-new-scm-10-0-26.md) | 正式发布 |
| 采购 | [防止工作流中包含多个采购申请时过度消耗常规预算预留](whats-new-scm-10-0-21.md) | 默认打开 |
| 采购 | [采购协议负责方](../procurement/purchase-agreements.md) | 强制 |
| 采购 | [采购订单的已保存视图](saved-views-scm.md) | 强制 |
| 产品信息管理 | 预处理物料清单报表以避免超时 | 强制 |
| 产品信息管理 | 使用物料模板时分别对应的默认财务维度 | 强制 |
| 产品信息管理 | 启用物料模板的产品维度组 | 强制 |
| 产品信息管理 | 物料 - 条码实体改进 | 强制 |
| 产品信息管理 | 根据命名法重新生成产品变型名称 | 强制 |
| 产品信息管理 | [已发放产品的已保存视图](saved-views-scm.md) | 强制 |
| 产品信息管理 | [变型建议页改进](../pim/tasks/create-predefined-product-variants.md) | 强制 |
| 销售和市场营销 | [销售订单上的费用分配](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | 强制 |
| 销售和市场营销 | 清除销售订单更新历史记录 | 强制 |
| 销售和市场营销 | [根据使用时间清除销售更新历史记录](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | 强制 |
| 销售和市场营销 | [联系人数据实体导出优化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | 强制 |
| 销售和市场营销 | 复制销售贷方通知单的总折扣组 | 强制 |
| 销售和市场营销 | [启用对销售报价单文档介绍和文档结论字段的查找](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | 强制 |
| 销售和市场营销 | [改善“前 100 位”客户的报表性能](whats-new-scm-10-0-23.md) | 强制 |
| 销售和市场营销 | 在历史记录清除任务中包括等待记录 | 强制 |
| 销售和市场营销 | 限制每个批处理任务的销售订单行数 | 默认打开 |
| 销售和市场营销 | [限制可选择进行过帐的销售订单数](whats-new-scm-10-0-21.md) | 强制 |
| 销售和市场营销 | 重新计算估计的客户余额 | 强制 |
| 销售和市场营销 | [包含和不包含实际称重的销售退货单行登记(具有小数精度)](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | 强制 |
| 销售和市场营销 | [销售和市场营销的已保存视图](saved-views-scm.md) | 强制 |
| 销售和市场营销 | [一键销售订单确认](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | 强制 |
| 运输管理 | 允许在没有已过帐的供应商发票日记帐的情况下使来自货运发票行的货运账单不匹配 | 默认打开 |
| 运输管理 | [放弃货运帐单时启用创建供应商发票日记帐](whats-new-scm-10-0-20.md) | 默认打开 |
| 运输管理 | [小型包裹装运](../warehousing/small-parcel-shipping.md) | 强制 |
| 运输管理 | [USMCA 原产地证明文档](../transportation/usmca-certification-of-origin.md) | 默认打开 |
| 仓库管理 | [其他位置区域](../warehousing/additional-location-zones.md) | 强制 |
| 仓库管理 | [取消工作](../warehousing/cancel-warehouse-work.md) | 强制 |
| 仓库管理 | [合并装运](../warehousing/configure-shipment-consolidation-policies.md) | 强制 |
| 仓库管理 | [通过仓库应用创建和处理转移单](../warehousing/create-transfer-order-from-warehouse-app.md) | 强制 |
| 仓库管理 | 带有库位指令的越库配送模板 | 默认打开 |
| 仓库管理 | [将储存工作与 ASN 分离](whats-new-scm-10-0-21.md) | 强制 |
| 仓库管理 | [延迟 PUT 操作](../warehousing/deferred-processing-manual-inventory-movement.md) | 强制 |
| 仓库管理 | 延迟的放置 - 集装箱 | 默认打开 |
| 仓库管理 | 延迟放置处理 – 针对触发事件设置为“以前”的审计模板功能启用 | 强制 |
| 仓库管理 | [禁用从锁定库存取样的质检订单的预期收货](../inventory/inventory-blocking.md) | 默认打开 |
| 仓库管理 | 启用仓库移动设备的快速验证 | 强制 |
| 仓库管理 | [用于 GS1 条码的增强型分析器](../warehousing/gs1-barcodes.md) | 正式发布 |
| 仓库管理 | [灵活的订单承诺牌照预留](../warehousing/flexible-warehouse-level-dimension-reservation.md) | 强制 |
| 仓库管理 | [可变的仓库级别维度预留](../warehousing/flexible-warehouse-level-dimension-reservation.md) | 强制 |
| 仓库管理 | [物料合并库位利用率](../warehousing/item-consolidation-location-utilization.md) | 默认打开 |
| 仓库管理 | 牌照接收历史记录 | 默认打开 |
| 仓库管理 | [手动装运合并](../warehousing/consolidate-shipments-manual-workbench.md) | 默认打开 |
| 仓库管理 | [针对管理员或类似的受信任用户的转移行手动领料服务](whats-new-scm-10-0-28.md) | 正式发布 |
| 仓库管理 | [物料处理设备接口](../warehousing/mhax.md) | 强制 |
| 仓库管理 | [新装载计划工作台页面](whats-new-scm-10-0-24.md) | 正式发布 |
| 仓库管理 | [出站工作负荷可视化](../warehousing/outbound-workload-visualization.md) | 强制 |
| 仓库管理 | [计划越库配送](../warehousing/planned-cross-docking.md) | 强制 |
| 仓库管理 | [处理仓库应用事件](../warehousing/warehouse-app-events.md) | 强制 |
| 仓库管理 | 针对联产品和副产品储存工作模板的查询增强 | 强制 |
| 仓库管理 | [在发放到仓库时将数量向下舍入到最近的销售单位](whats-new-scm-10-0-19.md) | 强制 |
| 仓库管理 | [用于装载计划工作台的已保存视图](saved-views-scm.md) | 强制 |
| 仓库管理 | [工作详细信息页的已保存视图](saved-views-scm.md) | 强制 |
| 仓库管理 | [用于波次处理的已保存视图](saved-views-scm.md) | 强制 |
| 仓库管理 | [用于负荷处理的已保存视图](saved-views-scm.md) | 强制 |
| 仓库管理 | [用于装运处理的已保存视图](saved-views-scm.md) | 强制 |
| 仓库管理 | [扫描 GS1 条码](../warehousing/gs1-barcodes.md) | 正式发布 |
| 仓库管理 | 装运波次标签详细信息 | 强制 |
| 仓库管理 | [放入混合单位](whats-new-scm-10-0-21.md) | 强制 |
| 仓库管理 | [对装箱工作站上关闭/重新打开的集装箱使用更快的 API](whats-new-scm-10-0-21.md) | 默认打开 |
| 仓库管理 | [验证为补货作业选择的模板](whats-new-scm-10-0-20.md) | 默认打开 |
| 仓库管理 | [仓库应用提升的字段](../warehousing/warehouse-app-promoted-fields.md) | 强制 |
| 仓库管理 | [仓库应用步骤说明](../warehousing/mobile-app-titles-instructions.md) | 强制 |
| 仓库管理 | [仓库库位状态](../warehousing/warehouse-location-status.md) | 强制 |
| 仓库管理 | [Warehouse Management 应用绕过](../warehousing/warehouse-app-detours.md) | 默认打开 |
| 仓库管理 | [波次批处理作业详细信息](../warehousing/wave-processing.md) | 强制 |
| 仓库管理 | [波次执行通知](../warehousing/wave-execution-notifications.md) | 强制 |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.29 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.29 的平台更新（2022 年 10 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md)。

### <a name="bug-fixes"></a>缺陷修复

有关版本 10.0.29 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559)。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 和行业云：2022 版本第 1 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2022 版本第 2 波计划](/dynamics365-release-plan/2022wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management 中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)一文中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
