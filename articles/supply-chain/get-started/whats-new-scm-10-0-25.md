---
title: Dynamics 365 Supply Chain Management 10.0.25 中的新增功能或更改（2022 年 4 月）
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.25 中的新增功能或更改的功能。
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: af344d3771583a99851c070e3735258ac964b5d7
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954482"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management 10.0.25 中的新增功能或更改（2022 年 4 月）

[!include [banner](../includes/banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.25 中的新增或更改的功能。 此版本的构建版本号为 10.0.1149，并以下面的形式提供：

- **版本预览：** 2022 年 2 月
- **版本的正式发布时间（自行更新）：** 2022 年 3 月
- **版本的正式发布时间（自动更新）：** 2022 年 4 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 库存和物流&nbsp;&nbsp; | [危险物料增强](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | 即将推出 | 功能管理：<br>*危险物料增强* |
| 库存和物流&nbsp;&nbsp; | [装箱工作站的装箱工作](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | 即将推出 | 功能管理：<br>*装箱工作站的装箱工作* |
| 库存和物流&nbsp;&nbsp; | [使用 GS1 格式标准扫描仓库中的条码](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 条码和 QR 码](../warehousing/gs1-barcodes.md) | 功能管理：<br>*扫描 GS1 条码* |
| 制造 | [生产车间执行界面的物料消耗和预留](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [工作人员如何使用生产车间执行界面](../production-control/production-floor-execution-use.md) | 功能管理：<br>*(预览版)在生产车间执行界面(非 WMS)上登记物料消耗量*<br><br>与/或：<br><br>功能管理：<br>*(预览版)在生产车间执行界面(启用了 WMS)上登记物料消耗量* |
| 制造 | [在缩放单元上登记物料消耗量](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [云和边缘缩放单元的制造执行工作负载](../cloud-edge/cloud-edge-workload-manufacturing.md) | 功能管理：<br>*使用移动应用登记缩放单元中的物料消耗量* |
| 计划 | [计划优化集中日历维护](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [日历和主计划](../master-planning/supply-chain-calendars-master-planning.md) | 默认启用 |
| 计划 | [优化现有供应的计划优化建议](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [行动消息](../master-planning/action-messages.md) | 默认启用 |
| 计划 | 已简化的计划订单 | [已简化的计划订单](../master-planning/planning-optimization/planned-orders-simplified.md ) | 功能管理：<br>*已简化的计划订单* |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 库存和仓库管理 | (波兰)允许在一个 SAD 中将多个 SAD 发票链接到一个采购订单行 | 利用此功能，当过帐多个不同发票（如不同的装运）的采购订单行时，您可以拆分这些采购订单行并将它们链接到单个管理文档 (SAD)。 |
| 采购 | 按会计日期将多个采购申请合并到单个采购订单中 | 此功能允许将多个采购申请合并到单个采购订单（如果不同的采购申请具有不同的会计日期）。 可以设置采购订单创建和需求合并采购策略规则，来自动执行在采购订单级别按会计日期对申请行进行分组的决定。 如果启用预算控制，将不支持按会计日期进行采购订单合并，因为会计日期用于预算预留和保留款。 因此，在从采购申请到采购订单的过渡过程中应该保留它。 |
| 采购 | 显示旧式默认询价回复字段设置 | 此功能重新引入了旧版默认询价 (RFQ) 回复字段设置，这些设置以前已从用户界面中删除。 这些设置不提供任何现成功能，但可以进行自定义来根据需要提供。 如果您的组织已为默认询价回复字段设置添加了功能或计划添加，请启用此功能。 启用此功能后，您可以通过转到 **采购参数** 页面，打开 **询价** 选项卡并选择 **默认询价回复字段** 来访问设置。 |
| 采购 | 将供应商的财务维度与采购订单上的有效维度链接财务维度合并 | 如果您在财务维度和站点库存维度之间设置链接，此功能允许您在采购申请被批准后将来自供应商的财务维度与有效维度链接财务维度合并。 可以设置采购订单创建和需求合并采购策略规则，来推动在采购订单标头级别将供应商的财务维度与有效维度链接财务维度合并的决定。 |
| 生产控制 | （俄罗斯）为生产配方/物料清单和生产中的自动 GTD 预留/消耗启用默认库位设置 | 此功能为根据导入的原材料进行生产提供了更多选项（仅限俄罗斯本地化）：<ul><li>用于为资源组和仓库上的生产配方和物料清单设置自动默认位置的选项。</li><li>根据非 WMS 预留算法在激活 WMS 的仓库中按 *GTD 编号* 维度自动预留原材料。 当存在 *原材料领料* 的工作策略且 **工作创建方法** 设置为 *从不*，并且仓库、位置和物料编号设置与生产（批次）订单的库存交易记录匹配时，适用此功能。</li><li>根据之前所述而获取的预留，在进行领料单过帐时按 *GTD 编号* 维度自动消耗原材料。</li></ul> |
| 仓库管理 | (预览版)入站和出站仓库订单的缩放单元支持 | 此功能将导致系统在发放到仓库过程中创建出站仓库订单，以及将转移单过帐为已装运订单时创建入站仓库订单。 然后，系统将每个入站或出站仓库订单同步到负责装运或接收订单的缩放单元。 请注意，启用此功能后，必须升级仓库执行工作负荷。 有关详细信息，请参阅 [Cloud Scale Unit 和 Edge Scale Unit 的仓库管理工作负荷](../cloud-edge/cloud-edge-workload-warehousing.md)。<br><br>此功能需要 *将储存工作与 ASN 分离* 功能，将启用使用 Warehouse Management 移动应用上的牌照接收流程接收转移单的功能。 |

## <a name="feature-state-changes-in-this-release"></a>此版本中的功能状态更改

下表列出了从 10.0.25 开始强制或默认启用的功能。 更新到 10.0.25 后，系统即会自动启用所有这些功能。 强制功能无法关闭，但仍可使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)关闭默认开启的功能。

此表还列出了以前处于公开预览状态，但在 10.0.25 中已变为正式发布的功能，这意味着现在建议在生产环境中使用它们。 除非另有说明，否则这些功能默认处于关闭状态，因此如果您想要使用它们，必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)进行启用。

| 模块 | 功能名称 | 功能状态 |
| --- | --- | --- |
| 资产管理 | [在运行维护计划时应用对工作订单进行分组的规则](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | 正式发布 |
| 资产管理 | [基于计数器的维护增强](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | 正式发布 |
| 成本管理 | [成本计算级别](../cost-management/cost-calculation-level.md) | 正式发布 |
| 成本管理 | 为库存结转冲销启用用户定义的批处理号设置 | 正式发布 |
| 成本管理 | [库存结算进度详细信息](whats-new-scm-10-0-21.md) | 正式发布 |
| 成本管理 | [用于库存标准成本重估的默认财务维度的选项](../cost-management/manage-standard-cost-updates.md) | 正式发布 |
| 成本管理 | 库存值报表数据清除 | 默认打开 |
| 成本管理 | [库存值报表存储](../cost-management/inventory-value-report-storage.md) | 默认打开 |
| 成本管理 | 在网格中显示库存结算日志 | 默认打开 |
| 工程更改管理 | [对现有产品启用更改管理](../engineering-change-management/change-management-existing-products.md) | 默认打开 |
| 工程更改管理 | [工程更改管理](../engineering-change-management/product-engineering-overview.md) | 默认打开 |
| 工程更改管理 | [面向生产部门的工程通知](../engineering-change-management/engineering-change-management.md) | 默认打开 |
| 工程更改管理 | [工程更改管理的已改进属性继承](../engineering-change-management/engineering-attributes-and-search.md) | 默认打开 |
| 工程更改管理 | [管理对配方及其成分的更改](../engineering-change-management/manage-formula-changes.md) | 默认打开 |
| 工程更改管理 | [产品准备情况检查](../engineering-change-management/product-readiness.md) | 默认打开 |
| 工程更改管理 | [生成工程产品的变型](../engineering-change-management/engineering-variants.md) | 默认打开 |
| 库存和仓库管理 | 从物料清单行导航到物料清单版本 | 强制 |
| 主计划 | [计划散装批次订单和包装批次订单的可批处理确认和合并](whats-new-scm-10-0-20.md) | 正式发布 |
| 主计划 | 资源计划与维护 | 正式发布 |
| 主计划 | 启用主计划设置向导功能 | 强制 |
| 主计划 | [需求预测详细信息中的预测模型选择](../master-planning/manual-adjustments-baseline-forecast.md) | 强制 |
| 主计划 | [主计划进度可视化](../master-planning/tasks/monitor-master-planning-run.md) | 强制 |
| 主计划 | [并行确认计划订单](../master-planning/planning-optimization/planned-order-firming.md) | 强制 |
| 主计划 | [通过筛选确认计划订单](../master-planning/planning-optimization/planned-order-firming.md) | 默认打开 |
| 主计划 | [计划订单的已保存视图](saved-views-scm.md) | 默认打开 |
| 采购 | 禁用采购申请分配重置按钮 | 正式发布 |
| 采购 | [启用重置与采购相关的工作流](whats-new-scm-10-0-20.md) | 正式发布 |
| 采购 | 批量确认通过供应商协作接受的采购订单的能力 | 强制 |
| 采购 | 采购协议“已关闭”状态 | 强制 |
| 采购 | 向与采购协议关联的采购订单发票中添加行 | 默认打开 |
| 采购 | 将“订购数量”字段添加到“过账物料收货”页 | 默认打开 |
| 采购 | [允许供应商通过供应商协作申请采购类别](../procurement/category-requests-from-vendors.md) | 默认打开 |
| 采购 | 采购订单上起始金额和终止金额 | 默认打开 |
| 采购 | 站点和仓库的费用设置 | 默认打开 |
| 采购 | 启用基于年度关税的进项税计算 | 默认打开 |
| 采购 | [采购协议负责方](../procurement/purchase-agreements.md) | 默认打开 |
| 采购 | [采购订单的已保存视图](saved-views-scm.md) | 默认打开 |
| 产品信息管理 | [对默认订单数量的严格验证](../production-control/default-order-settings.md) | 强制 |
| 产品信息管理 | 预处理物料清单报表以避免超时 | 默认打开 |
| 产品信息管理 | 使用物料模板时分别对应的默认财务维度 | 默认打开 |
| 产品信息管理 | 启用物料模板的产品维度组 | 默认打开 |
| 产品信息管理 | 根据命名法重新生成产品变型名称 | 默认打开 |
| 产品信息管理 | [变型建议页改进](../pim/tasks/create-predefined-product-variants.md) | 默认打开 |
| 生产控制 | 改进的生产实际称重数量领料 | 正式发布 |
| 生产控制 | 已将一个“停止休息”新按钮添加到“作业卡终端”页面 | 强制 |
| 生产控制 | [在作业卡设备中报告为完工入库时，启用牌照编号的自动生成](../production-control/production-floor-execution-configure.md) | 强制 |
| 生产控制 | 启用分包物料的部分收货，并解决有关“供应商”类型的物料清单行的废料计算问题 | 强制 |
| 生产控制 | [用于锁定作业卡设备和作业卡终端以便对其进行净化的功能](../production-control/production-floor-execution-configure.md) | 强制 |
| 生产控制 | 对“审核”和“转移作业”对话框进行的改进 | 强制 |
| 生产控制 | [用于报告为完工入库的牌照已添加作业卡设备](../production-control/production-floor-execution-configure.md) | 强制 |
| 生产控制 | [通过作业卡设备打印标签](../production-control/production-floor-execution-configure.md) | 强制 |
| 生产控制 | [生产车间执行](../production-control/production-floor-execution-configure.md) | 强制 |
| 生产控制 | [生产车间执行界面的资产管理功能](../production-control/production-floor-execution-configure.md) | 默认打开 |
| 生产控制 | [生产车间执行界面的作业搜索](../production-control/production-floor-execution-configure.md) | 默认打开 |
| 生产控制 | [覆盖默认生产预留](../production-control/override-default-reservation-principle.md) | 默认打开 |
| 生产控制 | [在生产车间执行界面中显示完整序列、批处理和牌照编号](whats-new-scm-10-0-21.md) | 默认打开 |
| 销售和市场营销 | [销售订单详细信息性能增强](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | 正式发布 |
| 销售和市场营销 | 销售报价详细信息性能增强 | 正式发布 |
| 销售和市场营销 | 销售订单引用数据导出策略 | 强制 |
| 销售和市场营销 | [销售订单到采购订单行删除策略](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | 强制 |
| 销售和市场营销 | [销售报价引用数据导出策略](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| 强制 |
| 销售和市场营销 | [联系人数据实体导出优化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | 默认打开 |
| 销售和市场营销 | 启用对销售报价单文档介绍和文档结论字段的查找 | 默认打开 |
| 销售和市场营销 | [改善“前 100 位”客户的报表性能](whats-new-scm-10-0-23.md) | 默认打开 |
| 销售和市场营销 | 重新计算估计的客户余额 | 默认打开 |
| 销售和市场营销 | [包含和不包含实际称重的销售退货单行登记(具有小数精度)](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | 默认打开 |
| 销售和市场营销 | [销售和市场营销的保存视图](saved-views-scm.md) | 默认打开 |
| 销售和市场营销 | 一键销售订单确认 | 默认打开 |
| 仓库管理 | [带有库位指令的越库配送模板](../warehousing/planned-cross-docking.md) | 正式发布 |
| 仓库管理 | [禁用从锁定库存取样的质检订单的预期收货](../inventory/inventory-blocking.md) | 正式发布 |
| 仓库管理 | 牌照接收历史记录 | 正式发布 |
| 仓库管理 | [物料处理设备接口](../warehousing/mhax.md) | 正式发布 |
| 仓库管理 | [在发放到仓库时将数量向下舍入到最近的销售单位](whats-new-scm-10-0-19.md) | 正式发布 |
| 仓库管理 | 对仓库应用工作列表的缩放单元支持 | 正式发布 |
| 仓库管理 | 装运波次标签详细信息 | 正式发布 |
| 仓库管理 | [对装箱工作站上关闭/重新打开的集装箱使用更快的 API](whats-new-scm-10-0-21.md) | 正式发布 |
| 仓库管理 | [验证为补货作业选择的模板](whats-new-scm-10-0-20.md) | 正式发布 |
| 仓库管理 | 允许补货模板使用现有的即时补货工作(跨单位) | 强制 |
| 仓库管理 | 创建 WHS 用户时自动分配 GUID | 强制 |
| 仓库管理 | 在接收负荷物料期间捕获仓库应用中的产品变型和跟踪维度 | 强制 |
| 仓库管理 | [更改由跟踪维度控制的物料的库存状态](../inventory/inventory-statuses.md) | 强制 |
| 仓库管理 | [更改工作的工作池](../warehousing/change-work-pool-on-work.md) | 强制 |
| 仓库管理 | [群集位置已满](../warehousing/cluster-position-full.md) | 强制 |
| 仓库管理 | [群集储存功能](../warehousing/putaway-clusters.md) | 强制 |
| 仓库管理 | [确认并转移](../warehousing/confirm-and-transfer.md) | 强制 |
| 仓库管理 | [确认来自批处理作业的出站装运](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | 强制 |
| 仓库管理 | [控制是否在移动设备上显示接收汇总页](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | 强制 |
| 仓库管理 | [延迟处理手动库存变动操作](../warehousing/deferred-processing-manual-inventory-movement.md) | 强制 |
| 仓库管理 | 不允许创建不符合波次负荷构建模板要求的负荷 | 强制 |
| 仓库管理 | [增强的牌照标签布局](../warehousing/document-routing-layout-for-license-plates.md) | 强制 |
| 仓库管理 | [评估针对多 SKU 库位指令的所有操作](/troubleshoot/dynamics-365/supply-chain/warehousing/evaluate-multiple-location-directive-actions) | 强制 |
| 仓库管理 | 隐藏“所有负荷”和“负荷详细信息”页上的“总值”字段 | 强制 |
| 仓库管理 | 牌照标签生成配置 | 强制 |
| 仓库管理 | 针对管理员或类似的受信任用户的负荷行手动更正 | 强制 |
| 仓库管理 | [场所牌照定位](../warehousing/location-license-plate-positioning.md) | 强制 |
| 仓库管理 | [库位产品维度混合](../warehousing/location-product-dimension-mixing.md) | 强制 |
| 仓库管理 | 使移动设备库存移动库存状态字段可编辑 | 强制 |
| 仓库管理 | 针对管理员或类似的受信任用户的销售行手动领料服务 | 强制 |
| 仓库管理 | [阻止转移单已装运牌照用于目标仓库以外的其他仓库](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | 强制 |
| 仓库管理 | 提示解析不明确的“位置/牌照”名称 | 强制 |
| 仓库管理 | [质量检查](../warehousing/quality-check.md) | 强制 |
| 仓库管理 | [新仓库应用的用户设置、图标和步骤标题](../warehousing/install-configure-warehouse-management-app.md) | 强制 |
| 仓库管理 | [其他位置区域](../warehousing/additional-location-zones.md) | 默认打开 |
| 仓库管理 | [通过仓库应用创建和处理转移单](../warehousing/create-transfer-order-from-warehouse-app.md) | 默认打开 |
| 仓库管理 | 启用仓库移动设备的快速验证 | 默认打开 |
| 仓库管理 | [仓库管理现有条目清理作业的最长执行时间](../warehousing/onhand-cleanup.md) | 默认打开 |
| 仓库管理 | [出站工作负荷可视化](../warehousing/outbound-workload-visualization.md) | 默认打开 |
| 仓库管理 | [处理仓库应用事件](../warehousing/warehouse-app-events.md) | 默认打开 |
| 仓库管理 | [用于装载计划工作台的已保存视图](saved-views-scm.md) | 默认打开 |
| 仓库管理 | [工作详细信息页的已保存视图](saved-views-scm.md) | 默认打开 |
| 仓库管理 | [用于波次处理的已保存视图](saved-views-scm.md) | 默认打开 |
| 仓库管理 | [用于负荷处理的已保存视图](saved-views-scm.md) | 默认打开 |
| 仓库管理 | [用于装运处理的已保存视图](saved-views-scm.md) | 默认打开 |
| 仓库管理 | [波次批处理作业详细信息](../warehousing/wave-processing.md) | 默认打开 |
| 仓库管理 | [波次执行通知](../warehousing/wave-execution-notifications.md) | 默认打开 |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.25 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.25 的平台更新（2022 年 4 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.25 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868)。

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
