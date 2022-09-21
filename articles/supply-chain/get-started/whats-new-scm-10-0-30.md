---
title: Dynamics 365 Supply Chain Management 10.0.30 预览版（2022 年 11 月）
description: 本文介绍 Microsoft Dynamics 365 Supply Chain Management 10.0.30 中的新增功能或更改的功能。
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429115"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>Dynamics 365 Supply Chain Management 10.0.30 预览版（2022 年 11 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文列出了 Microsoft Dynamics 365 Supply Chain Management 预览版本 10.0.30 中的新增功能或更改的功能。 此版本的构建版本号为 10.0.1362，并按以下时间表提供：

- **预览版本：** 2022 年 9 月
- **版本的正式发布时间（自我更新）：** 2022 年 10 月
- **版本的正式发布时间（自动更新）：** 2022 年 11 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---|---|---|---|
| 制造 | [使用 Sensor Data Intelligence 监视设备](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligence 主页](../sensor-data-intelligence/sdi-home-page.md) | 功能管理：<br>*(预览版)传感器数据智能* |
| 仓库管理 | Warehouse Management 移动应用的多级绕过 <!-- KFM: Add link when RP updates --> | [为移动设备菜单项中的步骤配置绕过](../warehousing/warehouse-app-detours.md) | 功能管理：<br>*Warehouse Management 移动应用的多级绕过* |

## <a name="feature-enhancements-included-in-this-release"></a>此版本中包含的功能增强

下表列出了此版本中包含的功能增强。 这些增强每一项都提供了对现有功能的渐进性改进。 由于它们仅是功能增强，因此未列在[发布计划](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features)中。 但是，为确保这些功能增强不会与您现有的自定义或首选项冲突，默认情况下，每项增强均处于关闭状态（除非另有说明）。

如果您想要打开或关闭这些功能中的任何功能，必须在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中进行。

| 模块 | 功能管理中的功能名称 | 更多信息… |
|---|---|---|
| 生产控制 | “要下达的生产订单”页面中的现有信息 | 在 **要下达的生产订单** 页面的行部分为行项的现有库存数量添加一列。 |
| 运输管理 | 将装运分配给相关的路线细分 | 系统利用此功能可以更准确地分摊装运运费成本，包括具有沿单一路线交付到各个细分目的地的多个装运的负载。 系统基于装运和细分的目的地地址来将每个装运分配给最适合的路线细分。 然后，此功能基于装运的相对重量、体积、数量和行程距离来计算每个装运的货运成本（按负荷的总运费成本的比例形式）。 此功能仅适用于使用运输管理 (TMS) 模块管理的装运。 |

## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Microsoft Dynamics 365 Supply Chain Management 10.0.30 中包含平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.30 的平台更新（2022 年 11 月）](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md)。 <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>缺陷修复

有关版本 10.0.29 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468)。

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
