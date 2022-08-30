---
title: Dynamics 365 Supply Chain Management 10.0.26（2022 年 5 月）中的新增功能或更改
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.26 中的新增功能或更改的功能。
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: dd98b22a2dfcd8cad62bdef2d31ac2880b3422f8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334706"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Dynamics 365 Supply Chain Management 10.0.26（2022 年 5 月）中的新增功能或更改

[!include [banner](../includes/banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.26 中的新增或更改的功能。 此版本的构建版本号为 10.0.1192，并以下面的形式提供：

- **版本预览：** 2022 年 3 月
- **版本正式发布（自行更新）：** 2022 年 4 月
- **版本正式发布（自动更新）：** 2022 年 5 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 库存和物流 | [支持高级仓库管理物料的库存可见性现有查询](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [WMS 物料的库存可见性支持](../inventory/inventory-visibility-whs-support.md) | 功能管理：<br>*在库存可见性中启用仓库物料* |
| 库存和物流 | [库存可见性加载项的可承诺](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [库存可见性现有库存更改计划与可承诺](../inventory/inventory-visibility-available-to-promise.md) | 通过服务配置启用 |
| 制造 | [生产车间执行界面的实际称重物料](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [工作人员如何使用生产车间执行界面](../production-control/production-floor-execution-use.md) | 功能管理：<br>*报告生产车间执行界面中的实际称重物料* |
| 制造 | 生产车间执行界面上的“我的工作”选项卡 <!-- KFM: Add link to release plan when available --> | [工作人员如何使用生产车间执行界面](../production-control/production-floor-execution-use.md) | 功能管理：<br>*生产车间执行界面上的“我的工作”选项卡* |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 采购 | 过帐收据和供应商发票的贮存产品的登记数量和非贮存产品的剩余数量 | 此功能更改了在按照采购订单处理供应商发票和入站装运时过帐非贮存产品（如服务）数量的方式。 此功能修改了用于过帐收货和供应商发票的 *已登记数量和服务* 数量选项的行为，方法是将其更改为与在过帐销售装箱单的数量时提供的 *已登记数量和非贮存产品* 选项的行为相匹配。<br><br>当您使用 *已登记数量和服务* 数量选项过帐产品收据或供应商发票时，系统会过帐已登记的贮存产品数量并过帐非贮存产品的剩余数量（包括服务和非服务）。 如果没有此功能，系统仍会过帐已登记的贮存产品数量（包括配置为贮存物料的服务），但始终会过帐非贮存服务产品的全部订购数量（忽略不属于 *服务* 类型的非贮存产品）。 |
| 采购 | 同步内部公司销售和采购订单行上的跟踪维度 | 此功能使您可以控制是否跨内部公司销售和采购订单行同步序列号和批号跟踪维度。 它为客户和供应商的 **内部公司** 设置页面的 **采购订单策略** 和 **销售订单策略** 选项卡添加了新设置。 为了清楚起见，还更新了一些相关的附近设置的名称。<br><br>如果您使用的是仓库管理流程 (WMS)，请注意，只有当这些维度高于目标目的地预留层次结构中的位置时，此功能才会同步批号和序列号。 |
| 产品信息管理 | 清除产品属性值 | 此功能将添加一个名为 **清除产品属性值** 的定期任务，这将清除不再通过产品类别与任何产品关联的产品属性值记录。 |
| 库存和仓库管理 | (俄罗斯)在针对包括启用了 WMS 的物料的采购订单签发 GTD 时防止差异 | 此功能只能用于俄语本地化。 它可以防止在为包含启用仓库管理流程 (WMS) 的物料的进口采购订单发放俄罗斯海关申报编号 (GTD) 时出现差异。 GTD 发放流程更改了自定义日记帐中包含的发票的相关库存交易记录上的一些库存维度值，这导致采购订单的工作记录与采购的库存交易记录之间存在差异。 启用此功能后，GTD 发放流程会生成消除此类差异的调整工作。 |
| 仓库管理 | 用于 GS1 条码的增强型分析器 | 此功能添加了增强的 GS1 符号数据分析程序。 新分析程序实现了 GS1 一般规范算法来解析 GS1 符号并提供更强大的数据验证。 有关详细信息，请参阅 [GS1 条码扫描](../warehousing/gs1-barcodes.md)。 |
| 仓库管理 | 仓库管理应用程序 - 空白 GTD | 此功能只能用于俄语本地化。 它允许使用 Warehouse Management 移动应用的工作人员在需要时将俄罗斯海关申报编号 (GTD) 留空。 如果 GTD 跟踪维度设置为允许空白值，系统将接受库存操作的 GTD 值为空白，前提是现有库存量可用。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助文章。 按照前几节的列举，这些文章未必与此发行版中增加的新功能有关。 但是，可能可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新文章 |
|---|---|
| 成本管理 | 以下每篇文章都添加了更新的示例和图表：<ul><li>[具有实际成本和标记的先进先出](../cost-management/fifo-physical-value-marking.md)</li><li>[具有实际成本和标记的先进先出](../cost-management/lifo-physical-value-marking.md)</li><li>[具有实际成本和标记的后进先出日期](../cost-management/lifo-date-physical-value-marking.md)</li><li>[移动平均成本价](../cost-management/running-average-cost-price.md)</li><li>[具有实际成本和标记的加权平均](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>财务和运营应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.26 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.26 的平台更新（2022 年 5 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.26 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864)。

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

