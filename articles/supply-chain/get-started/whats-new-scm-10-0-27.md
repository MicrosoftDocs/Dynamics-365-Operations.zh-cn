---
title: Dynamics 365 Supply Chain Management 10.0.27 的新增功能或更改（2022 年 7 月）
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.27 中的新增功能或更改的功能。
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ff92e6904b8042232159a0aea095d7a91c17d4b7
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124091"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10027-july-2022"></a>Dynamics 365 Supply Chain Management 10.0.27 的新增功能或更改（2022 年 7 月）

[!include [banner](../includes/banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.27 中的新增或更改的功能。 此版本的构建版本号为 10.0.1227，并按以下时间表提供：

- **版本预览：** 2022 年 4 月
- **版本正式发布（自行更新）：** 2022 年 6 月
- **版本正式发布（自动更新）：** 2022 年 7 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 库存和物流 | [库存可见性加载项的库存分配](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [库存可见性库存分配](../inventory/inventory-visibility-allocation.md) | 默认启用 |
| 制造 | 生产车间执行界面的“我的一天”视图 | [工作人员如何使用生产车间执行界面](../production-control/production-floor-execution-use.md)并在[生产车间执行界面中显示休假余额](../production-control/production-floor-execution-payroll-stats.md) | 功能管理：<br>*生产车间执行界面的“我的一天”视图* |
| 计划 | [转包计划优化支持](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [管理生产中的转包工作](../production-control/manage-subcontract-work-production.md) | 默认启用 |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 主计划 | 创建计划转移单时考虑库存提前期 | 创建计划转移单后，在将交货日期控制设置的计划转移单的收货日期计算为 *无* 或 *销售* 类型的提前期时，此功能会导致系统考虑物料默认订单设置中指定的库存提前期。 指定了转移提前期后，将采用其值计算收货日期，并将忽略运输天数。 |
| 采购 | 供应商发票行上的默认代理人合同税务信息 | 此功能引入了为代理合同供应商发票行上的 **销售税** 和 **物料销售税** 字段设置默认值的逻辑。 仅当代理合同行上的费用类型为分类帐/分类帐时才应用此逻辑。 物料销售税组将从经纪采购类别（如果已设置）或费用类型中获取其默认值。 销售税组将会根据供应商帐户采用其默认值。 |
| 采购 | 限制每个批处理任务的采购订单行数 | 此功能可帮助您在过帐确认和物料收货时优化系统性能。 它将名为 **每个任务的行数** 的新设置添加到 **采购参数** 页面的 **交货** 选项卡。 通过此新设置，您可以限制每个批任务处理的采购订单行数。 因此，它可以帮助防止大型批任务减慢系统运行速度。 |
| 产品信息管理 | 填充产品属性值 | 此功能添加名为 *填充产品属性值* 的定期任务。 此新定期任务按产品类别为与产品关联的属性创建缺失的产品属性值记录。 |
| 生产控制 | 生产车间执行界面上的其他配置 | <p>此功能将以下选项添加到 **配置生产车间执行** 页面：</p><ul><li>**完成搜索时自动打开开始对话框** – 如果启用了此选项，那么当工作人员使用搜索栏查找作业时，将自动打开 **开始作业** 对话框。</li><li>**完成搜索时自动打开报告进度对话框** – 如果启用了此选项，那么当工作人员使用搜索栏查找作业时，将自动打开作业的 **报告进度** 对话框。</li><li>**在报告进度对话框中默认剩余数量** - 启用此选项后，**报告进度** 对话框将显示要在生产作业中报告的剩余数量。</li></ul><p>有关详细信息，请参阅[配置生产车间执行界面](../production-control/production-floor-execution-configure.md)。</p> |
| 生产控制 | 生产车间执行界面中的生产团队 | <p>将多个工作人员分配到同一生产作业后，他们现在可以指定一个工作人员作为指导员。 剩下的工作人员会自动成为该指导员的助手。 对于生成的团队，只有指导员必须登记作业状态，而时间记录将应用于所有团队成员。 此功能还支持一个名称为 *辅助资源* 的方案。 在此方案中，工作人员可以登记为另一个工作人员的助手，然后成为新形成的组的指导员。</p><p>有关详细信息，请参阅[工作人员如何使用生产车间执行界面](../production-control/production-floor-execution-use.md)。</p> |
| 生产控制 | 在生产车间执行界面中报告计划物料 | 此功能简化了在生产车间执行界面中报告计划物料的批次订单的流程。 为具有 *计划物料* 生产类型的产品创建批次订单后，只能对该批次订单的联产品和副产品报告为已完工入库。 计划物料的批次订单通常用于支持拆卸流程，其中原材料产品将拆卸成多个独特的产品。 当工作人员将计划物料的批次订单报告为完工入库时，**报告进度** 对话框现在将仅显示联产品和副产品。 之前，它还显示了计划物料，并且此行为可能会使工作人员混淆。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助文章。 按照前几节的列举，这些文章未必与此发行版中增加的新功能有关。 但是，它们可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新文章 |
|---|---|
| 成本管理 | [具有“包括实际成本和标记”的加权平均日期](../cost-management/weighted-average-date.md) |
| 分布式混合拓扑 | [试用分布式混合拓扑中的缩放单元](../cloud-edge/cloud-edge-try-out.md) |
| 双重写入 | [按需与 Supply Chain Management 定价引擎同步](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| 仓库管理 | [发放到仓库](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>财务和运营应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.27 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.27 的平台更新（2022 年 6 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.27 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271)。

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

