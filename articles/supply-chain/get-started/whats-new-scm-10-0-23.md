---
title: Dynamics 365 Supply Chain Management 10.0.23 预览
description: 此主题介绍了 Microsoft Dynamics 365 Supply Chain Management 10.0.23 中的新增功能或更改的功能。
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 3cf30c203d936f171796d9dd8d766cbbb8c997e0
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647789"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10023"></a>Dynamics 365 Supply Chain Management 10.0.23 预览

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题列出了 Microsoft Dynamics 365 Supply Chain Management 预览版 10.0.23 中的新增功能或更改的功能。 此版本的构建版本号为 10.0.1037，并以下面的形式提供：

- **预览版：** 2021 年 10 月
- **版本的正式发布时间（自行更新）：** 2021 年 12 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 *功能* 列提供了指向[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)的链接，您可以在那里查看每项功能的官方发布日期。 *更多信息* 列提供了更多详细信息和/或相关文档的链接。 若要确定如何开启功能，请参阅 *启用方式* 列。 有关如何使用功能管理的详细信息，请参阅[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的功能。

| 特征区域 | 功能 | 更多信息 | 启用者: ，时间:  |
|---|---|---|---|
| 全球通讯簿 | 在地址设置中为每个国家/地区定义默认省/自治区/直辖市 | 现在，您可以在全球通讯簿的地址设置中为每个国家/地区定义默认省/自治区/直辖市。 设置默认省/自治区/直辖市时，当您为国家/地区创建新的县或市/市记录时，它将是省/自治区/直辖市字段中输入的默认值。 另请参阅[地址设置](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | 默认启用。 |
| 库存和物流&nbsp;&nbsp; | [在 Warehouse Management 移动应用中暂停任务](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [为移动设备菜单项中的步骤配置绕过](../warehousing/warehouse-app-detours.md) | 功能管理（*Warehouse Management 应用绕过*） |
| 库存和物流&nbsp;&nbsp; | [仓库应用提升的字段](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [为移动设备中的步骤配置提升的字段](../warehousing/warehouse-app-promoted-fields.md)| 功能管理（*仓库应用提升的字段*） |
| 生产控制 | [报告来自生产车间执行界面的联产品和副产品](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [工作人员如何使用生产车间执行界面](../production-control/production-floor-execution-use.md) | 功能管理（*报告来自生产车间执行界面的联产品和副产品*） |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本新增的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何一个，您必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中执行此操作，其中使用下表的 *功能管理中的功能名称* 列中显示的名称列出了这些功能。

| 模块 | 功能管理中的功能名称 | 更多信息 |
|---|---|---|
| 资产管理 | 工作订单日记帐中的支出的对方科目 | 利用此功能，您可以为工作订单日记帐中列出的每笔费用指定抵销帐户。 您通常可以将供应商帐户与每笔费用关联，但也支持其他帐户类型。 它向 **工作订单日记帐** 页上的 **费用** 快速选项卡添加了两个新列（**抵销帐户类型** 和 **抵销帐户**）。|
| 库存和仓库管理 | \[俄罗斯\] 根据销售订单的财务凭证中的更正标志过帐 Storno 财务库存交易记录 | 此功能将影响俄罗斯的贷方通知单更正功能。 它支持根据总帐中的更正选项过帐销售发票的库存交易记录。 启用此功能后，库存交易的财务凭证上的 **更正** 标记和库存交易记录上的 **Storno** 标记之间不再存在差异。 |
| 库存和仓库管理 | (俄罗斯)以分批方式运行库存余额交易额报表计算 | 在 Supply Chain Management 的俄语本地化方面，通过此功能能够以批处理方式运行 *库存余额交易额* 报表，以存储该报表和查看先前生成的报表。 |
| 库存和仓库管理 | (俄罗斯)在库存管理的特定于国家/地区的主要窗体中使用当地语言的翻译 | 在 Supply Chain Management 的俄语本地化方面，通过此功能可以在以下特定于俄罗斯的库存打印输出中使用产品/物料名称和度量单位的俄罗斯语翻译：盘点清单 (INV-3)、盘点清单 (INV-5) 和盘点清单 (INV-6)。 |
| 采购 | 清理采购订单更新历史记录 | 利用此功能，您可以清理与采购订单更新相关的临时历史记录。 它向 **所有采购订单** 页上的操作窗格添加了一个名为 **清理采购订单更新历史记录** 的新按钮。 默认情况下启用了此功能。 |
| 生产控制 | (预览版)自动领取支持仓库的物料以便自动过帐领料单 | 通过此功能可以自动领取和解析库存维度，以便自动过帐、派生和倒冲领料单日记帐。 |
| 生产控制 | 根据计划消耗日期验证原材料的到期日期 | 此功能更改了在预留要在生产过程中使用的原材料批次时验证批次到期日期的方式。 启用此功能后，批次到期日期将根据在生产物料清单行或批次订单配方行上设定的计划消耗日期（原材料日期）进行验证。 禁用此功能后，批次到期日期将根据生产或批次订单的计划交货日期（与之前一样）进行验证。 |
| 销售和市场营销 | 清除销售订单更新历史记录 | 利用此功能，您可以清理与销售订单更新相关的临时历史记录。 它将一个名为 **清理销售更新历史记录** 的新按钮添加到销售订单的详细信息和列表页的操作窗格中。 |
| 销售和市场营销 | 改善“前 100 位”客户的报表性能 | 此功能通过始终运行所有客户的报表（作为其目标用途），而不是通过允许自定义查询，来改善 **前 100 位** 客户的报表性能。 启用此功能后，**前 100 位** 报表对话中将禁用所有 **要包括的记录** 设置。 |
| 仓库管理 | 对于发布到出站订单仓库的缩放单元支持 | 启用此功能后，出站订单可从中心直接发布到履行订单的缩放单元。 |

## <a name="new-and-updated-documentation-resources"></a>新的和更新的文档资源

我们最近添加或大幅更新了以下帮助主题。 按照上一部分的列举，这些主题未必与此发行版中增加的新功能有关。 但是，可能可以帮助您更加受益于现有功能。

| 特征区域 | 新增或更新主题 |
|---|---|
| 工程更改管理 | [工程属性和工程属性搜索](../engineering-change-management/engineering-attributes-and-search.md)现在介绍工程属性继承的工作原理。 |
| 主计划 | [具有需求预测的总体规划](../master-planning/planning-optimization/demand-forecast.md)和[预测缩减参数](../master-planning/reduction-keys.md)现在提供有关如何使用缩减参数的详细信息。 |
| 主计划 | [物料的安全存货履行](../master-planning/safety-stock-replenishment.md)现在提供有关使用最小/最大参数的详细信息。 |
| 主计划 | [库存预测](../master-planning/inventory-forecast.md)现在提供有关分配预测的详细信息。 |
| 主计划 | [供应计划](../master-planning/supply-schedule.md) |
| 仓库管理 | [全局移动设备参数](../warehousing/mobile-device-parameters.md) |
| 仓库管理 | [定位](../warehousing/anchoring.md) |
| 销售和市场营销 | 现在详细介绍了内部公司交易，从[设置内部公司交易](../sales-marketing/intercompany-trade-set-up.md)及其相关主题开始。 |
| 库存管理 | 库存可见性文档已扩展和更新，从[库存可见性加载项概述](../inventory/inventory-visibility.md)及其相关主题开始。 |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.23 中包含平台更新。 要了解详细信息，请参阅 [Finance and Operations 应用版本 10.0.23 的平台更新（2021 年 11 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md)。

### <a name="bug-fixes"></a>缺陷修复

有关 10.0.23 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910)。

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
